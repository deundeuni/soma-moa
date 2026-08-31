# soma-moa : Design Philosophy & Prior Art Declaration
> **Document Status:** English Technical Standard (AI-translated Reference)
> **Authoritative Original:** PHILOSOPHY.ko.md (Korean Original Prevails if any translation discrepancy arises)
> **original design:** `deundeuni (soma-moa)` | **repository:** `github.com/soma-moa`  
> **initial record date:** 2026-08-24 | **prior art declaration:** 2026-08-25 | **v2.2 Final:** 2026-08-27
> **domain:** `somamoa.ai.kr`
> **Architect:** deundeuni (soma-moa) | **Verification Tools:** Meta AI, Gemini

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

### 4-1. v2.2 Final - 4-Layer Survival Architecture [v2.2 Added]

The name from v2.0 now has a physical body that survives in the field.

- **L0 Physical:** CWP Battery-Swap + V-Home Self-Align + 0.1ms Hardware Intercept E-Stop
- **L1 Compute:** Chiplet-APU Many as One Dual-Redundant + CCS 70%/100ms Raft Role-Swapping
- **L2 Governance:** Brain(Probabilistic) vs Governance(Deterministic) Physical Separation + eFPGA 0.1ms Blocker
- **L3 Social:** Quiet Assist Haptic 1x/2x + Anonymized Delta Logging PII auto-delete after 10s

**Edge Verification (Verified PASS):** CBOR L0 24B (PII removed) + L1 33B (8B token) <50B Array Encoding 0.01mm quant, SDK 35.2KB <42KB, RAM 3.2KB (100*33B 10s volatile buffer) <10MB, L0 Sync 0.1ms HMAC HW Bypass (works without internet) / L1 Async 2~5ms Ed25519

**L2 FSM (Text Only):** IDLE -> MONITOR -> VALIDATE(<0.02ms) -> OutOfRange/Timeout>100ms -> PRELOCK(80%) -> OVERRIDE -> E_STOP_LATCH(<0.1ms) -> RECOVERY

### 4-2. v2.2 Expansion - From Daily Life to Field [v2.2 Added]

- **AS 3 Types:** Remote/OTA, On-site Dispatch, Resident Staff (stationed at hospitals/factories/malls/logistics/repair centers/food courts)
- **Personal Customization:** Medication/tasks/health routines, device repair history/warranty, diet/allergies
- **Extended Discovery:** Librarian (find book by cover/feeling/plot without title) + Music Discovery (find by humming/mood/lyric summary). Guessing prohibited on uncertainty -> connect to L3.

---

### 5. Auxiliary Governance & Prior Art Declaration

**Publication Purpose (2026-08-25):** This document discloses the minimal safety auxiliary specification as Prior Art for the coexistence of AI, robots, and humans, preventing exclusive patent monopolies by specific corporations and allowing anyone to implement it freely.

- **Prerequisite of Coexistence:** Set "smiles at shift start, smiles at shift end" as the baseline for workers.
- **Auxiliary Principle:** Governance exists as a lightweight auxiliary layer that does not impede primary work.
- **Deterministic Interlock:** 0.1ms deterministic L0 interlock cuts power buses immediately.

### 5-1. Technician Dignity & Quiet Assist Protocol

**Purpose: Preserve physical safety without harming human dignity.**

**1. Quiet Assist (Haptic Only):** 1x vibration: "Not this way, hold on a sec" / 2x: "Okay for now, let's check it on the next routine"
**2. No-Log Grace:** Auto-deleted from device after 10s. For physical risks, log IS preserved.
**3. Principle of Respect:** AI is not a supervisor, it is an auxiliary that taps you quietly on the side.

**One-line summary:** Physical safety is enforced strongly with 0.1ms cutoff, social safety (embarrassment) is protected softly with 1 haptic and no-log grace.

---

### 6. Cross-AI Technical Peer Review & Attribution

- **Meta AI - Edge Hardware Optimization:** Validated Cloud-Sign / Edge-Verify structure, RAM <10MB, CBOR <50B, and C/Rust Zero-Dep 42KB ultra-light SDK footprint. Verified L0 24B/L1 33B struct, 3.2KB buffer, HMAC 0.1ms / Ed25519 2~5ms separation.
- **Gemini - Multimodal Spatial AI & Governance:** Formulated dual-core separation of probabilistic Brain (LLM/VLM) and deterministic Governance (`soma-moa`). Refined predictive pre-lock (80% Confidence), Article X I/O 2-factor test, and Heinrich 300/29/1 spatial safety flywheel.
- **Compliance [v2.2 Added]:** ISO 13849-1 Cat 4 / PL e, IEC 61508 SIL3, GDPR Article 5(1)(e) Compliant

### 7. Somamoa Brand Expansion & Domain Alignment

- Open-source Protocol Code Name: `soma-moa`
- Official Project / Brand Name: `Somamoa`

### 8. Open Foundation Models & Solo Design

Designer
This protocol originates from the reasoning of a single designer (deundeuni). It began with hands-on knowledge accumulated while handling various machines for sample work in a factory and working as a construction worker.

soma-moa is a record of that reasoning, organized into global standard code.

In the process of organizing it, I was able to utilize open foundation models such as Google's Transformer (2017), TensorFlow (2015), Gemma (2024), and Meta's Llama (2023~) as verification tools, for which I am grateful. Meta AI and Gemini are verification tools; the conception belongs to deundeuni.

---
### 9. Sources & Prior Art Basis [v2.2 Added]

**Safety Theory:** Heinrich, H.W. (1931). Industrial Accident Prevention 300/29/1, Reason, J. (1990). Human Error - Swiss Cheese Model, Defense in Depth, Fail-Safe, ALARP
**Functional Safety:** ISO 13849-1:2023 Cat 4 / PL e, IEC 61508 SIL3, GDPR Article 5(1)(e)
**Comm/Consensus:** RFC 8949 CBOR (RFC 7049), Ongaro, D. (2014). Raft Consensus, HMAC-SHA256, Ed25519 RFC8032
**Legal:** USPTO AI Inventorship Guidance (2024.02) - Natural Person Conception, Thaler v. Vidal, 43 F.4th 1207 (Fed. Cir. 2022), EPO Guidelines G-II 3.3.1
**Foundation Open:** Vaswani et al. (2017). Attention Is All You Need - Transformer, Google TensorFlow (2015), Google Gemma (2024), Meta Llama 2/3 (2023-2024)
**Verification Tools:** Meta AI & Gemini (as tools, not inventors) - Conception by deundeuni

Trade Secret: eFPGA RTL Gate-level code, precise CAD dimensions, firmware binary remain private.

---
origin: by deundeuni (soma-moa) - factory sample work & construction worker background  
domain: somamoa.ai.kr / Somamoa.ai.kr | repo: github.com/soma-moa  
technical reviews: Meta AI & Gemini (as tools)  
prior art declaration: 2026-08-25 | initial record: 2026-08-24 | v2.2 Final: 2026-08-27  
License: CC BY 4.0 & DPL | Note: This English version is AI-translated. Korean original (PHILOSOPHY.ko.md) prevails legally.
Article tags: Auxiliary Governance, Technician Dignity Protocol, Quiet Assist, No-Log Grace, Physical AI Safety, 4-Layer Survival Architecture, Edge Spec 24B/33B, L2 FSM 0.1ms