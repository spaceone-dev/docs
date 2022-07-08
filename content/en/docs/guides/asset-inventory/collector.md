---
title: "Collector"
linkTitle: "Collector"
weight: 4
date: 2022-06-07
description: >
    클라우드포레는 **컬렉터**를 통해 [클라우드 리소스](/ko/docs/guides/asset-inventory)들을 수집하며, 스케줄링을 통해 수집 시기를 결정할 수 있습니다.

---

## 개요

컬렉터로 데이터를 수집하기 위해서는 다음 두 가지 요소가 필요합니다.

### 컬렉터 플러그인

[클라우드 프로바이더](/ko/docs/guides/asset-inventory)로부터 어떤 리소스들을 수집할지, 수집한 데이터들을 어떻게 화면에 보여줄지에 대한 스펙이 정의된 요소입니다. 

프로바이더 별로 가지고 있는 데이터의 구조와 내용이 상이하므로 컬렉터는 철저히 **컬렉터 플러그인**에 의존하여 리소스들을 수집합니다.

이에 대한 자세한 설명은 [여기](/ko/docs/guides/plugins/asset-inventory-collector)를 참고 하십시오.
 
### 서비스 계정 

리소스를 수집하기 위해서는 [클라우드 프로바이더](/ko/docs/guides/asset-inventory)의 계정에 연결이 필요합니다.

**서비스 계정**은 프로바이더의 계정에 연결하기 위한 계정 정보입니다. 

컬렉터는 기존에 프로바이더 별로 만들어져 있는 서비스 계정을 통해 프로바이더 계정에 접근합니다. 

이에 대한 자세한 설명은 [여기](/ko/docs/guides/asset-inventory/service-account)를 참고 하십시오.

## 컬렉터 생성하기

(1) 왼쪽 상단의 [생성] 버튼을 클릭합니다.

![collector-create-button](/ko/docs/guides/asset-inventory/collector-img/collector-create-button.png)

(2) 플러그인 목록 페이지에서 원하는 컬렉터 플러그인을 찾아 [생성] 버튼을 클릭합니다.

![collector-plugin-lists](/ko/docs/guides/asset-inventory/collector-img/collector-plugin-lists.png)

(3) [컬렉터 생성] 페이지에서 아래 단계를 거칩니다.

(3-1) [컬렉터 설정] 탭에서 이름과 플러그인의 버전을 선택합니다.

![collector-create-base-info](/ko/docs/guides/asset-inventory/collector-img/collector-create-base-info.png)

{{<alert title="버전 및 자동 업그레이드">}}
버전은 앞에서 선택한 컬렉터 플러그인의 버전을 의미하며, 자동 업그레이드를 비활성화하면 선택할 수 있습니다. 이 경우에는 항상 지정한 버전의 플러그인으로 데이터가 수집됩니다.

반면, 자동 업그레이드를 활성화하면 항상 최신 버전의 플러그인으로 데이터가 수집됩니다.
{{</alert>}}

(3-2) 필요한 경우, [태그 추가] 탭에서 컬렉터에 대한 추가 정보를 입력합니다.

![collector-create-tags](/ko/docs/guides/asset-inventory/collector-img/collector-create-tags.png)

(4) [확인] 버튼을 클릭하여 컬렉터 생성을 완료합니다.

## 컬렉터 목록 조회하기

컬렉터 페이지에서 생성되어 있는 모든 컬렉터 목록을 조회할 수 있습니다.

**고급 검색**을 통해 세밀한 조건으로 목록을 필터링할 수 있습니다. 상세 설명은 [여기](/ko/docs/guides/advanced/search/)를 참고 하십시오.

![collector-list-inquiry](/ko/docs/guides/asset-inventory/collector-img/collector-list-inquiry.png)

## 컬렉터 상세 정보 확인하기

(1) 컬렉터 목록에서 상세 내용을 확인하고 싶은 컬렉터를 선택합니다.

(2) 목록 아래의 [상세 정보] 탭에서 컬렉터의 상세한 정보를 확인할 수 있습니다.

![collector-detail-info-tab](/ko/docs/guides/asset-inventory/collector-img/collector-detail-info-tab.png)

## 컬렉터 편집하기

(1) 컬렉터 목록에서 편집하고자 하는 컬렉터를 선택합니다.

(2) [작업] 드롭다운에서 [편집] 메뉴를 선택합니다.

![collector-edit-menu](/ko/docs/guides/asset-inventory/collector-img/collector-edit-menu.png)

