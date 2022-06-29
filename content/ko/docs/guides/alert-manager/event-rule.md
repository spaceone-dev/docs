---
title: "이벤트 규칙"
linkTitle: "이벤트 규칙"
weight: 5
date: 2022-06-07
description: >
    [**얼럿**](/ko/docs/guides/project/project/)이 발생하면 <u>조건을 만족할 경우</u>, 자동으로 지정된 작업을 수행할 수 있도록 정의합니다.
    <br/>
    이는 얼럿을 수작업으로 관리해야 하는 번거로움을 줄여줍니다.
    <br/>
    이벤트 규칙은 프로젝트에 종속되므로, 프로젝트 상세 페이지에서 관리할 수 있습니다.
---



## 이벤트 규칙 생성하기

(1) 프로젝트 상세 페이지의 [얼럿] 탭 내부의 [설정] 탭에서 이벤트 규칙의 [편집] 아이콘 버튼을 클릭합니다.

![create-event-rule-1](/ko/docs/guides/alert-manager/event-rule-img/create-event-rule-1.png)

(2) [이벤트 규칙 추가] 버튼을 클릭합니다.

![create-event-rule-2](/ko/docs/guides/alert-manager/event-rule-img/create-event-rule-2.png)

(3) 이벤트 규칙 페이지에서 원하는 설정 값들을 입력합니다.

![create-event-rule-3](/ko/docs/guides/alert-manager/event-rule-img/create-event-rule-3.png)

(3-1) 수신한 얼럿에 대하여 추가적인 작업을 수행할 조건을 설정합니다.

조건은 반드시 한 개 이상 작성되어야 하며, 오른쪽의 [추가] 버튼을 클릭하여 조건을 추가하거나, [삭제] 아이콘 버튼을 클릭하여 삭제할 수 있습니다.

![create-event-rule-3-1](/ko/docs/guides/alert-manager/event-rule-img/create-event-rule-3-1.png)


(3-2) 위에서 정의한 조건에 맞는 얼럿에 대하여 수행될 작업을 지정합니다.

![create-event-rule-3-2](/ko/docs/guides/alert-manager/event-rule-img/create-event-rule-3-2.png)


#### 이벤트 규칙 설정 목록

| 작업       | 설명                                                                                                                                                                       |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 알림 중지    | 해당 조건의 얼럿에 대하여 [알림](/ko/docs/guides/alert-manager/notification/)을 발생시키지 않기                                                                                               |
| 프로젝트 라우팅 | 해당 조건의 얼럿을 현재의 프로젝트가 아닌 선택한 프로젝트에 등록하기 (현재 프로젝트에는 얼럿이 생성되지 않음)                                                                                                           |
| 프로젝트 의존성 | 지정된 프로젝트에 얼럿 함께 등록하기 (현재 프로젝트에도 얼럿이 생성됨)                                                                                                                                 |
| 긴급도      | 해당 조건의 얼럿에 자동으로 긴급도 지정하기<br/>높음, 낮음, 미설정을 지정할 수 있으며, 미설정의 경우 아래의 규칙에 따라 설정됨<br/>• 외부 모니터링 얼럿: [개체의 긴급도](/ko/docs/guides/alert-manager/alert/#긴급도)<br/>• 직접 생성: 높음(기본값)   |
| 담당자      | 해당 조건의 얼럿에 자동으로 담당자 지정하기                                                                                                                                                 |
| 추가 수신자   | 해당 조건의 얼럿에 대하여 [알림](/ko/docs/guides/alert-manager/notification/) 발생 시, 지정한 사용자에게도 함께 알림 보내기                                                                              |
| 추가 정보    | 해당 조건의 얼럿에 자동으로 정보 추가하기                                                                                                                                                  |

[이후 작업 실행하지 않기] 체크박스는 해당 이벤트 규칙까지만 검사하고, 다음 이벤트 규칙들은 실행하지 않도록 설정하는 옵션입니다. 자세한 내용은 [이벤트 규칙 동작 방식과 순서](/ko/docs/guides/alert-manager/event-rule-img/#이벤트-규칙-동작-방식과-순서) 가이드를 참조하세요.

## 이벤트 규칙 편집하기

(1) 이벤트 규칙 페이지에서 [편집] 버튼을 클릭합니다.

![update-event-rule-1](/ko/docs/guides/alert-manager/event-rule-img/update-event-rule-1.png)

(2) 이벤트 규칙에서 원하는 설정 값들을 입력합니다. ([설정 목록 상세보기](/ko/docs/guides/alert-manager/event-rule-img/#이벤트-규칙-설정-목록))

![update-event-rule-2](/ko/docs/guides/alert-manager/event-rule-img/update-event-rule-2.png)

(3) [저장] 버튼을 클릭하여 이벤트 규칙 변경을 완료합니다.

## 이벤트 규칙 삭제하기

(1) 이벤트 규칙 페이지에서 [삭제] 버튼을 클릭합니다.

(2) [이벤트 규칙 삭제] 모달에서 [확인] 버튼을 눌러 삭제를 완료합니다.

## 이벤트 규칙 동작 방식과 순서

얼럿이 발생했을 때 사용자가 설정한 이벤트 규칙이 있으면 순차적으로 실행됩니다.

![event-working-system](/ko/docs/guides/alert-manager/event-rule-img/event-working-system.png)

위의 예시와 같이 이벤트 규칙들이 생성되어 있다면 가장 상위에 있는 이벤트 규칙부터 [#1], [#2], [#3] 순서대로  실행됩니다.

[위 화살표], [아래 화살표] 아이콘 버튼을 클릭하여 이벤트 규칙의 순서를 쉽게 변경할 수 있습니다.

### 이후 작업 실행하지 않기

이벤트 규칙을 생성 또는 편집 시에 [이후 작업 실행하지 않기] 옵션을 확인할 수 있습니다.

![then-stop-processing](/ko/docs/guides/alert-manager/event-rule-img/then-stop-processing.png)

해당 옵션에 체크한 이벤트 규칙의 경우, 이벤트 규칙 조건에 해당하는 얼럿이 들어왔을 때 다음 이벤트 규칙에 대해 검사를 진행하지 않습니다.
