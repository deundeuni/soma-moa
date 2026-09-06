# soma-moa : Spec v2.2 Final
> **domain:** `somamoa.ai.kr` | **repo:** `github.com/soma-moa` | **v2.2 Final:** 2026-08-27  
> **Status:** English/Korean Technical Standard | **Authoritative:** `PHILOSOPHY.ko.md`  
> **License:** CC BY 4.0 & DPL | **Origin:** by deundeuni (soma-moa)  
> **Authoritative Original Clause:** Korean original (`PHILOSOPHY.ko.md`) is the authoritative source document, and translations are provided for reference only.

---

### 1. Core Architecture

$$\text{[Brain: LLM/VLM Probabilistic]} \longrightarrow \text{[Governance: soma-moa Deterministic eFPGA]} \longrightarrow \text{[Actuator/APK]}$$

- **L0 Physical —** CWP Battery-Swap (60T/61T Diff) + V-Home Self-Align $\pm 5\text{mm}$ + $0.1\text{ms}$ HW Intercept E-Stop (Motor EN PIN LOW cutoff control)
- **L1 Compute —** Chiplet-APU Many as One Dual-Redundant + CCS $70\% / 100\text{ms}$ Raft Role-Swapping + Shoulder 3-Tier Monitoring (Token Bucket + T-Reg $15\%$ + Tri-State)
- **L2 Governance —** Brain vs Governance physical separation + eFPGA $0.1\text{ms}$ Blocker + FSM
  $$\text{IDLE} \longrightarrow \text{MONITOR} \longrightarrow \text{VALIDATE (<0.02ms)} \longrightarrow \text{PRELOCK (80\%)} \longrightarrow \text{OVERRIDE} \longrightarrow \text{E\_STOP\_LATCH (<0.1ms)} \longrightarrow \text{RECOVERY}$$
- **L3 Social —** Quiet Assist 1x/2x Haptic + Anonymized Delta Logging PII $10\text{s}$ auto-deletion orientation + Just Culture

#### 1.1 Edge Quantitative Parameters & Constraints
- **CBOR Data Payload —** L0 24B (PII removed) + L1 33B (8B token) $< 50\text{B}$ Array Encoding ($0.01\text{mm}$ quantization)
- **SDK Constraint —** $35.2\text{KB} < 42\text{KB}$ Zero-Dep C/Rust
- **RAM Memory —** $3.2\text{KB}$ ($100 \times 33\text{B}$, $10\text{s}$ volatile buffer)
- **Verification Latency —** L0 Sync $0.1\text{ms}$ HMAC HW Bypass / L1 Async $2\sim5\text{ms}$ Ed25519

---

### 1.2 Location Mapping - Enterprise / Daily / Personal Sub-categories

- **[A] Enterprise — High-availability operational continuity environments (L0/L1/L2 focused)**
  - Logistics Center — Vehicle ID / Dock assignment / Safety training integration, L0 collision $0.1\text{ms}$ cutoff control, L1 inventory lookup integration.
  - Factory / Cloud Farm — Chiplet-APU Many as One + CCS Raft + $85\%$ backpressure throttling + leukocyte scan isolation.
  - Equipment Repair Center (Laptops/Smartphones/Cameras) — Model name / Serial / Symptoms / Warranty / Repair history / Engineer assignment integration. Resident terminals perform daily inspections, L1 diagnosis, and L3 mediation without rebooting privileges.
  - Department Store / Hospital Resident — Returns / Lost & Found / VIP / Missing children / Multilingual support, L1 inventory lookup, and L3 escalation integration.

- **[B] Daily — Assistive and exploratory environments (L3 + Vibe Search focused)**
  - Food Court / Restaurant — Menu / Allergy / Queue number / Seating / Pickup call and health routine integration. Refrains from speculative guessing when allergy data is uncertain, escalating to L3.
  - Department Store Service Center Visitors — Lost & Found / Missing children / Multilingual assistance support.
  - Library Librarian Vibe Search — Search books via cover / vibe / synopsis when title is unknown.
  - Music Search — Search via humming / melody / vibe / lyrics context. Refrains from assertive speculation when confidence $< 90\%$, connecting to L3.

- **[C] Personal — Privacy-focused and quiet environments (L3 focused)**
  - Personal Customization — Medication / Task / Health routines, device repair history / warranty, diet / allergy management.
  - Quiet Assist — Utilizes discreet Haptic 1x (caution) / 2x (stop) alerts felt only by the operator instead of public alarms.
  - No-Record Consideration — Minor operational slips are auto-deleted after $10\text{s}$ to mitigate operational friction, while physical risk logs are preserved (GDPR 5(1)(e)).

