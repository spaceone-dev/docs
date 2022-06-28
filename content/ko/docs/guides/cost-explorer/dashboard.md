---
title: "대시보드"
linkTitle: "대시보드"
weight: 2
date: 2022-06-22
description: >
    **비용 대시보드**에서 사용자는 기본 대시보드, 혹은 원하는 위젯을 조합한 커스텀 대시보드를 통해 비용 데이터를 한눈에 볼 수 있습니다.
---

## 기본 대시보드
아래는 현재 기본으로 제공되는 대시보드입니다.

### 월별 비용 통계
클라우드 비용 발생 현황 및 예산 사용 상태를 다양한 그룹별 통계 기준으로 차트화한 대시보드입니다.

![cost-dashboard-intro-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-intro-01.png)

### CDN 및 트래픽 비용
AWS Data-Transfer와 AWS CloudFront의 데이터 전송 및 비용 발생 현황을 차트화한 대시보드입니다.

![cost-dashboard-intro-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-intro-02.png)


## 대시보드 생성하기
(1) [비용 관리 > 대시보드] 페이지의 좌측 메뉴 목록에서 [대시보드 생성] 아이콘 버튼을 클릭합니다.

![cost-dashboard-create-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-create-01.png)

(2) [대시보드 생성] 페이지에 진입하여 새로운 대시보드에 적용될 템플릿을 선택합니다.

(2-1) 클라우드포레가 제공하는 기본 템플릿을 선택하거나, 기존 대시보드를 복제할 수 있습니다.

![cost-dashboard-create-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-create-02.png)

(2-2) 기존 대시보드를 복제할 경우, 해당 대시보드에 적용된 필터도 포함할 것인지 선택할 수 있습니다.

![cost-dashboard-create-03](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-create-03.png)

(3) 노출방식을 선택합니다. `My Dashboard`는 사용자 본인에게만, `Public`은 [비용 관리 > 대시보드] 페이지에 대한 `VIEW` 권한을 가진 모든 사용자들에게 보여집니다.

![cost-dashboard-create-04](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-create-04.png)

{{<alert title="Public 옵션이 보이지 않는 경우">}}
[비용 관리 > 대시보드] 페이지에 대한 `MANAGE` 권한이 있을 경우 Public과 My Dashboard를 모두 생성할 수 있습니다. 하지만 사용자가 `VIEW` 권한만을 가지고 있을 경우 My Dashboard만 생성할 수 있습니다.

