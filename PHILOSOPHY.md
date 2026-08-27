# soma-moa : Design Philosophy & Prior Art Declaration
> **original design:** `deundeuni (soma-moa)` | **repository:** `github.com/soma-moa`  
> **initial record date:** 2026-08-24 | **prior art declaration:** 2026-08-25
> **domain:** `somamoa.ai.kr`

This document is a record of why `soma-moa` was designed this way.
It is not about the final result, but the process; not about technical specifications, but traces of thought.

---

### 0. Designed in Native Language

`soma-moa` was not built in English first and then translated into Korean.
It originally began from knowledge accumulated in daily life while working with various machines doing sample work in factories and working as a construction laborer. With the recent discovery of AI, it started from the simple thought: *"Could I also create documentation with this?"*

It is a protocol conceived through deep thought in Korean, then proven as global standard code.
Therefore, `moa` is not an alias; it is its true name.

While English words like *gather* or *collect* translate to "모으다," the nuance of "embracing and bringing together fragmented error logs and distributed edge devices" is uniquely captured in the native Korean word *moa*.

This is the identity of `soma-moa` and the starting point of its design.

---

### 1. v0.1 OSRP - The Skeleton Days

**Project Name: OSRP (Open Symbiotic Routine Protocol)**

It started by defining the bare minimal skeleton:
- **Zero-Trust Security:** Authorize key exchange only; direct sensor telemetry strictly through internal networks.
- **3-Step Escalation:** WebRTC Video Stream -> Telemetry Log -> On-site Human Dispatch.
- **Ultimate Human Control:** Prevent autonomous decision-making by robots acting alone.

The word 'Routine' was abandoned because it sounded like a simple scheduler, and was recognized as non-intuitive engineering jargon.

---

### 2. v1.0 SOMA - Taking Physical Form

**Project Name: SOMA (Symbiotic Operations & Machine Architecture)**

Elevated to a full governance framework when virtual AI takes on physical bodies (Greek: *Soma*).

- **Architectural Structure:** Separated into a higher-level governance layer responsible for safety and control, regardless of the physical chassis (wheeled, quadrupedal, or humanoid).
- **Charter Axiom 0 Established:**  
  *"Robots/AI are Sub, System Governance is Main, but even Governance itself is Auxiliary to human primary operations."*

---

### 3. v1.5 Naming Search - Criteria Beyond 20 Candidate Names

Beyond the English name SOMA, over 20 candidate names were reviewed to find an intuitive and easily pronounceable identity.

- **Bodeum, Gyeol, Irum:** Too heavy in pronunciation.
- **Nuri, Miso, Uri:** Lacks technical intuition.
- **Gori, Dari, Sai:** Too narrow in scope to encompass N:1 data collection platforms.

**3 Established Criteria:**
1. Must be pronounceable within 0.1 seconds.
2. Must convey operational structure upon hearing it.
3. Must hold scalability to gather distributed edge nodes into one.

---

### 4. v2.0 soma-moa - Perfection of Name and Typography

**Official Designation: soma-moa by deundeuni**

- **moa:** The core essence of gathering scattered error logs and technical standards.
- **Linguistic Symmetry:** Visual and phonetic rhythm alignment of S O M A (o/a) - m o a (o/a).
- **Lowercase Standard:** Officially finalized in lowercase with a hyphen (`soma-moa`) to reflect its open-source protocol identity for seamless code integration.

---

### 5. Auxiliary Governance & Prior Art Declaration

**Publication Purpose (2026-08-25):**  
This document discloses the minimal safety auxiliary specification as Prior Art for the coexistence of AI, robots, and humans, preventing exclusive patent monopolies by specific corporations and allowing anyone to implement it freely.

- **Prerequisite of Coexistence:** Set "smiles at shift start, smiles at shift end" as the baseline for workers. There is no coexistence without guaranteed safety.
- **Auxiliary Principle:** Governance exists as a lightweight auxiliary layer that does not impede primary work (construction, service, logistics).
- **Deterministic Interlock:** In cases of probabilistic AI hallucinations, a 0.1ms deterministic L0 interlock cuts power buses immediately to ensure human physical safety.

