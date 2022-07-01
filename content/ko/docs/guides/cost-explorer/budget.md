---
title: "예산"
linkTitle: "예산"
weight: 4
date: 2022-06-23
description: >
    **예산**은 프로젝트 별로 비용 발생 기준을 설정해, 예산을 관리하는 서비스입니다.
---

## 예산 생성하기
(1) [비용 관리 > 예산] 페이지의 우측 상단에 있는 [예산 생성] 버튼을 클릭합니다.

![budget-create-01](/ko/docs/guides/cost-explorer/budget-img/budget-create-01.png)

(2) 기본 정보 입력하기

![budget-create-02](/ko/docs/guides/cost-explorer/budget-img/budget-create-02.png)

(2-1) 예산의 이름을 입력합니다.

(2-2) 타겟 항목에서 예산 관리의 대상이 될 프로젝트를 선택합니다.

(2-3) 비용 발생 기준을 선택합니다. 비용 발생 기준을 `모두`로 선택할 경우, 해당 프로젝트와 관련된 모든 비용 데이터를 가져옵니다. 한편 `계정`이나 `지역` 등을 선택할 경우, 특정 리소스에 의해 발생된 비용만을 가져옵니다.

(3) 예산 계획 입력하기

![budget-create-03](/ko/docs/guides/cost-explorer/budget-img/budget-create-03.png)

(3-1) 예산을 관리할 기간을 정합니다.

(3-2) 어떤 방식으로 예산을 관리할 것인지 선택합니다.

(3-3) 예산 금액을 설정합니다. 앞서 `총 예산 설정`을 선택했다면 총 예산 금액을 입력하고, `월별 예산 설정`을 선택했다면 월별 예산 금액을 입력합니다.

## 설정된 예산 및 사용현황 확인
예산 페이지에서는 예산 데이터의 요약과 프로젝트 별 예산을 한눈에 볼 수 있습니다. 상단의 필터를 활용해 기간을 지정하거나 환율을 적용할 수 있으며, 고급 검색을 통해 특정 프로젝트나 이름 등을 검색할 수 있습니다.

![budget-full-page-01](/ko/docs/guides/cost-explorer/budget-img/budget-full-page-01.png)

## 예산 상세 페이지
예산 상세 페이지에서, 생성된 예산의 구체적인 데이터를 볼 수 있습니다.

### 예산 요약
[예산 요약]에서는 월별 예산과 비용 추이를 차트와 테이블을 통해 확인할 수 있습니다.

![budget-detail-01](/ko/docs/guides/cost-explorer/budget-img/budget-detail-01.png)

### 예산 사용 알림 설정
[예산 사용 알림 설정]에서는 예산을 일정 기준 이상으로 사용했을 경우 알림을 받도록 설정할 수 있습니다. 예산 금액을 일정 비율 이상 사용했거나, 실 사용액이 일정 금액을 초과했을 경우 미리 등록해 둔 알림 채널로 알림을 받을 수 있습니다.

![budget-alert-01](/ko/docs/guides/cost-explorer/budget-img/budget-alert-01.png)

{{<alert>}}
알림을 받기 위해서는 **알림 채널**이 있어야 합니다. 알림 채널에 대해서는 [여기](/ko/docs/guides/my-page/notification-channel/)를 참고 하십시오.
{{</alert>}}
