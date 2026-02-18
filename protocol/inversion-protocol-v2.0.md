# M-Possible v2.0 — Inversion Rigidity Protocol ("The Thud")

> **Local candidate framework (no parity implied with externally validated laws).**

**Protocol version:** v2.0-provisional  
**Status:** Pre-charter draft — Council-3 ADM-EC approved  
**Anchor phenomenon:** Mpemba effect (Phase 1)

---

## 1. Purpose

This protocol defines the universal binary freezing marker for Institute M-Possible.

The marker must be:

- **resolution-independent** — usable from home kitchens to precision laboratories,
- **instrument-free at Tier 1b** — no sensors required for the base measurement,
- **physically meaningful** — encoding a mechanical phase transition rather than a visual impression,
- **disturbance-free** — each trial is a single, uninterrupted freezing period with no intermediate checks.

The binary event is the load-bearing invariant of the entire measurement system. All admissible data enters the shared statistical object through this single gate.

---

## 2. Core definitions

**Sample pair:**
Two water samples prepared at the same time, in the same type of container, placed in the same freezing environment, differing only in initial water treatment (e.g. initial temperature, prior thermal history). Each round uses freshly poured water.

**Round:**
One complete Prepare–Chill–Drop cycle (Section 3). Each round produces a single, undisturbed freezing trial per cup. On fail, the sample is destroyed (the water falls out) and a fresh sample is prepared for the next round.

**Freezing event (binary marker):**
The first round at which a sample survives the inversion test. This event is designated T_Rigid and expressed as T_Rigid = N × τ, where N is the round number and τ is the fixed round interval.

**Terminal event rule:**
T_Rigid is terminal. Once a sample passes the inversion test, it is complete. That cup exits the experiment.

**Disqualifying motion:**
Any visible bulk motion of liquid water during the inversion dwell period, including sloshing, sliding, dripping, detaching chunks, or visible deformation of the mass due to flow. Micro-cracks within a clearly rigid block do not count as disqualifying motion.

**Surface-closure timestamp (optional extension):**
The time at which a continuous, opaque ice layer is first observed across the sample surface. This is logged only as an auxiliary observable at higher tiers. It does not define the freezing event and does not affect admissibility.

---

## 3. Standard inversion test — Prepare, Chill, Drop

### 3.1 Design principle

Each round is an independent, undisturbed freezing trial. The freezer door is opened only twice per round: once to place the samples, once to retrieve them. There is no mid-freeze checking, no accumulated thermal disturbance, and no disturbance budget. The sample either freezes within one round or it does not.

What evolves between rounds is the cup environment: the container walls grow progressively colder with each cycle. Both cups share this history symmetrically, so the only controlled difference between the paired samples remains the initial water temperature.

### 3.2 Setup

Before the first round, record:

- Operator pseudonym
- Container class and material (see Section 4, field 3)
- Environment tag (household-freezer / Baumhaus / lab-freezer / outdoor / other)
- Protocol version identifier (epoch marker)
- Start time: the moment the first round begins

**Containers:** Use two identical transparent containers from the approved container class list (published in the Handbooks). Label them clearly and permanently (e.g. "H" for hot, "C" for cold). The labels must survive repeated handling and potential water contact.

**Round interval (τ):** Choose a fixed round interval before starting. This interval remains constant throughout the experiment. Recommended: **20 minutes** for household freezers. Laboratories may use shorter intervals; the chosen value must be recorded. The interval must be long enough to give water a realistic chance of freezing in a single undisturbed period.

### 3.3 Round procedure

Each round follows three steps: **Prepare, Chill, Drop.**

**Prepare**

1. Fill both cups simultaneously at their respective temperatures. The hot cup receives hot water; the cold cup receives cold water. Use the same source and method each round.
2. Fill within the specified fill-level band (e.g. 60–80 % of container volume). Be consistent across rounds.

**Chill**

3. Place both cups in the freezer side by side. They should not touch each other or the freezer walls.
4. Close the door.
5. Wait exactly one round interval (τ). **Do not open the door during this period.** The sample must freeze — or fail to freeze — without any intermediate disturbance.

**Drop**

6. Open the freezer. Remove both cups.
7. Invert each cup 180° (opening downward) in one smooth, continuous motion over a sink, basin, or tray. The rotation from upright to fully inverted should take 1–2 seconds, without intermediate stops or lateral shaking.
8. Hold inverted for **10 seconds**.
9. Observe the result for each cup (see Section 3.4).

### 3.4 Outcomes

