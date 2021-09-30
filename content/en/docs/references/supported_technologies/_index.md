---
title: "Supported Technologies"
linkTitle: "Supported Technologies"
weight: 3
date: 2021-07-31
description: >
    SpaceONE plugin supported providers

---

## Overview

SpaceONE은 Plugin Architecture 기반으로 개발되어, 각각의 Core Service를 지원하는 수많은 Eco System을 가지고 있습니다.
아래의 리스트에 포함되지 않은 기술들이 플러그인으로서 지원되야 할 경우, 문의 주세요.

## Inventory

_**Inventory.Collector**_ Type의 Plugin은 SpaceONE의 Asset 관리 기능의 핵심 역할을 수행합니다. 
다양한 리전에 숨어있는 여러 Provider의 Cloud Resource를 자동으로 탐색하여 체계적으로 분류하여 줍니다. 

### [AWS Cloud Service Plugin](https://github.com/spaceone-dev/plugin-aws-ec2-inven-collector)
수백개 이상의 AWS 에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다.

### [MS Azure Cloud Service Plugin](https://github.com/spaceone-dev/plugin-azure-cloud-service-inven-collector)
Azure에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다.

### [Google Cloud Service Plugin](https://github.com/spaceone-dev/plugin-google-cloud-service-inven-collector)
Google Cloud 에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다.

### [Oracle Cloud Service Plugin](https://github.com/spaceone-dev/plugin-oracle-cloud-service-inven-collector)
Oracle Cloud 에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다.

### [Alibaba Cloud Service Plugin](https://github.com/spaceone-dev/plugin-alibaba-cloud-ecs-inven-collector)
  Alibaba Cloud 에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다.


<!-- {{< cardpane >}}
{{< card header="**Amazon Web Service**" title="AWS Cloud Service Plugin" subtitle="수백개 이상의 AWS 에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다." footer="[See AWS Cloud Service Plugin](https://github.com/spaceone-dev/plugin-aws-ec2-inven-collector)">}}
![AWS](/docs/references/supported_technologies/supported_technologies_img/aws_img.png)
{{< /card >}}
{{< card header="**MS Azure**" title="MS Azure Cloud Service Plugin" subtitle="Azure에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다." footer="[See Azure Cloud Service Plugin](https://github.com/spaceone-dev/plugin-azure-cloud-service-inven-collector)" >}}
![Azure](/docs/references/supported_technologies/supported_technologies_img/azure_img.png)
{{< /card >}}
{{< card header="**Google Cloud**" title="Google Cloud Service Plugin" subtitle="Google Cloud 에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다." footer="[See Google Cloud Service Plugin]()" >}}
![Google Cloud](/docs/references/supported_technologies/supported_technologies_img/google_cloud_img.png)
{{< /card >}}
{{< card header="**Oracle Cloud**" title="Oracle Cloud Service Plugin" subtitle="Oracle Cloud 에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다." footer="[See Oracle Cloud Service Plugin]()" >}}
![Oracle Cloud](/docs/references/supported_technologies/supported_technologies_img/oracle_cloud_img.png)
{{< /card >}}
{{< card header="**Alibaba Cloud**" title="Alibaba Cloud Service Plugin" subtitle="Alibaba Cloud 에서 주로 사용되는 Cloud Resource를 자동으로 탐색하여 분류 합니다." footer="[See Alibaba Cloud Service Plugin]()" >}}
![Alibaba Cloud](/docs/references/supported_technologies/supported_technologies_img/alibaba_cloud_img.png)
{{< /card >}}
{{< /cardpane >}}--> 


## Identity

_**Identity.auth**_ Type의 Plugin은 SpaceONE User의 인증 관리 역할을 수행합니다. 
Plugin을 통해 사용자의 회사 계정과 SSO를 유지할 수 있습니다. 

### [Google oAuth Identity Plugin](https://github.com/spaceone-dev/plugin-googleoauth2-identity-auth)
### [KeyCloak Identity Plugin](https://github.com/spaceone-dev/plugin-keycloak-identity-auth)

<!-- {{< cardpane >}}
{{< card header="**Google oAuth2**" title="Google oAuth Identity Plugin" subtitle="" footer="[See Google Auth Plugin]()" >}}
![Google oAuth](/docs/references/supported_technologies/supported_technologies_img/google_img.png)
{{< /card >}}
{{< card header="**KeyCloak**" title="KeyCloak Identity Plugin" subtitle="" footer="[See KeyCloak Auth Plugin]()" >}}
![Keycloak](/docs/references/supported_technologies/supported_technologies_img/keycloak_img.png)
{{< /card >}}
{{< /cardpane >}} -->

## Monitoring

### DataSource

### [AWS CloudWatch DataSource Plugin](https://github.com/spaceone-dev/plugin-aws-cloudwatch-mon-datasource)
### [Azure Monitor DataSource Plugin](https://github.com/spaceone-dev/plugin-azure-monitor-mon-datasource)
### [Google Cloud Monitor DataSource Plugin](https://github.com/spaceone-dev/plugin-google-stackdriver-mon-datasource)
<br>
<!-- {{< cardpane >}}
{{< card header="**AWS CloudWatch**" title="AWS CloudWatch DataSource Plugin" subtitle="" footer="[See AWS CloudWatch DataSource Plugin]()" >}}
![AWS CloudWatch DataSource](/docs/references/supported_technologies/supported_technologies_img/aws_cloudwatch_img.png)
{{< /card >}}
{{< card header="**Azure Monitor**" title="Azure Monitor DataSource Plugin" subtitle="" footer="[See Azure Monitor DataSource Plugin]()" >}}
![Azure Monitor DataSource](/docs/references/supported_technologies/supported_technologies_img/azure_monitor_img.png)
{{< /card >}}
{{< card header="**Google StackDriver**" title="Google Cloud Monitor DataSource Plugin" subtitle="" footer="[See Google Monitor DataSource Plugin]()" >}}
![Google Cloud Monitor DataSource](/docs/references/supported_technologies/supported_technologies_img/google_cloud_monitor_img.jpg)
{{< /card >}}
{{< /cardpane >}} -->

