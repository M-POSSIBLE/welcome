# M-Possible v1.0 — Inversion Rigidity Protocol ("The Thud")

> **Local candidate framework (no parity implied with externally validated laws).**

**Protocol version:** v1.0-provisional  
**Status:** Pre-charter draft — Council-3 ADM-EC approved  
**Anchor phenomenon:** Mpemba effect (Phase 1)

---

## 1. Purpose

This protocol defines the universal binary freezing marker for Institute M-Possible.

The marker must be:

- **resolution-independent** — usable from home kitchens to precision laboratories,
- **instrument-free at Tier 1b** — no sensors required for the base measurement,
- **physically meaningful** — encoding a mechanical phase transition rather than a visual impression.

The binary event is the load-bearing invariant of the entire measurement system. All admissible data enters the shared statistical object through this single gate.

---

## 2. Core definitions

**Sample pair:**
Two water samples prepared at the same time, in the same type of container, placed in the same freezing environment, differing only in initial water treatment (e.g. initial temperature, prior thermal history).

**Freezing event (binary marker):**
The first instant at which a sample no longer flows as a liquid under gravity in the standard inversion test (Section 3). This event is designated T_Rigid.

**Terminal event rule:**
T_Rigid is terminal. The freezing event is the first pass of the inversion test. Subsequent thermal evolution of the sample does not alter this timestamp.

**Disqualifying motion:**
Any visible bulk motion of liquid water during the inversion dwell period, including sloshing, sliding, dripping, detaching chunks, or visible deformation of the mass due to flow. Micro-cracks within a clearly rigid block do not count as disqualifying motion.

**Surface-closure timestamp (optional extension):**
The time at which a continuous, opaque ice layer is first observed across the sample surface. This is logged only as an auxiliary observable at higher tiers. It does not define the freezing event and does not affect admissibility.

---

## 3. Standard inversion test

### 3.1 Setup

- Use a transparent container from the approved container class list (published in the Handbooks).
- Fill within the specified fill-level band (e.g. 60–80 % of container volume).
- Place both samples in the freezing environment side by side, with sufficient space to retrieve and invert them safely.
- Record before starting:
  - Operator pseudonym
  - Container class and material (see Section 4, field 3)
  - Environment tag (household-freezer / Baumhaus / lab-freezer / outdoor / other)
  - Protocol version identifier (epoch marker)
  - Start time: the moment both samples enter the freezing environment

### 3.2 Test schedule

- Begin inversion testing after a minimum waiting period (recommended: 15 minutes for household freezers) to avoid continuous thermal disturbance.
- Thereafter, perform inversion tests at fixed intervals. Recommended: every 5 minutes for household environments. Laboratories may use finer schedules; the chosen interval must be recorded.
- At each interval, test both samples in immediate succession.

### 3.3 Test procedure

For each sample:

1. Remove the container from the freezer, holding it upright.
2. Without shaking, invert the container 180° (opening downward) in one smooth, continuous motion. The rotation from upright to fully inverted should take 1–2 seconds, without intermediate stops or lateral shaking. Rotations completed in under 0.5 seconds or exceeding 3 seconds must be marked "ambiguous — inversion speed out of range" in the notes field.
3. Hold inverted for **10 seconds**.
4. Observe:
   - **Pass** — no part of the bulk contents flows, slides, drips, or visibly deforms under gravity during the full 10-second dwell. The sample has reached mechanical arrest.
   - **Fail** — any bulk flow is observed. The sample has not yet frozen for protocol purposes.
5. Return the container to its upright orientation and place it back in the freezer promptly.

### 3.4 Disturbance budget

Each removal-inversion-return cycle exposes the sample to ambient temperature. Over many checks, this accumulated disturbance alters the freezing process — particularly in household freezers with slow recovery times.

Total time outside the freezing environment prior to T_Rigid must not exceed 90 seconds per sample. If this limit is exceeded, the run must be marked "disturbance-heavy" in the notes field. Disturbance-heavy runs remain admissible but carry the flag into the statistical object for downstream analysis.

Operators should aim to complete each inversion check (removal, inversion, 10-second dwell, return) within 20 seconds.

### 3.5 Handling ambiguity

The protocol does not ask operators to resolve edge cases. It asks them to record what they see.

