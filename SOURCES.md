# soma-moa : Sources & Prior Art Basis (v2.2 Final)
> domain: somamoa.ai.kr | origin: deundeuni (soma-moa) | v2.2 Final: 2026-08-27
> Document Status: Bilingual Technical Reference (EN/KO)

### [Safety] 물리적 안전 이론
[S-01] Heinrich 1931 - EN: 300:29:1 Pyramid / KO: 무벌점 텔레메트리 뼈대 (1 중대사고 전 29경상 300무상해)
[S-02] Swiss Cheese - EN: James Reason 1990 Human Error / KO: 다중 방어막 모델
[S-03] Defense in Depth - EN: US NRC, NSA / KO: 심층 방어
[S-04] Fail-Safe - EN: Fail to Safe State, EN LOW / KO: L2 Lock & E-Stop Latch
[S-05] ALARP - EN: UK HSE, As Low As Reasonably Practicable / KO: 최저 위험 확장
[S-06] Quiet Assist - EN: Haptic 1x/2x, No-Log Grace 10s / KO: 조용한 보조, 자체 정의 - Technician Dignity

### [Standard] 기능안전 & 개인정보
[F-01] ISO 13849-1:2023 - EN: Cat 4 / PL e / KO: eFPGA 0.1ms HW Intercept 충족
[F-02] IEC 61508:2010 - EN: SIL3 / KO: L2 Deterministic Blocker SIL3
[F-03] GDPR Article 5(1)(e) - EN: Storage Limitation, PII 10s deletion / KO: L0 PII 배제 + L1 휘발
[F-04] ISO 12100:2010 - EN: Risk Assessment Machinery / KO: 위험성 평가

### [Tech-Crypto] 서명 & 인코딩
[T-01] Ed25519 - EN: Bernstein et al. 2011, RFC 8032 / KO: 서명 없이는 차단, Cloud-Sign/Edge-Verify
[T-02] CBOR - EN: RFC 8949 (RFC 7049), Array Encoding 0.01mm quant / KO: L0 24B + L1 33B <50B 근거
[T-03] HMAC-SHA256 - EN: RFC 2104, FIPS 180-4 / KO: L0 Sync 0.1ms HW Bypass Fast-Path
[T-04] Zero Trust - EN: NIST SP 800-207 2020 / KO: 승인망만 (Proof-of-Clearance)
[T-05] APK Signing - EN: Android v2/v3 Scheme / KO: 리패키징 방지, 무결성 검증

### [Tech-Comm] 통신 & 합의
[T-06] MQTT-SN/BLE/WebRTC - EN: OASIS / BT SIG / W3C / KO: L1/L2/L3 에스컬레이션
[T-07] Raft Consensus - EN: Ongaro & Ousterhout 2014 In Search of Understandable Consensus / KO: L1 Chiplet-APU Many as One 70%/100ms Role-Swapping
[T-08] Chiplet-APU / CWP Battery-Swap / V-Home - EN: UCIe, CXL, Self-Align Docking / KO: 물리적 생존 구조

### [Tech-Search] 검색 & 발견
[T-09] Vibe/Semantic Search - EN: Embedding Vector Search, Query2Doc / KO: 의미/흥얼검색
[T-10] Librarian Model - EN: Reference Interview, Taylor 1968 / KO: 사서 레퍼런스 인터뷰 - 제목 몰라도 표지/느낌/줄거리로 찾기
[T-11] Music Hum Search - EN: Query by Humming, Dannenberg 2007 / KO: 흥얼거림으로 찾기

### [Arch] 구조 & 헌장 (자체 정의)
[A-01] Article X - EN: Form-factor Agnostic Control, I/O 2-Factor / KO: 구조 무관 통제 (바퀴/4족/휴머노이드 동일)
[A-02] Charter Axiom 0 - EN: Human Final Control, Auxiliary Governance / KO: 0번 헌장 - 로봇/AI는 부, 거버넌스는 주, 그조차 인간 주작업엔 보조

### [Legal] 법적 & 발명자
[L-01] USPTO AI Inventorship Guidance - EN: 2024.02.13 Federal Register, Natural Person Conception / KO: 자연인 단독 구상 원칙 (deundeuni)
[L-02] Thaler v. Vidal - EN: 43 F.4th 1207 (Fed. Cir. 2022) / KO: 발명자 자격 인격체 한정 판례
[L-03] EPO Guidelines G-II 3.3.1 - EN: AI-assisted inventions / KO: 기술적 기여 인간 귀속 규정
[L-04] Pannu v. Iolab Corp. - EN: 155 F.3d 1344 (Fed. Cir. 1998) / KO: 인간 실질적 기여 평가 기준 (Pannu Factors)
[L-05] USPTO AI Guidance Principle 3 - EN: Refinement and Error Correction of AI Output / KO: AI 출력물 오류 검증 및 수정자 발명자 인정 기준
[L-06] Burroughs Wellcome v. Barr Labs - EN: 40 F.3d 1223 (Fed. Cir. 1994) / KO: 작동 가능한 최종 구상 완성자 귀속 판례

### [Open] 기반 개방 & 검증 도구
[O-01] Transformer - EN: Vaswani et al. 2017 Attention Is All You Need / KO: 구글 뼈대 공개1 - 현대 LLM 기반
[O-02] TensorFlow - EN: Google 2015 Open Source / KO: 구글 뼈대 공개2 - 개인 AI 접근성 개방
[O-03] Gemma - EN: Google 2024 Open Models / KO: 구글 뼈대 공개3 - 경량 개방 모델
[O-04] Llama 2/3 - EN: Meta 2023-2024 Open Release / KO: Meta 개방 - 엣지 검증 기반
[O-05] Verification Tools - EN: Meta AI & Gemini as Verification Tools / KO: 검증 및 시뮬레이션 도구 (Conception by deundeuni)

---
origin: by deundeuni (soma-moa) | domain: somamoa.ai.kr
v2.2 Final: 2026-08-27 | License: CC BY 4.0 & DPL | Korean Original Prevails
Trade Secret: eFPGA RTL, precise CAD, firmware binary remain private
