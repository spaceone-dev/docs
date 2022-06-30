---
title: "유지 관리 기간"
linkTitle: "유지 관리 기간"
weight: 6
date: 2022-06-07
description: >
    정기, 비정기적인 시스템 작업 기간 내에 발생하는 [얼럿](/ko/docs/guides/alert-manager/alert/)에 대하여서는 [알림](/ko/docs/guides/alert-manager/notification/) 발송을 차단해야 할 필요가 있습니다.
    <br>
    **유지 관리 기간**을 설정하여 해당 기간 동안에는 알림이 일어나지 않도록 차단할 수 있습니다.

---


유지 관리 기간은 프로젝트에 종속되며, 프로젝트 상세 페이지에서 관리할 수 있습니다.

![maintenance](/ko/docs/guides/alert-manager/maintenance-img/maintenance.png)



## 유지 관리 기간 생성하기

(1) 프로젝트 상세 페이지의 우측 상단에 있는 [유지 관리 기간 생성] 버튼을 클릭합니다.

![create-maintenance-window-1](/ko/docs/guides/alert-manager/maintenance-img/create-maintenance-window-1.png)

(2) 유지 관리 기간의 [제목]을 입력하고, 얼럿 발생을 제한할 스케줄을 설정합니다.

![create-maintenance-window-2-1](/ko/docs/guides/alert-manager/maintenance-img/create-maintenance-window-2-1.png)

스케줄을 지정할 때 바로 시작하거나 예정된 시간에 시작하도록 할 수 있습니다.
<br>
바로 시작하기를 원한다면 [지금 시작하고 끝내기] 옵션을, 예정된 작업 일정을 등록하려면 [예정된 시간에 시작하기] 옵션을 선택하십시오.

![create-maintenance-window-2-2](/ko/docs/guides/alert-manager/maintenance-img/create-maintenance-window-2-2.png)


(3) [확인] 버튼을 클릭하면 생성이 완료됩니다.



## 유지 관리 기간 편집하기

아직 종료되지 않은 유지 관리 기간만 편집이 가능합니다.

(1) 프로젝트 상세 페이지의 [얼럿] 탭 아래의 [유지 관리 기간] 탭을 선택합니다.

(2) 편집하려는 대상을 선택하고 [편집] 버튼을 클릭합니다.

![update-maintenance-window-1](/ko/docs/guides/alert-manager/maintenance-img/update-maintenance-window-1.png)


(3) 원하는 항목을 변경한 후 [확인] 버튼을 클릭하여 완료합니다.

![update-maintenance-window-2](/ko/docs/guides/alert-manager/maintenance-img/update-maintenance-window-2.png)


## 유지 관리 기간 종료하기

(1) 프로젝트 상세 페이지의 [얼럿] 탭 아래의 [유지 관리 기간] 탭을 선택합니다.

(2) 편집하려는 대상을 선택하고 [종료] 버튼을 클릭하여 종료합니다.

![delete-maintenance-window](/ko/docs/guides/alert-manager/maintenance-img/delete-maintenance-window.png)