(3) [컬렉터 편집] 모달에서 값을 변경한 후 [확인] 버튼을 클릭하여 편집을 완료합니다.

![collector-edit-modal](/ko/docs/guides/asset-inventory/collector-img/collector-edit-modal.png)

## 컬렉터 활성화/비활성화 하기

컬렉터를 활성화하거나 비활성화할 수 있습니다. 컬렉터를 비활성화하면 스케줄러에 의한 데이터 수집이 이뤄지지 않습니다.

(1) 컬렉터 목록에서 활성화 혹은 비활성화 하려는 컬렉터를 선택합니다. 여러 개를 선택하여 일괄 적용이 가능합니다.

(2) [작업] 드롭다운에서 [활성화] 혹은 [비활성화] 항목을 선택합니다.

![collector-multi-select-for-disable](/ko/docs/guides/asset-inventory/collector-img/collector-multi-select-for-disable.png)

(3) [컬렉터 활성화] 혹은 [컬렉터 비활성화] 모달에서 선택한 항목들을 확인한 후, [확인] 버튼을 클릭하여 활성화/비활성화를 완료합니다.

![collector-disable-modal](/ko/docs/guides/asset-inventory/collector-img/collector-disable-modal.png)

## 컬렉터 삭제하기

컬렉터를 영구히 삭제할 수 있습니다.

(1) 컬렉터 목록에서 삭제하려는 컬렉터를 선택합니다. 여러 개를 선택하여 일괄 삭제가 가능합니다.

(2) [작업] 드롭다운에서 [삭제] 메뉴를 선택합니다.

![collector-delete-menu](/ko/docs/guides/asset-inventory/collector-img/collector-delete-menu.png)

(3) [컬렉터 삭제] 모달에서 선택한 항목들을 확인한 후, [확인] 버튼을 클릭하여 삭제를 완료합니다.

![collector-delete-modal](/ko/docs/guides/asset-inventory/collector-img/collector-delete-modal.png)

## 일회성 데이터 수집하기

스케줄링하지 않고 일회성으로 데이터를 수집할 수 있습니다.

이 기능을 사용하면 컬렉터가 비활성화 상태여도 데이터 수집이 이뤄집니다.

데이터 수집은 두 가지 방식으로 동작합니다.

