---
title: "Quick Start"
linkTitle: "Quick Start"
weight: 1
date: 2022-06-23
description: >
    **에셋 인벤토리** 서비스를 빠르게 사용하기 위한 과정을 소개합니다.
---

## 서비스 계정 생성하기
[에셋 인벤토리 > 서비스 계정] 페이지에서 클라우드 서비스 계정을 추가합니다.

(1) 추가할 클라우드 서비스를 선택합니다.

![service-account-provider-menu](/ko/docs/guides/asset-inventory/quick-start-img/service-account-provider-menu.png)

(2) [추가] 버튼을 클릭합니다.

![service-account-add-button](/ko/docs/guides/asset-inventory/quick-start-img/service-account-add-button.png)

(3) 서비스 계정 생성 폼을 작성합니다.

(3-1) 기본 정보를 입력합니다.

![service-account-add-base-info](/ko/docs/guides/asset-inventory/quick-start-img/service-account-add-base-info.png)

(3-2) 해당 서비스 계정에 따른 리소스를 수집할 프로젝트를 지정합니다.

![service-account-connect-project](/ko/docs/guides/asset-inventory/quick-start-img/service-account-connect-project.png)

(3-3) 암호화 키 정보를 입력합니다.

![service-account-add-key](/ko/docs/guides/asset-inventory/quick-start-img/service-account-add-key.png)

## 컬렉터 생성하기
[에셋 인벤토리 > 컬렉터] 페이지에서 리소스를 수집할 컬렉터를 생성합니다.

(1) [생성] 버튼을 클릭합니다.

![collector-create-button](/ko/docs/guides/asset-inventory/quick-start-img/collector-create-button.png)

(2) 리소스 수집 시 사용할 플러그인을 선택합니다.

![collector-plugin-list](/ko/docs/guides/asset-inventory/quick-start-img/collector-plugin-list.png)

(3) 컬렉터 생성 폼을 작성합니다.
(3-1) 이름과 버전 등 기본 정보를 입력합니다.

![collector-create-base-info](/ko/docs/guides/asset-inventory/quick-start-img/collector-create-base-info.png)

(3-2) 필요 시 태그를 추가합니다.

![collector-create-tag](/ko/docs/guides/asset-inventory/quick-start-img/collector-create-tag.png)

(4) 컬렉터 실행을 위한 스케줄을 생성합니다.

(4-1) [에셋 인벤토리 > 컬렉터] 페이지에서 테이블의 컬렉터 하나를 선택한 뒤, [스케줄] 탭에서 [추가] 버튼을 클릭합니다.

![collector-single-select](/ko/docs/guides/asset-inventory/quick-start-img/collector-single-select.png)

(4-2) [스케줄 추가] 모달에서 컬렉터를 실행할 시간을 설정한 뒤 [확인] 버튼을 클릭합니다.

![collector-schedule-modal](/ko/docs/guides/asset-inventory/quick-start-img/collector-schedule-modal.png)


## 수집된 리소스 확인하기
[에셋 인벤토리 > 클라우드 서비스]에서 수집된 리소스를 조회할 수 있습니다.

![collector-resource-inquiry](/ko/docs/guides/asset-inventory/quick-start-img/collector-resource-inquiry.png)
