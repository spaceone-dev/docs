---
title: "Webhook"
linkTitle: "Webhook"
weight: 4
date: 2022-06-07
description: >
    **웹훅**을 통해 외부 모니터링 서비스에서 발생한 이벤트를 수신할 수 있습니다.
---

## 웹훅 생성하기

<!--이 항목은 [얼럿 매니저 > quick start]의 '웹훅 생성하기' 항목과 동일합니다. 수정 시 유의 바람 -->

외부 모니터링 서비스로부터 발생하는 이벤트 메시지를 수신하려면 웹훅을 생성해야 합니다.
<br>
웹훅은 프로젝트 상세 페이지에서 생성 가능합니다.


(1) 프로젝트 상세 페이지의 [얼럿] 탭으로 이동 후, [웹훅] 탭을 선택합니다.

![create-webhook-step-1](/ko/docs/guides/alert-manager/quick-start-img/create-webhook-step-1,2.png)

(2) [추가] 버튼을 클릭합니다.

(3) [웹훅 추가] 모달에서 이름을 작성하고, 연동할 외부 모니터링 서비스의 플러그인을 선택합니다.

![create-webhook-step-3](/ko/docs/guides/alert-manager/quick-start-img/create-webhook-step-3.png)

(4) [확인] 버튼을 클릭하여 설정을 완료합니다.

{{<alert title="외부 모니터링 서비스 연동">}}
웹훅을 사용하기 위해서는 생성된 웹훅의 URL을 통해 외부 모니터링 서비스와 연결해야 합니다.

외부 모니터링 서비스를 연동하는 방법은 [여기](/ko/docs/guides/plugins/alert-manager-webhook/)를 참고 하십시오.
{{</alert>}}






## 웹훅 목록 조회하기

### 상세 검색
검색 창에 검색어를 입력하여 조건에 부합하는 웹훅 목록을 확인할 수 있습니다. 고급 검색에 대한 상세 설명은 [여기](/ko/docs/guides/advanced/search/)를 참고 하십시오.

![webhook-search](/ko/docs/guides/alert-manager/webhook-img/webhook-search.png)

## 웹훅 수정 및 삭제하기

목록에서 조회한 웹훅을 선택하여 활성화, 비활성화, 변경, 삭제할 수 있습니다.

![update-webhook](/ko/docs/guides/alert-manager/webhook-img/update-webhook.png)

### 웹훅 활성화 / 비활성화 하기

웹훅을 활성화하면, 해당 웹훅에 연동된 외부 모니터링 서비로부터 수신된 이벤트를 [얼럿](/ko/docs/guides/alert-manager/alert/)으로 받을 수 있습니다.
<br>
반대로 웹훅을 비활성화하면, 수신되는 이벤트는 무시되어 얼럿을 발생시키지 않습니다.

(1) 활성화할 웹훅을 선택하고 [작업] 드롭다운에서 [활성화] 혹은 [비활성화] 메뉴를 선택합니다.

![enable-webhook-1](/ko/docs/guides/alert-manager/webhook-img/enable-webhook-1.png)

(2) [웹훅 활성화/비활성화] 모달에서 내용을 확인하고 [확인] 버튼을 클릭합니다.

![enable-webhook-2](/ko/docs/guides/alert-manager/webhook-img/enable-webhook-2.png)
![disable-webhook-2](/ko/docs/guides/alert-manager/webhook-img/disable-webhook-2.png)


### 웹훅 이름 변경하기

(1) 웹훅 목록에서 변경할 웹훅을 선택하고, [작업] 드롭다운에서 [변경] 메뉴를 선택합니다.

![update-webhook-name-1](/ko/docs/guides/alert-manager/webhook-img/update-webhook-name-1.png)

(2) 변경할 이름을 작성하고 [확인] 버튼을 눌러 변경을 완료합니다.

![update-webhook-name-2](/ko/docs/guides/alert-manager/webhook-img/update-webhook-name-2.png)

### 웹훅 삭제하기
    
(1) 웹훅 목록에서 삭제할 웹훅을 선택하고, [작업] 드롭다운에서 [삭제] 메뉴를 선택합니다.

![delete-webhook-1](/ko/docs/guides/alert-manager/webhook-img/delete-webhook-1.png)

(2) 선택한 웹훅의 이름을 정확히 입력한 뒤, [삭제] 버튼을 클릭하여 웹훅을 삭제합니다. 

![delete-webhook-2](/ko/docs/guides/alert-manager/webhook-img/delete-webhook-2.png)
