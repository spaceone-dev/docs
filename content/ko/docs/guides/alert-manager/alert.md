---
title: "얼럿"
linkTitle: "얼럿"
weight: 3
date: 2022-06-07
description: >
    **얼럿**은 서비스 운영 시 발생하는 모든 이슈를 정의한 것입니다.
    <br/>
    주로 관계자에게 알림을 발송하는 목적으로 생성됩니다.
---

### 얼럿의 생성 조건

- **수동 생성**: 지정된 프로젝트에 수동으로 알림이 필요한 경우 얼럿을 생성합니다.
- **웹훅 연동을 통한 자동 생성**: [웹훅](/ko/docs/guides/plugins/)은 외부 모니터링 서비스로부터 발생된 이벤트를 수신합니다. 그리고 수신한 이벤트 메시지를 정제하여 얼럿을 자동으로 생성합니다.

### 상태

얼럿은 아래와 같은 상태들을 가지고 있습니다.

| 상태 | 설명 |
| --- | --- |
| 확인 | 얼럿에 담당자가 할당되어 처리중인 상태 |
| 생성 | 얼럿이 최초 등록된 상태 |
| 완료 | 장애, 점검 등 얼럿의 내용이 처리 완료된 상태 |
| 에러 | 웹훅 연동을 통해 이벤트가 수신되었으나, 오류로 인해 얼럿이 정상적으로 등록되지 않은 상태 |

### 긴급도

클라우드포레에서 얼럿의 긴급도는 `높음`과 `낮음` 두 가지가 존재합니다.

