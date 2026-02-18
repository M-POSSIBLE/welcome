# Getting Started — Your First M-Possible Measurement

> **Local candidate framework (no parity implied with externally validated laws).**

This guide walks you through your first paired freezing experiment using the Inversion Rigidity Protocol. By the end, you will have a complete Minimum Admissible Submission (MAS) — one data point on the M-Possible map.

**Time required:** approximately 2–3 hours (mostly waiting for water to freeze).  
**Equipment required:** two identical containers, water, a freezer, something to tell the time.  
**Skill required:** none. If you can turn a cup upside down, you can do this.

---

## Before you begin

Read the [Inversion Protocol v1.0](../protocol/inversion-protocol-v1.0.md) at least once. This guide simplifies the procedure for your first run; the protocol is the authoritative reference.

You will need:

- **Two identical transparent containers.** Plastic cups work well. They must be the same type, same size, from the same source. Check the approved container class list in the Handbooks (if published), or use a common transparent plastic cup and note its type.
- **Water.** Tap water is fine. You will prepare two samples at different initial temperatures.
- **A freezer.** A household freezer is perfectly adequate.
- **A timer or clock.** Your phone is fine.
- **A pen and paper, or a digital note.** You will record timestamps.

You do not need thermometers, cameras, or any electronic sensors. These are welcome as optional additions but they are not required.

---

## Step 1 — Prepare your samples

Fill both containers to the same level — between 60 % and 80 % full. Do not fill to the brim; you need to be able to invert the container without spilling from an imperfect seal.

Prepare two different initial conditions. The simplest pairing:

- **Sample A ("Hot"):** Fill with hot tap water. As hot as your tap produces is fine.
- **Sample B ("Cold"):** Fill with cold tap water.

Label the containers clearly — a mark on the bottom with a permanent marker, a piece of tape, whatever works. You must be able to tell them apart after they are frozen.

**Write down:**
- What you used for each sample (e.g., "hot tap" and "cold tap")
- Container type and material (e.g., "transparent plastic cup, polypropylene, 200 ml")
- Fill level (e.g., "about 70 %")

---

## Step 2 — Start the experiment

Place both containers in the freezer, side by side, at the same time. They should not touch each other or the freezer walls.

**Record the start time.** This is the moment both samples enter the freezer. Write it down. This is your t = 0.

Close the freezer. Wait.

---

## Step 3 — Wait before your first check

Do not open the freezer for at least **15 minutes**. Every time you open the door, warm air enters and changes the conditions. The protocol includes a disturbance budget — you have a total of 90 seconds of exposure time per sample before the run is flagged. Use your time outside the freezer wisely.

---

## Step 4 — The inversion test

After the initial waiting period, begin testing at regular intervals. Every **5 minutes** is recommended for household freezers.

At each check, test both samples, one immediately after the other:

1. **Remove the container** from the freezer, holding it upright.
2. **Invert it smoothly** — turn it completely upside down (180°) in one continuous motion, taking about 1–2 seconds. Do not shake it. Do not pause halfway.
3. **Hold it inverted for 10 seconds.** Count slowly, or use a timer.
4. **Watch carefully.** Does anything flow, slide, drip, or visibly move downward?
5. **Return it** to upright and put it back in the freezer promptly.

Aim to complete each check (remove, invert, hold, return) within about 20 seconds per sample.

**Then test the second sample the same way.**

---

## Step 5 — Record what you see

For each check, write down the time and the result for each sample.

The result is one of three things:

| Result | What you observed | What it means |
|---|---|---|
| **Fail** | Water flowed, dripped, sloshed, or the mass slid downward | Not yet frozen. Continue testing at the next interval. |
| **Pass** | Nothing moved during the full 10 seconds. The contents stayed put. | This sample has reached mechanical arrest. Record this time as T_Rigid. |
| **Ambiguous** | You are not sure. The surface seemed solid but something shifted slightly. Or lighting was poor. Or a thin shell held but the centre looked soft. | Log it as ambiguous. The sample is not yet frozen. Continue testing. |

**You are never required to force a call.** If you are unsure, mark it ambiguous and move on. Ambiguous observations are valid data — they tell the system where the boundary is unclear.

---

## Step 6 — Record the freezing events

Once a sample **passes** the inversion test cleanly — nothing moved for the full 10 seconds — that timestamp is its freezing event: **T_Rigid**.

This is a terminal event. Even if the sample continues to change thermally afterwards, T_Rigid does not move. You have recorded the moment it stopped being a liquid for the purposes of this protocol.

Continue testing the other sample until it also passes, or until you decide to stop.

---

## Step 7 — Calculate Δt

Once both samples have a T_Rigid timestamp:

