---
title: "Member"
linkTitle: "Member"
weight: 4
date: 2022-06-07
description: ""
---
<br>

[**프로젝트**](/ko/docs/guides/project/project)와 [**프로젝트 그룹**](/ko/docs/guides/project/project-group)에 **멤버**를 초대하고 [**역할(Role)**](/ko/docs/guides/administration/iam-role)을 부여할 수 있습니다.
<br>
<br>
멤버들에게는 반드시 하나의 역할(Role)이 부여되며, 이를 통해 해당 프로젝트와 프로젝트 그룹에 대한 접근을 관리할 수 있습니다.

역할(Role)에 연결된 [**정책(Policy)**](/ko/docs/guides/administration/iam-policy)에 따라 접근 권한이 달라집니다.
<br>
<br>
역할(Role)은 아래의 규칙에 따라 하위 계층에 전파됩니다.
- **프로젝트 그룹 멤버 역할**은 그 하위에 있는 모든 프로젝트 그룹과 프로젝트에 대하여서도 동일하게 적용됩니다.
- **프로젝트 멤버 역할**은 해당 프로젝트에만 적용됩니다.
- 상위 계층에 존재하는 여러 프로젝트 그룹에 대하여 멤버 역할이 존재하는 경우, 각각에 부여된 역할이 모두 병합되어 적용됩니다.


## 프로젝트 그룹 멤버 관리하기
<br>

[프로젝트 그룹 멤버 관리] 페이지로 이동하여 멤버를 관리할 수 있습니다.
<br>
<br>

(1) [프로젝트] 메뉴를 선택하여 프로젝트 페이지로 이동합니다.

(2) 왼쪽의 [프로젝트 그룹] 목록에서 멤버를 관리하려는 프로젝트 그룹을 선택합니다.

(3) 오른쪽 상단에 [프로젝트 그룹 멤버 관리] 아이콘 버튼을 클릭합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/795ada39-1a85-4a94-8ec8-060432f44ae8/Untitled.png)

{{<alert title="">}}
해당 프로젝트 그룹을 관리할 수 있는 권한이 있어야 오른쪽 상단의 버튼이 보입니다.
{{</alert>}}

(4) 프로젝트 그룹 멤버 관리 페이지에서 검색어를 입력하여 조건에 부합하는 프로젝트 목록을 조회하고, 새로운 멤버를 초대하거나, 멤버를 편집 / 삭제할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/63805943-2e6b-40d6-a68f-9e672b1d49a7/Untitled.png)

{{<alert title="">}}
해당 프로젝트 그룹을 관리할 수 있는 권한이 있어야 멤버 초대 / 편집 / 삭제가 가능합니다.
{{</alert>}}

### 프로젝트 그룹 멤버 초대하기

(1) [프로젝트 그룹 멤버 관리] 페이지에서 [초대] 버튼을 클릭하여 [멤버 초대] 모달을 엽니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3fbee7c6-d7dd-48cc-8fa1-caa12c251834/Untitled.png)

(2) 초대하려는 멤버를 선택합니다. 한 번에 여러 멤버를 선택하여 초대할 수 있습니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2addd334-1b6c-495c-8d20-72344d0841f9/Untitled.png)

(3) 초대할 멤버들에게 부여할 역할(Role)을 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/424d247f-d473-43f0-8c48-d594efc1463c/Untitled.png)

{{<alert title="멤버 역할(Role)">}}

프로젝트의 멤버에게 부여할 수 있는 역할(Role)은 `User` 타입의 역할만 가능합니다. 

자세한 설명은 [여기](/ko/docs/guides/administration/iam-role)를 참고하세요.

{{</alert>}}

(4) 초대할 멤버들에 대한 라벨을 입력 후, 엔터 키를 눌러 추가합니다.

(5) [확인] 버튼을 클릭하여 멤버 초대를 완료합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cd480753-44d2-44ef-b2fc-600675e1bdcc/Untitled.png)

### 프로젝트 그룹 멤버 편집하기

프로젝트 그룹에 대하여 멤버에게 부여한 역할(Role)과 라벨을 변경할 수 있습니다.
<br>
<br>

(1) [프로젝트 그룹 멤버 관리] 페이지에서 편집하려는 멤버를 선택합니다.

(2) [작업] 드롭다운에서 [편집]을 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1f54c30e-50a8-4064-b958-239b842e44ec/Untitled.png)

(3) [멤버 정보 변경] 모달에서 변경하려는 내용을 입력한 후 [확인] 버튼을 클릭하여 변경을 완료합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a3072023-a0c4-47d2-bd77-70b497fde3a1/Untitled.png)

### 프로젝트 그룹 멤버 삭제하기

(1) [프로젝트 그룹 멤버 관리] 페이지에서 삭제하려는 멤버를 선택합니다. 복수 선택이 가능합니다.

(2) [작업] 드롭다운에서 [삭제]를 선택합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7ead56ce-51e7-448e-b441-b7df25cf957a/Untitled.png)

(3) [멤버 제거] 모달에서 [확인] 버튼을 클릭하여 해당 멤버를 제거합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bfc290c4-982e-420c-bde3-567c8710c755/Untitled.png)

## 프로젝트 멤버 관리하기
<br>

프로젝트 상세 페이지의 [멤버] 탭으로 이동하여 멤버를 관리할 수 있으며, 모든 방식과 내용은 프로젝트 그룹 멤버 관리하기(링크)와 동일합니다.
<br>
<br>

(1) 프로젝트 페이지에서 멤버를 관리하려는 프로젝트를 선택하여 프로젝트 상세 페이지로 이동합니다.

(2) [멤버] 탭을 선택합니다.
![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8cba04ff-8c71-4f26-b036-767bd1429733/Untitled.png)