- [모든 서비스 계정에 대하여 데이터 수집](/ko/docs/guides/asset-inventory/collector/#연결된-모든-서비스-계정에-대하여-데이터-수집하기)
- [하나의 서비스 계정에 대하여 데이터 수집](/ko/docs/guides/asset-inventory/collector/#하나의-서비스-계정에-대하여-데이터-수집하기)

### 연결된 모든 서비스 계정에 대하여 데이터 수집하기

컬렉터는 데이터 수집을 위해 [프로바이더](/ko/docs/guides/asset-inventory)의 계정 정보를 필요로 하며, 이는 [서비스 계정](/ko/docs/guides/asset-inventory/service-account)을 통해 등록됩니다.

컬렉터는 기본적으로 프로바이더의 모든 서비스 계정에 대하여 데이터를 수집합니다.

(1) 컬렉터 목록에서 데이터를 수집할 컬렉터를 선택합니다.

(2) [작업] 드롭다운에서 [데이터 수집] 메뉴를 선택합니다.

![collector-collect-data-menu](/ko/docs/guides/asset-inventory/collector-img/collector-collect-data-menu.png)

(3) [데이터 수집] 모달에서 [확인] 버튼을 클릭하여 데이터 수집을 시작합니다.

![collector-collect-data-modal](/ko/docs/guides/asset-inventory/collector-img/collector-collect-data-modal.png)

(4) 해당 컬렉터가 데이터 수집을 완료했는지 여부는 [컬렉터 히스토리](ko/docs/guides/asset-inventory/collector/#데이터-수집-내역-확인하기)에서 확인 가능합니다. 선택한 컬렉터의 [상세 보기] 링크를 클릭하여 해당 페이지로 이동할 수 있습니다.

![collector-history-at-table](/ko/docs/guides/asset-inventory/collector-img/collector-history-at-table.png)

### 하나의 서비스 계정에 대하여 데이터 수집하기

컬렉터로 데이터를 수집할 때에 특정한 클라우드 프로바이더 계정의 데이터만을 수집할 수도 있습니다.

(1) 컬렉터 목록에서 데이터를 수집할 컬렉터를 선택합니다.

(2) 아래의 [서비스 계정] 탭을 선택합니다.

![collector-service-account-tab](/ko/docs/guides/asset-inventory/collector-img/collector-service-account-tab.png)

여기에는 선택한 컬렉터를 통해 데이터 수집 시 사용되는 서비스 계정 목록이 표시됩니다.

{{<alert title="서비스 계정">}}
[서비스 계정](/ko/docs/guides/asset-inventory/service-account)은 데이터 수집에 필요한 프로바이더 계정에 대한 접근 정보를 가지고 있습니다.

만약 여기에서 아무런 정보를 확인할 수 없다면, 프로바이더에 접근할 수 있는 계정 정보가 없는 것이므로 컬렉터가 실행되더라도 데이터 수집이 일어나지 않습니다.

따라서 컬렉터로 데이터를 수집하려면 [서비스 계정] 메뉴에서 해당 프로바이더의 계정 정보를 먼저 등록해두어야 합니다.

{{</alert>}}

(3) 데이터를 수집하고자 하는 서비스 계정의 오른쪽 [데이터 수집] 버튼을 클릭합니다.

(4) [데이터 수집] 모달에서 [확인] 버튼을 클릭하여 데이터 수집을 시작합니다.

![collector-data-collect-one-account-modal](/ko/docs/guides/asset-inventory/collector-img/collector-data-collect-one-account-modal.png)

## 데이터 수집 스케줄 설정하기

주기적으로 리소스들을 수집해오도록 컬렉터에 스케줄링을 할 수 있습니다.

(1) 컬렉터 목록에서 스케줄을 설정할 컬렉터를 선택합니다.

(2) 아래의 [스케줄] 탭을 선택합니다.

여기에서 스케줄 목록을 확인하거나 추가/변경/삭제할 수 있습니다.

![collector-schedule-tab](/ko/docs/guides/asset-inventory/collector-img/collector-schedule-tab.png)

### 스케줄 추가하기

(1) [추가] 버튼을 클릭합니다.

(2) [스케줄 추가] 모달에서 값을 입력합니다.

![collector-schedule-modal](/ko/docs/guides/asset-inventory/collector-img/collector-schedule-modal.png)

(2-1) 식별 가능한 이름과 설정한 스케줄이 동작할 시간대(타임존)를 선택합니다.

(2-2) 컬렉터가 데이터를 수집할 스케줄을 설정합니다. 

<br>
<br>

스케줄을 설정할 때에는 두 가지 방식이 있습니다.

![collector-schedule-type](/ko/docs/guides/asset-inventory/collector-img/collector-schedule-type.png)

- 시간으로 설정: 반복을 원하는 시간을 입력하면, 입력한 모든 시간마다 데이터를 수집합니다. 이를 매일 반복합니다.
- 반복 주기로 설정: 입력한 시간 주기로 데이터를 수집합니다. 플러그인에서 지원하는 시간 단위(시, 분, 초)에 따라 입력 양식도 달라집니다.

{{<alert title="반복 주기 설정이 보이지 않는 경우">}}
선택한 컬렉터의 **플러그인**이 무엇인지에 따라 반복 주기 설정 양식이 때로는 보이지 않거나, 그 시간 단위(시, 분, 초) 입력 양식이 다를 수 있습니다.

컬렉터의 데이터 수집은 철저히 컬렉터 플러그인에 의존합니다. 그런데 만약 해당 플러그인이 수집하는 데이터의 양이 방대하다면, 반복 주기 설정은 매우 위험할 수 있습니다. 이런 문제를 방지하기 위해 반복 주기 설정은 기본 값으로 제공되지 않습니다.

반면, 오히려 자주 데이터를 수집해야 하는 플러그인도 있습니다. 이 경우에는 플러그인이 지원하는 조건에 따라 반복 주기 설정 양식이 화면에 표시됩니다.

플러그인에 대한 자세한 설명은 [여기](/ko/docs/guides/plugins/asset-inventory-collector)를 참고 하십시오.

{{</alert>}}

(3) [확인] 버튼을 클릭하여 컬렉터를 생성합니다.

### 스케줄 변경하기

(1) 스케줄 목록에서 변경할 항목을 선택합니다.

(2) [작업] 드롭다운에서 [변경]을 선택합니다.

![collector-schedule-edit-menu](/ko/docs/guides/asset-inventory/collector-img/collector-schedule-edit-menu.png)

(2-1) [스케줄 변경] 모달에서 변경할 내용을 입력합니다. 스케줄 추가 양식과 동일하므로, 위의 스케줄 추가하기(링크)를 참고하세요.

![collector-schedule-edit-modal](/ko/docs/guides/asset-inventory/collector-img/collector-schedule-edit-modal.png)

(3) [확인] 버튼을 클릭하여 변경을 완료합니다.

### 스케줄 삭제하기

(1) 스케줄 목록에서 변경할 항목을 선택합니다.

(2) [작업] 드롭다운에서 [삭제] 메뉴를 선택합니다.

![collector-schedule-delete-menu](/ko/docs/guides/asset-inventory/collector-img/collector-schedule-delete-menu.png)

(3) [스케줄 삭제] 모달에서 삭제할 스케줄의 내용을 확인하고, [확인] 버튼을 클릭하여 삭제를 완료합니다.

![collector-schedule-delete-modal](/ko/docs/guides/asset-inventory/collector-img/collector-schedule-delete-modal.png)

## 데이터 수집 내역 확인하기

**컬렉터 히스토리** 페이지에서 데이터 수집 내역을 확인할 수 있습니다.

컬렉터 페이지 상단의 [컬렉터 히스토리] 버튼을 클릭하여 컬렉터 히스토리 페이지로 이동할 수 있습니다.

특정 컬렉터의 데이터 수집 내역만을 확인하고 싶다면, 컬렉터 목록의 [상세 보기] 버튼을 클릭하여 이동할 수도 있습니다.

![collector-history-at-table](/ko/docs/guides/asset-inventory/collector-img/collector-history-at-table.png)

### 데이터 수집 목록 조회하기

컬렉터 히스토레 페이지 상단의 차트를 통해, 날짜별 데이터 수집 현황을 빠르게 확인할 수 있습니다.

하단의 목록에서는 고급 검색과 상태 필터 조건에 맞는 데이터 수집 목록이 표시됩니다. 고급 검색에 대한 자세한 설명은 [여기](/ko/docs/guides/advanced/search/)를 참고 하십시오.

데이터 수집이 진행중인 항목의 경우, Job Progress 필드의 상태바를 통해 수집 현황을 확인할 수 있습니다.

![collector-history-full-page](/ko/docs/guides/asset-inventory/collector-img/collector-history-full-page.png)

### 데이터 수집 내역 상세 정보 확인하기

위의 데이터 수집 목록에서 수집 내역을 선택하면 수집 내역 상세 페이지로 이동합니다.

데이터 수집 상태와 기본 정보, 그리고 **서비스 계정 별 수집 내역**을 확인할 수 있습니다.

![collector-history-detail-full-page](/ko/docs/guides/asset-inventory/collector-img/collector-history-detail-full-page.png)

#### 서비스 계정 별 수집 내역 확인하기

컬렉터를 실행하면 연결된 서비스 계정 별로 수집이 각각 이뤄집니다.

여기에서는 서비스 계정 별로 수집 작업이 어떻게 이뤄졌는지에 대한 정보 확인할 수 있습니다.

{{<alert title="">}}
컬렉터는 데이터 수집 시 서비스 계정을 통해 클라우드 프로바이더의 계정에 접근하여 데이터를 가져옵니다.
{{</alert>}}

![collector-history-detail-table](/ko/docs/guides/asset-inventory/collector-img/collector-history-detail-table.png)

###### 주요 필드 정보
- Created Count: 새롭게 추가된 리소스의 개수
- Updated Count: 가져온 리소스의 개수
- Disconnected Count: 가져오지 못한 리소스의 개수
- Deleted Count: 삭제된 리소스의 개수 (여러 번 가져오지 못하면 삭제된 것으로 간주됩니다.)

#### 수집 에러 내용 확인하기

(1) 계정 별 수집 목록에서 에러 내용을 확인하고자 하는 항목을 선택합니다.

(2) 아래의 [에러 목록] 탭에서 오류에 대한 자세한 내역을 확인할 수 있습니다.

![collector-history-error-list](/ko/docs/guides/asset-inventory/collector-img/collector-history-error-list.png)

## 컬렉터 태그 관리하기

컬렉터에 태그를 추가하여 관리할 수 있습니다.

(1) [태그] 탭 내부의 [편집] 버튼을 클릭합니다.

![collector-tag-edit](/ko/docs/guides/asset-inventory/collector-img/collector-tag-edit.png)

(2) 태그 페이지에서 `키: 값` 형태로 태그를 입력 후 [저장] 버튼을 클릭하여 완료합니다.

![collector-tag-filled](/ko/docs/guides/asset-inventory/collector-img/collector-tag-filled.png)

