---
title: "웹훅"
linkTitle: "웹훅"
weight: 4
date: 2022-06-07
description: >
    클라우드포레의 **얼럿 매니저**는 외부 모니터링 서비스에서 발생한 이벤트들을 **웹훅**을 통해 받아올 수 있습니다.
    <br/>
    <br/>
    웹훅은 다양한 외부 모니터링 서비스별로 존재하는 [**웹훅 플러그인**](/ko/docs/guides/plugins/alert-manager-webhook/)을 활용하여 생성할 수 있습니다.
    <br/>
    생성한 웹훅 URL을 통해 모니터링 서비스로부터 이벤트를 수신할 수 있으며, 수신한 이벤트 메시지를 정제하여 [얼럿](/ko/docs/guides/alert-manager/alert/)을 발생시킵니다.
---

## 웹훅 생성하기

외부 모니터링 서비스로부터 발생하는 로그를 수신하기 위해서는 웹훅을 생성해야 합니다.

웹훅은 프로젝트별로 생성이 가능하며, 프로젝트 상세 페이지에서 생성할 수 있습니다.

[프로젝트 생성하기](/ko/docs/guides/project/project/#프로젝트-생성하기)

(1) 프로젝트 상세 페이지의 [얼럿] 탭으로 이동 후, [웹훅] 탭을 선택합니다.

![create-webhook-step-1](/ko/docs/guides/alert-manager/webhook-img/create-webhook-step-1,2.png)

(2) [추가] 버튼을 클릭합니다.

![create-webhook-step-2](/ko/docs/guides/alert-manager/webhook-img/create-webhook-step-1,2.png)

(3) [웹훅 추가] 모달에서 이름을 작성하고, 연동할 외부 모니터링 서비스의 [웹훅 플러그인](/ko/docs/guides/plugins/alert-manager-webhook/)을 선택합니다.

![create-webhook-step-3](/ko/docs/guides/alert-manager/webhook-img/create-webhook-step-3.png)

(4) [확인] 버튼을 클릭하여 설정을 완료합니다.

![create-webhook-step-4](/ko/docs/guides/alert-manager/webhook-img/create-webhook-step-4.png)

## 웹훅 연동하기

생성된 웹훅의 URL을 통해 외부 모니터링 서비스와 연동할 수 있습니다.

![connect-webhook](/ko/docs/guides/alert-manager/webhook-img/connect-webhook.png)

외부 모니터링 서비스별로 연동 방식이 상이하며, 모니터링 서비스별 연동 가이드는 [여기](/ko/docs/guides/plugins/alert-manager-webhook/)에서 확인할 수 있습니다.

## 웹훅 목록 조회하기

### 상세 검색
![webhook-search](/ko/docs/guides/alert-manager/webhook-img/webhook-search.png)

검색 창에 검색어를 입력하여 조건에 부합하는 웹훅 목록을 확인할 수 있습니다. 고급 검색에 대한 상세 설명은 [여기](/ko/docs/guides/advanced/search/)를 참고하세요.

## 웹훅 수정 및 삭제하기

![update-webhook](/ko/docs/guides/alert-manager/webhook-img/update-webhook.png)

목록에서 조회한 웹훅을 선택하여 활성화, 비활성화, 변경, 삭제가 가능합니다.

### 웹훅 활성화하기

웹훅을 활성화하면, **웹훅 URL**로부터 수신한 이벤트를 [**얼럿**](/ko/docs/guides/alert-manager/alert/)으로 발생시킵니다.

(1) 활성화할 웹훅을 선택하고 [작업] 드롭다운에서 [활성화] 메뉴를 선택합니다.

![enable-webhook-1](/ko/docs/guides/alert-manager/webhook-img/enable-webhook-1.png)

(2) [웹훅 활성화] 모달에서 내용을 확인하고 [확인] 버튼을 눌러 활성화합니다.

![enable-webhook-2](/ko/docs/guides/alert-manager/webhook-img/enable-webhook-2.png)

### 웹훅 비활성화하기

웹훅을 비활성화하면 해당 **웹훅 URL**로부터 수신되는 이벤트는 무시되어, [**얼럿**](/ko/docs/guides/alert-manager/alert/)을 발생시키지 않습니다.

(1) 비활성화할 웹훅을 선택하고 [작업] 드롭다운에서 [비활성화] 메뉴를 선택합니다.

![disable-webhook-1](/ko/docs/guides/alert-manager/webhook-img/disable-webhook-1.png)

(2) [웹훅 비활성화] 모달에서 내용을 확인하고 [확인] 버튼을 눌러 비활성화합니다.

![disable-webhook-2](/ko/docs/guides/alert-manager/webhook-img/disable-webhook-2.png)

### 웹훅 변경하기

웹훅은 이름만 변경할 수 있습니다.

(1) 목록에서 변경할 웹훅을 선택하고, [작업] 드롭다운에서 [변경] 메뉴를 선택합니다.

![update-webhook-name-1](/ko/docs/guides/alert-manager/webhook-img/update-webhook-name-1.png)

(2) 변경할 이름을 작성하고 [확인] 버튼을 눌러 변경을 완료합니다.

![update-webhook-name-2](/ko/docs/guides/alert-manager/webhook-img/update-webhook-name-2.png)

### 웹훅 삭제하기
    
(1) 목록에서 삭제할 웹훅을 선택하고, [작업] 드롭다운에서 [삭제] 메뉴를 선택합니다.

![delete-webhook-1](/ko/docs/guides/alert-manager/webhook-img/delete-webhook-1.png)

(2) 삭제 확인을 위해 선택한 웹훅의 이름을 정확히 입력해야 [삭제] 버튼이 활성화됩니다. 

![delete-webhook-2](/ko/docs/guides/alert-manager/webhook-img/delete-webhook-2.png)

(3) [삭제] 버튼을 눌러 삭제를 완료합니다.
