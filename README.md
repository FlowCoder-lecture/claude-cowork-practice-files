# 연습용 기본 파일

본인 업무 데이터가 마땅치 않아도 책과 같은 결괏값을 확인하며 따라 할 수 있도록, 실습 입력에 쓰는 파일을 SECTION별로 모았습니다. 각 SECTION의 미리보기 준비물에서 여기 있는 파일명을 안내합니다.

## 어디에 풀어 놓습니까

압축을 푼 폴더를 컴퓨터 어디에 두어도 됩니다. 다만 실습 폴더와는 따로 두시기 바랍니다. 이 폴더는 원본 보관용이고, 실습은 아래 다섯 개의 작업 폴더에서 진행합니다.

| 작업 폴더 | 쓰는 곳 | 만드는 SECTION |
|---|---|---|
| `mini-agent` | PART 1 전체 | SECTION 01 |
| `morning-briefing` | CHAPTER 3과 확장 워크숍 | SECTION 08 |
| `work_pipeline` | CHAPTER 4 | SECTION 11 |
| `monitoring` | CHAPTER 5 | SECTION 16 |
| `request-board` | PART 3과 PART 4 | SECTION 20 |

파일을 옮길 때는 아래 표의 「복사할 위치」를 그대로 따르십시오. 폴더 이름의 글자 하나만 달라도 다음 SECTION이 파일을 찾지 못합니다.

## 두 가지 파일을 구분해 주십시오

- **입력** — 그 SECTION에서 독자가 직접 준비해야 하는 데이터입니다. 이 파일이 없으면 실습을 시작할 수 없습니다.
- **이어 하기** — 앞 SECTION에서 만드는 결과물의 완성 예시입니다. 앞 SECTION을 건너뛰었거나 결과가 책과 달라져 다음 단계로 넘어가기 어려울 때만 쓰십시오. 먼저 직접 만들어 보고, 막혔을 때 꺼내는 편이 남는 것이 많습니다.

## 함께 알아 두실 것

- 파일 안의 회사 이름, 사람 이름, 주소는 모두 가상의 값입니다. `example.com`과 `example.invalid`는 문서 예시용 주소라서 실제로 열리지 않습니다. 링크를 직접 열어 확인하는 단계는 공개된 실제 자료로 실습할 때 진행하십시오.
- 날짜는 연습용으로 고정해 두었습니다. 책과 같은 결괏값을 보려면 이 날짜를 그대로 쓰시고, 본인 업무로 옮길 때 실제 날짜로 바꾸십시오.

| 묶음 | 고정한 날짜 |
|---|---|
| CHAPTER 3 아침 브리핑 | 오늘 2026-07-23, 직전 실행 2026-07-22 |
| CHAPTER 4 업무 파이프라인 | 기간 기준일 2026-07-20, 완료 시각 2026-07-24 16:00 |
| CHAPTER 5 모니터링 | baseline 2026-07-18, current 2026-07-19 |
| PART 3 캡스톤 | 계약 검토 2026-07-20, 배포 2026-07-20 |

- 실제 업무 데이터로 옮길 때는 `00_contract.md`의 `주제`, `watchlist.md`의 원본 URL, 계약서의 완료 시각을 반드시 본인 값으로 바꿔 적으십시오. 예시 값을 그대로 두면 뒤 SECTION의 검토자가 판정할 수 없다고 되돌립니다.

## PART 1 — 작업 폴더 `mini-agent`