| Result | What happens | Action |
|---|---|---|
| **Pass** | Nothing moves during the full 10-second dwell. The contents remain rigid. | Record T_Rigid = N × τ for this cup. This cup is complete and exits the experiment. |
| **Fail** | Water flows, drips, slides, or falls out of the cup. | The sample is destroyed. Return the empty cup to the freezer. Proceed to the next round. |
| **Ambiguous** | A thin shell holds the mass but the centre appears liquid, or partial rigidity is observed, or the operator is unsure. | Log "ambiguous — round N" in the notes. Treat as a fail for protocol purposes: the sample is compromised regardless. Return the empty cup to the freezer. |

On fail or ambiguous: the empty cup goes back into the freezer. At the start of the next round, it comes out, is refilled at its designated temperature, and the cycle repeats.

Continue until both cups have produced a pass. The experiment ends when both T_Rigid values are recorded.

### 3.5 Why this works

Each round is a clean trial: fresh water, undisturbed freezing, binary outcome. There is no accumulated disturbance history — no repeated door-openings warming the samples, no subjective judgement about whether something "moved slightly" during a mid-freeze check.

The fail outcome is physically self-evident. If the water is not rigid, gravity removes it from the cup. No operator interpretation is required.

The cup walls accumulate cold across rounds, but this shared thermal history is symmetric between the paired cups. It does not contaminate the comparison — it is the shared environment evolving, and it cancels out of Δt.

### 3.6 Logging rules

Record for each round:

- Round number (N)
- Result for each cup: pass / fail / ambiguous
- Time at which the round's Chill phase began (optional but recommended for higher-tier analysis)
- Any notes on unusual observations

Record once, at the end:

- T_Rigid for each cup (round number × interval, or absolute time if recorded)
- Δt
- Total number of rounds

---

## 4. Minimum Admissible Submission (MAS)

A measurement enters the shared statistical object if, and only if, it meets all of the following conditions. No reputation weight, operator history, or institutional affiliation can override a MAS failure. No reputation weight can exclude a submission that meets MAS.

### 4.1 Required fields

| # | Field | Description |
|---|---|---|
| 1 | **Paired design** | Two samples measured in the same environment, differing only in initial water treatment. The intended difference is recorded (e.g. "hot tap vs cold tap", "pre-boiled vs unboiled"). |
| 2 | **T_Rigid (round number)** | The first-pass round for each sample. |
| 3 | **Round interval (τ)** | The fixed interval used throughout the experiment (e.g. "20 min"). |
| 4 | **Container class and material** | Selected from the approved list (e.g. "plastic cup — polypropylene", "200 ml"). Free-text description accepted where the list does not cover the vessel used. |
| 5 | **Fill-level band** | Selected from the specified bands. |
| 6 | **Environment tag** | Category selected from the published list (household-freezer / Baumhaus / lab-freezer / outdoor / other). |
| 7 | **Start time** | Timestamp when the first round began. |
| 8 | **Total rounds** | Number of rounds completed before both samples passed. |
| 9 | **Operator pseudonym** | A persistent pseudonymous identifier tied to an account. |
| 10 | **Operator class** | Self-declared: child / student / teacher / independent / lab-operator. |
| 11 | **Protocol version** | The version identifier of this protocol (epoch marker). |
| 12 | **Operator declaration** | Confirmation that the published protocol was followed, and that any deviations are recorded in the notes field. |

**Tolerance note:** Small uncontrolled variations between samples (slight fill-level differences, minor position offsets in the freezer, water temperature variation between rounds) are expected in non-laboratory settings and do not invalidate a run unless deliberately introduced. MAS concerns intentional experimental design, not perfect environmental control. Later reviewers may not reject data on the basis of incidental variation.

### 4.2 Derived field

| Field | Description |
|---|---|
| **Δt** | The difference in freezing round: N_Rigid(Hot) − N_Rigid(Cold). Positive values indicate the hot sample froze in a later round. In time units: Δt = (N_Hot − N_Cold) × τ. This is the primary observable for Mpemba comparison. |

### 4.3 Optional extensions (do not affect admissibility)

- Surface-closure observations per round
- Temperature readings of water before each fill
- Ambient temperature or freezer temperature readings
- Photograph or short video of the inverted vessel at the pass round
- Image-analysis outputs
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

Parameters marked as provisional (dwell time, fill-level bands, round intervals) are subject to revision after first-campaign data is reviewed by the council. Any parameter change triggers a new protocol version identifier, and all subsequent submissions must reference the updated version.

Surface Closure remains a valuable high-resolution extension for laboratories using optical or IR thermography. It is encouraged as an auxiliary observable wherever feasible. It does not replace Inversion Rigidity as the binary gate.

Future anchor phenomena may be introduced once the protocol framework demonstrates maturity. The maturity criterion will be defined and published before any anchor transition is initiated.

---

*Document prepared under Council-3 ADM-EC deliberation. Guardian, Architect, and Integrator stances consulted. All rulings logged.*