---

### 1.3 Organic Self-Resolution Principle

Aims to complete anomaly mitigation internally on-site through organic layer integration before human intervention.

$$\text{Self-Resolvable Anomalies (Misalignment, Overload, Packet Burst)} \longrightarrow \text{L0/L1/L2 Local Mitigation (Token Bucket, Raft, Tri-State, T-Reg)}$$
$$\text{Human Escalation (L3)} \longrightarrow \text{Reserved as Last Resort to Minimize Operator Fatigue}$$

- **L0 Local Mitigation —** V-Home $\pm 5\text{mm}$ mechanical alignment error absorption retry, CWP differential (60T/61T Diff) low-impact redocking, $0.1\text{ms}$ E-Stop self-re-enable retry.
- **L1 Local Mitigation —** Throttling upon detecting queue $85\%$ backpressure, CCS $70\%$ Raft $100\text{ms}$ re-election, leukocyte isolation buffer, T-Reg $15\%$ resource throttling, Tri-State permanent isolation.
- **L2 Local Mitigation —** eFPGA $0.02\text{ms}$ VALIDATE $\rightarrow$ $80\%$ PRELOCK $\rightarrow$ OVERRIDE $\rightarrow$ E_STOP_LATCH internal latch control. Preserves internal CBOR data without cloud telemetry logging.

---

### 2. Axiom 0 (0번 헌장)

*"Robots/AI are Sub, system governance is Main, but even governance itself is Auxiliary to human primary operations."*  
Guarantees ultimate human decision-making rights to foster a safe coexistence environment where workers "arrive with a smile, return home with a smile."

---

### 3. Security & Self-Healing

Proof-of-Clearance (Ed25519), Cloud-Sign / Edge-Verify, CBOR L0 24B + L1 33B $< 50\text{B}$ Array Encoding ($0.01\text{mm}$ quantization), SDK $35.2\text{KB} < 42\text{KB}$ Zero-Dep C/Rust, RAM $3.2\text{KB}$ ($10\text{s}$ volatile), L0 Sync $0.1\text{ms}$ HMAC HW Bypass / L1 Async $2\sim5\text{ms}$ Ed25519.

#### 3.1 APK Security & Integrity
- **Signature Verification & Integrity Control —** Prevents application execution upon signature verification failure.
- **Rooting & Jailbreak Mitigation —** Preserves L2 Lock and Telemetry logs upon detecting rooting or jailbreaking to safeguard hardware safety.
- **Log Minimization —** Refrains from unauthorized cloud log collection, maintaining a localized safety preservation system centered on internal CBOR encoded data.

#### 3.2 Self-Healing Reset Distinction (Soft Reset vs Hard Reset)
- **Soft Reset (Autonomous Control) —** Targets: Chiplet reboot, Raft re-election, Token Bucket reset, V-Home redocking, Leukocyte isolation release / Human Signature: Not required / Conditions: T-Reg $15\%$ quota limit applied, Tri-State permanent isolation upon 3 consecutive failures / Rationale: Safety-II Resilience, Graceful Degradation.
- **Hard Reset (Human Verification Mandatory) —** Targets: Motor EN LOW E_STOP_LATCH release $\rightarrow$ RECOVERY / Human Signature: Ed25519 Human Sign-off mandatory (permanent latch maintained without signature orientation) / Conditions: Restricts auto-restart (Self-restart) and enforces manual approval recovery / Rationale: ISO 13849-1 Cat 4 PL e, IEC 61508 SIL3 Fail-Safe.

---

### 4. Escalation & Operations

$$\text{L1 (BLE/MQTT-SN Haptic 1x/2x)} \longrightarrow \text{L2 (Lock \& Telemetry Risk Log)} \longrightarrow \text{L3 (WebRTC Sign-off Human Approval)}$$

- **4.1 3 AS Tiers —** Remote/OTA support, Dispatch service, Resident service (Hospitals/Factories/Department Stores/Logistics/Repair Centers/Food Courts). Resident staff lack simple restart privileges and execute compliance protocols rather than making arbitrary judgments.
- **4.2 Self-Resolution & Escalation Relationship —** Triggers L3 escalation only upon reaching 3 consecutive self-resolution failures or exceeding T-Reg/Tri-State thresholds, prioritizing the minimization of human fatigue (Quiet Assist).

