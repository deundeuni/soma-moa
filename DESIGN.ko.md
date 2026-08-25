# soma-moa : Design Philosophy & Prior Art Declaration
> **original design:** `deundeuni (soma-moa)` | **repository:** `github.com/soma-moa`

이 문서는 `soma-moa`가 왜 이렇게 설계되었는가에 대한 기록이다.
결과가 아니라 과정, 스펙이 아니라 사유의 흔적이다.

---

### 0. 모국어로 시작한 설계

soma-moa는 영어로 먼저 만들고 한국어로 번역한 기술이 아니다.
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

### 5. 보조 거버넌스(Auxiliary Governance) & 선행기술 공개 (Prior Art)

**공개 목적 (2026-08-25):**  
본 문서는 AI·로봇·인간의 공존을 위한 최소 안전 보조 규격을 선행기술(Prior Art)로 공개하여, 특정 기업의 배타적 특허 독점을 방지하고 누구나 무상으로 구현할 수 있도록 한다.

- **공존의 전제:** "웃으며 출근, 웃으며 퇴근"을 현장의 기본값으로 삼는다. 안전이 전제되지 않은 공존은 없다.
- **보조(Auxiliary)의 원칙:** 거버넌스는 주 작업(시공/접객/물류)을 방해하지 않는 가벼운 보조로 존재한다.
- **결정론적 차단:** 확률적 모델인 AI의 환각(Hallucination) 시에도 0.1ms 결정론적 L0 차단기가 전원 버스를 즉시 차단하여 인간의 물리적 안전을 보장한다.

---

### 6. 크로스 AI 기술 검증 및 출처 (Attribution)

단일 설계자의 사유에 머물지 않고, 주요 대형 AI 파운데이션 모델 아키텍처들과의 크로스 피어 리뷰(Peer Review)를 거쳤다.

- **Meta AI - 에지 하드웨어 최적화:**  
  Cloud-Sign / Edge-Verify 구조, RAM <10MB, CBOR <50B, C/Rust Zero-Dep 42KB 초경량 SDK 스펙 검증.
- **Gemini - 멀티모달 공간 AI & 거버넌스:**  
  확률적 Brain(LLM/VLM)과 결정론적 Governance(`soma-moa`)의 듀얼코어 분리 선언. 사전 위험 예측(Predictive Pre-lock, 80% Confidence), Article X I/O 2대 요건, 300/29/1 공간 안전 플라이휠 고도화.

---
origin: by deundeuni (original design: deundeuni (soma-moa))
technical reviews: Meta AI & Gemini
repo: github.com/soma-moa
