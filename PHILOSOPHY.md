# soma-moa : Design Philosophy & Prior Art Declaration
> **original design:** `deundeuni (soma-moa)` | **repository:** `github.com/soma-moa`  
> **initial record date:** 2026-08-24 | **prior art declaration:** 2026-08-25 | **v2.2 Final:** 2026-08-27  
> **domain:** `somamoa.ai.kr` | **License:** CC BY 4.0 & DPL  
> **Naming Pre-definition:** The open-source protocol and codebase are designated as `soma-moa` (lowercase with hyphen), while the service brand and overall project entity are designated as `Somamoa`, both representing the same identity.  
> **Authoritative Original Clause:** PHILOSOPHY.ko.md (Korean) is the authoritative original document, and translations are provided for reference only.

This document records why `soma-moa` was designed in this manner.  
It is a record of the thought process and journey, rather than just final specifications or results.

---

### 0. Design Rooted in the Native Language

soma-moa is not a technology that was conceived in English and translated into Korean.  
It originated from real-world insights gained while performing sample work with factory machinery and working as a construction laborer. With the advent of AI, it evolved from the question: 'Could this daily field knowledge be structured into a technical protocol?'

It is a protocol forged through deep thinking in native Korean and proven through globally compliant code.  
Thus, `moa` (모아) is not a nickname, but its core name.

While English words like "gather" or "collect" translate to "모은다", the warmth of "embracing and gathering fragmented error logs and distributed endpoints together" is uniquely expressed in the Korean word 'moa'.

This is the identity and starting point of the soma-moa design.

---

### 1. v0.1 OSRP - The Days of Bare Skeleton

**Project Name: OSRP (Open Symbiotic Routine Protocol)**

The initial stage focused on establishing the core foundation.
- **Zero-Trust Security:** Allows connection only through approved networks, aiming for direct transmission of sensor data to the internal network.
- **3-Stage Escalation:** WebRTC video -> Telemetry logging -> Direct human dispatch.
- **Human Ultimate Control:** Restricts autonomous decision-making by robots to guarantee human intervention rights.

The term 'Routine' was discarded as it resembled a simple scheduler, and engineering acronyms were recognized as lacking intuitive clarity for general operators.

---

### 2. v1.0 SOMA - Taking Physical Form

**Project Name: SOMA (Symbiotic Operations & Machine Architecture)**

The framework expanded into governance required when virtual AI takes on a physical body (Greek *Soma*).

- **Architectural Structure:** Separates physical chassis forms (wheeled, quadruped, humanoid) from the upper governance layer responsible for safety and control.
- **Establishment of Axiom 0 (0번 헌장):**  
  *"Robots/AI are Sub, system governance is Main, but even governance itself is Auxiliary to human primary operations."*

---

### 3. v1.5 Naming Search - Criteria After 20 Names

In addition to the English name SOMA, over 20 names were evaluated to find a term that was easy to pronounce and intuitive.

- **Bodeum, Gyeol, Irum** — Pronunciation felt heavy.
- **Nuri, Miso, Uri** — Technical identity was not clearly conveyed.
- **Gori, Dari, Sai** — Scope felt limited for representing a platform gathering N:1 endpoints.

**Three Established Criteria:**
1. Pronounceable within 0.1 seconds.
2. Operational structure immediately visualizable upon hearing.
3. Contains scalability to gather distributed endpoints into one entity.

---

### 4. v2.0 soma-moa - Completing the Name and Notation

**Official Name: soma-moa by deundeuni**

- **moa (모아):** The essence of gathering scattered error logs and technical standards into one framework.
- **Linguistic Symmetry:** Visual and auditory rhythm alignment between S O M A (ㅗㅏ) - m o a (ㅗㅏ).
- **Lowercase Confirmation:** Standardized as `soma-moa` in lowercase with a hyphen for seamless developer usability across open-source codebases.

---

### 4-1. v2.2 Final - 4-Layer Survival Architecture & L2 FSM Specification

On top of the v2.0 naming foundation, the v2.2 specification finalized the core survival architecture.

