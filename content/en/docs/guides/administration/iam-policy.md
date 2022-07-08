---
title: "[IAM] Policy"
linkTitle: "[IAM] Policy"
weight: 3
date: 2022-06-07
description: >
    **정책**은 실행 가능한 API 들의 권한으로, 사용자들에게 부여할 [역할](/ko/docs/guides/administration/iam-role)을 생성할 때 사용합니다.
---

## 정책이란?

정책(Policy)은 실행 가능한 API 들의 권한을 의미하며, Managed / Custom 타입의 정책이 존재합니다.

|            | Managed                                                                                                                | Custom                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| 정의         | Repository 서비스에 Global하게 정의된 Policy로,<br />Policy를 전체 시스템 Admin이 직접 관리하여 공유합니다.<br />대부분의 사용자들이 활용하기 편리한 공통 Policy입니다. | Domain 별로 자체 정의된 Policy로,<br />각 Domain별로 세부적인 권한을 관리하기에 유용합니다. |
| 생성, 수정, 삭제 | X (불가능)                                                                                                                | O (가능)                                                          |
| 읽기         | O (가능)                                                                                                                 | O (가능)                                                          |

{{<alert>}}
Repository 서비스란 Marketplace 에 연결하기 위한 공유 저장소 서비스를 말합니다.
{{</alert>}}

자세한 내용은 [Understanding Policy](/ko/docs/concepts/identity/rbac/understanding-policy)를 참고해주세요.


{{<alert>}}
Custom 정책만 생성 / 수정 / 삭제가 가능하니, 해당 기능을 이용할 때 타입을 확인 후 진행해주시길 바랍니다.
{{</alert>}}

## 정책 조회하기

조회하고자 하는 정책의 타입을 클릭 한 후, 테이블에 연결된 ID 필드를 통해 정책 상세페이지에 진입할 수 있습니다.

![policy-full-page](/ko/docs/guides/administration/iam-policy-img/policy-full-page.png)

## 정책 생성하기

우측의 [생성] 버튼을 통해서 정책을 생성하는 페이지에 진입합니다.

![policy-create-button](/ko/docs/guides/administration/iam-policy-img/policy-create-button.png)

이름과 설명, 권한을 입력 후 정책을 생성할 수 있습니다.

부여할 권한은 복수개를 입력할 수 있으며, 개행으로 구분합니다.

권한의 예시는 다음과 같으며, `{서비스}.{리소스}.{동작}` 의 형식을 지닙니다.

| 예시                      | 예시에 대한 설명                  |
|-------------------------|----------------------------|
| identity.Project.*      | Project 리소스에 대한 모든 권한      |
| identity.ProjectGroup.* | ProjectGroup 리소스에 대한 모든 권한 |
| identity.User.get       | User 리소스에 대한 get 권한        |
| identity.User.update    | User 리소스에 대한 update 권한     |
| identity.User.list      | User 리소스에 대한 list 권한       |

서비스와 리소스 등에 대한 자세한 정보는 (여기)를 참고 하십시오.

## 정책 편집하기

편집하고자 하는 정책의 페이지에 진입합니다.

### 정책 이름 편집하기

제목 우측의 편집 아이콘 버튼을 누른 후 생성된 모달에서 정책의 이름을 편집할 수 있습니다.

![policy-edit-icon-button](/ko/docs/guides/administration/iam-policy-img/policy-edit-icon-button.png)

### 정책 내용 편집하기

설명란의 입력창에서 설명을 수정할 수 있습니다.

하단의 코드블럭에서 권한을 수정할 수 있습니다. 복수개의 권한은 개행으로 구분됩니다.

![policy-detail-page-with-new-permission](/ko/docs/guides/administration/iam-policy-img/policy-detail-page-with-new-permission.png)

## 정책 삭제하기

삭제하고자 하는 정책 페이지에 진입합니다.

삭제 아이콘 버튼을 누른 후 생성된 모달에서 정책을 삭제할 수 있습니다.

![policy-delete-icon-button](/ko/docs/guides/administration/iam-policy-img/policy-delete-icon-button.png)

이때 역할(Role)이 연결되어있는 정책은 삭제가 불가하오니, 역할(Role) 페이지로 이동하여 검토를 진행해주세요.

![policy-cannot-delete-modal](/ko/docs/guides/administration/iam-policy-img/policy-cannot-delete-modal.png)
