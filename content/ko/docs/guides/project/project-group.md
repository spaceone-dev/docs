---
title: "프로젝트 그룹"
linkTitle: "프로젝트 그룹"
weight: 2
date: 2022-06-07
description: >
    **프로젝트 그룹**은 여러 [**프로젝트**](/ko/docs/guides/project/project)를 묶어 관리하기 위한 개념입니다.
    <br>
    <br>
    프로젝트 그룹 하위에는 프로젝트와 프로젝트 그룹 모두가 속할 수 있으며, 이러한 트리 계층 구조를 통해 조직의 규모와 구조에 맞는 프로젝트 계층 구조를 설계하여 관리할 수 있습니다.
---

프로젝트 그룹에 초대한 [**멤버**](/ko/docs/guides/project/member)에게 [**역할(Role)**](/ko/docs/guides/administration/iam-user)을 부여하면, 해당 멤버는 하위 프로젝트 그룹과 프로젝트에 대해 동일한 역할(Role)을 가지게 됩니다.

## 프로젝트 그룹 생성하기

### 최상위 프로젝트 그룹 생성하기

(1) [프로젝트] 메뉴를 선택해 프로젝트 페이지에 진입합니다.

(2) 왼쪽의 [프로젝트 그룹] 목록에서 [모든 프로젝트]를 선택합니다.

(3) 오른쪽의 [프로젝트 그룹 생성] 버튼을 클릭합니다.

{{<alert title="[프로젝트 그룹 생성] 버튼이 보이지 않는 경우">}}

관리자 역할(Role)을 가진 사용자 중에서도 프로젝트 페이지에 대하여 수정 권한을 가진 사용자만이 최상위 프로젝트 그룹을 생성/수정/삭제할 수 있습니다.

최상위에 프로젝트 그룹을 생성할 수 있는 역할(Role)이 부여되지 않은 사용자에게는 해당 버튼이 보이지 않습니다.

![project-group-full-page](/ko/docs/guides/project/project-group-img/project-group-full-page.png)

{{</alert>}}

(4) [프로젝트 그룹 생성] 모달에서 원하는 이름을 입력한 후 [확인] 버튼을 클릭하여 프로젝트 그룹 생성을 완료합니다.

![project-group-create-modal](/ko/docs/guides/project/project-group-img/project-group-create-modal.png)

### 하위 프로젝트 그룹 생성하기

특정 프로젝트 그룹 하위에 또 다른 프로젝트 그룹을 생성하려면 아래의 단계를 따릅니다.
<br>
<br>

(1) 왼쪽의 [프로젝트 그룹] 목록에서 하위에 프로젝트 그룹을 생성하고 싶은 상위 프로젝트 그룹에 마우스 커서를 올리면, 오른쪽에 표시되는  [+] 버튼을 클릭합니다.

![project-group-create-button-from-lnb](/ko/docs/guides/project/project-group-img/project-group-create-button-from-lnb.png)

{{<alert title="[+] 버튼이 비활성화된 경우">}}

해당 프로젝트 그룹의 멤버로 초대되어 있지 않거나 해당 그룹을 생성할 수 있는 권한이 없는 경우에 해당 버튼이 비활성화됩니다. 

관리자에게 프로젝트 그룹 멤버로 초대를 요청하거나 역할(Role) 변경을 요청하세요.