---

### 5-1. Technician Dignity & Quiet Assist Protocol

**Purpose: Preserve physical safety without harming human dignity.**

The fastest safety in the field is immediate correction. When people feel embarrassed, they hide instead of fixing, and hidden errors become accidents. This protocol prevents that.

**1. Quiet Assist (Haptic Only)**
When AI detects a minor error or risk, it does NOT trigger a loud alarm or pop-up for everyone to see. Instead, it notifies only the wearer via a private haptic signal (1x vibration on wristband/tool).
- 1x vibration: "Not this way, hold on a sec"
- 2x vibration: "Okay for now, let's check it on the next routine"
Other workers do not notice, so workflow and atmosphere remain intact.

**2. No-Log Grace (Local-Only, Auto-Delete in 10s)**
This quiet assist signal leaves NO cloud log. It is auto-deleted from the device after 10 seconds.
This is NOT for hiding mistakes. For physical risks (collision, electric shock), the 0.1ms L0 deterministic cutoff still activates instantly and its log IS preserved for safety.
No-Log applies only to minor, correctable errors like missed checks or wrong order. With no fear of performance review, technicians fix immediately, making the site safer.

**3. Principle of Respect**
AI is not a supervisor who teaches workers in front of others. It is an auxiliary that taps you quietly on the side.
This implements Axiom 0 of soma-moa: "Governance itself is only auxiliary to human's main work" as human-to-human courtesy.

**One-line summary:** Physical safety is enforced strongly with 0.1ms cutoff, social safety (embarrassment) is protected softly with 1 haptic and no-log grace. This enables "Leave with a smile, return with a smile."

---

### 6. Cross-AI Technical Peer Review & Attribution

Rather than relying solely on a single designer's rationale, technical precision was maximized through cross-peer reviews with major foundation AI architectures.

- **Meta AI - Edge Hardware Optimization:**  
  Validated Cloud-Sign / Edge-Verify structure, RAM <10MB, CBOR <50B, and C/Rust Zero-Dep 42KB ultra-light SDK footprint.
- **Gemini - Multimodal Spatial AI & Governance:**  
  Formulated dual-core separation of probabilistic Brain (LLM/VLM) and deterministic Governance (`soma-moa`). Refined predictive pre-lock (80% Confidence), Article X I/O 2-factor test, and Heinrich 300/29/1 spatial safety flywheel.

---

### 7. Somamoa Brand Expansion & Domain Alignment

Beyond the open-source protocol standard (`soma-moa`), the brand and domain (`Somamoa.ai.kr`) are unified under `Somamoa` for commercial ecosystem growth and brand consistency.
- Open-source Protocol Code Name: `soma-moa`
- Official Project / Brand Name: `Somamoa`

---

### 8. Open Foundation Models & Solo Design

This protocol originated from the thoughts of a single designer (`deundeuni`) rather than a giant organization.
It originally started from knowledge accumulated in daily life while working with various machines doing sample work in factories and working as a construction laborer. With the recent discovery of AI, it started from the thought, *"Could I also create documentation with this?"*

Thanks to Google opening up its AI foundation infrastructure alongside various other companies, making AI accessible to individuals, an ordinary person like me could gratefully use AI to create materials that can contribute to the world.

`soma-moa` is a record of that journey. It was refined through edge optimization verification with Meta AI and spatial governance verification with Gemini.
This serves as a factual record showing that the opening of foundation models enables ecosystem expansion—not exclusive monopolies by specific corporations—encompassing individuals and diverse physical machines on the ground (collaborative robots, AGVs, construction equipment, service robots).

---
origin: by deundeuni (soma-moa) - factory sample work & construction worker background  
domain: somamoa.ai.kr / Somamoa.ai.kr | repo: github.com/soma-moa  
technical reviews: Meta AI & Gemini (as tools)  
prior art declaration: 2026-08-25 | initial record: 2026-08-24  
Article tags: Auxiliary Governance, Technician Dignity Protocol, Quiet Assist, No-Log Grace, Physical AI Safety