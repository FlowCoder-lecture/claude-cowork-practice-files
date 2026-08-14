# Test fixture (current)

baseline 사본에서 값 세 곳만 바꾼 파일입니다. 실제 관찰 기록이 아닙니다.
기대 결과는 W01 CHANGED, W02 UNCHANGED, W03 UNKNOWN입니다.

- W01: 가격 숫자만 바꿨습니다. 카드의 다른 값과 겹치지 않는 숫자를 골랐습니다.
- W02: 낱말 사이 공백을 하나 더 넣었습니다. 정규화가 흡수하므로 값은 같습니다.
- W03: 수집 오류를 흉내 냈습니다. status와 함께 observed_value, evidence도 비웠습니다.

## Snapshot W01
- observed_value: KRW 23,500 / month
- source_type: WEB
- source_url: https://example.com/service-a/pricing
- source_published_at: 2026-07-20 (시간대 표기 없음)
- collected_at: 2026-07-20 09:00
- timezone: Asia/Seoul
- status: OK
- evidence: '월간 결제' 열의 '기본' 행
- error_message: 없음

## Snapshot W02
- observed_value: 검색  필터 개선
- source_type: RSS
- source_url: https://example.com/service-b/changelog/feed
- source_published_at: 2026-07-19T08:00:00+09:00
- collected_at: 2026-07-20 09:02
- timezone: Asia/Seoul
- status: OK
- evidence: 변경 기록 목록의 맨 위 항목 제목
- error_message: 없음

## Snapshot W03
- observed_value:
- source_type: WEB
- source_url: https://example.com/agency-c/notice/2026-support
- source_published_at:
- collected_at: 2026-07-20 10:00
- timezone: Asia/Seoul
- status: ERROR
- evidence:
- error_message: expected field not found
