---
title: "시작하기"
linkTitle: "Getting Started"
weight: 3
date: 2022-05-31
description: >
    이 페이지는 [SpaceOne Console](https://github.com/spaceone-dev/console) 개발을 시작하기 위한 안내문서입니다.
no_list: true
---

## 개발 환경 세팅


### Fork

현재 스페이스원의 콘솔은 오픈소스로 운영중에 있습니다.

개발에 기여하기위해 먼저 [console 레포지토리](https://github.com/spaceone-dev/console)를 개인 github 계정에 포크해 줍니다.

### Clone

이후 포크해온 레포지토리를 로컬로 클론해 줍니다.

서브모듈로 [assets](https://github.com/spaceone-dev/console-assets)과 [번역 관련 레포지토리](https://github.com/spaceone-dev/console-translation.git)가 사용중이기 때문에 함께 초기화합니다.

```shell
git clone --recurse-submodules https://github.com/[github username]/console

cd console
```

### Run Console

콘솔을 실행 실행시키기 위해 npm으로 의존성을 설치합니다.
```shell
npm install --no-save
```
이후 개발환경을 위한 config 파일을 `public/config/development.json` 작성합니다.
(config 파일 작성은 [여기]()를 참고 하십시오)

<br/>

마지막으로 스크립트를 실행합니다.
```shell
npm run serve
```

### Build

배포 가능한 zip을 생성하려면 아래의 스크립트를 실행하시면 됩니다.

```shell
npm run build
```


## 차트 라이선스

콘솔은 내부적으로 모든 차트에 대해 amCharts를 사용합니다.

콘솔을 사용하기 전에 amCharts의 라이선스를 확인하시고, 자신에게 맞는 amCharts 라이선스를 구매하여 콘솔에서 사용하려면 아래와 같이 진행해주십시오.

<br/>

`public/config/default.json`에 라이센스 키 추가

```shell
{
    "AMCHARTS_LICENSE": {
    "CHARTS": "",
    "MAPS": "",
    "TIMELINE": ""
    }
}
```

## 스타일

<br/>

스타일 정의에 있어 SpaceOne Console은 [tailwind css](https://tailwindcss.com)와 [postcss](https://postcss.org/)를 사용중에 있습니다.

SpaceOne의 color palette에 따라 tailwind 커스텀을 통해 적용되어 있습니다. (세부 정보는 [storybook](https://storybook.developer.spaceone.dev/?path=/docs/foundation-styles-colors--all-colors)을 참고해주세요)
