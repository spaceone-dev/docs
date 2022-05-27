---
title: "Commit Convention"
linkTitle: "Commit Convention"
weight: 3
date: 2022-05-27
description: >
    Frontend Commit Convention
no_list: true
---


프론트엔드 커밋 컨벤션에 대한 문서입니다.
[Console](https://github.com/spaceone-dev/console),
[Design System](https://github.com/spaceone-dev/spaceone-design-system),
[Core Lib](https://github.com/spaceone-dev/console-core-lib)

## 커밋 메시지 구조

```text
<타입>[적용 범위(선택 사항)]: <설명>

[본문(선택 사항)]

[꼬리말(선택 사항)]
```

## 커밋 메시지 구조적 요소

| Type            | Description                                                     | Remark  |
|-----------------|-----------------------------------------------------------------|---------|
| fix             | Bug Fix <br /> API 변경 사항 없이 내부 수정                               | PATCH   |
| feat            | 기능 추가 <br /> API 변경 (하위 호환)                                     | MINOR   |
| perf            | 성능 향상을 위한 코드 변경                                                 | MAJOR   |
| BREAKING CHANGE | API 의 변경, 큰 변화                                                  | MAJOR   |
| refactor        | 내부적인 리팩토링                                                       | 앵귤러 컨벤션 |
| ci              | CI 변경 (workflow, etc)                                           | 앵귤러 컨벤션 |
| build           | build 관련 변경 (webpack, dependencies, etc)                        | 앵귤러 컨벤션 |
| docs            | 문서 작성, 수정                                                       | 앵귤러 컨벤션 |
| style           | 코드 의미적으로는 변하지 않는 커밋 (css, formatting, missing semi-colons, etc) | 앵귤러 컨벤션 |
| revert          | 이전 커밋으로 revert                                                  | 앵귤러 컨벤션 |
| chore           | 그 외 자잘한 수정                                                      | 앵귤러 컨벤션 |

## 주의 사항
1. **반드시** 커밋 메시지 구조에 맞는 메시지를 작성하여야 합니다. 
   1. 컨벤션과 다를 시, commitLint 에 의해 commit 이 fail 할 수 있습니다.
2. 타입 뿐 아니라 적용 범위, 설명, 본문, 꼬리말 모두 **영어**로 작성하는 것을 지향합니다.

## References

- [Conventional Commits](https://www.conventionalcommits.org/ko/v1.0.0/)
- [Angular Commit Message Guides](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines)
