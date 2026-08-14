# release-check.md

아래 값은 연습용 예시입니다. 배포한 뒤 자신이 확인한 값으로 바꿔 적습니다.
주소는 문서 예시용(example.invalid)이라 실제로 열리지 않습니다.

## 배포 입력
- 후보 폴더: request-board-release-1
- index.html: 포함
- styles.css: 포함
- app.js: 포함
- 문서와 백업: 제외
- 비밀값 검사: 발견 없음

## 배포 결과
- 공개 주소: https://example.invalid/request-board
- 배포 시각: 2026-07-20 14:00 KST
- 배포 식별자: deploy-001
- 정상 기준: request-board-release-1
- 배포한 사람: 실습자
- 시험을 실행한 사람: 실습자

## 운영 시험
- PROD-A1: PASS / 14:05
- PROD-A2: PASS / 14:06
- PROD-A3: PASS / 14:07
- PROD-A4: PASS / 14:08
- PROD-A5: PASS / 14:10
- PROD-A6: PASS / 14:11

사용한 샘플 데이터: 홈페이지 문구 확인 / 민지 / 진행

## 운영 접근성 시험
- AX1: PASS / 14:12
- AX2: PASS / 14:12
- AX3: PASS / 14:13
- AX4: PASS / 14:14
- AX5: PASS / 14:14

## 복구 정보
- known-good: deploy-001
- 복구 방법: 이전 배포 선택 또는 같은 폴더 재배포
- 복구 뒤 시험: PROD-A1과 실패 시험
- 복구 연습 기록: deploy-002를 올린 뒤 deploy-001로 되돌림. 복구 완료 14:26 KST.

## 공개 범위
- 주소를 아는 사람은 누구나 열 수 있음
- 화면에 "연습용이며 민감한 내용을 입력하지 마세요" 문구 표시
- 실제 업무 사용에는 인증과 서버 저장이 별도로 필요함