**접근 권한**을 설정하는 방법은 [여기](/ko/docs/guides/administration/iam-role/#역할-생성하기)를 참고하세요.
{{</alert>}}

(4) [생성] 버튼을 클릭합니다.


## 대시보드 삭제하기

(1) 왼쪽의 대시보드 목록에서 삭제하려는 대시보드를 선택합니다.

![cost-dashboard-delete-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-delete-01.png)

(2) 선택한 대시보드 이름 옆의 [설정] 아이콘 버튼을 클릭한 뒤, 드롭다운에서 [삭제]를 선택합니다.

![cost-dashboard-delete-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-delete-02.png)

{{<alert title="[삭제] 버튼이 비활성화 되어 있는 경우">}}
[비용 관리 > 대시보드] 페이지에 대한 `MANAGE` 권한이 없거나, 삭제하려는 대시보드가 홈 대시보드로 설정되어 있으면 삭제할 수 없습니다.
{{</alert>}}

(3) [대시보드 삭제] 모달의 [확인] 버튼을 클릭하여 대시보드를 삭제합니다.

![cost-dashboard-delete-03](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-delete-03.png)


## 대시보드 편집하기
대시보드 페이지에서 오른쪽의 [편집] 버튼을 클릭하면 대시보드 편집 페이지로 이동하여, 대시보드의 이름이나 위젯 등을 편집할 수 있습니다.

![cost-dashboard-edit-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-edit-01.png)

{{<alert title="[편집] 버튼이 비활성화 되어 있는 경우">}}
[비용 관리 > 대시보드] 페이지에 대한 MANAGE 권한이 없으면 대시보드를 편집할 수 없습니다.
{{</alert>}}

### 대시보드 이름 편집하기
상단의 입력 폼에서 대시보드의 이름을 편집할 수 있습니다.

![cost-dashboard-edit-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-edit-02.png)

### 위젯 추가하기
추가할 수 있는 위젯은 두 가지로, 기본 위젯과 커스텀 위젯이 있습니다.
기본 위젯은 클라우드포레에서 제공하는 위젯 템플릿으로 만들 수 있는 위젯이며, 커스텀 위젯은 [비용 관리 > 비용 분석] 페이지에서 생성한 쿼리 기반의 위젯입니다.

#### 기본 위젯 추가하기
(1) 오른쪽의 [위젯 추가] 버튼을 클릭합니다.

![cost-dashboard-basic-widget-add-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-basic-widget-add-01.png)

(2) [새로운 위젯 추가] 모달에서 [기본] 탭을 선택합니다.

(2-1) 왼쪽의 [위젯 템플릿] 목록에서 템플릿을 선택합니다.

![cost-dashboard-basic-widget-add-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-basic-widget-add-02.png)

(2-2) 위젯의 [이름]을 입력합니다. 위젯의 종류에 따라 [그룹별 통계]를 선택해야 하는 경우도 있습니다.

![cost-dashboard-basic-widget-add-03](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-basic-widget-add-03.png)

(3) [확인] 버튼을 클릭하여 위젯 추가를 완료합니다.

#### 커스텀 위젯 추가하기
{{<alert title="비용 분석 쿼리">}}
커스텀 위젯을 생성하기 위해서는 **비용 분석 쿼리**가 필요합니다.
비용 분석 쿼리는 [비용 관리 > 비용 분석] 페이지에서 생성할 수 있습니다.
자세한 방법은 여기를 참고하세요.
{{</alert>}}

(1) 오른쪽의 [위젯 추가] 버튼을 클릭합니다.

![cost-dashboard-custom-widget-add-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-custom-widget-add-01.png)

(2) [새로운 위젯 추가] 모달에서 [커스텀] 탭을 선택합니다.

(2-1) 왼쪽 하단의 [비용 분석 쿼리] 목록에서, 커스텀 위젯에 적용하고 싶은 쿼리의 [커스텀 위젯에 추가] 버튼을 클릭합니다.

![cost-dashboard-custom-widget-add-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-custom-widget-add-02.png)

(2-2) 추가된 커스텀 위젯이 왼쪽 상단의 [위젯 템플릿] 목록에 나타나면, 그것을 선택합니다.

![cost-dashboard-custom-widget-add-03](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-custom-widget-add-03.png)

(2-3) 위젯의 이름을 입력합니다.

![cost-dashboard-custom-widget-add-04](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-custom-widget-add-04.png)

(2-4) [확인] 버튼을 클릭하여 위젯 추가를 완료합니다.


### 위젯 순서 변경하기
위젯 목록에서 위젯 이름의 왼쪽에 있는 [순서 변경] 아이콘 버튼을 드래그 & 드롭하여 순서를 변경할 수 있습니다.

![cost-dashboard-edit-widget-order-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-edit-widget-order-01.png)


### 위젯 편집하기
(1) 위젯의 우측 상단에 있는 [편집] 아이콘 버튼을 클릭합니다.

![cost-dashboard-widget-edit-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-edit-widget-01.png)

(2) 위젯의 이름이나 그룹별 통계를 편집한 뒤, [확인] 버튼을 클릭합니다.

![cost-dashboard-widget-edit-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-edit-widget-02.png)

### 위젯 삭제하기
(1) 위젯의 우측 상단에 있는 [삭제] 아이콘 버튼을 클릭합니다.

![cost-dashboard-widget-delete-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-widget-delete-01.png)

(2) [위젯 삭제] 모달이 열리면 [확인] 버튼을 클릭합니다.

![cost-dashboard-widget-delete-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-widget-delete-02.png)


## 대시보드 설정하기
### 대시보드 이름 편집하기
(1) 대시보드 제목 옆의 [편집] 아이콘 버튼을 클릭합니다.

![cost-dashboard-name-edit-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-name-edit-01.png)

(2) 대시보드의 이름을 변경한 뒤 [확인] 버튼을 클릭합니다.

![cost-dashboard-name-edit-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-name-edit-02.png)


### 필터 설정하기
필터를 설정하면 대시보드의 데이터를 원하는 조건으로 필터링하여 볼 수 있습니다.

(1) 대시보드 상단의 [필터] 아이콘 버튼을 클릭합니다.

![cost-dashboard-filter-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-filter-01.png)

(2) 원하는 필터를 선택한 뒤, [확인] 버튼을 클릭합니다.

![cost-dashboard-filter-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-filter-02.png)


### 기간 설정하기
대시보드 우측 상단의 [기간] 드롭다운에서 기간 메뉴를 선택하거나, [기간 선택] 메뉴를 통해 기간을 직접 설정할 수 있습니다.

![cost-dashboard-period-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-period-01.png)

직접 설정할 경우, 월 단위로 최대 12개월까지 설정 가능합니다.

![cost-dashboard-period-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-period-02.png)

만약 [기간] 드롭다운 왼쪽의 [날짜 고정] 옵션을 체크한다면, 설정한 날짜가 새로고침 시에도 유지됩니다.

![cost-dashboard-period-03](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-period-03.png)

### 환율 설정하기
대시보드 우측 상단의 [환율] 드롭다운에서 환율을 선택할 수 있습니다. 선택 시 모든 차트와 테이블의 데이터가 해당 환율로 변환되어 보여집니다.

![cost-dashboard-currency-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-currency-01.png)

### 홈 대시보드 설정하기
특정 대시보드를 홈 대시보드로 설정하면 비용 관리 > 대시보드 페이지로 진입 시 해당 대시보드 페이지로 바로 이동합니다. 홈 대시보드 설정은 사용자의 브라우저에 저장되는 정보로, 다른 사용자들과 공유되지 않습니다.

![cost-dashboard-home-dashboard-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-home-dashboard-01.png)

## 대시보드 복제하기 
대시보드를 복제할 시 다음 항목들을 설정할 수 있습니다.
- 대시보드 이름
- 필터 복제 여부: 해당 옵션을 활성화하면 대시보드의 필터 설정까지 그대로 복제합니다.
- 대시보드 노출방식: `Public`과 `My Dashboard` 중 하나를 선택합니다.

![cost-dashboard-duplicate-dashboard-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-duplicate-dashboard-01.png)
![cost-dashboard-duplicate-dashboard-02](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-duplicate-dashboard-02.png)

## 대시보드 PDF 다운로드하기
대시보드 우측 상단의 [다운로드] 아이콘 버튼을 클릭하면 대시보드를 PDF로 다운로드할 수 있습니다.

![cost-dashboard-pdf-download-01](/ko/docs/guides/cost-explorer/dashboard-img/cost-dashboard-pdf-download-01.png)
