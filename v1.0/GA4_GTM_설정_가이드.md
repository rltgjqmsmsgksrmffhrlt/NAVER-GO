# GA4 / GTM 설정 가이드 — AI 여정 만들기 UT

## 1. GTM 컨테이너

- **컨테이너 ID**: `GTM-KK56JZPX`
- **GA4 측정 ID**: `G-VEZGEESE2K`

---

## 2. GTM 변수 (데이터 영역 변수 25개)

모두 **변수 유형: 데이터 영역 변수**, **버전 2**로 설정

| GTM 변수 이름 | 데이터 영역 변수 이름 |
|---|---|
| `dlv_screen_name` | `screen_name` |
| `dlv_step` | `step` |
| `dlv_step_name` | `step_name` |
| `dlv_duration_sec` | `duration_sec` |
| `dlv_duration_ms` | `duration_ms` |
| `dlv_field` | `field` |
| `dlv_error_type` | `error_type` |
| `dlv_consent_result` | `consent_result` |
| `dlv_scope_count` | `scope_count` |
| `dlv_scope_items` | `scope_items` |
| `dlv_share_channel` | `share_channel` |
| `dlv_place_name` | `place_name` |
| `dlv_direction` | `direction` |
| `dlv_mode` | `mode` |
| `dlv_message_length` | `message_length` |
| `dlv_is_first_message` | `is_first_message` |
| `dlv_depth_threshold` | `depth_threshold` |
| `dlv_depth_actual` | `depth_actual` |
| `dlv_day_count` | `day_count` |
| `dlv_place_count` | `place_count` |
| `dlv_coach_mark_shown` | `coach_mark_shown` |
| `dlv_pulse_shown` | `pulse_shown` |
| `dlv_query` | `query` |
| `dlv_day_index` | `day_index` |
| `dlv_target_list` | `target_list` |

---

## 3. GTM 트리거 (맞춤 이벤트 25개)

모두 **트리거 유형: 맞춤 이벤트**, **실행 조건: 모든 맞춤 이벤트**

| 트리거 이름 | 이벤트 이름 |
|---|---|
| `trig_screen_view` | `screen_view` |
| `trig_option_step_complete` | `option_step_complete` |
| `trig_option_step_skip` | `option_step_skip` |
| `trig_option_step_duration` | `option_step_duration` |
| `trig_chat_message_sent` | `chat_message_sent` |
| `trig_chat_itinerary_received` | `chat_itinerary_received` |
| `trig_chat_dwell_time` | `chat_dwell_time` |
| `trig_journey_generate_duration` | `journey_generate_duration` |
| `trig_journey_generate_overlay_duration` | `journey_generate_overlay_duration` |
| `trig_journey_generate_complete` | `journey_generate_complete` |
| `trig_journey_save_click` | `journey_save_click` |
| `trig_journey_share` | `journey_share` |
| `trig_validation_error` | `validation_error` |
| `trig_destination_no_result` | `destination_no_result` |
| `trig_privacy_consent` | `privacy_consent` |
| `trig_privacy_dwell_time` | `privacy_dwell_time` |
| `trig_consent_withdraw` | `consent_withdraw` |
| `trig_data_scope_save` | `data_scope_save` |
| `trig_place_add` | `place_add` |
| `trig_place_delete` | `place_delete` |
| `trig_place_reorder` | `place_reorder` |
| `trig_recommendation_mode_change` | `recommendation_mode_change` |
| `trig_scroll_depth` | `scroll_depth` |
| `trig_no_data_modal_view` | `no_data_modal_view` |
| `trig_consent_decline_modal_view` | `consent_decline_modal_view` |

---

## 4. GTM 태그 (통합 태그 1개)

### GA4 - All Custom Events

| 항목 | 설정값 |
|---|---|
| **태그 유형** | Google 애널리틱스: GA4 이벤트 |
| **측정 ID** | `G-VEZGEESE2K` |
| **이벤트 이름** | `{{Event}}` |

**트리거**: 맞춤 이벤트 (정규식 일치 사용)

```
screen_view|option_step_complete|option_step_skip|option_step_duration|chat_message_sent|chat_itinerary_received|chat_dwell_time|journey_generate_duration|journey_generate_overlay_duration|journey_generate_complete|journey_save_click|journey_share|validation_error|destination_no_result|privacy_consent|privacy_dwell_time|consent_withdraw|data_scope_save|place_add|place_delete|place_reorder|recommendation_mode_change|scroll_depth|no_data_modal_view|consent_decline_modal_view
```

**이벤트 매개변수 (25개)**:

| 매개변수 이름 | 값 |
|---|---|
| `screen_name` | `{{dlv_screen_name}}` |
| `step` | `{{dlv_step}}` |
| `step_name` | `{{dlv_step_name}}` |
| `duration_sec` | `{{dlv_duration_sec}}` |
| `duration_ms` | `{{dlv_duration_ms}}` |
| `field` | `{{dlv_field}}` |
| `error_type` | `{{dlv_error_type}}` |
| `consent_result` | `{{dlv_consent_result}}` |
| `scope_count` | `{{dlv_scope_count}}` |
| `scope_items` | `{{dlv_scope_items}}` |
| `share_channel` | `{{dlv_share_channel}}` |
| `place_name` | `{{dlv_place_name}}` |
| `direction` | `{{dlv_direction}}` |
| `mode` | `{{dlv_mode}}` |
| `message_length` | `{{dlv_message_length}}` |
| `is_first_message` | `{{dlv_is_first_message}}` |
| `depth_threshold` | `{{dlv_depth_threshold}}` |
| `depth_actual` | `{{dlv_depth_actual}}` |
| `day_count` | `{{dlv_day_count}}` |
| `place_count` | `{{dlv_place_count}}` |
| `coach_mark_shown` | `{{dlv_coach_mark_shown}}` |
| `pulse_shown` | `{{dlv_pulse_shown}}` |
| `query` | `{{dlv_query}}` |
| `day_index` | `{{dlv_day_index}}` |
| `target_list` | `{{dlv_target_list}}` |

---

## 5. GA4 맞춤 정의

GA4 관리 > 맞춤 정의에서 등록

### 맞춤 측정기준 (텍스트 값)

| 측정기준 이름 | 범위 | 이벤트 매개변수 |
|---|---|---|
| Screen Name | 이벤트 | `screen_name` |
| Step Name | 이벤트 | `step_name` |
| Field | 이벤트 | `field` |
| Error Type | 이벤트 | `error_type` |
| Consent Result | 이벤트 | `consent_result` |
| Scope Items | 이벤트 | `scope_items` |
| Scope Count | 이벤트 | `scope_count` |
| Share Channel | 이벤트 | `share_channel` |
| Place Name | 이벤트 | `place_name` |
| Direction | 이벤트 | `direction` |
| Mode | 이벤트 | `mode` |
| Query | 이벤트 | `query` |
| Target List | 이벤트 | `target_list` |
| Coach Mark Shown | 이벤트 | `coach_mark_shown` |
| Pulse Shown | 이벤트 | `pulse_shown` |
| Is First Message | 이벤트 | `is_first_message` |

### 맞춤 측정항목 (숫자 값)

| 측정항목 이름 | 범위 | 이벤트 매개변수 | 측정 단위 |
|---|---|---|---|
| Duration Sec | 이벤트 | `duration_sec` | 일반 |
| Duration Ms | 이벤트 | `duration_ms` | 일반 |
| Step | 이벤트 | `step` | 일반 |
| Message Length | 이벤트 | `message_length` | 일반 |
| Depth Threshold | 이벤트 | `depth_threshold` | 일반 |
| Depth Actual | 이벤트 | `depth_actual` | 일반 |
| Day Count | 이벤트 | `day_count` | 일반 |
| Place Count | 이벤트 | `place_count` | 일반 |
| Day Index | 이벤트 | `day_index` | 일반 |

---

## 6. GA4 탐색 보고서 — UT KPI 확인 방법

GA4 > 탐색 > 자유형식 탐색에서 확인

### KPI 1: 개인정보 수집 동의율

> **가설 1** 검증: 개인정보 수집 목적과 활용 범위를 명확하게 안내한다면 사용자의 개인정보 제공 거부감이 감소할 것이다.

| 항목 | 설정 |
|---|---|
| **행** | `Consent Result` |
| **값** | `이벤트 수` |
| **필터** | 이벤트 이름 = `privacy_consent` |

**보는 법**: `agreed` 수 ÷ 전체 수 = 동의율

---

### KPI 2: 동의 완료 소요시간

> **가설 1** 검증: 약관 내용의 이해 난이도 및 의사결정 부담 정도

| 항목 | 설정 |
|---|---|
| **행** | `Consent Result` |
| **값** | `Duration Sec` (평균) |
| **필터** | 이벤트 이름 = `privacy_dwell_time` |

**보는 법**: `agreed` 행의 평균 초 = 동의까지 걸린 시간

---

### KPI 3: 전체동의 / 선택동의 비율

> **가설 2** 검증: 사용자가 직접 데이터 활용 범위를 선택할 수 있도록 제공한다면 서비스 신뢰도가 향상될 것이다.

