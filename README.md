soma-moa : Human-Centered Physical AI & Spatial Governance Protocol v2.2 Final
> original design: deundeuni (soma-moa) | repository: github.com/soma-moa
> domain: somamoa.ai.kr | v2.2 Final: 2026-08-27 | License: CC BY 4.0 & DPL
> Note: The Korean originals (README.ko.md / PHILOSOPHY.ko.md) are authoritative; translations are for reference only.

0. Definition
soma-moa is a visiting guide and spatial assistant robot protocol that starts from everyday life and scales to diverse sites including hospitals, factories, building lobbies, department store service centers, logistics centers, device after-service centers (laptop/smartphone/camera), and unmanned concierge in food courts / restaurants.

1. Axiom 0
"Robot/AI is Sub, System Governance is Main, but even that Governance is Auxiliary to human's main work."

2. Core Architecture
$$\text{[Brain]} \longrightarrow \text{[Governance: soma-moa eFPGA]} \longrightarrow \text{[Actuator/APK]}$$
 * Article X Spec — Aiming for unified integrated control with only 2 upper-level I/O requirements, regardless of hardware chassis structure such as wheels, quadruped, humanoid, kiosk, hologram, or snowball form.

3. 4-Layer Survival Architecture (4-Layer Survival System)
 * L0 Physical — CWP Battery Swap + V-Home Self-Align $\pm 5\text{mm}$ + $0.1\text{ms}$ Physical Cutoff E-Stop (Motor EN PIN LOW control)
 * L1 Compute — Chiplet-APU Many as One Redundancy + CCS $70\% / 100\text{ms}$ Raft Hitless Role Switch + Shoulder 3-stage Control (Token Bucket + T-Reg $15\%$ + Tri-State)
 * L2 Governance — Brain (Probabilistic) vs Governance (Deterministic) Physical Separation + eFPGA $0.1\text{ms}$ Deterministic Blocker
 * L3 Social — Quiet Assist Haptic 1x/2x + Anonymized Delta Logging with PII auto-deletion aimed at $10\text{s}$

4. Edge Verification
 * CBOR Payload — L0 24B (PII removed) + L1 33B (8B token) $< 50\text{B}$ ($0.01\text{mm}$ quantization)
 * Embedded Constraint — SDK size $35.2\text{KB} < 42\text{KB}$ Zero-Dep C/Rust, RAM $3.2\text{KB}$
 * Sync/Async Latency — L0 Sync $0.1\text{ms}$ HMAC Hardware Bypass / L1 Async $2\sim5\text{ms}$ Ed25519

```rust
// L0 Critical Log Structure (24 Bytes)
pub struct L0CriticalLog {
    pub ts_offset: u32,
    pub sev: u8,
    pub delta_q: [i16; 6],
    pub gov: bool,
    pub crc: u16,
}

// L1 Warning Log Structure (33 Bytes)
pub struct L1WarningLog {
    pub ts_offset: u32,
    pub sev: u8,
    pub op_token: u64,
    pub delta_q: [i16; 6],
    pub gov: bool,
    pub crc: u16,
}

```

5. Location Mapping • Enterprise — Environments focused on operational continuity such as logistics centers, factories, AS centers, department stores/hospitals on-site (No reboot authority granted to resident terminal).[A] • Daily — Vibe Search-centric environments such as food courts, libraries, music discovery (Avoiding definitive conjecture when confidence < 90\%).[B] • Personal — Personalized environments such as medication / todo / health / diet / repair history (PII deletion $10\text{s}$ + haptic 1x/2x notification).[C]  6. Security & Self-Healing • APK Security — Blocks installation/execution if electronic signature is missing, and transitions to L2 Lock state to protect hardware upon detecting repackaging, rooting, or jailbreak. • Soft Reset (Autonomous) — Chiplet restart, Raft re-election, Token Bucket reset, V-Home re-docking. T-Reg $15\%$ limit and permanent isolation after 3 consecutive failures. • Hard Reset (Human Confirmation Required) — Ed25519 human signature required to enter RECOVERY after Motor EN LOW E_STOP_LATCH release (Self-restart not aimed).  7. Safety Framework • S-01 Heinrich (1931) — 300:29:1 ratio is cited as historical/philosophical motivation, while actual implementation is based on Safety-II and Just Culture. • S-02 ~ S-05 and Functional Safety — Active blocking via Swiss Cheese, Defense in Depth, Fail-Safe (EN PIN LOW), ALARP extension and compliance with ISO 13849-1 Cat 4 PL e / IEC 61508 SIL3 / GDPR Article 5(1)(e) PII deletion $10\text{s}$ clause.  8. Prior Art & Disclaimer • Prior Art Registry (CERN Zenodo DOIs) — • deundeuni/CWP-Battery-Swap (DOI: 10.5281/zenodo.22373538) • deundeuni/CWP-Clamping-Battery-Swap-System (DOI: 10.5281/zenodo.22373722) • deundeuni/CWP-Rolling-Self-Align-Battery-Swap-System (DOI: 10.5281/zenodo.22373704) • deundeuni/LAST-LIGHT (DOI: 10.5281/zenodo.22373189) • deundeuni/MAX-LIFE-ICE-BELT (DOI: 10.5281/zenodo.22373686) • deundeuni/chiplet-apu-multi-system-survival-architecture (DOI: 10.5281/zenodo.22374987)
     (Listed in CERN Zenodo / DataCite Global Academic Registry / Active) • Prior Art Registration Notice — All commit hashes of this document and timestamps are registered in the CERN Zenodo / DataCite global academic registry. • Non-Intentional Omission & Non-Exhaustive Disclaimer — Technical standards cited are exemplary and not exhaustive. All derivative standards connected to the disclosed idea are deemed included in the prior art scope. 
origin: by deundeuni | domain: somamoa.ai.kr | repo: github.com/soma-moa | v2.2 Final: 2026-08-27 | PHILOSOPHY.ko.md is authoritative | CC BY 4.0 & DPL