- **Slush state:** The surface is hard but liquid escapes from underneath during inversion. This is a **fail**. The sample is not yet frozen.
- **Wall-adhesion masquerade:** A thin shell of ice holds the mass in place while the centre appears liquid or deforms slowly. This is **ambiguous**. Log as "partial rigidity — ambiguous" in the notes field. The sample remains unfrozen until a clear pass is observed at a later test.
- **Flash freeze:** The sample fails at check N and passes cleanly at check N+1. The freezing event timestamp is recorded as the time of check N+1.
- **Uncertain observation** (poor lighting, opaque container, unsure what was seen): Mark the test as **ambiguous**. The sample remains unfrozen until a clear pass is observed.
- **Dropped, broken, or substantially disturbed container:** The run is **invalidated**. Do not submit.

No operator is ever required to force a binary call. The system is designed to collect ambiguity, not suppress it. Ambiguous observations are valid scientific outcomes and remain part of the dataset. They reduce confidence in timing precision but never invalidate participation.

### 3.6 Logging rules

- Record, for each sample:
  - time of each inversion test,
  - the first **pass** time (this is the freezing event timestamp T_Rigid),
  - cumulative time outside the freezer (for disturbance budget tracking),
  - any notes on ambiguous behaviour (e.g. "partial rigidity", "inversion too fast", "disturbance-heavy").
- If uncertainty is high, mark the test as **ambiguous**; the sample remains "not frozen" until a clear pass is observed at a later test.

---

## 4. Minimum Admissible Submission (MAS)

A measurement enters the shared statistical object if, and only if, it meets all of the following conditions. No reputation weight, operator history, or institutional affiliation can override a MAS failure. No reputation weight can exclude a submission that meets MAS.

### 4.1 Required fields

| # | Field | Description |
|---|---|---|
| 1 | **Paired design** | Two samples measured under the same environment, differing only in initial water treatment. The intended difference is recorded (e.g. "hot tap vs cold tap", "pre-boiled vs unboiled"). |
| 2 | **Binary event timestamps** | T_Rigid for each sample, determined exclusively by the v1.0 inversion protocol. No alternative freezing definition is used. |
| 3 | **Container class and material** | Selected from the approved list (e.g. "plastic cup — polypropylene", "glass beaker — borosilicate"). Free-text description accepted where the list does not cover the vessel used. |
| 4 | **Fill-level band** | Selected from the specified bands. |
| 5 | **Environment tag** | Category selected from the published list (household-freezer / Baumhaus / lab-freezer / outdoor / other). |
| 6 | **Start time** | Timestamp when samples entered the freezing environment. |
| 7 | **Test interval** | The interval between inversion checks (e.g. "5 min"). |
| 8 | **Operator pseudonym** | A persistent pseudonymous identifier tied to an account. |
| 9 | **Operator class** | Self-declared: child / student / teacher / independent / lab-operator. |
| 10 | **Protocol version** | The version identifier of this protocol (epoch marker). |
| 11 | **Operator declaration** | Confirmation that the published protocol was followed, and that any deviations are recorded in the notes field. |

**Tolerance note:** Small uncontrolled variations between samples (slight fill-level differences, minor position offsets in the freezer, container pre-temperature) are expected in non-laboratory settings and do not invalidate a run unless deliberately introduced. MAS concerns intentional experimental design, not perfect environmental control. Later reviewers may not reject data on the basis of incidental variation.

### 4.2 Derived field

| Field | Description |
|---|---|
| **Δt** | The time difference T_Rigid(Hot) − T_Rigid(Cold). Positive values indicate the hot sample froze later. This is the primary observable for Mpemba comparison. |

### 4.3 Optional extensions (do not affect admissibility)

- Surface-closure timestamp
- Temperature readings or continuous thermal traces
- Photograph or short video of the inverted vessel at T_Rigid
- Image-analysis outputs
- Ambient temperature and humidity readings
- Any additional instrumented data

These enrich higher-tier analyses but are never required for Tier 1b entry.

---

## 5. Tier separation

### Tier 1b — Admissibility

A measurement either meets MAS and enters the map, or it does not. The gate is binary and public. The criteria are listed in Section 4 and nowhere else.

### Tier 2 — Reputation and weighting

Operator reliability history and apparatus calibration records may influence:

- the uncertainty envelope assigned to a measurement in statistical analyses,
- the weighting of entries in aggregate computations,
- the confidence intervals displayed on the public map.

Tier 2 may **never**:

- flip a binary outcome recorded at Tier 1b,
- exclude an MAS-compliant submission from the dataset,
- redefine what counts as an admissible measurement,
- assign zero statistical influence to any resolution class in public aggregates. Weighting may scale uncertainty but cannot eliminate a class entirely.

The boundary between admissibility and reputation is architectural, not negotiable.

---

## 6. Data protection and child participation

### 6.1 Principle: method-only visibility

The measurement system collects methods and outcomes. It does not collect personal identities.

### 6.2 Pseudonymous participation

All data is associated with a persistent Guild Pseudonym. No real names, contact details, email addresses, or dates of birth are stored alongside measurement data.

### 6.3 Proxy-operator model for minors

Participants under 16 do not hold accounts directly. A supervising adult — parent, guardian, or teacher — acts as **Fleet Coordinator**:

- The Fleet Coordinator holds the pseudonymous account and is the data subject under GDPR.
- The child conducts the experiment and is the experimenter.
- The Fleet Coordinator reviews the submission for protocol adherence before it is pushed to the public map.
- Age information is recorded only in coarse bands (under 10 / 10–14 / 15–17) for pedagogical analysis. No exact ages or dates of birth are collected.

This model preserves the "kindergarten to precision laboratory" span without requiring per-child data-processing consent.

### 6.4 Media policy

Uploaded photographs or videos must focus exclusively on the vessel and its contents. Any media containing faces, legible names, or identifying background information is disqualified and purged from the Reality Layer. Operators are instructed on this requirement before their first submission.

### 6.5 Retention separation

Persistent pseudonyms combined with precise timestamps and location data can, over many submissions, re-identify a household (GDPR "singling-out" risk). To mitigate this:

- **Public datasets** store coarse time (date only, no hour/minute) and region (city or district level) only.
- **Exact timestamps and fine-grained location** remain in protected research storage, accessible only to authorised analysts under data-processing agreements, and are not publicly released.
- Anonymisation for long-term statistical archives must be verified against re-identification risk before publication.

### 6.6 Data storage and rights

All data processing is carried out under EU data protection law (GDPR) on the basis of explicit consent from account holders and the project's legitimate interest in scientific research and science education. Data are stored on servers located within the EU with appropriate technical and organisational safeguards, retained only as long as necessary for the stated research and educational purposes, and may be anonymised for long-term statistical use. Account holders retain their rights of access, rectification, objection, and erasure. Contact information for exercising these rights is provided on the project website and at every participating institution.

---

## 7. Feedback language

All system responses to operators must comply with the no-confirmation principle. The system reports map status, not truth status.

**Permitted:**
- "Measurement received and logged."
- "Your submission has been added to the map."
- "Submission flagged for review — ambiguity noted in your log."

**Not permitted:**
- "Your data confirms…"
- "Your result supports the hypothesis."
- "This is consistent with the Mpemba effect."

The map updates. The map does not conclude.

### Public communication rule

This principle extends beyond the submission interface to all public summaries, press materials, and educational documents produced by or on behalf of the institute. Public summaries must describe distributions (e.g. "regions where earlier freezing of the initially hotter sample is more frequent") and must not state the existence or non-existence of the Mpemba effect as a binary fact. The institute maps a phenomenon; it does not adjudicate it.

---

## 8. Governance and versioning

This protocol is the mandatory gatekeeper for universal data integration during Phase 1 (Club) and Phase 2 (Guild) operations.

Parameters marked as provisional (dwell time, fill-level bands, waiting periods, test intervals) are subject to revision after first-campaign data is reviewed by the council. Any parameter change triggers a new protocol version identifier, and all subsequent submissions must reference the updated version.

Surface Closure remains a valuable high-resolution extension for laboratories using optical or IR thermography. It is encouraged as an auxiliary observable wherever feasible. It does not replace Inversion Rigidity as the binary gate.

Future anchor phenomena may be introduced once the protocol framework demonstrates maturity. The maturity criterion will be defined and published before any anchor transition is initiated.

---

*Document prepared under Council-3 ADM-EC deliberation. Guardian, Architect, and Integrator stances consulted. All rulings logged.*
