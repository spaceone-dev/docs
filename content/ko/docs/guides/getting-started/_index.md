---
title: "시작하기"
linkTitle: "시작하기"
weight: 1
date: 2022-06-07
description: >
    클라우드포레는 여러 클라우드 서비스 프로바이더에 분산된 리소스들을 통합하여 체계적으로 관리할 수 있는 서비스입니다.
    <br>
    <br>
    가이드를 통해 클라우드포레에 대한 모든 것을 알아보세요. 
---

클라우드포레의 서비스를 이용하기 위해서는 다음 세 가지 작업이 선행되어야 합니다.

- 사용자 설정
- 프로젝트 설정
- 서비스 계정 설정

## 사용자 설정

클라우드포레의 사용자는 내부 사용자, 외부 사용자, API 사용자, 이렇게 세 가지 타입으로 분류됩니다.

여기에서는 내부 사용자를 추가하는 방법만을 소개하며, 외부 사용자와 API 사용자 추가 방식은 [[IAM] 사용자 가이드](/ko/docs/guides/administration/iam-user)에서 확인할 수 있습니다.

### 사용자 추가하기

(1) [관리 > 사용자] 페이지에서 [생성] 버튼을 클릭합니다.

![user-page](/ko/docs/guides/getting-started/user-setup-img/user-page.png)

(2) [사용자 생성] 모달에서 [Local] 탭을 선택합니다.

(2-1) 아이디를 입력 후 [아이디 확인] 버튼을 클릭하여, 유효한 아이디인지 확인합니다.

![user-create-modal-local-id](/ko/docs/guides/getting-started/user-setup-img/user-create-modal-local-id.png)

(2-2) 사용자를 식별할 이름, 이메일, 그리고 비밀번호를 입력한 후 [확인] 버튼을 클릭하여 사용자 생성을 완료합니다.

![user-create-modal-local-filed](/ko/docs/guides/getting-started/user-setup-img/user-create-modal-local-filed.png)

{{<alert title="어드민 권한 할당">}}
사용자에게 어드민 권한을 부여하려면, [어드민 권한 할당] 드롭다운에서 선택하여 할당할 수 있습니다.

만약 아무것도 선택하지 않으면, 해당 사용자에게는 아무런 권한이 부여되지 않습니다.

권한에 대한 더 자세한 설명은 [여기](/ko/docs/guides/administration/iam-role)에서 확인할 수 있습니다.

![user-create-role-assign](/ko/docs/guides/getting-started/user-setup-img/user-create-role-assign.png)
{{</alert>}}


## 프로젝트 설정

체계적인 리소스 관리를 위해 [**프로젝트**](/ko/docs/guides/project/project)와 [**프로젝트 그룹**](/ko/docs/guides/project/project-group)을 생성합니다.

### 프로젝트 그룹 생성하기

프로젝트는 반드시 하나의 프로젝트 그룹에 속해있어야 하므로, 프로젝트를 생성하기 이전에 먼저 프로젝트 그룹을 생성해야 합니다.

(1) [프로젝트] 페이지에서 [프로젝트 그룹 생성] 버튼을 클릭합니다.

![project-group-create-button](/ko/docs/guides/getting-started/project-setup-img/project-group-create-button.png)

(2) [프로젝트 그룹 생성] 모달에서 프로젝트 그룹 이름을 입력 후, [확인] 버튼을 클릭하여 프로젝트 그룹을 생성합니다.

![project-group-create-modal](/ko/docs/guides/getting-started/project-setup-img/project-group-create-modal.png)

### 프로젝트 생성하기

프로젝트 그룹을 생성한 뒤, 그 하위에 속하게 될 프로젝트를 생성합니다.

(1) 왼쪽의 프로젝트 그룹 목록에서, 앞서 생성한 프로젝트 그룹을 선택합니다.

![project-group-select](/ko/docs/guides/getting-started/project-setup-img/project-group-select.png)

(2) 오른쪽 상단의 [프로젝트 생성] 버튼을 클릭합니다.

(3) [프로젝트 생성] 모달에서 프로젝트 이름을 입력한 후, [확인] 버튼을 클릭하여 프로젝트를 생성합니다.

![project-create-modal](/ko/docs/guides/getting-started/project-setup-img/project-create-modal.png)


### 프로젝트 그룹 멤버 초대하기

프로젝트 그룹에 사용자를 초대하여 프로젝트 그룹의 [**멤버**](/ko/docs/guides/project/member)로 등록할 수 있습니다.

