---
title: "프로젝트 설정"
linkTitle: "프로젝트 설정"
weight: 2
date: 2022-06-07
description: >
    체계적인 리소스 관리를 위해 [**프로젝트**](/ko/docs/guides/project/project)와 [**프로젝트 그룹**](/ko/docs/guides/project/project-group)을 생성합니다.
---

## 프로젝트 그룹 생성하기

프로젝트는 반드시 하나의 프로젝트 그룹에 속해있어야 하므로, 프로젝트를 생성하기 이전에 먼저 프로젝트 그룹을 생성해야 합니다.

### Steps

(1) [프로젝트] 메뉴를 선택해 프로젝트 페이지에 진입합니다.

(2) [프로젝트 그룹 생성하기] 버튼을 클릭합니다.

![project-group-create-button](/ko/docs/guides/getting-started/project-setup-img/project-group-create-button.png)

(3) [프로젝트 그룹 생성] 모달에서 프로젝트 그룹 이름을 입력 후 [확인] 버튼을 클릭하여 프로젝트 그룹을 생성합니다.

![project-group-create-modal](/ko/docs/guides/getting-started/project-setup-img/project-group-create-modal.png)

## 프로젝트 생성하기

프로젝트 그룹을 생성한 뒤, 그 하위에 속하게 될 프로젝트를 생성합니다.

### Steps

(1) 왼쪽의 프로젝트 그룹 목록에서, 앞에서 생성한 프로젝트 그룹을 선택합니다.

![project-group-select](/ko/docs/guides/getting-started/project-setup-img/project-group-select.png)

(2) 오른쪽 상단의 [프로젝트 생성] 버튼을 클릭합니다.

(3) [프로젝트 생성] 모달에서 프로젝트 이름을 입력한 후, [확인] 버튼을 클릭하여 프로젝트를 생성합니다.

![project-create-modal](/ko/docs/guides/getting-started/project-setup-img/project-create-modal.png)


## 프로젝트 그룹 멤버 초대하기

프로젝트 그룹에 사용자를 초대하여 프로젝트 그룹의 [**멤버**](/ko/docs/guides/project/member)로 등록할 수 있습니다.

{{<alert title="프로젝트 그룹 멤버 역할(Role)">}}
초대된 멤버들은 해당 프로젝트 그룹에 대하여 반드시 하나의 역할(Role)을 가지게 되며, 그 하위에 있는 모든 프로젝트 그룹과 프로젝트에 대하여서도 동일한 역할(Role)이 적용됩니다. 

상세한 내용은 [여기](/ko/docs/guides/administration/iam-role)를 참고하세요.
{{</alert>}}

### Steps

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