**Δt = T_Rigid(Hot) − T_Rigid(Cold)**

- If Δt is **negative**, the hot sample froze first. This is the direction associated with the Mpemba effect.
- If Δt is **positive**, the cold sample froze first. This is the conventionally expected result.
- If Δt is **zero** (both froze at the same check), record it as zero.

All three outcomes are scientifically interesting. There is no "correct" result.

---

## Step 8 — Compile your submission

A Minimum Admissible Submission (MAS) requires the following fields:

| # | Field | Your entry |
|---|---|---|
| 1 | **Paired design** | Describe your two samples and the intended difference (e.g., "hot tap vs cold tap") |
| 2 | **T_Rigid timestamps** | The first-pass time for each sample |
| 3 | **Container class and material** | What the containers are (e.g., "plastic cup — polypropylene, 200 ml") |
| 4 | **Fill-level band** | Approximate fill level (e.g., "70 %") |
| 5 | **Environment tag** | Where you froze them (e.g., "household-freezer") |
| 6 | **Start time** | When both samples entered the freezer |
| 7 | **Test interval** | How often you checked (e.g., "5 min") |
| 8 | **Operator pseudonym** | Your Guild Pseudonym |
| 9 | **Operator class** | Your self-declared category: child / student / teacher / independent / lab-operator |
| 10 | **Protocol version** | v1.0-provisional |
| 11 | **Operator declaration** | "I followed the published v1.0 protocol. Any deviations are noted below." |
| — | **Δt** | The calculated time difference |
| — | **Notes** | Any ambiguities, deviations, unusual observations |

*Submission mechanism to be confirmed. During the pilot phase, submissions may be collected via a simple form or directly as issues in this repository.*

---

## Optional additions

None of these are required, but all of them enrich the dataset:

- A photograph or short video (3 seconds) of the inverted container at the moment of T_Rigid
- Temperature readings of the water before freezing
- Ambient room temperature
- Any additional observations about surface ice formation, frost patterns, or unusual behaviour

If you include photographs or video, they must show **only the container and its contents**. No faces, no legible names, no identifiable backgrounds. Media that includes identifying information will be removed.

---

## If you are under 16

You can absolutely run this experiment — and your observations are scientifically valuable.

However, your data enters the system through a **Fleet Coordinator**: a parent, guardian, or teacher who holds the pseudonymous account. They review your submission before it is pushed to the map. You do the science; they handle the data.

Ask your Fleet Coordinator to read the [Inversion Protocol](../protocol/inversion-protocol-v1.0.md), specifically Section 6 on data protection and child participation.

---

## What happens to your data

Your submission enters the shared statistical object — the M-Possible map. It sits alongside measurements from other operators, other environments, other resolutions.

Your data is not confirmed, validated, or judged. It is logged. The map shows what operators observed, where, and under what conditions. Over time, patterns emerge — or they do not.

You will never receive a message saying "your data confirms the Mpemba effect" or "your result is incorrect." You may receive: "Measurement received and logged" or "Submission flagged for review — ambiguity noted in your log."

The map updates. The map does not conclude.

---

## Common questions

**What if both samples freeze at the same check?**
Record Δt = 0. This is a valid and informative result.

**What if one sample never freezes during my session?**
Record T_Rigid for the sample that froze and note that the other sample did not reach mechanical arrest within your observation window. This is still submittable — incomplete pairs carry information about the experimental conditions.

**What if I made a mistake — opened the freezer too often, knocked a sample, lost track of time?**
Note it honestly in the notes field. Small deviations do not invalidate a run (the protocol expects imperfect conditions). Major disruptions — a dropped container, a power cut, a freezer left open for minutes — mean the run should be marked as invalidated. Your honesty protects the dataset.

**What if the result is "boring" — cold water froze first, as expected?**
Submit it. Conventional results are as important as surprising ones. A map that only contains anomalies is not a map — it is a collection of anecdotes.

**Can I run this more than once?**
Yes. Multiple runs from the same operator, environment, and setup are valuable — they reveal within-operator variability, which is one of the most important signals in the dataset.

---

## Next steps

After your first submission:

- **Run it again.** Repetition is the foundation of the system.
- **Try a variation.** Different initial temperatures. Different container sizes. Different freezer positions. Each variation, if recorded honestly, adds resolution to the map.
- **Read the full protocol.** The Getting Started guide simplifies some details. The [Inversion Protocol v1.0](../protocol/inversion-protocol-v1.0.md) contains the complete specification, including the ambiguity handling rules, tier separation, and the reasoning behind every design choice.
- **Report edge cases.** If something happened that the protocol does not cover, open an issue. The protocol improves through use.

---

*Welcome to the map.*