[//]: # (![project-group-create-04]&#40;/ko/docs/guides/project/project-group-img/project-group-create-04.png&#41;)

{{</alert>}}

(2) [프로젝트 그룹 생성] 모달에 그룹 이름을 작성한 후 [확인] 버튼을 클릭하여 프로젝트 그룹을 생성합니다.

![project-group-child-create-modal](/ko/docs/guides/project/project-group-img/project-group-child-create-modal.png)

(3) 선택한 프로젝트 그룹 하위에 새롭게 생성한 프로젝트 그룹이 표시됩니다.

![project-group-child-tree](/ko/docs/guides/project/project-group-img/project-group-child-tree.png)

## 프로젝트 그룹 & 프로젝트 검색하기

왼쪽의 검색 창을 통해 프로젝트 그룹과 프로젝트를 검색할 수 있습니다.

검색된 프로젝트 그룹 목록에서 원하는 프로젝트 그룹을 선택하여 이동할 수 있습니다.

함께 검색된 프로젝트를 선택하면, 해당하는 프로젝트 상세 페이지가 새 탭으로 열립니다.

![project-group-search](/ko/docs/guides/project/project-group-img/project-group-search.png)

## 프로젝트 그룹 살펴보기

프로젝트 그룹을 생성하면 왼쪽의 [프로젝트 그룹] 목록에 생성한 프로젝트 그룹이 표시됩니다.

생성한 프로젝트 그룹을 선택하면 해당 그룹의 상세 정보를 확인할 수 있습니다.

![project-group-single-select-from-lnb](/ko/docs/guides/project/project-group-img/project-group-single-select-from-lnb.png)

### 프로젝트 목록 조회

프로젝트 그룹을 선택하면 해당 그룹에 속하는 프로젝트 목록을 확인할 수 있습니다. 자세한 내용은 [여기](/ko/docs/guides/project/project/#프로젝트-목록-조회하기)를 참고하세요.

## 프로젝트 그룹 편집하기

프로젝트 그룹의 이름을 변경하거나 그룹의 계층 구조를 변경할 수 있습니다.
<br>
<br>
왼쪽의 [프로젝트 그룹] 목록 상단의 [편집] 버튼을 클릭하여 편집 모드로 전환하여 편집할 수 있습니다.

![project-group-edit-button](/ko/docs/guides/project/project-group-img/project-group-edit-button.png)

{{<alert title="[편집] 버튼이 비활성화된 경우">}}
• 프로젝트 그룹을 선택하지 않은 상태에서 [편집] 버튼이 비활성화되어 있는 경우라면, 최상위 프로젝트 그룹을 수정할 수 있는 권한이 없기 때문입니다.

• 프로젝트 그룹을 선택한 상태에서도 버튼이 비활성화 되어있다면, 해당 프로젝트 그룹의 멤버로 초대되어 있지 않거나 해당 그룹을 수정할 수 있는 권한이 없는 경우입니다. 
관리자에게 [프로젝트 그룹 멤버로 초대](/ko/docs/guides/project/member/#프로젝트-그룹-멤버-초대하기)를 요청하거나 [멤버 역할(Role) 변경](/ko/docs/guides/project/member/#프로젝트-그룹-멤버-편집하기)을 요청하세요.
{{</alert>}}

### 프로젝트 그룹 이름 변경하기

(1) 왼쪽의 [프로젝트 그룹] 목록에서 이름을 변경하려는 프로젝트 그룹을 선택합니다.

(2) [프로젝트 그룹] 목록 상단의 [편집] 버튼을 클릭하여 편집 모드로 전환합니다.

(3) 선택한 프로젝트 그룹의 이름을 변경하기 위해, 해당 프로젝트 그룹을 클릭하여 입력 모드로 전환합니다.

![project-group-name-change-at-lnb](/ko/docs/guides/project/project-group-img/project-group-name-change-at-lnb.png)

(4) 입력 창이 나타나면 변경하려는 이름을 입력합니다. 그리고 입력 창을 제외한 다른 곳을 마우스로 클릭하여, 읽기 모드로 전환합니다.

### 프로젝트 그룹 계층 구조 편집하기

프로젝트 그룹 목록에서 드래그 앤 드롭을 통해 프로젝트 그룹의 계층 구조를 편리하게 편집할 수 있습니다.
<br>
<br>

(1) 왼쪽의 [프로젝트 그룹] 목록에서 계층 구조를 편집하려는 프로젝트 그룹을 선택합니다.

(2) [프로젝트 그룹] 목록 상단의 [편집] 버튼을 클릭하여 편집 모드로 전환합니다.

(3) 이동을 원하는 프로젝트 그룹을 클릭한 상태로 끌어서 원하는 위치에 내려놓습니다.

![project-group-project-tree-change](/ko/docs/guides/project/project-group-img/project-group-project-tree-change.png)

{{<alert title="프로젝트 그룹 이동이 안되는 경우">}}
• 선택한 프로젝트 그룹을 수정할 수 있는 권한이 없는 경우: 만약 편집 모드에서 프로젝트 그룹 선택이 안된다면, 해당 프로젝트 그룹을 이동할 수 있는 권한이 없는 것입니다.

• 내려놓은 위치의 상위 프로젝트 그룹을 수정할 수 있는 권한이 없는 경우: 만약 선택한 프로젝트 그룹을 내려놓으려는 위치가 흐릿하게 표현되어 있다면, 이동하려는 프로젝트 그룹에 대하여 수정 권한이 없기 때문입니다.
{{</alert>}}

### 프로젝트 이동하기

프로젝트 그룹 뿐만 아니라 그 하위에 존재하는 프로젝트 또한 다른 프로젝트 그룹으로 이동이 가능합니다.
<br>
<br>

(1) 왼쪽의 [프로젝트 그룹] 목록에서 이동하고자 하는 프로젝트를 가지고 있는 프로젝트 그룹을 선택합니다.

(2) [프로젝트 그룹] 목록 상단의 [편집] 버튼을 클릭하여 편집 모드로 전환합니다.

{{<alert title="[편집] 버튼이 활성화되지 않는 경우">}}
해당 프로젝트 그룹을 수정할 수 있는 권한이 없기 때문입니다. 
해당하는 그룹의 하위 프로젝트에 대하여서는 수정 권한이 있더라도, 프로젝트 그룹에는 권한이 없을 수 있습니다. 
프로젝트 그룹 관리자에게 [멤버 역할(Role) 변경](/ko/docs/guides/project/member/#프로젝트-그룹-멤버-편집하기)을 요청하세요.
{{</alert>}}

(3) [프로젝트 그룹 계층 구조 편집 방법](/ko/docs/guides/project/project-group/#프로젝트-그룹-계층-구조-편집하기)과 동일한 방법으로 프로젝트를 이동합니다.

## 프로젝트 그룹 삭제하기

(1) 왼쪽의 [프로젝트 그룹] 목록에서 삭제하려는 프로젝트 그룹을 선택합니다.

(2) 오른쪽 상단의 [설정] 버튼을 클릭한 후, 드롭다운에서 [선택한 그룹 삭제]를 선택합니다.

![project-group-delete-menu](/ko/docs/guides/project/project-group-img/project-group-delete-menu.png)

(2-1) [프로젝트 그룹 삭제] 모달에서 [확인] 버튼을 클릭하여 프로젝트 그룹을 영구히 삭제합니다.

![project-group-delete-modal](/ko/docs/guides/project/project-group-img/project-group-delete-modal.png)

{{<alert title="프로젝트 그룹 삭제가 안되는 경우">}}

• 선택한 프로젝트 그룹에 속한 프로젝트가 있는 경우, 프로젝트 그룹이 삭제되지 않습니다.

• 선택한 프로젝트 그룹에 속하지 않더라도, 그 하위의 그룹들에 프로젝트가 있는 경우, 프로젝트 그룹이 삭제되지 않습니다.
<br>
<br>
위의 두 가지 경우에는 프로젝트를 먼저 삭제해야 합니다. 프로젝트 삭제 방법은 [여기](/ko/docs/guides/project/project/#프로젝트-삭제하기)를 참고하세요.

{{</alert>}}
