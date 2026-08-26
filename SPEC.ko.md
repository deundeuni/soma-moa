# soma-moa : Spec v1.0-RC
> domain: somamoa.ai.kr

### 1. 아키텍처: [Brain] → [Governance: soma-moa] → [Actuator/APK]
### 1.1 장소 매핑
- 백화점 서비스센터: 반품/분실물/VIP/미아보호/다국어
- 물류센터: 차량번호/도크 배정/안전교육
- 기기 AS센터(노트북/스마트폰/카메라): 모델명/시리얼/증상/보증/수리이력/엔지니어 배정
- 푸드코너/식당: 메뉴/알러지/대기번호/자리/픽업 호출, 건강 루틴 연동. 알러지 불확실 시 추측 금지, L3 에스컬레이션.

### 2. 0번 헌장: 로봇은 부, 시스템이 주. 인간 최종 판단.
### 3. 보안: Proof-of-Clearance (Ed25519), Cloud-Sign/Edge-Verify, CBOR<50B, 42KB SDK
### 3.1 APK 보안: 서명 없으면 차단, 무결성 검증, 루팅 시 L2 Lock
### 4. 에스컬레이션: L1 BLE/MQTT-SN → L2 Lock & Telemetry → L3 WebRTC Sign-off
### 4.1 AS 3종: 원격/출동/상주. 상주 직원은 재가동 권한 없음.
### 5. 안전: [S-01] Heinrich 1931 기본, [S-02] Swiss Cheese, [S-03] Defense in Depth, [S-04] Fail-Safe, [S-05] ALARP 확장
### 6. Article X: 구조 무관, I/O 2대 요건으로 통제
### 6.1 Vibe Search: 도서관 사서(줄거리/느낌) + 음악 흥얼검색(멜로디/느낌). 90% 미만 시 L3.

---
origin: by deundeuni | domain: somamoa.ai.kr