얼럿 [수동 생성](/ko/docs/guides/alert-manager/alert/#얼럿-생성하기)의 경우에는 `높음` 과 `낮음` 두 가지로 생성되지만, [웹훅 연동을 통해 자동으로 생성](/ko/docs/guides/alert-manager/alert/#얼럿-생성하기)되는 경우에는 **심각도(Severity)** 에 따라 긴급도(Urgency)가 측정됩니다.

{{<alert title="심각도">}}
**심각도**는 일반적인 외부 모니터링 훅으로부터 받아오는 이벤트의 위험 강도를 나타냅니다.
`CRITICAL`, `ERROR`, `WARNING`, `INFO`, `NOT_AVAILABLE` 다섯 가지의 심각도가 있으며, 클라우드포레는 이를 얼럿으로 생성 시 아래와 같은 기준으로 긴급도를 설정합니다.

• `높음` : `CRITICAL`, `ERROR`, `NOT_AVAILABLE`

• `낮음` : `WARNING`, `INFO`
{{</alert>}}

## 얼럿 생성하기

(1) [콘솔에서 수동 얼럿 생성](/ko/docs/guides/alert-manager/alert/#콘솔에서-얼럿-수동-생성하기)

(2) [외부 모니터링 서비스에서 발생한 이벤트를 바탕으로 웹훅 연동을 통해 얼럿 자동 생성](/ko/docs/guides/alert-manager/alert/#외부-모니터링-서비스를-연결하여-얼럿-자동-생성하기) 

### 콘솔에서 얼럿 수동 생성하기

### Steps

(1) 얼럿 페이지로 이동 후 [생성] 버튼을 눌러줍니다.

![create-alert-step-1](/ko/docs/guides/alert-manager/alert-img/create-alert-step-1.png)

(2) 얼럿 생성 폼을 작성합니다.

![create-alert-step-2](/ko/docs/guides/alert-manager/alert-img/create-alert-step-2,3.png)

(2-1) 얼럿 제목을 입력하고 [긴급도](/ko/docs/guides/alert-manager/alert/#긴급도)를 선택합니다.

(2-2) 얼럿을 어떤 프로젝트에 대하여 발생시킬 것인지 지정해줍니다.

(2-3) 필요하다면 얼럿에 대한 추가적인 설명을 작성합니다.

(3) [확인] 버튼을 클릭하여 얼럿 생성을 완료합니다.

### 외부 모니터링 서비스를 연결하여 얼럿 자동 생성하기

웹훅 연동을 통한 얼럿 자동 생성을 하려면 **웹훅 생성**과 **연동 설정**이 필요합니다.

(1) 원하는 외부 모니터링 서비스에 해당하는 [웹훅을 추가](/ko/docs/guides/alert-manager/webhook/)합니다. 

![create-webhook-step-1](/ko/docs/guides/alert-manager/alert-img/create-webhook-step-1.png)

(2) 추가 된 웹훅의 웹훅 URL으로 각 [외부 모니터링 서비스와 연동](/ko/docs/guides/plugins/)해줍니다.

![create-webhook-step-2](/ko/docs/guides/alert-manager/alert-img/create-webhook-step-2.png)

(3) 연결되어 있는 모니터링 서비스에서 발생하는 이벤트의 메시지가 정제되어 얼럿으로 자동 생성됩니다.

### 얼럿 활용하기

클라우드포레의 얼럿을 활용한 여러가지 기능을 간단하게 살펴봅시다.

- [알림 채널](/ko/docs/guides/alert-manager/notification): 얼럿을 어떤 사용자에게 어떻게, 언제 전달할 것인지 등을 설정합니다.
- [에스컬레이션 정책](/ko/docs/guides/alert-manager/escalation-policy/): 단계별 규칙을 적용하여, 수신된 얼럿을 프로젝트의 멤버들에게 효과적으로 전달합니다.
- [이벤트 규칙](/ko/docs/guides/alert-manager/event-rule): 웹훅을 통해 수신된 이벤트는 조건에 따라 **얼럿**으로 생성됩니다.
- [유지 관리 기간](/ko/docs/guides/alert-manager/maintenance):  정기, 비정기적인 시스템 작업 일정을 등록하여 작업을 안내하고, 작업간 발생하는 **얼럿**을 차단합니다.


## 얼럿 목록 조회하기

자신의 계정이 관련된 모든 프로젝트의 얼럿을 조회할 수 있습니다.

얼럿 페이지에서 속성별로 정렬이 가능한 목록을 조회할 수 있으며, 얼럿의 `상태`, `긴급도`, `프로젝트` 등을 함께 보여줍니다.

### 얼럿 검색하기

![alert-search](/ko/docs/guides/alert-manager/alert-img/alert-search.png)

검색어를 입력하여 조건에 부합하는 얼럿 목록을 확인할 수 있으며, 원하는 얼럿의 제목을 클릭하여 얼럿 상세 페이지로 이동할 수 있습니다.
(고급 검색에 대한 상세 설명은 [여기](/ko/docs/guides/advanced/search/#고급-검색)를 참고하세요.)

### 얼럿 목록 탐색 조건

- [상태](/ko/docs/guides/alert-manager/alert/#상태) : 이전에 알아본 얼럿의 상태 별로 조회가 가능합니다.
- [긴급도](/ko/docs/guides/alert-manager/alert/#긴급도): 긴급도에 따라 검색이 가능합니다.
- 나에게 할당된 것만: 수신 받은 얼럿 중에서도 사용자에게 할당된 얼럿만 나열하여 목록을 조회할 수 있습니다.

### 목록에서 얼럿 상태 변경하기

목록에서 바로 얼럿의 상태 수정이 가능합니다.

(1) 상태를 수정할 얼럿을 선택하고, 오른쪽 상단의 [확인], [완료], [삭제] 중 원하는 버튼을 클릭합니다.

![update-alert-1](/ko/docs/guides/alert-manager/alert-img/update-alert-1.png)

(1-1) [확인] 버튼을 클릭하여 `확인` 상태로 변경하기

`확인` 상태는 담당자가 할당되어 처리중인 상태입니다.

상태 변경과 동시에 선택한 얼럿의 담당자를 본인으로 설정할 수 있으며, [확인] 버튼을 클릭하여 완료합니다.

![update-alert-1-1](/ko/docs/guides/alert-manager/alert-img/update-alert-1-1.png)

(1-2) [완료] 버튼을 클릭하여 `완료` 상태로 변경하기

`완료` 상태는 얼럿을 발생시킨 이슈가 처리 완료된 상태입니다. 

상태 변경과 동시에 노트를 작성할 수 있으며, [확인] 버튼을 클릭하여 완료합니다.

![update-alert-1-2](/ko/docs/guides/alert-manager/alert-img/update-alert-1-2.png)

(1-3) [삭제] 버튼을 클릭하여 얼럿 삭제하기

삭제할 얼럿 목록을 다시 한번 확인이 가능하며, [확인] 버튼을 클릭하여 삭제합니다.

![update-alert-1-3](/ko/docs/guides/alert-manager/alert-img/update-alert-1-3.png)

## 얼럿 살펴보기

얼럿 상세 페이지에서 얼럿에 대한 상세 정보와 히스토리를 조회하고, 관리할 수 있습니다.

![alert-detail-page](/ko/docs/guides/alert-manager/alert-img/alert-detail-page.png)

| 상세항목 | 설명 |
| --- | --- |
| 지속 시간 | 얼럿이 지속된 시간 |
| 설명 | 얼럿에 대한 설명으로, 사용자가 직접 작성한 내용 또는 외부 모니터링 서비스로부터 수신한 이벤트의 내용 |
| 규칙 | 외부 모니터링 서비스에서 얼럿이 발생한 조건 |
| 심각도 | 웹훅 이벤트의 데이터로부터 받은 심각도 |
| 에스컬레이션 정책 | 적용된 에스컬레이션 정책 |
| 프로젝트 | 얼럿이 발생된 프로젝트 |
| 생성 | 얼럿을 전송한 모니터링 서비스 |
| 리소스 이름 | 얼럿 발생 대상  |

### 이름 변경 및 삭제하기

[편집 아이콘] 버튼과 [삭제 아이콘] 버튼을 통해 얼럿의 이름 변경 및 얼럿 삭제가 가능합니다.

![update-alert-name-or-delete-alert](/ko/docs/guides/alert-manager/alert-img/update-alert-name-or-delete-alert.png)

### 상태 / 긴급도 / 담당자 변경하기

(1) 상태, 긴급도 변경

상태와 긴급도는 드롭다운을 통해 쉽게 수정할 수 있습니다.

![update-state-urgency](/ko/docs/guides/alert-manager/alert-img/update-state-urgency.png)

(2) 담당자 변경

(2-1) [할당] 버튼을 클릭합니다.

![update-assignee-1](/ko/docs/guides/alert-manager/alert-img/update-assignee-1.png)

(2-2) 담당자를 선택하고 [확인] 버튼을 눌러 담당자 할당을 완료합니다.

![update-assignee-2](/ko/docs/guides/alert-manager/alert-img/update-assignee-2.png)

### 설명 수정하기

해당 얼럿에 대하여 관리 권한이 있는 사용자만 편집이 가능합니다.

(1) [편집] 버튼을 클릭합니다.

![update-description-1](/ko/docs/guides/alert-manager/alert-img/update-description-1.png)

(2) 얼럿 상세설명란에 생성된 폼을 통해 변경사항을 작성하고 [변경사항 저장] 버튼을 클릭하여 설명 수정을 완료합니다.

![update-description-2](/ko/docs/guides/alert-manager/alert-img/update-description-2.png)

### 프로젝트 변경하기

얼럿과 관련된 프로젝트를 수정할 수 있습니다.

(1) 프로젝트 [변경] 버튼을 클릭합니다.

![update-project-1](/ko/docs/guides/alert-manager/alert-img/update-project-1.png)

(2) [프로젝트 선택] 드롭다운에서 프로젝트를 선택합니다.

프로젝트 드롭다운 목록에는 권한이 있는 프로젝트들만 표시됩니다.

변경하고자 하는 프로젝트를 선택한 후 [변경사항 저장] 버튼을 클릭하여 프로젝트 변경을 완료합니다.

![update-project-2](/ko/docs/guides/alert-manager/alert-img/update-project-2.png)

### 새로운 상태로 업데이트하기

얼럿의 진행 상황 등을 기록하여 빠르게 해당 얼럿의 상태를 파악할 수 있도록 도울 수 있습니다.

내용을 변경하면 이전의 상태 기록은 사라집니다.

(1) [새로운 업데이트] 버튼을 클릭합니다.

![update-status-1](/ko/docs/guides/alert-manager/alert-img/update-status-1.png)

(2) [새로운 상태 업데이트] 모달에서 상태를 작성하고 [확인] 버튼을 눌러 상태 업데이트를 완료합니다.

![update-status-2](/ko/docs/guides/alert-manager/alert-img/update-status-2.png)

### 수신인 추가하기

얼럿은 [에스컬레이션 정책](/ko/docs/guides/alert-manager/escalation-policy/)을 통해 수신자에게 전파됩니다.

해당 얼럿에 대하여 추가 사용자에게 얼럿의 전파가 필요하다면, [추가 수신인]을 설정하여 전파할 수 있습니다. 

![add-additional-responder-1](/ko/docs/guides/alert-manager/alert-img/add-additional-responder-1.png)

검색 창을 클릭하여 수신 가능한 사용자 목록을 조회 및 검색할 수 있으며, 다중 선택이 가능합니다.

![add-additional-responder-2](/ko/docs/guides/alert-manager/alert-img/add-additional-responder-2.png)

### 노트 추가하기

얼럿에 대해 구성원들이 코멘트를 남겨 처리 중 문의사항과 이에 대한 답변을 등록하여 의사소통할 수 있습니다.

![add-note](/ko/docs/guides/alert-manager/alert-img/add-note.png)

### 발생한 이벤트 살펴보기

한 얼럿에서 발생한 이벤트들을 로깅하여 히스토리를 볼 수 있습니다.

![view-pushed-event](/ko/docs/guides/alert-manager/alert-img/view-pushed-event.png)

이벤트 목록 중 하나를 클릭하면, 이벤트의 상세 정보를 조회할 수 있습니다.

![view-pushed-event-detail](/ko/docs/guides/alert-manager/alert-img/view-pushed-event-detail.png)

### 알림 정책 설정하기

프로젝트에 발생한 얼럿의 긴급도가 `긴급` 인 경우에만 얼럿이 발생하도록 설정할 수 있습니다.

(1) 프로젝트 상세 페이지에 [얼럿] 탭 내부에서, [설정] 탭으로 이동합니다.

![notification-policy-1](/ko/docs/guides/alert-manager/alert-img/notification-policy-1,2.png)

(2) 알림 정책 영역의 [편집] 아이콘 버튼을 클릭합니다.

![notification-policy-2](/ko/docs/guides/alert-manager/alert-img/notification-policy-1,2.png)

(3) 원하는 알림 정책을 클릭합니다.

![notification-policy-3](/ko/docs/guides/alert-manager/alert-img/notification-policy-3.png)

(4) [확인] 버튼을 클릭해 정책 설정을 완료합니다.

### 자동 복구 설정하기

자동 복구 기능은 시스템 장애가 복구되면 얼럿을 자동으로 `완료` 상태로 전환합니다.

{{< alert title="자동 복구 작동 원리" >}}

![auto-recovery-setting](/ko/docs/guides/alert-manager/alert-img/auto-recovery-setting.png)

자동 복구가 설정된 프로젝트의 얼럿이 추가 이벤트 수신할 때, 해당 이벤트의 event_type의 값이 `RECOVERY` 인 경우 자동으로 얼럿의 상태가 `완료` 로 전환됩니다.

{{< /alert >}}



(1) 프로젝트 상세 페이지에 [얼럿] 탭 내부에서, [설정] 탭으로 이동합니다.

![auto-recovery-1](/ko/docs/guides/alert-manager/alert-img/auto-recovery-1,2.png)

(2) 자동 복구 영역의 [편집] 아이콘 버튼을 클릭합니다.

![auto-recovery-2](/ko/docs/guides/alert-manager/alert-img/auto-recovery-1,2.png)

(3) 원하는 자동 복구 설정을 클릭합니다.

![auto-recovery-3](/ko/docs/guides/alert-manager/alert-img/auto-recovery-3.png)

(4) [확인] 버튼을 클릭해 자동 복구 설정을 완료합니다.