{{<alert title="프로젝트 그룹 멤버 역할(Role)">}}
초대된 멤버들은 해당 프로젝트 그룹에 대하여 반드시 하나의 역할(Role)을 가지게 되며, 그 하위에 있는 모든 프로젝트 그룹과 프로젝트에 대하여서도 동일한 역할(Role)이 적용됩니다.

상세한 내용은 [여기](/ko/docs/guides/administration/iam-role)를 참고하세요.
{{</alert>}}

(1) 앞에서 생성한 프로젝트 그룹을 왼쪽의 [프로젝트 그룹] 목록에서 선택합니다.

(2) 오른쪽 상단에 [프로젝트 그룹 멤버 관리] 아이콘 버튼을 클릭합니다.

![project-member-icon-button](/ko/docs/guides/getting-started/project-setup-img/project-member-icon-button.png)

{{<alert title="">}}
해당 프로젝트 그룹을 관리할 수 있는 권한이 있어야 오른쪽 상단의 버튼이 보입니다.
{{</alert>}}

(3) [프로젝트 그룹 멤버 관리] 페이지에서 [초대] 버튼을 클릭하여 [멤버 초대] 모달을 엽니다.

![project-member-invite-button](/ko/docs/guides/getting-started/project-setup-img/project-member-invite-button.png)

(3-1) 초대하려는 멤버를 선택합니다. 한 번에 여러 멤버를 선택하여 초대할 수 있습니다.

![project-member-invite-modal-member-added](/ko/docs/guides/getting-started/project-setup-img/project-member-invite-modal-member-added.png)

(3-2) 초대할 멤버들에게 부여할 역할(Role)을 선택합니다.

![project-member-invite-modal-role-added](/ko/docs/guides/getting-started/project-setup-img/project-member-invite-modal-role-added.png)

{{<alert title="멤버 역할(Role)">}}
프로젝트의 멤버에게 부여할 수 있는 역할(Role)은 `User` 타입의 [역할(Role)](/ko/docs/guides/administration/iam-role)만 가능합니다.
{{</alert>}}

(3-3) 초대할 멤버들에 대한 라벨을 입력 후, 엔터 키를 눌러 추가합니다.

(3-4) [확인] 버튼을 클릭하여 멤버 초대를 완료합니다.

![project-member-invited](/ko/docs/guides/getting-started/project-setup-img/project-member-invited.png)

## 서비스 계정 설정

서비스 계정이란 리소스를 수집하기 위해 필요한 계정 정보를 의미합니다.

{{<alert title="">}}
서비스 계정을 생성하려면, 먼저 프로젝트를 생성(링크)해야 합니다.
{{</alert>}}

### 클라우드 서비스 계정 추가

[에셋 인벤토리 > 서비스 계정] 페이지에서 클라우드 서비스 계정을 추가합니다.

(1) 추가할 클라우드 서비스를 선택합니다.

![service-account-provider-menu](/ko/docs/guides/getting-started/service-account-setup-img/service-account-provider-menu.png)

(2) 추가 버튼을 클릭합니다.

![service-account-add-button](/ko/docs/guides/getting-started/service-account-setup-img/service-account-add-button.png)

(3) 서비스 계정 생성 폼을 작성합니다.

(3-1) 기본 정보를 입력합니다.

![service-account-add-base-info](/ko/docs/guides/getting-started/service-account-setup-img/service-account-add-base-info.png)

(3-2) 해당 서비스 계정에 따른 리소스를 수집할 프로젝트를 지정합니다.

![service-account-connect-project](/ko/docs/guides/getting-started/service-account-setup-img/service-account-connect-project.png)

(3-3) 암호화 키 정보를 입력합니다.

![service-account-add-key](/ko/docs/guides/getting-started/service-account-setup-img/service-account-add-key.png)

{{<alert title="클라우드 서비스 별 계정 추가">}}
복수 개의 클라우드 서비스 계정을 추가할 수 있습니다.
클라우드 서비스 별로 필요한 요구사항이 다를 수 있으며, 자세한 사항은 아래 링크를 참고 바랍니다.

• AWS (링크)

• Azure (링크)

• GCP (링크)

• OCI (링크)

• Alibaba Cloud (링크)
{{</alert>}}

---

위의 과정을 완료하신 뒤, 클라우드포레의 서비스를 좀더 편리하고 다양하게 이용하고 싶다면 다음 가이드를 참고해주세요.

- [**에셋 인벤토리** 시작하기](/ko/docs/guides/asset-inventory/quick-start)
- [**비용 분석** 시작하기](/ko/docs/guides/cost-explorer/quick-start)
- [**얼럿 매니저** 시작하기](/ko/docs/guides/alert-manager/quick-start)
