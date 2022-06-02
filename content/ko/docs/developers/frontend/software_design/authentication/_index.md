---
title: "Frontend Authentication"
linkTitle: "Frontend Authentication"
weight: 4
date: 2022-05-13
description:
    How To Authenticate SpaceONE User

---


## 인증 플로우
<br />
SpaceONE은 현재 도메인 설정에 따라 Google Oauth2, Keycloak, KB SSO 세 가지의 인증 중 하나를 선택하여 제공하고, 인증 플로우는 다음과 같습니다.
<br />
![](/docs/developers/frontend/software_design/authentication/authentication_img/authentication_uml.png)

<br />
1. 우선 해당 도메인에서 어떤 Sign-in 방식(ID/PW인지, 외부 인증을 제공하는 지, 제공한다면 어떤 인증방식인지)을 사용하는 지 체크합니다.
2. 그 후, 각각 다른 Sign-in 방식에 맞는 UI를 보여주고, 해당 템플릿에서 Authenticator를 상속받은 커스텀 인증 모듈의 메소드를 호출합니다.
3. 각각의 커스텀 Auth들은 각자 필요한 Sign-in 절차를 수행한 후, 상속받은 Authenticator의 기본 Sign-in 로직을 수행합니다.

<br />
<br />
이후 이루어지는 인증 플로우는 다음과 같습니다.

![](/docs/developers/frontend/software_design/authentication/authentication_img/authentication_flow.png)

## Authenticator
<br />
Authenticator는 다음과 같은 구조를 가집니다.


![](/docs/developers/frontend/software_design/authentication/authentication_img/authenticator.png)

<br />
최상위 Authenticator는 아주 기본적인 signIn과 signOut 메서드만 가지는 추상 클래스입니다.
<br />
<br />

```typescript
abstract class Authenticator {
	static async signIn(필요한 매개변수): Promise<void> {
    	// sign in 로직
    }

    static async signOut(): Promise<void> {
    	// sign out 로직
    }
}

export {
	Authenticator,
}

```

signIn을 위해 백엔드 인증 서버에 보낼 credentials라는 데이터가 필수적이고, userId와 userType(일반 User인지, 관리자인지, API만 사용하는 API user인지)을 부수적으로 받습니다.
signOut에서는 vuex에 작성해놓은 signOut 메서드를 호출합니다.

<br />
## 커스텀 인증 구조
<br />
이제 기본적인 추상 클래스 작성이 끝났으니, 이 클래스를 상속받아 각 SSO에 맞는 Auth 클래스들을 작성합니다. 
위의 구조도를 보면 알 수 있듯이, Auth를 구현하는 데에 필요한 것은 두 가지가 있습니다. 바로 폼 렌더링(SSO 버튼 등)을 위한 템플릿과, 메서드들을 구현한 module(.ts) 파일입니다.
<br />

## 커스텀 인증 클래스 
<br />
각 커스텀 인증에 맞는 Sign In, Sign Out 로직과 추상 클래스 Authenticator의 인증(기본 인증)을 수행하는 로직이 필요합니다.
Authenticator의 Sign In은 credentials라는 data를 필요로 하고, 이 credentials 안에 들어가는 데이터는 모든 커스텀 인증마다 상이합니다.
<br />

```typescript
// custom-auth.ts

class CustomAuth extends Authenticator {
    const signIn = async () => {
        // 각 SSO, 커스텀 인증에 필요한 Sign in 로직
        const credentials = { // 각 커스텀 인증에서 생성된 credentials }
        super.signIn(credentials);
    }

    const signOut = async () => {
        // 각 SSO, 커스텀 인증에 필요한 Sign Out 로직
        super.signOut();
    }
}
```

결론적으로, 커스텀 Auth class 내부에 상속받은 Authenticator(=super)의 함수들을 호출하여 SpaceONE의 인증을 동시에 수행할 수 있도록 합니다.


## 커스텀 인증 클래스 loader
<br />
이제 어떤 인증 클래스를 부를 건지 결정하는 loader를 간단하게 만들어보도록 합니다.

```typescript
export const loadAuth = (authType?) => {
    if (authType === 'CUSTOM_AUTH') return CustomAuth;
    return SpaceAuth;
};
```

SignIn은 개별 템플릿을 가지지만, SignOut은 어디에서든 호출될 수 있기 때문에 위와 같은 loader를 사용하여 현재 도메인의 인증 타입을 넣으면 알맞은 인증 로직을 수행할 수 있도록 작성합니다.

## 커스텀 인증 템플릿
<br />
위의 작업을 하고난 후 마지막 작업은 폼 렌더링입니다.

```typescript
//Custom Auth의 template(external/custom/template/CUSTOM_AUTH.vue)

<template>
	<div>Custom 로그인을 위한 폼 버튼</div>
</template>

<script lang="ts">
 setup() {
 	//필요한 로직들
 	onMounted(async() => {
    		try {
            	await loadAuth('CUSTOM_AUTH').signIn(); //loader를 사용하여 customAuth 클래스의 signIn 함수 호출
            } catch (e) {
            	//에러 핸들링
            }
        }
    )
 }
</script>

```
<br />
각 커스텀 인증은 저마다의 폼 렌더링이 필요하기 때문에 위와 같이 해당 Auth에 맞는 커스텀 템플릿을 작성해줍니다.
<br />
그리고 마지막으로 커스텀 템플릿을 SignIn Page에서 보여줍니다.
vue에는 <component :is="xxx">라는 문법으로 다이나믹하게 컴포넌트를 불러올 수 있는 문법이 존재합니다.(https://kr.vuejs.org/v2/guide/components-dynamic-async.html) 
해당 문법을 이용하여
<br />
<br />

```vue
//sign-in page
<component :is="component" class="sign-in-template"
	@sign-in="handleSignIn"
/>

```

이렇게 템플릿 부분에 작성해주고, 아래 스크립트 부분에서

```vue
//sign-in page
  const state = reactive({
  	...
	component: computed(() => {
                let component;
                const auth = state.authType;
                if (auth) {
                    try {
                        component = () => import(`./external/${auth}/template/${auth}.vue`);
                    } catch (e) {
                        //필요한 에러 핸들링.
                    }
                }
                return component;
            }),
  })

```

<br />
위와 같이 dynamic import 방식을 사용하여 컴포넌트를 렌더링합니다.



## TL;DR

1. 외부 인증 뿐만 아니라 자체 인증 또한 성공해야 하기 때문에 자체 인증만을 구현한 추상 클래스를 만듭니다.
2. 해당 추상 클래스를 상속하여 구현한 커스텀 인증 클래스들을 만들어 해당 클래스 내부에서 커스텀 인증 로직을 처리하고, super class의 인증도 처리합니다.
3. 해당 커스텀 클래스를 불러오기 위한 loader를 추가합니다.
4. 커스텀 클래스의 폼을 렌더링하기 위한 template을 작성해줍니다.
5. Sign In 페이지에서 다이나믹하게 해당 template을 불러서 렌더링합니다.