| SECTION | 파일 | 구분 | 어느 단계의 입력인지 | 복사할 위치 |
|---|---|---|---|---|
| 01 | `section-01/repeat-work-list.txt` | 입력 | 1단계 반복 업무 적기, 4단계 프롬프트의 `[여기에 업무 목록 붙여 넣기]` | 붙여 넣기용이라 저장하지 않아도 됩니다 |
| 01 | `section-01/work-card-01.md` | 이어 하기 | SECTION 02·03의 준비물 | `mini-agent/` |
| 02 | `section-02/surface-map-01.md` | 이어 하기 | SECTION 03의 준비물과 프롬프트 입력 | `mini-agent/` |
| 03 | `section-03/agent-contract-mini.md` | 이어 하기 | SECTION 05·06 프롬프트의 붙여 넣기 자리 | `mini-agent/` |
| 04 | `section-04/inbox.txt` | 입력 | 3단계 만들기의 입력 파일 | `mini-agent/` |
| 04 | `section-04/tests/inbox-empty.txt` | 입력 | 판정 연습 시험 B(빈 입력) | `mini-agent/tests/` |
| 04 | `section-04/tests/inbox-ambiguous.txt` | 입력 | 판정 연습 시험 C(모호한 기한) | `mini-agent/tests/` |
| 05 | `section-05/runtime-decision.md` | 이어 하기 | SECTION 06 7단계 프롬프트의 붙여 넣기 자리 | `mini-agent/` |
| 06 | `section-06/data-policy-sample.md` | 입력 | 준비물의 데이터·보안 정책과 연결 후보 서비스 목록 | `mini-agent/` |
| 06 | `section-06/CLAUDE.md` | 이어 하기 | 6단계 기준 폴더 지침 | 작업 폴더의 맨 위 |
| 06 | `section-06/briefing-rules.md` | 이어 하기 | SECTION 09 검토 기준 | `morning-briefing/` |
| 06 | `section-06/connector-permissions.md` | 이어 하기 | SECTION 08 실습 8-1 대조, SECTION 25 권한 목록 | `morning-briefing/` |
| 06 | `section-06/environment-check.md` | 이어 하기 | SECTION 08 실습 8-1 대조 | `morning-briefing/` |

`section-04/tests/inbox-empty.txt`는 내용이 없는 파일입니다. 편집기에서 열면 아무것도 보이지 않는 것이 정상입니다.

## CHAPTER 3과 확장 워크숍 — 작업 폴더 `morning-briefing`

| SECTION | 파일 | 구분 | 어느 단계의 입력인지 | 복사할 위치 |
|---|---|---|---|---|
| 07 | `section-07/completion.md` | 이어 하기 | SECTION 08·09의 판정 기준, 워크숍 1 프롬프트 | `morning-briefing/` |
| 08 | `section-08/sources.md` | 입력 | SECTION 09 실습 9-1·9-2의 입력 파일 | `morning-briefing/` |
| 09 | `section-09/brief.md` | 이어 하기 | SECTION 10의 비교 대상, 워크숍 준비물 | `morning-briefing/` |
| 10 | `section-10/brief-2026-07-22.md` | 입력 | 「어제와 오늘을 비교합니다」의 직전 파일 | `morning-briefing/` |
| 워크숍 | `workshop/sources.md` | 입력 | 워크숍 3 블라인드 검토 세트의 원본 입력 | 워크숍용 새 폴더 |
| 워크숍 | `workshop/sample-a.md` ~ `sample-d.md` | 입력 | 워크숍 3의 검토 대상 네 개 | 같은 폴더 |
| 워크숍 | `workshop/blind-review-answers.md` | 정답표 | 검토를 마친 뒤 대조 | 같은 폴더 |
| 워크숍 | `workshop/operations-log.md` | 입력 | 워크숍 4 마지막 분석 프롬프트 | 같은 폴더 |

`workshop/blind-review-answers.md`는 검토를 마친 뒤에 여십시오. 먼저 읽으면 블라인드 검토가 되지 않습니다.

`workshop/sources.md`는 SECTION 08의 것과 한 줄이 다릅니다. Slack 항목이 `수집 실패`로 되어 있어야 「수집 실패를 없음으로 표시」한 오류를 판정할 수 있기 때문입니다.

## CHAPTER 4 — 작업 폴더 `work_pipeline`

| SECTION | 파일 | 구분 | 어느 단계의 입력인지 | 복사할 위치 |
|---|---|---|---|---|
| 11 | `section-11/00_contract.md` | 이어 하기 | SECTION 12~15 전 단계의 판정 기준 | `work_pipeline/` |
| 12 | `section-12/source-candidates-raw.md` | 입력 | 3단계 수집 요청에 붙여 넣는 후보 목록 | 붙여 넣기용 |
| 12 | `section-12/01_sources/source_index.md` | 이어 하기 | SECTION 13·14·15의 입력 | `work_pipeline/01_sources/` |
| 13 | `section-13/02_draft/draft.md` | 이어 하기 | SECTION 14의 검토 대상 | `work_pipeline/02_draft/` |
| 15 | `section-15/new-source-candidates.md` | 입력 | 준비물의 「새 실험용 자료 세 건」 | 붙여 넣기용 |
| 15 | `section-15/run_log.md` | 이어 하기 | SECTION 25의 최근 실행 기록 | `work_pipeline/` |

