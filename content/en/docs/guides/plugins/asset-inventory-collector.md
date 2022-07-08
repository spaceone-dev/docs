---
title: "[Asset Inventory] Collector"
linkTitle: "[Asset Inventory] Collector"
weight: 3
date: 2022-07-05
description: >

---

## 개요

클라우드포레는 컬렉터 플러그인을 사용해 각각의 [클라우드 프로바이더](/ko/docs/guides/asset-inventory)에서 사용중인 클라우드 리소스를 수집할 수 있습니다.  
현재 클라우드포레에서 지원하는 컬렉터 목록은 아래 **플러그인 지원목록**을 참조하세요.


먼저, 컬렉터 플러그인을 사용하기 위해서 [서비스 계정](/ko/docs/guides/asset-inventory/service-account) 등록을 선행합니다.  
그러나 AWS, Google Cloud, Azure 등 각 클라우드 프로바이더별 **서비스 계정 등록 방법이 상이**하기 때문에  
상세한 설정은 아래 플러그인 지원 목록의 **설정 가이드 링크**를 참고 하십시오.

## 플러그인 지원 목록

| **플러그인** | **설정 가이드 링크** |
| --- | --- |
| AWS Cloud Services collector | https://github.com/spaceone-dev/plugin-aws-cloud-service-inven-collector/blob/master/docs/ko/GUIDE.md |
| AWS EC2 Compute collector | https://github.com/spaceone-dev/plugin-aws-ec2-inven-collector/blob/master/docs/ko/GUIDE.md |
| AWS Personal Health Dashboard collector |https://github.com/spaceone-dev/plugin-aws-phd-inven-collector/blob/master/docs/ko/GUIDE.md|
| AWS Trusted Advisor collector | https://github.com/spaceone-dev/plugin-aws-trusted-advisor-inven-collector/blob/master/docs/ko/GUIDE.md
| Azure Cloud Service collector |https://github.com/spaceone-dev/plugin-azure-cloud-service-inven-collector/blob/master/docs/ko/GUIDE.md|
| Azure VM collector |https://github.com/spaceone-dev/plugin-azure-vm-inven-collector/blob/master/docs/ko/GUIDE.md|
| Google Cloud collector |https://github.com/spaceone-dev/plugin-google-cloud-inven-collector/blob/master/docs/ko/GUIDE.md|
| Monitoring Metric Collector of Collected Resources |https://github.com/spaceone-dev/plugin-monitoring-metric-inven-collector/blob/master/docs/ko/GUIDE.md|
