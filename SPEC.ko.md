# soma-moa : Spec v2.2 Final
> domain: somamoa.ai.kr | v2.2 Final: 2026-08-27 | Status: English/Korean Technical Standard
> PHILOSOPHY.ko.md is authoritative original

### 1. 아키텍처: [Brain: LLM/VLM Probabilistic] → [Governance: soma-moa Deterministic eFPGA] → [Actuator/APK]
- L0 Physical: CWP Battery-Swap + V-Home Align + 0.1ms HW Intercept (Motor EN PIN LOW)
- L1 Compute: Chiplet-APU Many as One + CCS 70%/100ms Raft
- L2 Governance: Brain vs Governance 물리 분리 + eFPGA 0.1ms Blocker + FSM: IDLE->MONITOR->VALIDATE(<0.02ms)->PRELOCK(80%)->OVERRIDE->E_STOP_LATCH->RECOVERY
- L3 Social: Quiet Assist 1x/2x Haptic + PII 10s auto-delete

### 1.1 장소 매핑
- 백화점 서비스센터: 반품/분실물/VIP/미아보호/다국어 + L1 재고조회 + L3 에스컬레이션
- 물류센터: 차량번호/도크 배정/안전교육 + L0 충돌 0.1ms 차단
- 기기 AS센터(노트북/스마트폰/카메라): 모델명/시리얼/증상/보증/수리이력/엔지니어 배정 + 상주: 일일점검 L1진단 L3중개, 재가동 권한 없음
- 푸드코너/식당: 메뉴/알러지/대기번호/자리/픽업 호출, 건강 루틴 연동. 알러지 불확실 시 추측 금지, L3 에스컬레이션. + 개인커스텀: 식단/알러지, 약/할일/건강

### 2. 0번 헌장: 로봇/AI는 부(Sub), 시스템 거버넌스는 주(Main), 그 거버넌스조차 인간의 주 작업에는 보조(Auxiliary). 인간 최종 판단.

### 3. 보안: Proof-of-Clearance (Ed25519), Cloud-Sign / Edge-Verify, CBOR L0 24B(PII 제거) + L1 33B(8B token) <50B Array Encoding 0.01mm 양자화, 35.2KB <42KB SDK Zero-Dep C/Rust, RAM 3.2KB(100*33B 10s 휘발), L0 Sync 0.1ms HMAC HW Bypass / L1 Async 2~5ms Ed25519

### 3.1 APK 보안: 서명 없으면 차단, 무결성 검증, 루팅/탈옥 시 L2 Lock & Telemetry 보존, 클라우드 로그 없음

### 4. 에스컬레이션: L1 BLE/MQTT-SN (Haptic 1x 주의/2x 정지) → L2 Lock & Telemetry (물리적 위험 시 기록 보존) → L3 WebRTC Sign-off (Ed25519 Human Sign-off 없으면 영구 래치, Self-restart 금지)

### 4.1 AS 3종: 원격/OTA, 출동, 상주(병원/공장/백화점/물류/AS센터/푸드코너). 상주 직원은 재가동 권한 없음, 판단 대신 집행만.

### 5. 안전: [S-01] Heinrich 1931 300/29/1, [S-02] Swiss Cheese, [S-03] Defense in Depth, [S-04] Fail-Safe (EN LOW), [S-05] ALARP 확장 + ISO 13849-1 Cat4 PL e / IEC 61508 SIL3 / GDPR 5(1)(e) PII 10s 파기

### 6. Article X: 하드웨어 섀시(바퀴/4족/휴머노이드) 구조 무관, I/O 2대 요건으로 통제. Brain은 제안만, Governance가 최종 집행

### 6.1 Vibe Search: 도서관 사서(제목 몰라도 표지/느낌/줄거리로 책찾기) + 음악 흥얼검색(멜로디/느낌/가사 줄거리로 찾기). Confidence 90% 미만 시 추측 금지, L3 연결.

---
origin: by deundeuni (soma-moa) | domain: somamoa.ai.kr / Somamoa.ai.kr | repo: github.com/soma-moa
v2.2 Final: 2026-08-27 | PHILOSOPHY.ko.md is authoritative | License: CC BY 4.0 & DPL