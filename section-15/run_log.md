# 실행 기록

## Run 2026-07-20-01
- started_at: 2026-07-20 10:40 Asia/Seoul
- contract_version: 1
- COLLECT: PASS
- DRAFT: PASS
- REVIEW: FAIL
- stop_reason: R01 업무 영향 문단에 출처 태그 없음
- external_action: NONE
- next_action: fix draft and resume REVIEW

## Run 2026-07-20-02
- started_at: 2026-07-20 13:10 Asia/Seoul
- contract_version: 1
- COLLECT: SKIPPED (앞 실행 결과 재사용, 사람 승인)
- DRAFT: PASS
- REVIEW: PASS
- PUBLISH_CANDIDATE: PASS
- external_action: NONE
- next_action: none

## Run 2026-07-20-03
- started_at: 2026-07-20 15:00 Asia/Seoul
- contract_version: 1
- 목적: 멈춤 규칙 시험 (S02 카드의 URL을 일부러 비움)
- COLLECT: PASS
- DRAFT: PASS
- REVIEW: STOP
- stop_reason: S02 URL missing
- external_action: NONE
- next_action: repair source card and resume REVIEW
- 비고: 시험 뒤 source_index_backup.md로 되돌림
