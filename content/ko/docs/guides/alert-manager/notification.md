---
title: "알림"
linkTitle: "알림"
weight: 7
date: 2022-06-07
description: >
    **알림**은 얼럿을 전달하기 위한 수단입니다.


    **알림 채널**을 통해 얼럿을 어떤 사용자에게 어떻게, 언제 전달할 것인지 등을 설정합니다.
---

알림 채널은 프로젝트에 종속되며, 프로젝트 상세 페이지에서 관리할 수 있습니다.

![notification-full-page](/ko/docs/guides/alert-manager/notification-img/notification-full-page.png)

## 알림 채널 생성하기

프로젝트 상세 페이지의 [알림] 탭에서는 **알림 채널 생성 및 알림 채널 활성화 여부**를 관리할 수 있습니다.

**알림 채널**은 알림 전송 방식과 레벨을 포함하여 체계적인 수신자 영역을 표현하는 단위입니다. 에스컬레이션 규칙에서 설정한 레벨에 맞춰 송신할 수 있도록 돕습니다.
<br>
<br>
(1) 프로젝트 상세 페이지에서 [알림] 탭을 선택한 뒤, 원하는 알림 채널의 [채널 추가] 버튼을 클릭합니다.

![notification-step-1](/ko/docs/guides/alert-manager/notification-img/notification-step-1.png)

{{< alert title="" >}}
**CloudForet User 채널**에 대한 자세한 설명은 [여기](/ko/docs/guides/alert-manager/notification/#클라우드포레-사용자-채널)를 확인하십시오.
{{< /alert >}}


(2) 알림 생성 페이지에서, 알림 채널을 생성하기 위한 설정들을 입력합니다.

(2-1) 필요한 채널 이름과 알림 레벨 등 생성하려는 알림 채널에 대한 기본적인 정보들을 입력합니다. [채널 이름]과 [알림 레벨]이 기본 설정 필드이며, 이후 나머지는 채널별로 입력받는 정보가 다릅니다.

{{<alert>}}
각 **알림 플러그인**에 대한 자세한 연동 가이드는 [여기](/ko/docs/guides/plugins/alert-manager-notification/)를 확인하십시오.
{{</alert>}}

![notification-step-2-1](/ko/docs/guides/alert-manager/notification-img/notification-step-2-1.png)

{{<alert title="알림 레벨">}}
알림 레벨은 얼럿 전파에 대한 규칙을 정의하는 [에스컬레이션 정책](/ko/docs/guides/alert-manager/escalation-policy/)과 관련이 있습니다. 

![notification-escalation-menu](/ko/docs/guides/alert-manager/notification-img/notification-escalation-menu.png)

에스컬레이션 정책에서 지정된 알림 레벨을 기준으로, 해당 레벨에 속한 알림 채널에 얼럿을 전파합니다.
{{</alert>}}

(2-2) 스케줄을 설정하여 특정 시간에말 알림을 수신할 수 있도록 설정할 수 있습니다.

![notification-step-2-2](/ko/docs/guides/alert-manager/notification-img/notification-step-2-2.png)

(2-3) 알림은 얼럿이 발생했을 때 혹은 예산 알림 기준에 도달했을 때에 수신할 수 있습니다. 토픽을 설정하여 어떤 알림을 받을 것인지 선택할 수 있습니다.
<br>
[모든 알림 받기]를 선택하면 두 가지 알림 모두를, [선택한 토픽 알림 받기]를 선택하면 선택한 알림만을 받을 수 있습니다.

![notification-step-2-3](/ko/docs/guides/alert-manager/notification-img/notification-step-2-3.png)

(3) [저장] 버튼을 클릭해 알림 채널 생성을 완료합니다.

{{<alert>}}
에스컬레이션 정책에서 설정된 레벨이 있더라도 알림 채널이 활성화 되어있지 않다면 알림은 발생하지 않습니다.
{{</alert>}}

## 알림 채널 편집/삭제하기

### 알림 채널 편집하기

생성된 알림 채널들은 각 알림 채널 선택지 아래에서 확인할 수 있습니다.

![update-notification-channel-1](/ko/docs/guides/alert-manager/notification-img/update-notification-channel-1.png)

왼쪽 상단 토글 버튼을 통해 활성/비활성 상태를 변경할 수 있으며, 각 알림 채널의 [편집] 버튼을 클릭해 각각의 항목을 편집할 수 있습니다.
<br>
작성이 완료되면 [변경사항 저장] 버튼을 클릭해 편집을 완료합니다.

![update-notification-channel-2](/ko/docs/guides/alert-manager/notification-img/update-notification-channel-2.png)

### 알림 채널 삭제하기
우측 상단의 [삭제 아이콘] 버튼을 클릭시 알림 채널 삭제가 가능합니다.

![delete-notification-channel](/ko/docs/guides/alert-manager/notification-img/delete-notification-channel.png)

## 클라우드포레 사용자 채널

프로젝트에서 [알림 채널] 항목에는 [Cloudforet User 채널 추가] 버튼이 존재합니다.

![cloud-foret-user-channel-1](/ko/docs/guides/alert-manager/notification-img/cloud-foret-user-channel-1.png)

클라우드포레 사용자 채널을 추가하면, 프로젝트 멤버들의 개인 채널로 얼럿이 전파됩니다. 이후 전파 받은 사용자의 **클라우드포레 사용자 알림 채널**을 통해 얼럿이 전달됩니다.

![cloud-foret-user-channel-2](/ko/docs/guides/alert-manager/notification-img/cloud-foret-user-channel-2.png)


### 클라우드포레 사용자 알림 채널 생성하기

사용자 알림 채널은 [마이페이지 > 알림 채널]에서 생성할 수 있습니다.

![create-user-channel](/ko/docs/guides/alert-manager/notification-img/create-user-channel.png)

프로젝트 알림 채널 생성과 다르게 **알림 레벨 설정이 없으며**, 이 외에 생성 절차는 [프로젝트 알림 채널 생성하기](/ko/docs/guides/alert-manager/notification/#알림-채널-생성하기)와 동일합니다.

