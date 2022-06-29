---
title: "Quick Start"
linkTitle: "Quick Start"
weight: 1
date: 2022-06-07
description: >
    **얼럿 매니저** 서비스를 빠르게 사용하기 위한 과정을 소개합니다.
---

## 얼럿 생성하기

얼럿은 크게 두 가지 방법을 통해 생성됩니다.

(1) 클라우드포레 콘솔에서 직접 얼럿 생성

(2) **외부 모니터링 서비스 연동**을 통한 얼럿 자동 생성

### 콘솔에서 직접 얼럿 생성하기

### Steps

(1) 얼럿 페이지로 이동 후 [생성] 버튼을 눌러줍니다.

![create-alert-step-1](/ko/docs/guides/alert-manager/quick-start-img/create-alert-step-1.png)

(2) 얼럿 생성 폼을 작성합니다.

![create-alert-step-2](/ko/docs/guides/alert-manager/quick-start-img/create-alert-step-2.png)

(2-1) [설명] 폼을 제외한 모든 입력 폼이 필수요소입니다.

(2-2) [얼럿 제목]을 입력하고 [긴급도]를 선택합니다.

(2-3) 다음으로 얼럿이 어떤 프로젝트에 대하여 발생한 것인지 지정해줍니다.

(2-4) 추가적인 설명이 필요하다면 [설명] 필드를 작성합니다.

(3) [확인] 버튼을 클릭하여 얼럿 생성을 완료합니다.

### 외부 모니터링 서비스를 연결하여 얼럿 수신하기

외부 모니터링으로부터 발생된 얼럿을 수신하기 위해 **웹훅** **생성**과 **연동 설정**이 필요합니다.

### Steps