| 항목 | 설정 |
|---|---|
| **행** | `Scope Count` |
| **값** | `이벤트 수` |
| **필터** | 이벤트 이름 = `data_scope_save` |

**보는 법**: `scope_count`가 7이면 전체동의, 7 미만이면 선택동의

---

### KPI 4: 항목별 데이터 선택률

> **가설 2** 검증: 유저의 데이터 활용 범위 선호도

| 항목 | 설정 |
|---|---|
| **행** | `Scope Items` |
| **값** | `이벤트 수` |
| **필터** | 이벤트 이름 = `data_scope_save` |

**보는 법**: 각 조합별 빈도로 어떤 항목이 자주 선택되는지 확인

---

### KPI 5: AI 추천 채택률

> **가설 3, 4** 검증: 개인화 데이터 기반 추천 결과 만족도 및 채택률

**기법**: GA4 > 탐색 > **유입경로 탐색**

| 단계 | 이벤트 | 설명 |
|---|---|---|
| 1단계 | `screen_view` (screen_name = `options`) | 여정 만들기 시작 |
| 2단계 | `chat_message_sent` | 채팅 진입 |
| 3단계 | `journey_save_click` | 저장 클릭 |
| 4단계 | `journey_generate_complete` | 생성 완료 |

**보는 법**: 1단계 → 4단계 전환율 = AI 추천 채택률

---

## 7. 구현된 전체 이벤트 목록

### 화면 추적
| 이벤트 | 매개변수 | 설명 |
|---|---|---|
| `screen_view` | `screen_name`, `option_step` | SPA 화면 전환 추적 |

### 타이머 이벤트
| 이벤트 | 매개변수 | 설명 |
|---|---|---|
| `privacy_dwell_time` | `duration_ms`, `duration_sec`, `consent_result` | 개인정보 동의 화면 체류시간 |
| `option_step_duration` | `duration_ms`, `duration_sec`, `step`, `step_name` | 옵션 단계별 소요시간 |
| `chat_dwell_time` | `duration_ms`, `duration_sec` | 채팅 화면 체류시간 |
| `journey_generate_duration` | `duration_ms`, `duration_sec` | AI 생성 응답시간 |
| `journey_generate_overlay_duration` | `duration_ms`, `duration_sec` | 생성 오버레이 표시시간 |

### 클릭/행동 이벤트
| 이벤트 | 매개변수 | 설명 |
|---|---|---|
| `privacy_consent` | `consent_result` | 개인정보 동의/거부 |
| `consent_decline_modal_view` | — | 동의 거부 모달 노출 |
| `consent_withdraw` | — | 동의 철회 |
| `data_scope_save` | `scope_count`, `scope_items` | 데이터 범위 저장 |
| `no_data_modal_view` | — | 데이터 미선택 안내 모달 |
| `option_step_complete` | `step`, `step_name` | 옵션 단계 완료 |
| `option_step_skip` | `step`, `step_name` | 옵션 단계 건너뛰기 |
| `chat_message_sent` | `message_length`, `is_first_message` | 채팅 메시지 전송 |
| `chat_itinerary_received` | `day_count`, `place_count` | AI 일정 수신 |
| `journey_save_click` | `coach_mark_shown`, `pulse_shown` | 여정 저장 클릭 |
| `journey_generate_complete` | 일정 상세 | 여정 생성 완료 |
| `place_add` | `place_name`, `target_list` | 장소 추가 |
| `place_delete` | `place_name`, `day_index` | 장소 삭제 |
| `place_reorder` | `day_index`, `direction` | 장소 순서 변경 |
| `recommendation_mode_change` | `mode` | 추천 모드 변경 |
| `journey_share` | `share_channel` | 여정 공유 |

### 에러 추적
| 이벤트 | 매개변수 | 설명 |
|---|---|---|
| `validation_error` | `field`, `error_type`, `input_value` | 입력 유효성 오류 |
| `destination_no_result` | `query` | 목적지 검색 결과 없음 |

### 스크롤 깊이
| 이벤트 | 매개변수 | 설명 |
|---|---|---|
| `scroll_depth` | `screen_name`, `depth_threshold`, `depth_actual` | 25/50/75/100% 스크롤 추적 |

---

## 8. 테스트 방법

1. GTM > **미리보기** 클릭
2. 프로토타입 URL 입력 후 연결
3. 프로토타입에서 동의, 옵션 선택, 채팅 등 동작 수행
4. Tag Assistant에서 이벤트 발동 확인
5. GA4 > **실시간** 보고서에서 이벤트 수신 확인
6. 확인 완료 후 GTM > **제출** > **게시**
