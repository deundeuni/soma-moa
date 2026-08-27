# soma-moa : Master Technical Specification (v2.2 Final)
> **Document Status:** English Technical Standard (AI-translated Reference)
> **Authoritative Original:** SPEC.ko.md / PHILOSOPHY.ko.md (Korean Original Prevails if any translation discrepancy arises)
> **Translation Note:** This English version is AI-translated and may contain imperfect or non-smooth expressions. For legal purposes, the Korean original shall prevail.
> **Architect:** deundeuni (soma-moa) | **Verification Tools:** Meta AI, Gemini (as tools, not inventors)
> **original design:** `deundeuni (soma-moa)` | **repository:** `github.com/soma-moa`
> **initial record date:** 2026-08-24 | **prior art declaration:** 2026-08-25 | **v2.2 Final:** 2026-08-27
> **domain:** `somamoa.ai.kr`

---

## 1. Governance Architecture (L0-L3 / 4-Layer Survival Architecture)

```text
+-------------------------------------------------------------------+
| [L3] Social: Quiet Assist Haptic 1x/2x + PII 10s Auto-Delete |
| [L2] Governance Core: Deterministic eFPGA 0.1ms Blocker + FSM |
| -> IDLE->MONITOR->VALIDATE(<0.02ms)->PRELOCK(80%)->OVERRIDE |
| -> E_STOP_LATCH(<0.1ms HW Intercept Motor EN LOW)->RECOVERY |
+-------------------------------------------------------------------+
                                  ▲ Proof-of-Clearance (Ed25519)
+-------------------------------------------------------------------+
| [L1] Compute: Chiplet-APU Many as One Dual-Redundant |
| -> CCS 70%/100ms Raft Role-Swapping, 3.2KB 10s Volatile Buffer |
+-------------------------------------------------------------------+
                                  ▲ Cloud-Sign / Edge-Verify
+-------------------------------------------------------------------+
| [L0] Physical: CWP Battery-Swap + V-Home Self-Align |
| -> 0.1ms HMAC HW Bypass Fast-Path, CBOR L0 24B (PII Removed) |
+-------------------------------------------------------------------+
                                  ▼
+-------------------------------------------------------------------+
| [Sub] Actuator & Sensor (Article X - Structure Agnostic) |
| -> Robots, AGVs, Construction Equip, Service Robots, |
| Notebooks/Smartphones/Cameras, AR Glasses |
+-------------------------------------------------------------------+