(1) 원하는 외부 모니터링 서비스에 해당하는 [웹훅을 추가](/ko/docs/guides/alert-manager/quick-start/#웹훅-설정하기)합니다.  

(2) 추가 된 웹훅의 웹훅 URL으로 각 외부 [모니터링 서비스와 연동](/ko/docs/guides/plugins/alert-manager-webhook/)해줍니다.

(3) 연결되어 있는 모니터링 서비스에서 발생하는 이벤트의 메시지가 정제되어 얼럿으로 자동 생성됩니다.



## 웹훅 설정하기

외부 모니터링 서비스로부터 발생하는 로그를 수신하는 웹훅을 생성해야 합니다.

웹훅은 프로젝트별로 생성이 가능하며, 프로젝트 상세 페이지에서 생성할 수 있습니다.

아직 프로젝트가 생성되어있지 않다면, [프로젝트 생성하기](/ko/docs/guides/project/project/#프로젝트-생성하기)를 참고해주십시오.

### Steps

(1) 프로젝트 상세 페이지의 [얼럿] 탭으로 이동 후, [웹훅] 탭을 선택합니다.

![create-webhook-step-1](/ko/docs/guides/alert-manager/quick-start-img/create-webhook-step-1,2.png)

(2) [추가] 버튼을 클릭하여 [웹훅 추가] 모달을 열어줍니다.

(3) [웹훅 추가] 모달에서 이름을 작성하고, 연동할 외부 모니터링 툴 플러그인 타입을 선택합니다.

![create-webhook-step-3](/ko/docs/guides/alert-manager/quick-start-img/create-webhook-step-3.png)

(4) [확인] 버튼을 클릭하여 설정을 완료합니다.

![create-webhook-step-4](/ko/docs/guides/alert-manager/quick-start-img/create-webhook-step-4.png)


{{< alert title="" >}}
이후 생성된 웹훅 URL으로 외부 모니터링 서비스와 연동을 진행해야합니다.

각각의 외부 모니터링 서비스 연동방식 가이드는 [여기](/ko/docs/guides/plugins/alert-manager-webhook/)를 확인해 주십시오.
{{< /alert >}}


## 에스컬레이션 정책 설정하기

웹훅을 통해 수신한 얼럿이 프로젝트의 멤버들에게 알림으로 전송될지 여부는 에스컬레이션 정책을 통해 결정됩니다. 

(1) 프로젝트 상세 페이지에 [얼럿] 탭 내부에서, [설정] 탭으로 이동합니다.

![create-escalation-policy-step-1](/ko/docs/guides/alert-manager/quick-start-img/create-escalation-policy-step-1,2.png)

(2) 에스컬레이션 정책 영역에서 [편집] 버튼을 클릭합니다.

![create-escalation-policy-step-2](/ko/docs/guides/alert-manager/quick-start-img/create-escalation-policy-step-1,2.png)

(3) [새로운 정책 생성] 탭을 클릭합니다.

![create-escalation-policy-step-3](/ko/docs/guides/alert-manager/quick-start-img/create-escalation-policy-step-3.png)

(4) 에스컬레이션 정책을 생성하기 위한 설정들을 입력합니다.

![create-escalation-policy-step-4](/ko/docs/guides/alert-manager/quick-start-img/create-escalation-policy-step-4.png)

| 정책                             | 설명                                                                                                |
|--------------------------------|---------------------------------------------------------------------------------------------------|
| 종료 조건(상태)                      | 발생된 알람이 중지되는 조건을 정의 합니다.                                                                          |
| 범위                             | 에스컬레이션 정책을 사용할 수 있는 범위를 나타냅니다. 글로벌인 경우 도메인 내 모든 프로젝트에서 사용 가능하고, 프로젝트인 경우 지정된 프로젝트 내에서만 사용 가능합니다.  |
| 에스컬레이션 규칙                      | 전체 레벨 LV1 ~ LV5 까지 추가 가능합니다. <br/> 설정된 레벨에 속하는 알림 채널에 얼럿을 전달하며, 2단계 이상부터 단계 간 텀을 분단위로 부여할 수 있습니다. |
| 반복 횟수                          | Alert 알림을 몇 회 반복할 것인지 정의합니다. 최대 9회까지 반복 가능합니다.                                                    |
| 프로젝트 (에스컬레이션 규칙 페이지에서 생성하는 경우) | 범위가 프로젝트인 경우 대상이 되는 프로젝트를 나타냅니다.                                                                  |

(5) 모든 설정이 완료되었다면 [확인] 버튼을 클릭해 에스컬레이션 정책을 생성합니다.

## 알림 설정하기

프로젝트 상세 페이지의 [알림] 탭에서는 알림 채널 생성 및 알림 채널 활성화 여부를 관리할 수 있습니다.

**알림 채널**은 알림 전송 방식과 **레벨**을 포함하여 체계적인 수신자 영역을 표현하는 단위입니다. 에스컬레이션 규칙에서 설정한 레벨에 맞춰 송신할 수 있도록 돕습니다.

### Steps

(1) 프로젝트 상세 페이지의 [알림] 탭에서 생성할 수 있습니다.

![notification-step-1](/ko/docs/guides/alert-manager/quick-start-img/notification-step-1,2.png)

(2) 원하는 알림 채널을 클릭하여 알림 생성 페이지로 이동합니다.

(3) 알림 채널을 생성하기 위해 알맞은 설정들을 입력합니다.

(3-1) 필요한 채널 이름과 알림 레벨 등 생성하려는 알림 채널에 대한 기본적인 정보들을 입력합니다.

[채널 이름]과 [알림 레벨]이 기본 설정 필드이며, 이후 나머지는 채널별로 입력받는 정보가 다릅니다.

![notification-step-3-1](/ko/docs/guides/alert-manager/quick-start-img/notification-step-3-1.png)


#### 알림 레벨

알림 레벨은 에스컬레이션 정책의 규칙 설정과 관련이 있습니다. 규칙의 대상을 지정할 때 채널을 선택하는게 아닌 레벨을 선택하고, 선택된 레벨의 모든 채널에 얼럿을 전파합니다.

(3-2) 스케줄을 설정하여 특정 시간에말 알림을 수신할 수 있도록 설정할 수 있습니다.

![notification-step-3-2](/ko/docs/guides/alert-manager/quick-start-img/notification-step-3-2.png)

(3-3) 알림은 얼럿이 발생했을 때, 예산 알림 기준에 도달했을 때에 수신할 수 있습니다. 여기에서는 어떤 토픽에 대하여 알림을 수신할 것인지를 설정할 수 있습니다.

![notification-step-3-3](/ko/docs/guides/alert-manager/quick-start-img/notification-step-3-3.png)

{{< alert title="" >}}
각 플러그인의 자세한 연동 가이드는 [이곳](/ko/docs/guides/plugins/alert-manager-notification/)을 확인하십시오.
{{< /alert >}}

(4) [저장] 버튼을 클릭해 알림 채널 생성을 완료합니다.

(5) 생성이 완료된 알림 채널들은 [알림] 탭 하단에서 확인할 수 있습니다.

![notification-step-5](/ko/docs/guides/alert-manager/quick-start-img/notification-step-5.png)

왼쪽 상단의 토글 버튼을 통해 해당 알림 채널의 활성여부를 조작할 수 있습니다.

{{< alert title="" >}}
에스컬레이션 정책에서 설정된 레벨이 있더라도 알림 채널이 활성화 되어있지 않다면 알림은 발생하지 않습니다.
{{< /alert >}}

