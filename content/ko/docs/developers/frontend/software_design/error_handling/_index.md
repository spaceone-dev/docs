---
title: "Frontend Error Handling"
linkTitle: "Frontend Error Handling"
weight: 4
date: 2022-06-02
description:
    How To Handle Error

---

## Error 구분에 따른 처리 (API)
<br>
다양한 API Error를 처리하기 위해 미리 에러 타입을 정의한다.
<br>
<br>

- NotFoundError : 리소스를 찾을 수 없을 때 (status: 404)

- BadRequestError : 잘못된 요청을 보낼 때 (status: 400)

- AuthenticationError: 인증이 실패했을 때 (status: 401)

- AuthorizationError: 권한 검증에 실패했을 때 (status: 403)

- APIError: 이외의 모든 API Error 및 서버 에러 (status: 500 등)

이 에러들을 axios api client의 interceptor에서 받아 핸들링한다. 위에 명시된 에러 이외에 다른 에러 코드를 정의할 수도 있다.

<br>
이 에러들을 SpaceConnector(axios api client)의 interceptor에서 받아 핸들링한다.

axios의 interceptor에서 error가 왔을 때, 각 statusCode를 보고 판별하여 위에 미리 정의해둔 Error로 throw해준다.


## Error Handler (Client)
<br>
Client 쪽에서 API client를 통해 넘어온 Error의 유형을 판단하여 다음과 같이 핸들링한다.

<br>

### AuthenticationError의 경우

Token이 유효한 지 확인하고, 유효하지 않을 경우 Authentication Error Handler를 호출하여 에러를 처리한다. 

Authentication Error Handler는 다음과 같은 동작을 한다.
- Session 만료 모달을 보여줌

- User의 Session을 만료시킴

### AuthorizationError의 경우

Authorization Error Handler를 호출한다. 이 핸들러는 다음과 같은 동작을 한다.

상단에 권한이 없다는 경고창을 노출시킴 

### NoResourceError의 경우
No Resource라는 토스트를 보여주고, redirect url이 있을 시 해당 url로 이동시킨다.

### APIError의 경우
콘솔창에 API Error라고 명시된 로그를 남긴다.

### BadRequestError의 경우
페이지에서 넘겨준 Error Message가 적힌 toast 경고창을 띄운다.

<br>

## Error를 추가하는 방법
<br>

1. SpaceConnector(console-core-lib > space-connector/error.ts)에 새로운 에러를 정의한다.

2. SpaceConnector의 Error Interceptor(console-core-lib > space-connector/api.ts)에 새로운 에러를 throw해주는 부분을 추가해준다.

3. API의 error가 아니라 Client 자체에서 필요한 에러의 경우 Client(console > common/error.ts)에 새로운 에러를 정의하고, 에러가 발생할 시 해당 에러를 throw한다.

4. Error Handler(console > common/composables/error/errorHandler.ts)에 새롭게 추가된 Error를 핸들링하는 코드를 추가한다.

## Error를 사용하는 방법 
<br>

에러 클래스를 작성하고, 그 에러 클래스를 이용해 만든 에러 핸들러를 실제 프로젝트에서는 아래와 같이 사용한다.

<br>

- list 등 일반적인 작업
```typescript
try {
    특정 동작
} catch (e) {
    ErrorHandler.handleError(e);
}
```

- create/update 등 실패 시 toast message를 보여주어야 하는 작업
<br>

```typescript
try {
    특정 동작
} catch (e) {
    ErrorHandler.handleRequestError(e, 번역을 위한 i18n key값 or string);
}
```
