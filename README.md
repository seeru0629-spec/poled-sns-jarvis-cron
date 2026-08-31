# poled-sns-jarvis-cron

`poled-sns-jarvis` 웹앱의 "예약 발행" 기능을 위한 트리거 전용 저장소.

Vercel Hobby 플랜은 Cron Job이 하루 1회로 제한돼 있고, 실제 서비스 리포(`suzy`)는
비공개(private)라 GitHub Actions 무료 한도(월 2,000분)를 짧은 주기로 금방 넘길 수 있음.
그래서 이 저장소만 별도의 **공개(public)** 저장소로 만들어 — 공개 저장소는 GitHub Actions가
무제한 무료 — 5~10분 간격으로 웹앱의 예약발행 체크 API를 호출한다.

이 저장소 자체엔 실제 코드나 민감한 로직이 없음. 필요한 시크릿(`POLED_SNS_JARVIS_CRON_SECRET`)만
Settings → Secrets and variables → Actions에 등록하면 됨.
