---
title: "[Alert Manager] Webhook"
linkTitle: "[Alert Manager] Webhook"
weight: 3 
date: 2022-07-05 
description: >

---

## 개요

클라우드포레는 **다양한 모니터링 서비스**로부터 발생하는 이벤트 메시지를 수신받기 위해 플러그인 형태의 웹훅을 지원하고 있습니다.  
현재 클라우드포레에서 지원하는 웹훅 플러그인 목록은 **플러그인 지원 목록**을 참조하세요.

특히, **AWS CloudWatch**와 **AWS PHD**(PersonalHealthDashboard)에서 발생하는 이벤트 메세지는   
**AWS SNS**(Simple Notification Service) Webhook을 통해 클라우드포레로 수집됩니다.

모니터링 서비스 별 설정 가이드는 아래 플러그인 지원목록의 **설정 가이드 링크**를 참고 하십시오.

## 플러그인 지원 목록

| **플러그인** | **설정 가이드 링크** |
| --- | --- |
| AWS SNS | https://github.com/spaceone-dev/plugin-aws-sns-mon-webhook/blob/master/docs/ko/GUIDE.md |
| Grafana | https://github.com/spaceone-dev/plugin-grafana-mon-webhook/blob/master/docs/ko/GUIDE.md |
| Prometheus |https://github.com/spaceone-dev/plugin-prometheus-mon-webhook/blob/master/docs/ko/GUIDE.md|
| Zabbix |https://github.com/spaceone-dev/plugin-zabbix-mon-webhook/blob/master/docs/ko/GUIDE.md|