---

### 5. Safety Framework & Quantitative Standards

- **[S-01] Heinrich 1931 (300:29:1) —** Cited solely for historical/philosophical motivation; actual implementation relies on Safety-II, Just Culture, and anonymous near-miss reporting systems.
- **[S-02] Swiss Cheese (Reason 1990) —** Active detection and mitigation of systemic defense flaws.
- **[S-03] Defense in Depth —** Multi-layered defense architecture.
- **[S-04] Fail-Safe —** Motor EN PIN LOW physical signal cutoff control.
- **[S-05] ALARP Extension & Standards Compliance —** ISO 13849-1 Cat 4 PL e, IEC 61508 SIL3, GDPR Article 5(1)(e) PII $10\text{s}$ auto-deletion orientation.

#### 5.1 Modernized Safety Application
- **Safety-II (Hollnagel) —** Focuses on maintaining stable conditions for $9,999$ successful everyday operations alongside accident prevention (realized via Many as One + Raft).
- **Just Culture —** Auto-deletes minor slips after $10\text{s}$ and encourages voluntary defect reporting via anonymous CBOR logging.
- **Active Swiss Cheese Model —** Preemptively closes systemic vulnerabilities via leukocyte scans, T-Reg $15\%$ throttling, and Tri-State isolation.

---

### 6. Article X & Extended Interfaces

- **Article X —** Controls chassis operations via dual I/O requirements regardless of physical form factor (wheeled/quadruped/humanoid). Brain (AI) acts as a proposer, while Governance executes deterministic control.
- **6.1 Vibe Search —** Library book search (cover/vibe/synopsis) and music humming search (melody/vibe/lyrics) integration. Refrains from assertive speculation when confidence $< 90\%$, triggering L3 escalation.

---

### 7. Specification Verification & Standards

- **Communication & Consensus Standards —** CBOR RFC 8949, Raft Ongaro 2014, HMAC-SHA256, Ed25519 RFC 8032.
- **Functional Safety & Legal Compliance —** ISO 13849-1:2023 PL e, IEC 61508 SIL3, GDPR 5(1)(e), USPTO AI Inventorship Guidance (2024.02), Thaler v. Vidal (2022), EPO G-II 3.3.1.

---

### 8. Open Foundation Models & Solo Conception Attribution

This protocol originated from the practical domain insights of a single human designer (`deundeuni`), derived from factory machinery sample work and construction site labor experience.

Open foundation models and AI tools—including Transformer (2017), TensorFlow (2015), Gemma (2024), Llama series (2023~), and Claude (2023~)—were utilized as verification instruments during formalization. Meta AI, Gemini, and Claude served as technical review tools; core technical conception and architectural design reside with `deundeuni`.

Trade secrets—including eFPGA RTL code, precision CAD drawings, and firmware binary source files—remain confidential.

---

### 9. Prior Art Registration & Disclaimer

- **Prior Art Global Registry Identifiers (Zenodo DOIs / GitHub Repositories) —**
  - `deundeuni/CWP-Battery-Swap` (DOI: `10.5281/zenodo.22373538`)
  - `deundeuni/CWP-Clamping-Battery-Swap-System` (DOI: `10.5281/zenodo.22373722`)
  - `deundeuni/CWP-Rolling-Self-Align-Battery-Swap-System` (DOI: `10.5281/zenodo.22373704`)
  - `deundeuni/LAST-LIGHT` (DOI: `10.5281/zenodo.22373189`)
  - `deundeuni/MAX-LIFE-ICE-BELT` (DOI: `10.5281/zenodo.22373686`)
  - `deundeuni/chiplet-apu-multi-system-survival-architecture` (DOI: `10.5281/zenodo.22374987`)
  *(Registered / Active on CERN Zenodo & DataCite Global Registries)*

- **Non-Intentional Omission & Non-Exhaustive Disclaimer —** Standards and repositories cited herein serve as illustrative examples and do not imply exhaustive limitations. Derived standards, revised specifications, and equivalent prior art connected to the underlying concepts fall within the defensive scope of this whitepaper.

---
origin: by deundeuni (soma-moa) | domain: somamoa.ai.kr / Somamoa.ai.kr | repo: github.com/soma-moa
v2.2 Final: 2026-08-27 | PHILOSOPHY.ko.md is authoritative | License: CC BY 4.0 & DPL