- **L0 Physical:** CWP Battery-Swap + V-Home Self-Align + 0.1ms Hardware Intercept E-Stop (Motor EN PIN LOW cutoff control)
- **L1 Compute:** Chiplet-APU Many as One Dual-Redundant + CCS 70%/100ms Raft Role-Swapping + Shoulder 3-Tier Monitoring
- **L2 Governance:** Brain (Probabilistic) vs Governance (Deterministic) physical separation + eFPGA 0.1ms Blocker + FSM
- **L3 Social:** Quiet Assist Haptic 1x/2x + Anonymized Delta Logging PII 10s auto-deletion

**Edge Verification Parameters:** CBOR L0 24B + L1 33B <50B, SDK 35.2KB <42KB, RAM 3.2KB <10MB, L0 Sync 0.1ms HMAC HW Bypass / L1 Async 2~5ms Ed25519

**L2 FSM State Transitions and Roles:**
- **IDLE:** Normal standby state
- **MONITOR:** Real-time monitoring of edge sensors and telemetry logs
- **VALIDATE (<0.02ms):** eFPGA-based deterministic safety rule verification
- **PRELOCK (80%):** Preemptive hardware lock preparation upon reaching an 80% risk probability threshold
- **OVERRIDE:** Phase where L2 deterministic governance and human control physically override and nullify anomalous AI inference (Brain) attempts to secure immediate priority
- **E_STOP_LATCH (<0.1ms):** Latching motor power pin to LOW within 0.1ms
- **RECOVERY:** Permanently holds the latched state; recovery is prohibited without Ed25519 human cryptographic signature sign-off

---

### 4-2. v2.2 Expansion - From Daily Life to On-Site

- **3 AS Tiers:** Remote/OTA, Dispatch, Resident (Hospitals, Factories, Department Stores, Logistics, Repair Centers, Food Courts)
- **Personal Customization:** Medication/Task/Health routines, Equipment repair history/Warranty, Diet/Allergy tracking
- **Extended Discovery:** Library Librarian (Book search via cover/vibe/synopsis) + Music Discovery (Search via humming/vibe/lyrics)

---

### 4-3. v2.2 Sub-categorization - Enterprise / Daily / Personal

While `moa` gathers everything, lightweight execution requires functional categorization into three domains:

- **Enterprise:** High-availability operational environments. Factories, logistics, hospitals, resident AS centers. Centered on L0 0.1ms cutoff + L1 Many as One + L2 deterministic execution. Guarantees ultimate human decision-making.
- **Daily:** Assistive and exploratory environments. Food courts, customer service centers, libraries, music search. Centered on Vibe Search + L3 escalation. Avoids assertive speculation when confidence is under 90%.
- **Personal:** Privacy-focused environments. Medication/Tasks/Health, Diet/Allergy, Repair history. Centered on PII 10s auto-deletion + Haptic 1x/2x + minimal unnecessary logging.

Connecting all endpoints while distributing operational friction is the core principle of `Auxiliary` governance.

---

### 4-4. Inheritance of Safety Philosophy - Heinrich as Foundational Motivation Only

Heinrich's 300:29:1 ratio (1931) serves as a historical and philosophical motivation regarding why preventive measures must be gathered, rather than an absolute mathematical law.

Actual implementation adopts modern safety frameworks:
- **Safety-II / Resilience (Hollnagel):** Focuses on maintaining stable conditions for the 9,999 successful everyday operations alongside accident prevention, realized via Many as One and Raft-based architecture.
- **Just Culture + Anonymous Reporting:** Encourages voluntary defect reporting through CBOR 24B anonymous logging + PII 10s auto-deletion + minimal logging for minor operational slips.
- **Active Swiss Cheese Model:** Actively scans for systemic vulnerabilities via leukocyte scans, T-Reg 15% throttling, and Tri-State isolation before latent flaws align into accidents.
- **Quantitative Standard Alignment:** Replaces empirical ratios with formal functional safety standards: ISO 13849-1 Cat 4 PL e / IEC 61508 SIL3 / GDPR 5(1)(e).

> [S-01] Heinrich 1931 is cited solely for historical/philosophical motivation; actual implementation relies on Safety-II, Just Culture, deterministic override control, and anonymous near-miss reporting.

