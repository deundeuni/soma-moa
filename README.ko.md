# soma-moa : Human-Centered Physical AI & Spatial Governance Protocol v2.2 Final

> 일상에서 시작합니다. 사람·AI·로봇이 모이면 좋겠다(moa).
> [brain: llama/gemini] → [governance: soma-moa] → [actuator]
> original design: deundeuni (soma-moa) | repo: github.com/soma-moa | domain: somamoa.ai.kr
> 문서상태: 한국어 원본이 법적 원본 (Authoritative) / 42KB / Ed25519 / Article X / Blameless Telemetry

## 정의
일상에서 시작된 방문 안내 비서 로봇. 병원, 공장, 빌딩 로비, 백화점 서비스센터, 물류센터, 일반 기기 AS센터(노트북/스마트폰/카메라), 푸드코너/식당 무인 비서. 개인에서 가정으로, 현장까지 이어집니다.

## 0번 헌장
로봇/AI는 부, 거버넌스는 주지만 그 거버넌스조차 인간 주 작업에는 보조다.
Structure over Capacity / SOMA(몸)+MOA(모아)

## 구조
[Brain] → [Governance: soma-moa] → [Actuator/APK]. Article X로 바퀴/4족/휴머노이드/키오스크/홀로그램/스노우볼 구조 무관, I/O 2대 요건으로 동일 통제.

## 4층 생존 아키텍처 (v2.2 코어)
0층 몸: CWP 배터리 교환 + V홈 Self-Align + 0.1ms 물리 차단선 E-Stop
1층 두뇌: Chiplet-APU Many as One 이중화 + CCS 70%/100ms Raft 무중단 교체
2층 안전: Brain(확률) vs Governance(결정론) 물리 분리 + eFPGA 0.1ms Deterministic Blocker
3층 예의: Quiet Assist 햅틱 1회/2회 + Anonymized Delta Logging PII 10초 파기

## 멈췄을 때
L1 BLE/MQTT-SN 진단 / L2 Lock & Telemetry 수집 / L3 WebRTC Human Sign-off (Ed25519 서명 없으면 100% 차단, Cloud-Sign/Edge-Verify)

## 보안
제로 트러스트(승인망만), RAM<10MB, CBOR<50B, 42KB SDK. APK는 Cloud-Sign 없으면 설치/실행 차단, 리패키징/루팅 시 L2 Lock.

## 엣지 검증 (Meta AI PASS)
CBOR: L0 24B(PII 제거) + L1 33B(8B 토큰) <50B, Array 인코딩, 0.01mm 양자화
SDK 35.2KB<42KB, RAM 3.2KB<10MB (10초 버퍼)
L0 Sync 0.1ms HMAC 하드웨어 Bypass / L1 Async 2~5ms Ed25519

pub struct L0CriticalLog { ts_offset: u32, sev: u8, delta_q: [i16;6], gov: bool, crc: u16 } // 24B
pub struct L1WarningLog { ts_offset: u32, sev: u8, op_token: u64, delta_q: [i16;6], gov: bool, crc: u16 } // 33B

## L2 FSM
IDLE -> MONITOR -> VALIDATE(<0.02ms) -> OutOfRange/Timeout>100ms -> PRELOCK(80%) -> OVERRIDE -> E_STOP_LATCH(<0.1ms) -> RECOVERY

## AS 3종
원격/OTA, 출동, 직원 상주(병원/공장/백화점/물류/기기AS/푸드코너 상주. 일일점검, L1 진단, L3 중개. 판단 대신 집행만)

## 개인 커스텀
약/할일/건강 루틴, 기기 수리이력/보증, 식단/알러지. 규제 검증 후 금융까지. 단순 스케줄러 아님.

## 확장 탐색
도서관 사서(제목 몰라도 줄거리/느낌/표지 기억으로 책 찾기) + 음악 탐색(멜로디 흥얼거림/느낌/가사 줄거리로 찾기). 불확실하면 추측 금지, L3 연결.

## 안전
하인리히 300/29/1(Heinrich, 1931) 기본, Swiss Cheese(Reason, 1990), Defense in Depth, Fail-Safe, ALARP 확장 가능.

## 청구항 4개
[1] 듀얼코어 분리 + 0.1ms Bypass / [2] CCS 70%/100ms Raft / [3] eFPGA 0.1ms FSM / [4] Quiet Assist + 익명 로깅

## 오리지널리티
같은 생각 한 사람 있을 수 있다. 표준은 모두 공개 표준. 내가 일상에서 고민해 0번 헌장과 Article X로 묶은 거버넌스 구조가 오리지널. AI(Meta AI & Gemini)는 검토 도구로 활용.
- 철학: PHILOSOPHY.ko.md / 스펙: SPEC.ko.md / 출처: SOURCES.md / 라이선스: LICENSE.md / 교육: EDUCATION.md

## 선언
2026-08-22 GitHub SHA + RFC3161 + somamoa.ai.kr 3중 박제, CC BY 4.0 & DPL, 독점 특허 불가
v2.2-Final-2026-08-27 APPROVED
원본: 공장/건설 현장 deundeuni - 한국어로 사유하고 글로벌 코드로 증명

## 선행기술 검증 명령어
git log --show-signature -1 v2.2-Final-2026-08-27