`section-13/02_draft/draft.md`에는 검토자가 찾아야 할 문제가 일부러 들어 있습니다. 업무 영향의 마지막 문단에 출처 태그가 없고 근거 없는 단정이 들어 있으니, SECTION 14에서 판정하면 차단 문제 한 건이 나오는 것이 정상입니다. 제목의 범위가 넓다는 경고가 함께 나올 수 있습니다.

## CHAPTER 5 — 작업 폴더 `monitoring`

| SECTION | 파일 | 구분 | 어느 단계의 입력인지 | 복사할 위치 |
|---|---|---|---|---|
| 16 | `section-16/watchlist.md` | 이어 하기 | SECTION 17·18·19의 판정 기준 | `monitoring/` |
| 17 | `section-17/snapshots/2026-07-18.md` | 입력 | SECTION 18 비교의 baseline | `monitoring/snapshots/` |
| 17 | `section-17/snapshots/2026-07-19.md` | 입력 | SECTION 18 비교의 current | `monitoring/snapshots/` |
| 17 | `section-17/tests/test_fixture_previous.md` | 입력 | SECTION 18 5단계 비교기 시험 | `monitoring/tests/` |
| 17 | `section-17/tests/test_fixture_current.md` | 입력 | SECTION 18 5단계 비교기 시험 | `monitoring/tests/` |
| 18 | `section-18/changes/2026-07-19.md` | 이어 하기 | SECTION 19 알림 선별의 입력 | `monitoring/changes/` |

두 스냅샷으로 비교하면 세 대상이 모두 `CHANGED`로 나옵니다. 시험 파일 두 개로 비교하면 차례로 `CHANGED`, `UNCHANGED`, `UNKNOWN`이 나옵니다. 다른 값이 나오면 baseline과 current를 거꾸로 넣지 않았는지 먼저 확인하십시오.

## PART 3과 PART 4 — 작업 폴더 `request-board`

| SECTION | 파일 | 구분 | 어느 단계의 입력인지 | 복사할 위치 |
|---|---|---|---|---|
| 20 | `section-20/project-contract.md` | 이어 하기 | SECTION 21~26의 판정 기준 | `request-board/` |
| 20 | `section-20/CLAUDE.md` | 이어 하기 | 캡스톤을 여는 모든 세션의 지침 | `request-board/` |
| 20 | `section-20/tests/acceptance.md` | 이어 하기 | SECTION 22·23·26의 합격 시험 | `request-board/tests/` |
| 21 | `section-21/screen-spec.md` | 이어 하기 | SECTION 22 구현 요청의 입력 | `request-board/` |
| 21 | `section-21/sample-list-data.txt` | 입력 | 6단계 목록 높이 확인, SECTION 22 화면 확인 | 붙여 넣기용 |
| 23 | `section-23/release-check.md` | 이어 하기 | SECTION 25·26의 실행 기록 | `request-board/` |
| 24 | `section-24/monitor-contract.md` | 이어 하기 | SECTION 25·26의 자동화 계약 | `request-board/` |
| 25 | `section-25/risk-register.md` | 이어 하기 | SECTION 26 검토 패키지의 05번 파일 | `request-board/` |
| 26 | `section-26/failure-log.md` | 입력 | 검토 패키지의 06번 파일 | `review-package-v1/` |
| 26 | `section-26/rollback.md` | 입력 | 검토 패키지의 08번 파일 | `review-package-v1/` |

## 연습 파일이 없는 SECTION

| SECTION | 이유 |
|---|---|
| 14 | 필요한 입력이 SECTION 11~13의 파일로 모두 채워집니다. |
| 19 | `alert_state.md`는 이 SECTION에서 처음 만들어지는 파일이라 미리 드리지 않습니다. |
| 22 | 코드 세 파일은 직접 만드는 단계입니다. 완성 코드를 넣으면 실습이 성립하지 않습니다. |

## 실제 업무로 옮길 때

연습 파일로 한 바퀴를 돌았다면, 같은 파일 이름을 그대로 두고 내용만 본인 업무 값으로 바꾸십시오. 파일 이름은 단계 사이의 계약이라서, 이름을 유지하면 프롬프트를 다시 쓰지 않아도 됩니다. 한 번에 여러 값을 바꾸지 말고 한 항목씩 바꾼 뒤 결과를 확인하시기 바랍니다.