---

### 4-5. Organic Integration and Self-Mitigation Philosophy

The system aims to resolve anomalies locally within the site through organic layer integration.

- L0: V-Home mechanically absorbs physical docking alignment errors up to ±5mm.
- L1: Resolves compute issues internally via 70% Raft re-election, 85% backpressure throttling, and leukocyte node isolation.
- L2: eFPGA executes lock control within 0.02ms VALIDATE and logs events internally.

Only when local mitigation is insufficient does L3 issue a Haptic 1x/2x notification before escalating to human operators via WebRTC, preserving technician dignity by treating human intervention as the ultimate authority.

---

### 4-6. System Specification Summary

For prior art verification and technical review alignment, key quantitative parameters are compiled below:

- **L0 Physical Cutoff Latency —** 0.1ms Hardware Intercept E-Stop (Motor EN PIN LOW)
- **L0 Physical Alignment Tolerance —** V-Home Self-Align ±5mm physical tolerance absorption
- **L0/L1 Verification Latency —** L0 Sync 0.1ms HMAC HW Bypass / L1 Async 2~5ms Ed25519
- **L1 Compute Consensus Threshold —** CCS Raft 70% quorum / 100ms Role-Swapping
- **L1 Compute Backpressure Threshold —** Automatic throttling upon detecting 85% fabric backpressure
- **L1 Compute Data Payload —** CBOR packet L0 24B + L1 33B (<50B constraint)
- **L2 Governance Verification Latency —** eFPGA deterministic VALIDATE <0.02ms
- **L2 Governance Predictive Threshold —** PRELOCK hardware lock prep at 80% risk probability
- **L2 Governance Self-Healing Limits —** T-Reg 15% quota limit; permanent isolation after 3 consecutive failures
- **L3 Social Confidence Threshold —** Daily Vibe Search refrains from guessing if confidence <90%
- **L3 Social PII Purge Cycle —** Anonymized Delta Logging auto-deleted within 10 seconds
- **Edge Embedded Resource Constraints —** SDK size 35.2KB (<42KB limit), RAM 3.2KB (<10MB limit)

---

### 5. Auxiliary Governance & Prior Art Declaration

**Public Declaration Purpose (2026-08-25):** This document publicly discloses minimum safety governance specifications for AI-robot-human coexistence as defensive prior art, aiming to mitigate risk of third-party patent monopolization and establish public-domain technology.

- **Premise of Coexistence:** "Safe arrival at work, safe return home."
- **Auxiliary Principle:** Governance functions as a lightweight assistant without interfering with primary operations.
- **Deterministic Override:** Ensures physical power bus cutoff via L0 intercept even during AI hallucination or erratic inference.

---

### 5-1. Technician Dignity & Quiet Assist Protocol

- **Quiet Assist:** Utilizes discreet Haptic 1x/2x vibration alerts felt only by the operator instead of loud public alarms.
- **No-Record Consideration:** Minor operational slips are auto-deleted after 10 seconds to alleviate stress, while physical risk logs are preserved.
- **Technician Dignity Principle:** Establishes technology as an auxiliary helper rather than a surveillance tool.

**Summary:** Physical safety is enforced via 0.1ms L0 cutoff, while social safety is achieved via gentle haptics and auto-deleting privacy controls.

---

### 5-2. Self-Healing Reset Philosophy - Soft vs Hard

- **Soft Reset (Autonomous, No Human Signature):** L0/L1 self-healing — Chiplet reboot, Raft re-election, Token Bucket reset, V-Home redocking. Executed autonomously under T-Reg 15% limit and 3-failure isolation rules.
- **Hard Reset (Human Signature Mandatory):** L2 E_STOP_LATCH release. Clearing Motor EN LOW latch and entering RECOVERY requires an Ed25519 cryptographic signature from a human operator. Prohibits auto-restart in compliance with ISO 13849-1 / IEC 61508.

---

### 6. Cross-AI Technical Verification & Legal Doctrine

