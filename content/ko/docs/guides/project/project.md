---
title: "프로젝트"
linkTitle: "프로젝트"
weight: 3
date: 2022-06-07
description: >
    **프로젝트**는 리소스를 관리하기 위한 묶음 단위입니다.
    <br>
    <br>
    프로젝트는 반드시 특정한 [**프로젝트 그룹**](/ko/docs/guides/project/project-group)에 속해야 하며, 프로젝트 아래에는 더 이상의 계층이 존재할 수 없습니다.
    <br>
    <br>
    프로젝트에 [**멤버**](/ko/docs/guides/project/member)를 초대하고 [**역할(Role)**](/ko/docs/guides/administration/iam-role)을 부여할 수 있으며, 부여된 역할(Role)에 따라 프로젝트 리소스에 대한 접근 권한이 달라집니다.
---

## 프로젝트 생성하기

{{<alert>}}
프로젝트는 프로젝트 그룹 하위에만 존재할 수 있으므로, 먼저 **프로젝트 그룹**이 있어야 합니다.
프로젝트 그룹을 생성하는 방법은 [여기]((/ko/docs/guides/project/project-group/#프로젝트-그룹-생성하기))를 참고 하십시오.
{{</alert>}}

(1) [프로젝트] 페이지 왼쪽의 [프로젝트 그룹] 목록에서 프로젝트를 생성할 프로젝트 그룹을 선택합니다.

![project-full-page](/ko/docs/guides/project/project-img/project-full-page.png)

(2) 오른쪽 상단의 [프로젝트 생성] 버튼을 클릭합니다.

(3) [프로젝트 생성] 모달에서 프로젝트 이름을 입력한 후, [확인] 버튼을 클릭하여 프로젝트를 생성합니다.

![project-create-modal](/ko/docs/guides/project/project-img/project-create-modal.png)

## 프로젝트 목록 조회하기

프로젝트 목록에서 각 프로젝트의 주요 카테고리에 대한 리소스 현황을 간편하게 확인할 수 있습니다.
<br>
또한 검색어를 입력하여 조건에 부합하는 프로젝트 그룹과 프로젝트 목록을 확인할 수 있습니다.

### 모든 프로젝트 목록 조회하기

왼쪽의 [프로젝트 그룹]에서 [모든 프로젝트]를 선택하여 전체 프로젝트 목록을 조회할 수 있습니다.

![project-click-all-project](/ko/docs/guides/project/project-img/project-click-all-project.png)

### 프로젝트 그룹 내 프로젝트 목록 조회하기

왼쪽의 [프로젝트 그룹] 목록에서 원하는 프로젝트 그룹을 선택하여 해당 그룹에 속한 프로젝트만을 조회할 수 있습니다.

![project-click-single-project-group](/ko/docs/guides/project/project-img/project-click-single-project-group.png)

만약 선택한 프로젝트 그룹 아래에 또다른 프로젝트 그룹들이 있다면, 다른 프로젝트 그룹에 속한 프로젝트들은 여기에 표시되지 않습니다.

```
- Project Group A
    - Project Group B
        - Project B-1
        - Project B-2
    - Project A-1
    - Project A-2
```

위의 구조로 예를 들면, `Project Group A` 를 선택하면 `Project A-1`, `Project A-2` 만 목록에 표시됩니다.

## 프로젝트 살펴보기

프로젝트 목록에서 프로젝트를 선택하여 프로젝트 상세 페이지로 이동합니다.

### 프로젝트 대시보드

[요약 정보] 탭에서 프로젝트 대시보드를 통해 해당 프로젝트에 속한 리소스의 집약된 정보를 확인할 수 있습니다.

![project-dashboard-full-page](/ko/docs/guides/project/project-img/project-dashboard-full-page.png)

<br>
프로젝트 대시보드에서는 카테고리 별, 지역 별 리소스 사용 현황과 트렌드를 보여줍니다.

그 밖에도 여러 위젯들을 통해 다양한 형태로 프로젝트에 대한 통계 정보를 제공함으로써, 리소스를 더욱 효율적으로 관리하고 비용을 최소화 할 수 있도록 돕습니다.

아래는 프로젝트 대시보드의 위젯 목록입니다.

| 프로젝트 대시보드 위젯 이름 | 설명 |
| -- | -- |
| 얼럿 | 해당 프로젝트에 발생한 얼럿 정보 |
| 비용 | 해당 프로젝트의 비용 정보 |
| 오늘의 리소스 업데이트 | 로컬 시간 기준으로 자정부터 현재까지 업데이트된 리소스 정보 |
| 클라우드 서비스 | 서비스 중인 주요 클라우드 서비스 정보 |
| AWS Personal Health Dashboard | AWS의 Personal Health Dashboard 정보 |
| AWS Trusted Advisor | AWS의 Trusted Advisor 정보 |

## 프로젝트 편집하기

### 프로젝트 이름 변경하기

(1) 프로젝트 이름 우측의 [편집] 아이콘 버튼을 클릭합니다.

![project-name-edit-icon-button](/ko/docs/guides/project/project-img/project-name-edit-icon-button.png)

(2) [프로젝트 변경] 모달에서 변경할 이름을 입력한 후 [확인] 버튼을 클릭하여 프로젝트 이름을 변경합니다.

![project-name-edit-modal](/ko/docs/guides/project/project-img/project-name-edit-modal.png)

### 프로젝트 태그 관리하기

프로젝트에 태그를 추가하여 관리할 수 있습니다.
<br>
<br>

(1) [태그] 탭 내부에서 [편집] 버튼을 클릭합니다.

![project-tag-table](/ko/docs/guides/project/project-img/project-tag-table.png)

(2) [태그] 페이지에서 [태그 추가] 버튼을 클릭합니다.

(3) 추가하고자 하는 값을 `키: 값` 형태로 입력합니다.

![project-tag-add](/ko/docs/guides/project/project-img/project-tag-add.png)

(3-1) 태그를 더 추가하고자 한다면, 원하는 개수만큼 [태그 추가] 버튼을 클릭합니다.

(4) [저장] 버튼을 클릭하여 태그 추가를 완료합니다.

## 프로젝트 삭제하기

(1) 프로젝트 이름 우측의 [삭제] 아이콘 버튼을 클릭합니다.

![project-delete-icon-button](/ko/docs/guides/project/project-img/project-delete-icon-button.png)

(2) [프로젝트 삭제] 모달의 [확인] 버튼을 클릭하여 프로젝트를 삭제합니다.

![project-delete-modal](/ko/docs/guides/project/project-img/project-delete-modal.png)
