---
title: "접근 설정(API & CLI)"
linkTitle: "접근 설정(API & CLI)"
weight: 2
date: 2022-06-23
description: >
    스페이스원에 연결하기 위한 인증 키인 **API 키**를 생성하고, 이를 이용하여 프로그래밍을 하거나 **CLI**를 통해 커맨드로 클라우드포레를 제어할 수 있습니다.
---

클라우드포레가 제공하는 커맨드라인 도구인 [**Spacectl**](https://github.com/spaceone-dev/spacectl)을 사용하기 위해서는 **API 키**가 필요합니다.

## API 키 생성하기

(1) [마이페이지 > 접근 설정(API & CLI)] 페이지에서 [API Key 생성] 버튼을 클릭하면 즉시 API 키가 생성됩니다.

![apikey-create-01](/ko/docs/guides/my-page/access-with-api-cli-img/apikey-create-01.png)

(2) [더 보기] 버튼을 클릭하면 JSON 형식의 API 키와 YAML 형식의 Spacectl 환경설정 파일 내용을 확인하고 다운받을 수 있습니다.

![apikey-create-02](/ko/docs/guides/my-page/access-with-api-cli-img/apikey-create-02.png)

{{<alert title="API 키 발급 시 주의사항">}}
• API 키는 생성 시에 단 한 번만 확인할 수 있습니다.

• API 키는 사용자 아이디 당 2개까지 발급할 수 있습니다.
{{</alert>}}

## API 키 활성화 / 비활성화 하기

발급된 API 키는 삭제하거나 활성화/비활성화 할 수 있습니다.

(1) [작업] 드롭다운에서 [활성화] 또는 [비활성화] 메뉴를 선택합니다.

![apikey-enable-01](/ko/docs/guides/my-page/access-with-api-cli-img/apikey-enable-01.png)

(2) 모달이 열리면 [확인] 버튼을 클릭합니다.

![apikey-enable-02](/ko/docs/guides/my-page/access-with-api-cli-img/apikey-enable-02.png)
![apikey-enable-03](/ko/docs/guides/my-page/access-with-api-cli-img/apikey-enable-03.png)

## API 키 삭제하기

(1) [작업] 드롭다운에서 [삭제] 메뉴를 선택합니다.

![apikey-delete-01](/ko/docs/guides/my-page/access-with-api-cli-img/apikey-delete-01.png)

(2) [API 키 삭제] 모달이 열리면 [확인] 버튼을 클릭합니다. 

![apikey-delete-02](/ko/docs/guides/my-page/access-with-api-cli-img/apikey-delete-02.png)