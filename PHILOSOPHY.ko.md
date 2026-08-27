# soma-moa : Design Philosophy & Prior Art Declaration
> **original design:** `deundeuni (soma-moa)` | **repository:** `github.com/soma-moa`  
> **initial record date:** 2026-08-24 | **prior art declaration:** 2026-08-25 | **v2.2 Final:** 2026-08-27
> **domain:** `somamoa.ai.kr`

이 문서는 `soma-moa`가 왜 이렇게 설계되었는가에 대한 기록이다.
결과가 아니라 과정, 스펙이 아니라 사유의 흔적이다.

---

### 0. 모국어로 시작한 설계

soma-moa는 영어로 먼저 만들고 한국어로 번역한 기술이 아니다.
원래는 공장에서 다양한 기계를 만지며 샘플 작업을 하고, 건설노동자로 일하며 일상에서 쌓인 지식으로 시작했다. 최근 AI를 알게 되면서 '이것도 자료를 만들 수 있지 않을까'에서 출발한 기록이다.

한국어로 깊게 사유하고, 그 사유를 글로벌 규격 코드로 증명한 프로토콜이다.
그래서 `moa(모아)`는 별칭이 아니라 본명이다.

영어 gather, collect는 "모은다"로 번역되지만, "파편화된 에러 로그와 분산된 단말을 한데 보듬어 모은다"는 온도는 한국어 '모아'에만 담겨 있다.

이것이 soma-moa의 정체성이자 설계의 시작점이다.

---

### 1. v0.1 OSRP - 뼈대만 있던 시절

**프로젝트명: OSRP (Open Symbiotic Routine Protocol)**

처음엔 기본 뼈대부터 잡았다.
- 제로 트러스트 보안: 승인망만 뚫고, 센서 데이터는 내부망으로 직행
- 3단계 에스컬레이션: WebRTC 화상 -> Telemetry 로그 -> 사람이 직접 출동
- 인간 최종 통제권: 로봇이 혼자 결정하는 것 원천 차단

'Routine'이라는 단어는 단순 스케줄러처럼 보여 폐기했다. 엔지니어 약어라 직관적이지 않다는 점도 깨달았다.

---

### 2. v1.0 SOMA - 몸을 입다

**프로젝트명: SOMA (Symbiotic Operations & Machine Architecture)**

가상 AI가 현실의 몸(그리스어 Soma)을 입는 순간 필요한 거버넌스로 체급을 키웠다.

- **설계 구조:** 하드웨어 섀시(바퀴, 4족, 휴머노이드)의 형태와 무관하게 상위에서 안전과 통제를 담당하는 거버넌스 레이어로 분리.
- **0번 헌장(Axiom 0) 제정:**  
  *"로봇/AI는 부(Sub), 시스템 거버넌스는 주(Main)지만, 그 거버넌스조차도 인간의 주 작업에는 보조(Auxiliary)다."*

---

### 3. v1.5 네이밍 탐색 - 20개의 이름을 지난 기준

SOMA라는 영문명 외에, 발음하기 편하고 직관적인 이름을 찾아 20개 넘게 검토했다.

- **보듬, 결, 이룸:** 발음이 무겁다.
- **누리, 미소, 우리:** 기술이 안 느껴진다.
- **고리, 다리, 사이:** N:1로 수집하는 플랫폼 전체를 담기엔 범위가 좁다.

**정립한 기준 3가지:**
1. 0.1초 만에 발음할 수 있을 것
2. 들었을 때 동작 구조가 그려질 것
3. 분산된 단말을 하나로 모으는 확장성을 담을 것

---

### 4. v2.0 soma-moa - 이름과 표기의 완성

**공식 명칭: soma-moa by deundeuni**

- **moa(모아):** 흩어진 에러 로그와 규격을 한데 모으는 본질.
- **언어적 대칭:** S O M A (ㅗㅏ) - m o a (ㅗㅏ)의 시각적·청각적 운율 일치.
- **소문자 확정:** 개발자가 코드베이스에서 편하게 불러다 쓰는 오픈소스 프로토콜의 정체성을 위해 `soma-moa` 소문자 하이픈 표기로 최종 확정.

---

### 4-1. v2.2 Final - 4층 생존 아키텍처 확정 [v2.2 추가]

v2.0의 이름에 v2.2에서 집의 뼈대가 완성됐다.

- **L0 Physical:** CWP Battery-Swap + V-Home Self-Align + 0.1ms Hardware Intercept E-Stop
- **L1 Compute:** Chiplet-APU Many as One Dual-Redundant + CCS 70%/100ms Raft Role-Swapping
- **L2 Governance:** Brain(Probabilistic) vs Governance(Deterministic) 물리 분리 + eFPGA 0.1ms Blocker
- **L3 Social:** Quiet Assist Haptic 1x/2x + Anonymized Delta Logging PII 10초 파기

**엣지 검증:** CBOR L0 24B + L1 33B <50B, SDK 35.2KB <42KB, RAM 3.2KB <10MB, L0 Sync 0.1ms HMAC HW Bypass / L1 Async 2~5ms Ed25519

