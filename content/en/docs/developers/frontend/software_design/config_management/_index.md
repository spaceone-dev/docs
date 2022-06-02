---
title: "Config Management"
linkTitle: "Config Management"
weight: 4
date: 2022-06-2
description:
    How To Manage Frontend Configuration
---

App에 필요한 구성 요소를 정의한다. 주로, **환경 별로 다른 값**을 다룬다.

## 환경 별 우선순위

`default.json`이 우선적으로 적용된다.

development 환경일 경우, `development.json`의 값이 덮어 쓰여 적용된다.

## 환경 설정 방법

### Dockerfile 수정

Dockerfile에서 `npm run build` 커맨드 전 **NODE_ENV**로 환경 설정 가능

```
...
ENV NODE_ENV development
...
```

### Webstorm Configurations 수정

Run/Debug Configuration 설정 시 Environment 필드값 수정

![](/docs/developers/frontend/software_design/config_management/config_management_img/config_management_webstorm_setting.png)



## Default Config 정보
| Name             | Description                                                                                                            |
|------------------|------------------------------------------------------------------------------------------------------------------------|
| CONSOLE_API      | 콘솔에서 사용하는 API의 엔드포인트를 정의                                                                                               |
| GTAG_ID          | Google Analytics를 위해 사용                                                                                                |
| DOMAIN_NAME      | 사이트 도메인 이름                                                                                                             |
| DOMAIN_NAME_REF  | ‘hostname’ 일 경우, 사이트 도메인 이름을 추출하여 Domain 정보 로드                                                                         |
| ADMIN_DOMAIN     |                                                                                                                        |
| AMCHARTS_LICENSE | 차트 라이브러리인 amcharts의 라이센스 정보                                                                                            |
| MOCK             | MOCK API 사용 여부 및 MOCK API의 엔드포인트 정의                                                                                    |
| ASSET_PATH       | asset에 사용되는 엔드포인트 정보                                                                                                   |
| DOMAIN_IMAGE     | SignIn 페이지 및 GNB에 사용되는 이미지의 url 정의                                                                                     |
| DOCS             | 관련 문서 링크를 만들기 위한 정보<br>- label, link 를 가진 객체 배열<br>- ejs template 문법을 지원<br>&nbsp;- 제공 변수: lang (사용자 언어 코드. e.g. "en") |
| BILLING_ENABLED  | billing 서비스 이용 가능한 도메인 리스트 정의                                                                                          |
| CONTACT_LINK     | SignIn 페이지의 contact us 링크 정의                                                                                           |

- development.json 권장 예시
    ```json
    {
        "VUE_APP_API": {
          "ENDPOINT": "https://sample.com"
        },
        "GTAG_ID": "DISABLED",
        "DOMAIN_NAME": "sample",
        "DOMAIN_NAME_REF": "config",
        "ASSETS_ENDPOINT": "https://sample-asset.com/assets/"
    }
    ```


## Config 파일 위치

- Default: `<SOURCE_ROOT>/public/config/default.json`
- Each Environment: `<SOURCE_ROOT>/public/config/<NODE_ENV>.json`


## Config 사용 방법

```typescript
import config from '@/lib/config'

config.get(); // All Values
config.get('VUE_APP_API.ENDPOINT'); // Value of specific key
```

