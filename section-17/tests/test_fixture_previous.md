# Test fixture (baseline)

비교기를 시험하기 위한 파일입니다. 실제 관찰 기록이 아닙니다.
2026-07-19 스냅샷을 그대로 복사한 사본입니다.

## Snapshot W01
- observed_value: KRW 21,000 / month
- source_type: WEB
- source_url: https://example.com/service-a/pricing
- source_published_at: 2026-07-19 (시간대 표기 없음)
- collected_at: 2026-07-19 09:00
- timezone: Asia/Seoul
- status: OK
- evidence: '월간 결제' 열의 '기본' 행
- error_message: 없음

## Snapshot W02
- observed_value: 검색 필터 개선
- source_type: RSS
- source_url: https://example.com/service-b/changelog/feed
- source_published_at: 2026-07-19T08:00:00+09:00
- collected_at: 2026-07-19 09:02
- timezone: Asia/Seoul
- status: OK
- evidence: 변경 기록 목록의 맨 위 항목 제목
- error_message: 없음

## Snapshot W03
- observed_value: 2026-07-25 18:00
- source_type: WEB
- source_url: https://example.com/agency-c/notice/2026-support
- source_published_at: 2026-07-19 (시간대 표기 없음)
- collected_at: 2026-07-19 10:00
- timezone: Asia/Seoul
- status: OK
- evidence: 공고 본문 '접수 기간' 행의 종료 시각
- error_message: 없음
