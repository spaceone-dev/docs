---
title: "Service Account"
linkTitle: "Service Account"
weight: 5
date: 2022-06-07
description: >
    **서비스 계정**에서 각 클라우드 서비스의 계정들을 손쉽게 통합, 관리, 추적할 수 있습니다.
---

## 서비스 계정 추가하기

(1) [에셋 인벤토리 > 서비스 계정] 페이지에서 추가할 클라우드 서비스를 선택합니다.

![service-account-provider-menu](/ko/docs/guides/asset-inventory/service-account-img/service-account-provider-menu.png)

(2) [추가] 버튼을 클릭합니다.

![service-account-add-button](/ko/docs/guides/asset-inventory/service-account-img/service-account-add-button.png)

(3) 서비스 계정 생성 폼을 작성합니다.

(3-1) 기본 정보를 입력합니다.

![service-account-add-base-info](/ko/docs/guides/asset-inventory/service-account-img/service-account-add-base-info.png)

(3-2) 해당 서비스 계정에 따른 리소스를 수집할 프로젝트를 지정합니다.

![service-account-connect-project](/ko/docs/guides/asset-inventory/service-account-img/service-account-connect-project.png)

(3-3) 암호화 키 정보를 입력합니다.

![service-account-add-key](/ko/docs/guides/asset-inventory/service-account-img/service-account-add-key.png)

(4) [저장] 버튼을 클릭하여 완료합니다.

## 서비스 계정 관리하기

### 프로젝트 변경하기

프로젝트를 변경하고자 하는 서비스 계정을 선택한 뒤, 작업 메뉴에서 [프로젝트 변경] 버튼을 클릭합니다.

![service-account-project-change-menu](/ko/docs/guides/asset-inventory/service-account-img/service-account-project-change-menu.png)

생성된 모달에서 변경할 프로젝트를 선택한 후 [확인] 버튼을 클릭합니다.

![service-account-project-change-selected](/ko/docs/guides/asset-inventory/service-account-img/service-account-project-change-selected.png)

서비스 계정의 프로젝트를 선택 해제 하고 싶은 경우는, 모달 하단의 [프로젝트 선택 안 함] 항목을 선택한 후 [확인] 버튼을 클릭합니다.

![service-account-project-unselect-selected](/ko/docs/guides/asset-inventory/service-account-img/service-account-project-unselect-selected.png)

### 콘솔 연결하기

콘솔에 연결하고자 하는 서비스 계정을 선택한 뒤, [작업] 드롭다운에서 [콘솔 연결] 메뉴를 클릭합니다.

![sevice-account-console-connect-menu](/ko/docs/guides/asset-inventory/service-account-img/sevice-account-console-connect-menu.png)

## 상세 정보 확인하기

상세 정보를 확인하고자 하는 프로젝트를 선택하면 하단 테이블에 정보가 표시됩니다.

![service-account-single-select](/ko/docs/guides/asset-inventory/service-account-img/service-account-single-select.png)

- [상세 정보] 탭에서 다음과 같은 정보를 확인할 수 있습니다.
<br />
  • 아이디
<br />
  • 이름
<br />
  • 프로젝트
<br />
  • 생성날짜
<br />
- [태그] 탭에서 태그에 대해 조회, 편집 그리고 추가가 가능합니다.
- [암호화 키] 탭에서 키를 조회 및 검색이 가능합니다.
- [연관된 멤버] 탭에서 해당 서비스계정에 대해 조회 및 검색이 가능합니다.
<br />
  • 연결되어 있는 프로젝트의 멤버 중 Project Admin 권한을 가진 사람이 연관된 멤버로 배정됩니다.
<br />
  • 자세한 내용은 [멤버](/ko/docs/guides/project/member)에서 확인 가능합니다.

## 서비스 계정 삭제하기
{{<alert>}}
삭제한 서비스 계정은 복구가 불가능하니 유의해주시길 바랍니다.
{{</alert>}}

삭제하고자 하는 서비스 계정을 선택한 뒤, [작업] 드롭다운에서 [삭제] 메뉴를 클릭합니다.

![service-account-delete-menu](/ko/docs/guides/asset-inventory/service-account-img/service-account-delete-menu.png)

[서비스 계정 삭제] 모달에서 삭제하고자 하는 서비스 계정의 이름을 입력한 후 [확인] 버튼을 클릭합니다.

![service-account-delete-modal2](/ko/docs/guides/asset-inventory/service-account-img/service-account-delete-modal2.png)
