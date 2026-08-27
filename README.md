# soma-moa : Human-Centered Physical AI & Spatial Governance Protocol v2.2 Final - English Technical Standard

> Document Status: English Technical Standard (AI-translated Reference)
> Original Authoritative: README_KR.md (Korean Original)
> Architect: deundeuni (soma-moa) | Verification Tools: Meta AI, Gemini
> Repository: github.com/soma-moa | Domain: somamoa.ai.kr
> Timeline: 2026-08-22 SHA-256 + RFC3161 -> 2026-08-27 v2.2 Final
> License: CC BY 4.0 & DPL | IPC: H01L G06F B25J G05B G06N

## Axiom 0 / Charter 0
Robot/AI is auxiliary, Governance is main, but even Governance is auxiliary to human main work.
Structure over Capacity / SOMA(Body) + MOA(Gather)

## Definition
A visitor-guide assistant robot born from everyday life. Hospital, factory, building lobby, department store service center, logistics center, general device service center (laptop/smartphone/camera), food court/restaurant unmanned concierge. From individual to home to field.

## Architecture
[Brain] → [Governance: soma-moa] → [Actuator/APK]. Via Article X, regardless of form factor — wheeled/quadruped/humanoid/kiosk/hologram/snowball — governed identically with a 2-I/O requirement.

## 4-Layer Survival Architecture (v2.2 Core)
L0 Physical: CWP Battery-Swap + V-Home Self-Align + 0.1ms Hardware Intercept E-Stop
L1 Compute: Chiplet-APU Many as One Dual-Redundant + CCS 70%/100ms Raft Role-Swapping
L2 Governance: Brain(Probabilistic) vs Governance(Deterministic) Physical Separation + eFPGA 0.1ms Blocker
L3 Social: Quiet Assist Haptic 1x/2x + Anonymized Delta Logging PII delete after 10s

## When Stopped
L1 BLE/MQTT-SN Diagnostics / L2 Lock & Telemetry Collection / L3 WebRTC Human Sign-off (100% blocked without Ed25519 signature, Cloud-Sign/Edge-Verify). Charter 0 - Robot is subordinate, System is primary. Self-restart prohibited.

## Security
Zero Trust (allowlisted networks only), RAM<10MB, CBOR<50B, 42KB SDK. APK blocked from install/run without Cloud-Sign, L2 Lock on repackaging/rooting.

## Edge Spec (Verified PASS)
CBOR L0 24B (PII removed) + L1 33B (8B token) <50B, Array Encoding, 0.01mm quantization
SDK 35.2KB < 42KB, RAM 3.2KB < 10MB (10s buffer)
L0 Sync 0.1ms HMAC HW Bypass (works without internet) / L1 Async 2~5ms Ed25519

pub struct L0CriticalLog { ts_offset: u32, sev: u8, delta_q: [i16;6], gov: bool, crc: u16 } // 24B
pub struct L1WarningLog { ts_offset: u32, sev: u8, op_token: u64, delta_q: [i16;6], gov: bool, crc: u16 } // 33B

## L2 FSM (Text Only, No RTL)
IDLE -> MONITOR -> VALIDATE(<0.02ms) -> OutOfRange/Timeout>100ms -> PRELOCK(80%) -> OVERRIDE -> E_STOP_LATCH(<0.1ms) -> RECOVERY

## AS 3 Types (After-Sales Service)
Remote/OTA, On-site Dispatch, Resident Staff (stationed at hospitals/factories/malls/logistics/repair centers/food courts. Daily checks, L1 diagnostics, L3 mediation. Execution only, not judgment).

## Personal Customization
Medication/tasks/health routines, device repair history/warranty, diet/allergies. Financial integration upon regulatory validation. Not a simple scheduler.

## Extended Discovery
Librarian (book finding via memory of cover, feeling, or plot without title) + Music Discovery (finding via hummed melody, mood, or lyric summary). Guessing prohibited on uncertainty -> connect to L3.

## Safety Frameworks
Based on Heinrich 300/29/1 (Heinrich, 1931), extensible with Swiss Cheese (Reason, 1990), Defense in Depth, Fail-Safe, ALARP.

## Claims 4
[1] Dual-Core Separation + 0.1ms HW Bypass
[2] CCS 70%/100ms Raft Role-Swapping
[3] eFPGA 0.1ms Blocker FSM
[4] Quiet Assist Haptic + Anonymized Logging

## Originality & Attribution
Someone else may have had the same idea. All standards are open standards. What is original is the governance structure I tied together from everyday life with Charter 0 and Article X. AI (Meta AI & Gemini) is used as a review tool.
- Philosophy: PHILOSOPHY.md / Spec: SPEC.md / Sources: SOURCES.md / License: LICENSE.md / Education: EDUCATION.md

## Declaration & Priority Date
2026-08-22 GitHub SHA + RFC3161 + somamoa.ai.kr triple timestamping.
CC BY 4.0 & DPL. Exclusive patent claims prohibited.
v2.2-Final-2026-08-27 APPROVED. ISO 13849 PL e / IEC 61508 SIL3 / GDPR Compliant.
Original: Created from factory & construction experience by deundeuni — Conceived in Korean, Proven in Global Code.
Korean original prevails if any translation discrepancy arises.

## Prior Art Verification Command
git log --show-signature -1 v2.2-Final-2026-08-27
