---
title: "[IAM] Authentication"
linkTitle: "[IAM] Authentication"
weight: 3
date: 2022-07-05
description: >

---

## 개요

클라우드포레는 사용자의 인증를 위한 수단으로 타 서비스의 계정을 사용하는 인증방식을 플러그인으로 제공하고 있습니다.   
현재 클라우드포레에서 지원하는 인증 플러그인 목록은 **플러그인 지원 목록**을 참조하세요.

구글의 계정을 통해 사용자 인증을 받는 **Google Oauth2** 플러그인과  
표준 프로토콜을 통한 SSO(Single Sign-On)을 지원하는 **Keycloak** 플러그인을 사용할 수 있습니다.  
보다 자세한 설정은 아래 **설정 가이드 링크**를 참조하세요.



## 플러그인 지원 목록

| **플러그인** | **설정 가이드 링크** |
| --- | --- |
| Google Oauth2 | https://github.com/spaceone-dev/plugin-googleoauth2-identity-auth/blob/master/docs/ko/GUIDE.md |
| Keycloak | https://github.com/spaceone-dev/plugin-keycloak-identity-auth/blob/master/docs/ko/GUIDE.md |