### Webhook

### [AWS Simple Notification Webhook Plugin](https://github.com/spaceone-dev/plugin-aws-sns-mon-webhook)
### [Zabbix Webhook Plugin](https://github.com/spaceone-dev/plugin-zabbix-mon-webhook)
### [Grafana Webhook Plugin](https://github.com/spaceone-dev/plugin-grafana-mon-webhook)
<br>
<!-- {{< cardpane >}}
{{< card header="**AWS SNS**" title="AWS Simple Notification Webhook Plugin" subtitle="" footer="[See AWS Simple Monitoring Webhook Plugin]()" >}}
![AWS Simple Notification Webhook Plugin](/docs/references/supported_technologies/supported_technologies_img/aws_sns_img.png)
{{< /card >}}
{{< card header="**Zabbix**" title="Zabbix Webhook Plugin" subtitle="" footer="[See Zabbix Monitoring Webhook Plugin]()" >}}
![Zabbix Webhook Plugin](/docs/references/supported_technologies/supported_technologies_img/zabbix_img.png)
{{< /card >}}
{{< card header="**Grafana**" title="Grafana Webhook Plugin" subtitle="" footer="[See Grafana Monitoring Webhook Plugin]()" >}}
![Grafana Webhook Plugin](/docs/references/supported_technologies/supported_technologies_img/grafana_img.png)
{{< /card >}}
{{< /cardpane >}} -->

### Notification

### [API Direct Connect Protocol Plugin](https://github.com/spaceone-dev/plugin-api-direct-mon-webhook)
### [AWS SNS Protocol Plugin](https://github.com/spaceone-dev/plugin-aws-sns-mon-webhook)
### [Slack Protocol Plugin](https://github.com/spaceone-dev/plugin-slack-noti-protocol)
### [Telegram Protocol Plugin](https://github.com/spaceone-dev/plugin-telegram-noti-protocol)
### [Email Protocol Plugin](https://github.com/spaceone-dev/plugin-email-noti-protocol)

<!-- {{< cardpane >}}
{{< card header="AWS Direct Connect" title="AWS Direct Connect Protocol Plugin" subtitle="" footer="[See AWS Direct Connect Protocol Plugin]()" >}}
![AWS Direct Connect Protocol Plugin](/docs/references/supported_technologies/supported_technologies_img/aws_direct_connect_img.png)
{{< /card >}}
{{< card header="AWS SES" title="AWS SES Protocol Plugin" subtitle="" footer="[See AWS SES Protocol Plugin]()" >}}
![AWS SES Protocol Plugin](/docs/references/supported_technologies/supported_technologies_img/aws_simple_email_service_img.png)
{{< /card >}}
{{< card header="AWS SNS" title="AWS SNS Protocol Plugin" subtitle="" footer="[See AWS SNS Protocol Plugin]()" >}}
![AWS SNS Protocol Plugin](/docs/references/supported_technologies/supported_technologies_img/aws_simple_notification_service_img.png)
{{< /card >}}
{{< card header="Slack" title="Slack Protocol Plugin" subtitle="" footer="[See Slack Protocol Plugin]()" >}}
![Slack Protocol Plugin](/docs/references/supported_technologies/supported_technologies_img/slack_img.png)
{{< /card >}}
{{< card header="Telegram" title="Telegram Protocol Plugin" subtitle="" footer="[See Telegram Protocol Plugin]()" >}}
![Telegram Protocol Plugin](/docs/references/supported_technologies/supported_technologies_img/telegram_img.png)
{{< /card >}}
{{< /cardpane >}} -->


## Billing

### [Megazone Hyperbilling Billing Service](https://github.com/spaceone-dev/plugin-aws-hyperbilling-bill-datasource)

<!-- {{< cardpane >}}
{{< card header="**Megazone Hyperbilling**" title="Megazone Hyperbilling Billing Service" subtitle="" footer="[See Hyperbilling DataSource Plugin]()" >}}
![Hyperbilling DataSource Plugin](/docs/references/supported_technologies/supported_technologies_img/megazone_img.png)
{{< /card >}}
{{< /cardpane >}} -->



## Power Scheduler

<!-- {{< cardpane >}}
{{< card header="**AWS Power Controller**" title="AWS Power Controller Plugin" subtitle="" footer="[See AWS Power Controller Plugin]()" >}}
![AWS Power Controller Plugin](/docs/references/supported_technologies/supported_technologies_img/aws_autoscaling_img.png)
![AWS Power Controller Plugin](/docs/references/supported_technologies/supported_technologies_img/aws_rds_img.png)
{{< /card >}}
{{< card header="**Google Power Controller**" title="Google Power Controller Plugin" subtitle="" footer="[See Google Power Controller Plugin]()" >}}
![Google Power Controller Plugin](/docs/references/supported_technologies/supported_technologies_img/google_cloud_compute_engine_img.jpg)
{{< /card >}}
{{< /cardpane >}} -->
