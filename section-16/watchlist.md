# watchlist

관찰 대상 세 개를 카드 한 장씩으로 적습니다.
아래 주소는 문서 예시용 도메인(example.com)이라 실제로 열리지 않습니다.
공개된 실제 페이지로 옮길 때는 원본 URL과 기준선 값을 사람이 직접 확인해 다시 적습니다.

## W01
- 이름: 서비스 A 기본 요금
- 원본 URL: https://example.com/service-a/pricing
- 관찰 질문: 공식 가격표의 기본 요금이 바뀌었는가?
- 관찰 필드: 기본 요금 숫자와 통화
- selector_description: '월간 결제' 열의 '기본' 행
- expected_currency: KRW
- expected_interval: monthly
- baseline_status: HUMAN_APPROVED
- 확인 주기: 매일 09:00 Asia/Seoul
- 주기를 고른 이유: 가격은 한 달 넘게 그대로인 경우가 많고, 바뀌면 다음 갱신 비용에 바로 영향을 줍니다.
- 중요 변화: 숫자 또는 통화 변경
- 무시 변화: 공백, 문장부호, 디자인 순서
- 알림 채널: monitoring/alerts/
- 하루 최대 알림: 1건
- 조용한 시간: 20:00~08:00
- 중단 조건: 연속 3회 접근 실패
- 예상 변화 예시: 19000 → 21000

## W02
- 이름: 서비스 B 변경 기록
- 원본 URL: https://example.com/service-b/changelog
- 관찰 질문: 제품 변경 기록에 새 항목이 추가되었는가?
- 관찰 필드: 최신 항목의 제목
- selector_description: 변경 기록 목록의 맨 위 항목 제목
- expected_currency: 해당 없음
- expected_interval: 해당 없음
- baseline_status: HUMAN_APPROVED
- 확인 주기: 6시간마다 (00:00, 06:00, 12:00, 18:00 Asia/Seoul)
- 주기를 고른 이유: 주 1~3회 항목이 추가되지만 즉시 대응할 일은 아닙니다.
- 중요 변화: 최신 항목의 제목이 다른 항목으로 바뀜
- 무시 변화: 양끝 공백, 연속 공백, 목록 순서, 같은 항목 안의 띄어쓰기와 문장부호 수정
- 알림 채널: monitoring/alerts/
- 하루 최대 알림: 1건
- 조용한 시간: 20:00~08:00
- 중단 조건: 연속 3회 접근 실패
- 예상 변화 예시: 검색 필터 개선 → 파일 연결 권한 변경

## W03
- 이름: 공공기관 C 지원사업 공고
- 원본 URL: https://example.com/agency-c/notice/2026-support
- 관찰 질문: 기관 공고의 접수 마감일이 수정되었는가?
- 관찰 필드: 접수 종료 시각과 시간대
- selector_description: 공고 본문의 '접수 기간' 행 가운데 종료 시각
- expected_currency: 해당 없음
- expected_interval: 해당 없음
- baseline_status: HUMAN_APPROVED
- 확인 주기: 매일 10:00 Asia/Seoul
- 주기를 고른 이유: 수정은 드물지만 마감이 당겨지면 남는 시간이 바로 줄어듭니다.
- 중요 변화: 종료 날짜 또는 시각 변경
- 무시 변화: 날짜 표기 형식, 띄어쓰기
- 알림 채널: monitoring/alerts/
- 하루 최대 알림: 1건
- 조용한 시간: 20:00~08:00
- 중단 조건: 연속 3회 접근 실패
- 예상 변화 예시: 2026-07-31 18:00 → 2026-07-25 18:00

## 전체 알림 예산
- 하루 최대 알림: 3건
- 같은 변화는 한 번만 알림
- 조용한 시간에 생긴 변화는 파일에 보관했다가 다음 허용 시간에 요약

## Baseline approval
- watch_id: W01
- observed_value: KRW 19000 monthly
- checked_by: human
- checked_at: 2026-07-18 09:00 Asia/Seoul
- source_opened: yes
- note: 가격표의 기본 요금 행을 확인함

## Baseline approval
- watch_id: W02
- observed_value: 검색필터 개선
- checked_by: human
- checked_at: 2026-07-18 09:00 Asia/Seoul
- source_opened: yes
- note: 변경 기록 맨 위 항목의 제목을 확인함

## Baseline approval
- watch_id: W03
- observed_value: 2026-07-31 18:00 Asia/Seoul
- checked_by: human
- checked_at: 2026-07-18 09:00 Asia/Seoul
- source_opened: yes
- note: 공고 본문의 접수 종료 시각을 확인함

## 카드 관리
| watch_id | 시작일 | 재검토일 | 소유자 | 종료 조건 |
|---|---|---|---|---|
| W01 | 2026-07-18 | 2026-08-18 | 본인 | 해당 서비스를 더 쓰지 않게 되면 RETIRED |
| W02 | 2026-07-18 | 2026-08-18 | 본인 | 공식 RSS로 옮기면 카드 교체 |
| W03 | 2026-07-18 | 2026-08-18 | 본인 | 접수 마감일이 지나면 RETIRED |
