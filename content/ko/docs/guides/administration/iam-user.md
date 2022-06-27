---
title: "[IAM] 사용자"
linkTitle: "[IAM] 사용자"
weight: 1
date: 2022-06-23
description: >
    **사용자**에서는 클라우드포레의 사용자를 생성/삭제하거나 활성화/비활성화 할 수 있습니다. 또한 사용자에게 역할을 할당하여 도메인에 대한 권한을 부여할 수 있습니다.
---

{{<alert>}}
[관리 > 사용자] 페이지에서 사용자에게 할당할 수 있는 역할은 `Admin` 타입입니다. `User` 타입은 프로젝트의 멤버에게 할당할 수 있습니다.
프로젝트 멤버에게 역할을 부여하는 방법은 [여기](/ko/docs/guides/project/project-group/#프로젝트-그룹-멤버-초대하기)를 참고하세요.
{{</alert>}}

## 사용자 추가하기
추가할 수 있는 사용자의 종류는 세 가지입니다.
- **내부 사용자**: 로그인 페이지에서 아이디와 비밀번호를 사용해 로그인 할 수 있는 사용자
- **외부 사용자**: 도메인이 가지고 있는 외부 사용자 인증을 따름
- **API Only**: 오직 API만 사용 가능하며 클라우드포레 콘솔 접근이 불가함

### 내부 사용자 추가하기
내부 사용자는 로그인 페이지에서 아이디와 비밀번호를 사용해 로그인 할 수 있는 사용자입니다.

(1) [관리 > 사용자] 페이지에서 [생성] 버튼을 클릭합니다.

![user-create-01](/ko/docs/guides/administration/iam-user-img/user-create-01.png)

(2) [사용자 추가] 모달이 열린 뒤, 내부 사용자 추가를 위해 [Local] 탭을 선택합니다.

![user-create-02](/ko/docs/guides/administration/iam-user-img/user-create-02.png)

(2-1) 내부 사용자의 아이디를 입력한 뒤, [아이디 확인] 버튼을 클릭합니다. 사용자 아이디는 이메일 형식이어야 하며, 기존 사용자 목록에 없는 아이디어야 합니다.

(2-2) 이름과 이메일을 선택적으로 입력합니다.

(2-3) 필요 시 [어드민 역할 할당] 메뉴에서 역할을 선택합니다.
{{<alert>}}
사용자에게 할당된 역할에 따라, 페이지 접근 권한이나 API 정책이 상이하게 적용됩니다. 역할에 대한 자세한 사항은 [여기](/ko/docs/guides/administration/iam-role)를 참고하세요.
{{</alert>}}

(2-4) 사용자가 첫 로그인 시 사용할 비밀번호를 입력합니다.

(3) [확인] 버튼을 클릭합니다.


### 외부 사용자 추가하기
외부 사용자 추가는 해당 도메인이 가지고 있는 외부 사용자 인증을 따릅니다. 만약 인증된 외부 사용자가 아닐 경우 사용자로 추가할 수 없습니다.

![user-create-03](/ko/docs/guides/administration/iam-user-img/user-create-03.png)


### API Only 사용자 추가하기
API 사용자는 클라우드포레 콘솔 접근이 불가하며, 오직 API만 사용할 수 있습니다.

![user-create-04](/ko/docs/guides/administration/iam-user-img/user-create-04.png)


## 사용자 상세 보기
사용자 페이지의 테이블에서 특정 사용자를 선택하면, 해당 사용자에 대한 상세한 정보를 볼 수 있습니다.

![user-detail-01](/ko/docs/guides/administration/iam-user-img/user-detail-01.png)
