# soma-moa: Human-Centered Physical AI & Spatial Governance Protocol.
일상에서 시작합니다.
[brain: llama/gemini] → [governance: soma-moa] →
사람이 판단하고 AI가 생각하고 로봇이 움직여서, 개인에서 가정으로, 현장까지 이어집니다.[actuator]

> original design: deundeuni (soma-moa) | repo: github.com/soma-moa | domain: somamoa.ai.kr
> 42KB / Ed25519 / Article X / Blameless Telemetry / APK Secured

**정의:** 일상에서 시작된 방문 안내 비서 로봇. 병원, 공장, 빌딩 로비, 백화점 서비스센터, 물류센터, 일반 기기 AS센터(노트북/스마트폰/카메라), 푸드코너/식당 무인 비서. 개인에서 가정으로, 현장까지 이어집니다.

**구조:** [Brain] → [Governance: soma-moa] → [Actuator/APK]. Article X로 바퀴/4족/휴머노이드/키오스크/홀로그램/스노우볼 구조 무관, I/O 2대 요건으로 동일 통제.

**멈췄을 때:** 0번 헌장 - 로봇은 부, 시스템이 주. 스스로 재가동 금지.
L1 BLE/MQTT-SN 진단 / L2 Lock & Telemetry 수집 / L3 WebRTC Human Sign-off (Ed25519 서명 없으면 100% 차단, Cloud-Sign/Edge-Verify)

**보안:** 제로 트러스트(승인망만), RAM<10MB, CBOR<50B, 42KB SDK. APK는 Cloud-Sign 없으면 설치/실행 차단, 리패키징/루팅 시 L2 Lock.

**AS 3종:** 원격/OTA, 출동, 직원 상주(병원/공장/백화점/물류/기기AS/푸드코너에 상주. 일일점검, L1 진단, L3 중개. 판단 대신 집행만)

**개인 커스텀:** 약/할일/건강 루틴, 기기 수리이력/보증, 식단/알러지. 규제 검증 후 금융까지. 단순 스케줄러 아님.

**확장 탐색:** 도서관 사서(제목 몰라도 줄거리/느낌/표지 기억으로 책 찾기) + 음악 탐색(멜로디 흥얼거림/느낌/가사 줄거리로 찾기). 불확실하면 추측 금지, L3 연결.

**안전:** 하인리히 300/29/1(Heinrich, 1931) 기본, Swiss Cheese(Reason, 1990), Defense in Depth, Fail-Safe, ALARP 확장 가능.

**오리지널리티:** 같은 생각 한 사람 있을 수 있다. 표준은 모두 공개 표준. 내가 일상에서 고민해 0번 헌장과 Article X로 묶은 거버넌스 구조가 오리지널. AI(Meta AI & Gemini)는 검토 도구로 활용.

- 철학: DESIGN.md / 스펙: SPEC.md / 출처: SOURCES.md / 라이선스: LICENSE.md / 교육: EDUCATION.md / 도메인: somamoa.ai.kr

---
일상에서 시작합니다. 사람·AI·로봇이 모이면 좋겠다(moa).
origin: by deundeuni (soma-moa) | reviews: Meta AI & Gemini (tools) | repo: github.com/soma-moa | domain: somamoa.ai.kr