---
title: "Escalation Policy"
linkTitle: "Escalation Policy"
weight: 8
date: 2022-06-07
description: >
    에스컬레이션 정책을 통해 얼럿에 단계별 규칙을 적용하여, 수신된 얼럿을 프로젝트의 멤버들에게 효과적으로 전달합니다.


    각 규칙에는 설정된 레벨이 존재하고, 레벨마다 해당하는 알림 채널에 얼럿이 전파됩니다.
---

웹훅을 통해 수신한 얼럿이 프로젝트의 멤버들에게 알림으로 전송될지 여부는 **에스컬레이션 정책**을 통해 결정됩니다.
<br>
에스컬레이션 정책은 다음 두 곳에서 관리할 수 있습니다.

- **[얼럿 매니저 > 에스컬레이션 정책]** 페이지: `글로벌`과 `프로젝트` 범위의 에스컬레이션 정책 관리
- **[프로젝트]** 상세 페이지: `프로젝트` 범위의 에스컬레이션 정책 관리

## 에스컬레이션 정책 생성하기

[에스컬레이션 정책] 페이지에 대한 `MANAGE` 권한을 가진 사용자일 경우, 에스컬레이션 정책을 생성할 수 있습니다.

### [에스컬레이션 정책] 페이지에서 생성하기
(1) [얼럿 매니저 > 에스컬레이션 정책] 페이지에서 [생성] 버튼을 클릭합니다.

![escalation-policy-full-page](/ko/docs/guides/alert-manager/escalation-policy-img/escalation-policy-full-page.png)

(2) 에스컬레이션 정책을 생성하기 위한 설정들을 입력합니다.

![escalation-policy-create-modal](/ko/docs/guides/alert-manager/escalation-policy-img/escalation-policy-create-modal.png)

| 정책        | 설명                                                                                                  |
|-----------|-----------------------------------------------------------------------------------------------------|
| 종료 조건(상태) | 발생된 알람이 중지되는 조건을 정의합니다.                                                                             |
| 범위        | 에스컬레이션 정책을 사용할 수 있는 범위를 나타냅니다. `글로벌`인 경우 도메인내 모든 프로젝트에서 사용 가능하고, `프로젝트`인 경우 지정된 프로젝트 내에서만 사용 가능합니다. |
| 프로젝트      | 범위가 `프로젝트`인 경우 대상이 되는 프로젝트를 나타냅니다.                                                                  |
| 에스컬레이션 규칙 | 단계별 알림 송신을 위해 규칙을 정의합니다.<br/>설정된 레벨에 속하는 알림 채널에 얼럿을 전달하며, 2단계 이상부터 단계 간 텀을 분 단위로 부여할 수 있습니다.        |
| 반복 횟수     | 얼럿 알림을 몇회 반복할 것인지 정의합니다. 최대 9회까지 반복 가능합니다.                                                          |

{{<alert>}}
**범위**와 **프로젝트** 항목은 [얼럿 매니저 > 에스컬레이션 정책] 페이지에서 생성할 경우에만 나타납니다.
<br>
[프로젝트] 상세 페이지에서 생성할 경우, 범위는 자동으로 `프로젝트`가 선택되며, 해당 프로젝트가 대상으로 지정됩니다.
{{</alert>}}

### [프로젝트] 상세 페이지에서 생성하기
[프로젝트] 상세 페이지에서 에스컬레이션 정책을 생성하면, 자동으로 해당 프로젝트가 에스컬레이션 정책 대상으로 지정됩니다.

(1) 프로젝트 상세 페이지의 [얼럿] 탭 내부에서, [설정] 탭으로 이동합니다.

![create-escalation-policy-1](/ko/docs/guides/alert-manager/escalation-policy-img/create-escalation-policy-1.png)

(2) 에스컬레이션 정책 영역에서 [변경] 버튼을 클릭합니다.

![create-escalation-policy-2](/ko/docs/guides/alert-manager/escalation-policy-img/create-escalation-policy-2.png)

(3) [새로운 정책 생성] 탭을 클릭합니다.

![create-escalation-policy-3](/ko/docs/guides/alert-manager/escalation-policy-img/create-escalation-policy-3.png)

(4) 에스컬레이션 정책을 생성하기 위한 설정들을 입력합니다.

![create-escalation-policy-4](/ko/docs/guides/alert-manager/escalation-policy-img/create-escalation-policy-4.png)

### 레벨

레벨은 얼럿을 단계별로 전송할 때, 해당 단계에서 얼럿을 전송할 전송 범위입니다.

해당 프로젝트에 알림 채널을 설정할 수 있으며, 알림 채널은 각각 자신의 레벨을 가집니다.

![escalation-policy-level](/ko/docs/guides/alert-manager/escalation-policy-img/escalation-policy-level.png)

에스컬레이션 규칙을 정의할 때, [알림 레벨]을 설정하게 됩니다. 설정된 단계마다 해당하는 레벨의 알림 채널들로 얼럿을 전송하게 됩니다.

{{<alert>}}
얼럿이 상위 레벨으로 단계별 진행 되기 위한 기간 차이를 충분히 설정하는 것이 좋습니다.
{{</alert>}}

(5) 모든 설정이 완료되었다면 [확인] 버튼을 클릭해 에스컬레이션 정책을 생성합니다.




## 기본 정책으로 설정하기

에스컬레이션 정책 목록에서 하나를 선택한 뒤, [작업] 드롭다운에서 [기본으로 설정하기] 메뉴를 선택해 해당 정책을 기본으로 설정할 수 있습니다.

새로운 프로젝트가 생성되고 얼럿을 활성화하면, 해당 정책이 자동으로 적용됩니다.

![set-as-default](/ko/docs/guides/alert-manager/escalation-policy-img/set-as-default.png)

{{< alert title="" >}}
단, 범위가 `글로벌` 인 정책만 [기본으로 설정하기]가 가능합니다.
{{< /alert >}}




## 에스컬레이션 편집 및 삭제하기

에스컬레이션 정책 목록에서 대상을 선택 후 [작업] 드롭다운에서 [편집] 및 [삭제]가 가능합니다.

![escalation-policy-update-delete](/ko/docs/guides/alert-manager/escalation-policy-img/escalation-policy-update-delete.png)

### 편집하기

편집의 경우 [생성] 버튼 클릭 시 생성되는 모달과 같은 형태이며, 범위를 제외한 모든 항목을 편집할 수 있습니다.

![update-escalation-policy](/ko/docs/guides/alert-manager/escalation-policy-img/update-escalation-policy.png)

### 삭제하기

삭제의 경우 아래와 같은 확인 모달을 통해 삭제를 진행할 수 있습니다.

![delete-escalation-policy](/ko/docs/guides/alert-manager/escalation-policy-img/delete-escalation-policy.png)

{{<alert>}}
기본 값으로 설정된 정책과 사용중인 정책은 삭제할 수 없습니다.
{{</alert>}}