- **Meta AI — Edge Hardware Optimization & Cloud-Sign / Edge-Verify Dual Verification:** Establishes an authentication architecture where Ed25519 signatures are issued from cloud/server (Cloud-Sign), while L0 real-time synchronous layers utilize 0.1ms HMAC HW Bypass and L1 asynchronous layers execute 2~5ms Ed25519 offline verification (Edge-Verify) on resource-constrained edge devices. Validated RAM <10MB, CBOR <50B, and SDK 42KB limits.
- **Gemini — Multimodal Spatial AI & Governance:** Validated Brain vs Governance physical separation, Predictive Pre-lock 80%, Article X dual I/O, and 300/29/1 safety flywheel.
- **Claude (Anthropic) — Technical Document Architecture Review & Structural Consistency:** Utilized for cross-checking layer specifications, verifying narrative and quantitative parameter consistency, and formatting the defensive prior art whitepaper layout.
- **Human Sole Inventorship & Legal Doctrine Citation (USPTO / EPO / Case Law):** Cites US Supreme Court/CAFC precedent rejecting AI inventorship (*Thaler v. Vidal*), USPTO AI Inventorship Guidance (2024.02), and EPO Examination Guidelines (G-II 3.3.1). Establishes legally that AI models (Meta AI, Gemini, Claude) acted strictly as verification and formatting tools, while technical conception (Conception) resides solely with the human designer (`deundeuni`).
- **Standards Compliance:** Designed to meet ISO 13849-1 Cat 4 / PL e, IEC 61508 SIL3, and GDPR 5(1)(e) functional safety and privacy criteria.

---

### 7. Defensive Rights & Somamoa Brand Expansion

- **Open-Source Protocol Codebase:** `soma-moa`
- **Official Service & Brand Name:** `Somamoa`
- **Official Domains:** `somamoa.ai.kr` / `Somamoa.ai.kr`
- **Defensive Publication:** Technical concepts disclosed herein are released as public prior art to prevent exclusive patent claims by third parties and safeguard the open technology ecosystem.

---

### 8. Open Foundation Models and Solo Conception & Attribution

This protocol originated from the sole human designer (`deundeuni`). It started from practical domain knowledge accumulated while operating factory machinery, performing sample work, and participating in construction site labor.

soma-moa represents the formalization of this field-derived thought process into globally standardized code as defensive prior art.

During this formalization, open foundation models and AI tools—including Google's Transformer (2017), TensorFlow (2015), Gemma (2024), Meta's Llama series (2023~), and Anthropic's Claude—were utilized as technical verification instruments. Meta AI, Gemini, and Claude served as verification and review tools; the core technical conception and architecture design belong to `deundeuni`.

---

### 9. Sources and Prior Art Foundations

- **Safety Theory:** Heinrich (1931) 300/29/1 — Philosophical motivation, Reason (1990) Swiss Cheese, Hollnagel Safety-II/Resilience, Defense in Depth, Fail-Safe, ALARP, Just Culture
- **Functional Safety & Privacy:** ISO 13849-1:2023 PL e, IEC 61508 SIL3, GDPR Article 5(1)(e)
- **Networking & Consensus:** RFC 8949 CBOR, Ongaro 2014 Raft, HMAC-SHA256, Ed25519 RFC8032
- **Legal Doctrines:** USPTO AI Inventorship Guidance 2024.02, Thaler v. Vidal 2022, EPO G-II 3.3.1
- **Open Foundations:** Vaswani et al. 2017 Transformer, Google TensorFlow 2015, Google Gemma 2024, Meta Llama 2/3 2023-2024, Anthropic Claude 2023-2026
- **Verification Tools:** Meta AI, Gemini, Claude as Verification Tools; Conception by `deundeuni`
- **Trade Secrets:** eFPGA RTL, precision CAD, and binary firmware source files remain undisclosed

---
origin: by deundeuni (soma-moa) - factory sample work & construction worker background  
domain: somamoa.ai.kr / Somamoa.ai.kr | repo: github.com/soma-moa  
Zenodo DOI: 10.5281/zenodo.22373538 / 22373722 / 22373704 / 22373189 / 22373686 / 22374987 (Active / Registered)  
prior art: 2026-08-25 | v2.2 Final: 2026-08-27 | License: CC BY 4.0 & DPL