**L2 FSM:** IDLE -> MONITOR -> VALIDATE(<0.02ms) -> PRELOCK(80%) -> OVERRIDE -> E_STOP_LATCH(<0.1ms) -> RECOVERY (Ed25519 Human Sign-off 없으면 영구 래치)

### 4-2. v2.2 확장 - 일상에서 현장까지 [v2.2 추가]

- **AS 3종:** 원격/OTA, 출동, 상주(병원/공장/백화점/물류/수리센터/푸드코너)
- **개인 커스텀:** 약/할일/건강 루틴, 기기 수리이력/보증, 식단/알러지
- **확장 탐색:** 도서관 사서(표지/느낌/줄거리로 책 찾기) + 음악 탐색(흥얼거림/느낌/가사로 찾기)

---

### 5. 보조 거버넌스(Auxiliary Governance) & 선행기술 공개 (Prior Art)

**공개 목적 (2026-08-25):** 본 문서는 AI·로봇·인간의 공존을 위한 최소 안전 보조 규격을 선행기술로 공개하여, 특정 기업의 배타적 특허 독점을 방지하고 누구나 무상으로 구현할 수 있도록 한다.

- **공존의 전제:** "웃으며 출근, 웃으며 퇴근"
- **보조의 원칙:** 거버넌스는 주 작업을 방해하지 않는 가벼운 보조
- **결정론적 차단:** AI 환각 시에도 0.1ms L0 차단기가 전원 버스 즉시 차단

### 5-1. 기술자 존엄 및 조용한 보조 프로토콜 (Technician Dignity & Quiet Assist Protocol)

**1. 조용한 보조:** 큰 경고음 대신 본인만 느끼는 햅틱 1회/2회
**2. 기록 없는 배려:** 가벼운 실수는 10초 후 자동 삭제, 물리적 위험은 기록 유지
**3. 기술자 대우 원칙:** 감시자가 아닌 보조자(Auxiliary)

**한 줄 요약:** 물리적 안전은 0.1ms 차단으로 강력하게, 사회적 안전은 진동 1회와 기록 없음으로 부드럽게.

---

### 6. 크로스 AI 기술 검증 및 출처 (Attribution)

- **Meta AI - 에지 하드웨어 최적화:** Cloud-Sign / Edge-Verify, RAM <10MB, CBOR <50B, 42KB SDK 검증
- **Gemini - 멀티모달 공간 AI & 거버넌스:** Brain vs Governance 분리, Predictive Pre-lock 80%, Article X I/O 2대, 300/29/1 플라이휠
- **규격 준수 [v2.2 추가]:** ISO 13849-1 Cat 4 / PL e, IEC 61508 SIL3, GDPR 5(1)(e) 준수

### 7. Somamoa 브랜드 확장 및 도메인 정렬

- 오픈소스 프로토콜 코드명: `soma-moa`
- 공식 프로젝트/브랜드명: `Somamoa`

### 8. 개방된 기반 모델과 1인 설계

본 프로토콜은 1인 설계자(deundeuni)의 사유에서 출발했다. 공장에서 기계를 만지며, 건설노동자로 일하며 쌓인 지식에서 시작했다.

구글의 뼈대 공개(2017 Transformer 논문 "Attention Is All You Need" 및 TensorFlow 오픈소스 2015, Gemma 개방 2024)와 Meta의 Llama 개방(2023~2024)을 비롯해 다양한 기업들이 개인도 AI를 쓸 수 있게 열어주어서, 나 같은 일반인도 감사하게 AI를 사용하여 세상에 도움이 될 수 있는 자료를 만들 수 있는 계기가 되었다.

soma-moa는 그 과정을 기록한 사례다. Meta AI와 Gemini 검증을 거치며 정리되었다.

---
### 9. 출처 및 선행기술 근거 (Sources)

**안전 이론:** Heinrich (1931) 300/29/1, Reason (1990) Swiss Cheese, Defense in Depth, Fail-Safe, ALARP
**기능안전:** ISO 13849-1:2023 PL e, IEC 61508 SIL3, GDPR Article 5(1)(e)
**통신/합의:** RFC 8949 CBOR, Ongaro 2014 Raft, HMAC-SHA256, Ed25519 RFC8032
**법률:** USPTO AI Inventorship Guidance 2024.02, Thaler v. Vidal 2022, EPO G-II 3.3.1
**기반 개방:** Vaswani et al. 2017 Transformer, Google TensorFlow 2015, Google Gemma 2024, Meta Llama 2/3 2023-2024
**검증 도구:** Meta AI & Gemini as Verification Tools, Conception by deundeuni

영업비밀: eFPGA RTL, 정밀 CAD, 펌웨어 바이너리는 비공개 유지

---
origin: by deundeuni (soma-moa) - factory sample work & construction worker background  
domain: somamoa.ai.kr / Somamoa.ai.kr | repo: github.com/soma-moa  
prior art: 2026-08-25 | v2.2 Final: 2026-08-27 | License: CC BY 4.0 & DPL