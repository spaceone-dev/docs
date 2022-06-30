---
title: "대시보드"
linkTitle: "대시보드"
weight: 2
date: 2022-06-07
description: >
    현재 로그인된 사용자에게 발생한 얼럿을 한눈에 조회 가능한 대시보드입니다.
---

크게 3가지의 파트 별로 얼럿들을 확인할 수 있으며 아래와 같습니다.

## 상태별 얼럿 확인하기

대시보드의 최상단에서는 얼럿을 [상태별](/ko/docs/guides/alert-manager/alert/#상태)로 볼 수 있습니다.
<br>
각 항목을 클릭하면 [얼럿 상세 페이지](/ko/docs/guides/alert-manager/alert/#얼럿-살펴보기)로 이동하여 상세 정보를 확인하거나 세부 설정을 할 수 있습니다.

![view-alert-by-status](/ko/docs/guides/alert-manager/dashboard-img/view-alert-by-status.png)

## 얼럿 히스토리

[프로젝트](/ko/docs/guides/project/project/)에서 발생한 얼럿 히스토리를 보여줍니다.
<br>
차트에서 일별 데이터를 확인할 수 있으며, 카드에서는 전달 대비 얼럿의 증감량을 확인할 수 있습니다.

![alert-history-1](/ko/docs/guides/alert-manager/dashboard-img/alert-history-1.png)

## 프로젝트 상태 보드

[프로젝트 상태 보드]에서는 사용자와 관련된 각각의 프로젝트들의 얼럿 정보를 보여줍니다.

[Top 5 프로젝트 활동]의 경우, [오픈] 상태의 얼럿이 많은 순서대로 프로젝트를 보여줍니다.

![project-board-1](/ko/docs/guides/alert-manager/dashboard-img/project-board-1.png)

검색 창 아래에는 얼럿이 발생한 프로젝트가 활동이 높은 순서대로 보여집니다.
<br>
`이슈` 상태인 프로젝트만 보이며, 모든 얼럿이 `완료` 상태가 되면 `정상` 상태의 프로젝트로 변경되어 대시보드에서 보이지 않습니다.

![project-board-2](/ko/docs/guides/alert-manager/dashboard-img/project-board-2.png)

