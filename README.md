# 머니집 계산기 (PWA)

## 배포 방법 (GitHub Pages — MoneyZip과 동일한 방식)

1. 새 GitHub 저장소 생성 (예: `moneyzip-calc`)
2. 이 폴더의 파일 전체(`index.html`, `manifest.json`, `service-worker.js`, `icons/`)를 저장소에 업로드
3. 저장소 Settings → Pages → Branch를 `main`(또는 `master`)으로 설정 후 저장
4. 몇 분 뒤 `https://[깃허브아이디].github.io/moneyzip-calc/` 로 접속 가능
5. 카카오톡으로 링크 공유 시 바로 열리고, 모바일에서 "홈 화면에 추가"로 앱처럼 설치 가능

## 커스텀 도메인 연결 시 (예: calc.moneyzip.co.kr)
- 저장소에 `CNAME` 파일 추가 후 도메인 입력
- 도메인 관리 페이지에서 CNAME 레코드를 `[깃허브아이디].github.io`로 설정

## 광고 삽입
- `index.html`의 `<div class="adslot">광고 영역</div>` 부분에 Kakao AdFit / Google AdSense 스크립트 삽입
- 결과 화면 하단(`.result` 안)에도 광고 슬롯 추가 가능

## 다음 단계 (TWA 전환)
- 트래픽 확인 후 Bubblewrap으로 TWA 패키징 → 플레이스토어 등록
- 이 PWA 코드는 수정 없이 그대로 재사용 가능

## 계산 로직 기준
- 2026년 4대보험 요율(국민연금 4.75%, 건강보험 3.595%, 장기요양 13.14%, 고용보험 0.9%)
- 2026년 실업급여 상한 68,100원 / 하한 66,048원
- 소득세는 종합소득세 누진세율표 기준 간이 추정 (참고용, 실제 원천징수와 차이 가능)
