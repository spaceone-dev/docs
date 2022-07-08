---
title: "Notification Channel"
linkTitle: "Notification Channel"
weight: 3
date: 2022-06-23
description: >
    **알림 채널**은 클라우드포레의 모니터링 시스템이나 예산 서비스에서 발생하는 여러 얼럿과 이벤트, 또는 클라우드포레 자체 알림 등을 받아볼 수 있는 서비스입니다.
---

## 알림 생성하기
[마이페이지 > 알림 채널] 페이지에는 각 프로토콜에 해당하는 [채널 추가] 버튼이 있습니다.

![notification-channel-01](/ko/docs/guides/my-page/notification-channel-img/notification-channel-01.png)

[채널 추가] 버튼을 클릭할 시 아래와 같은 페이지에 진입합니다. 기본 정보 입력 폼은 프로토콜마다 상이하며, 채널명과 알림 스케줄, 구독할 토픽 선택란은 모든 프로토콜이 동일합니다.

![notification-channel-02](/ko/docs/guides/my-page/notification-channel-img/notification-channel-02.png)

스케줄을 `모든 시간`으로 선택할 경우 모든 시간에 알림을 받아볼 수 있습니다. `시간 설정`을 선택할 경우, 원하는 요일과 시간을 선택할 수 있습니다.

![notification-channel-03](/ko/docs/guides/my-page/notification-channel-img/notification-channel-03.png)

토픽 또한 `모든 알림을 받기`를 선택할 수도 있고, `Alert`과 `Budget` 중 선택한 토픽에 한해 알림을 받을 수 있습니다.

![notification-channel-04](/ko/docs/guides/my-page/notification-channel-img/notification-channel-04.png)

## 생성한 알림 채널 확인하기
모든 입력 폼을 채우고 알림 채널을 생성할 시, 다음과 같이 새롭게 생성된 채널을 확인할 수 있습니다.

![notification-channel-created-01](/ko/docs/guides/my-page/notification-channel-img/notification-channel-created-01.png)

## 알림 채널 편집하기
생성한 알림은 목록에서 바로 편집할 수 있습니다.

입력한 데이터를 편집할 수 있는 프로토콜의 경우(ex. SMS, Voice Call) 데이터와 채널명, 스케줄, 토픽을 모두 수정할 수 있습니다.
데이터를 편집할 수 없는 프로토콜(ex. Slack, Telegram)은 [편집] 버튼이 활성화되지 않습니다.

![notification-channel-edit-01](/ko/docs/guides/my-page/notification-channel-img/notification-channel-edit-01.png)
