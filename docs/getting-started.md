# Getting Started — Your First M-Possible Measurement

> **Local candidate framework (no parity implied with externally validated laws).**

This guide walks you through your first paired freezing experiment using the Inversion Rigidity Protocol. By the end, you will have a complete Minimum Admissible Submission (MAS) — one data point on the M-Possible map.

**Time required:** approximately 2–4 hours (mostly waiting between rounds).  
**Equipment required:** two identical cups, water, a freezer, a sink or basin, something to tell the time.  
**Skill required:** none. If you can fill a cup and turn it upside down, you can do this.

---

## Before you begin

Read the [Inversion Protocol v2.0](../protocol/inversion-protocol-v2.0.md) at least once. This guide simplifies the procedure for your first run; the protocol is the authoritative reference.

You will need:

- **Two identical transparent cups.** Plastic cups work well. They must be the same type, same size, from the same source. Note the type and material.
- **Water.** Tap water is fine. You will prepare a hot sample and a cold sample.
- **A freezer.** A household freezer is perfectly adequate.
- **A sink, basin, or tray.** When the test fails, the water comes out. You need somewhere for it to go.
- **A timer or clock.** Your phone is fine.
- **A pen and paper, or a digital note.** You will record round results.

You do not need thermometers, cameras, or any electronic sensors. These are welcome as optional additions but they are not required.

---

## The core idea

The experiment works in rounds. Each round follows three steps: **Prepare, Chill, Drop.**

- **Prepare** — fill both cups with fresh water at their designated temperatures.
- **Chill** — place both in the freezer for one fixed interval. Door stays closed.
- **Drop** — remove both cups, turn each upside down. Either the water stays (pass) or it falls out (fail).

On fail, the cup is empty. You refill it and go again. On pass, that cup is done.

Each round is a clean, independent trial. No mid-freeze checking, no opening the freezer door to peek, no accumulated disturbance. The water either froze in that round or it didn't — and gravity makes the answer obvious.

---

## Step 1 — Set up

Label your two cups clearly — "H" for hot, "C" for cold. The labels must survive getting wet.

Choose your round interval before you start. This is the time each round spends in the freezer. **20 minutes** is recommended for household freezers. Write it down. It stays the same for every round.

**Write down before you begin:**
- Container type and material (e.g., "transparent plastic cup, polypropylene, 200 ml")
- Round interval (e.g., "20 min")
- Environment tag (e.g., "household-freezer")
- Your operator pseudonym

---

## Step 2 — Round 1

**Prepare.** Fill cup H with hot tap water — as hot as your tap produces. Fill cup C with cold tap water. Fill both to the same level, between 60 % and 80 % full.

**Chill.** Place both cups in the freezer, side by side. They should not touch each other or the freezer walls. Close the door. Start your timer. **Do not open the freezer until the interval is up.** No peeking.

**Drop.** When the timer sounds, open the freezer and remove both cups. Take them to the sink. One at a time, turn each cup smoothly upside down — one continuous motion, about 1–2 seconds — and hold it inverted for **10 seconds**.

Watch what happens:

- **Water falls out → Fail.** Not frozen yet. The cup is now empty.
- **Nothing moves for the full 10 seconds → Pass.** This cup has reached mechanical arrest. Record the round number.
- **Not sure — something partially held, or a thin shell broke → Ambiguous.** Log it. Treat as a fail — the sample is compromised either way.

**Write down:** Round 1 — Cup H: fail/pass/ambiguous. Cup C: fail/pass/ambiguous.

---

## Step 3 — Repeat

For any cup that failed or was ambiguous:

1. **Refill it** at its original temperature. Hot cup gets hot water. Cold cup gets cold water. Same source, same method as round 1.
2. **Place both cups back in the freezer** (refilled cups and any cup still waiting for its pair to finish).
3. **Close the door. Wait one interval. Do not open.**
4. **Remove, invert, observe.** Same as before.

If one cup has already passed, it exits the experiment. Continue with the remaining cup: refill, chill, drop, until it also passes.

Record every round's result for both cups.

---

## Step 4 — Record the freezing events

When a cup passes, its freezing event is:

**T_Rigid = round number × round interval**

For example, if your hot cup passes on round 4 with a 20-minute interval: T_Rigid(Hot) = 4 × 20 min = 80 min.

---

## Step 5 — Calculate Δt

Once both cups have a T_Rigid:

**Δt = N_Rigid(Hot) − N_Rigid(Cold)**

This is the difference in rounds, not just time. In time units: Δt = (N_Hot − N_Cold) × τ.

- If Δt is **negative** — the hot cup froze in an earlier round. This is the direction associated with the Mpemba effect.
- If Δt is **positive** — the cold cup froze first. The conventionally expected result.
- If Δt is **zero** — both froze in the same round.

All three outcomes are scientifically interesting. There is no "correct" result.

---

## Step 6 — Compile your submission

A Minimum Admissible Submission (MAS) requires the following:

| # | Field | Your entry |
|---|---|---|
| 1 | **Paired design** | Describe your two samples and the intended difference (e.g., "hot tap vs cold tap") |
| 2 | **T_Rigid (round number)** | The first-pass round for each cup |
| 3 | **Round interval (τ)** | Your fixed interval (e.g., "20 min") |
| 4 | **Container class and material** | What the cups are (e.g., "plastic cup — polypropylene, 200 ml") |
| 5 | **Fill-level band** | Approximate fill level (e.g., "70 %") |
| 6 | **Environment tag** | Where you froze them (e.g., "household-freezer") |
| 7 | **Start time** | When round 1 began |
| 8 | **Total rounds** | How many rounds you completed |
| 9 | **Operator pseudonym** | Your Guild Pseudonym |
| 10 | **Operator class** | Your category: child / student / teacher / independent / lab-operator |
| 11 | **Protocol version** | v2.0-provisional |
| 12 | **Operator declaration** | "I followed the published v2.0 protocol. Any deviations are noted below." |
| — | **Δt** | The difference in rounds (and in time) |
| — | **Notes** | Any ambiguous rounds, deviations, unusual observations |

*Submission mechanism to be confirmed. During the pilot phase, submissions may be collected via a simple form or directly as issues in this repository.*

---

## Optional additions

None of these are required, but all of them enrich the dataset:

- A photograph or short video (3 seconds) of the inverted cup at the pass moment
- Temperature readings of the water before each fill
- Ambient room temperature or freezer temperature
- Observations about ice patterns, frost on cup walls, or other visual details

If you include photographs or video, they must show **only the cup and its contents**. No faces, no legible names, no identifiable backgrounds. Media that includes identifying information will be removed.

---

## If you are under 16

You can absolutely run this experiment — and your observations are scientifically valuable.

However, your data enters the system through a **Fleet Coordinator**: a parent, guardian, or teacher who holds the pseudonymous account. They review your submission before it is pushed to the map. You do the science; they handle the data.

Ask your Fleet Coordinator to read the [Inversion Protocol](../protocol/inversion-protocol-v2.0.md), specifically Section 6 on data protection and child participation.

---

## What happens to your data

Your submission enters the shared statistical object — the M-Possible map. It sits alongside measurements from other operators, other environments, other resolutions.

Your data is not confirmed, validated, or judged. It is logged. The map shows what operators observed, where, and under what conditions. Over time, patterns emerge — or they do not.

You will never receive a message saying "your data confirms the Mpemba effect" or "your result is incorrect." You may receive: "Measurement received and logged" or "Submission flagged for review — ambiguity noted in your log."

The map updates. The map does not conclude.

---

## Common questions

**What if both cups freeze in the same round?**
Record Δt = 0. This is a valid and informative result.

**What if I run out of time before one cup passes?**
Record T_Rigid for the cup that passed and note that the other did not reach mechanical arrest within your observation window. State the last round completed. This is still submittable — incomplete pairs carry information about the experimental conditions.

**What if I accidentally used different water temperatures when refilling?**
Note it honestly. Small variations between rounds are expected and do not invalidate the run. If you consistently used a different temperature from what you intended, note the deviation.

**What if the result is "boring" — cold water froze first, as expected?**
Submit it. Conventional results are as important as surprising ones. A map that only contains anomalies is not a map — it is a collection of anecdotes.

**Why do I refill with fresh water each round instead of putting the same sample back?**
Because each door-opening, each removal and return, disturbs the freezing process. The Prepare–Chill–Drop cycle eliminates this problem entirely: every round is a clean, independent trial with no disturbance history. The cup walls still accumulate cold between rounds — that is the shared environment evolving — but the water in each trial has had exactly one uninterrupted period to freeze.

**Can I run this more than once?**
Yes. Multiple runs from the same operator, environment, and setup are valuable — they reveal within-operator variability, which is one of the most important signals in the dataset.

**Does it matter that the cups get colder over rounds?**
No — for the comparison. Both cups share the same thermal history. Whatever the cup walls are doing, they are doing it together. The only controlled difference is the water temperature at fill. That is what Δt measures.

---

## Next steps

After your first submission:

- **Run it again.** Repetition is the foundation of the system.
- **Try a variation.** Different initial temperatures. Different cup sizes. Different round intervals. Each variation, if recorded honestly, adds resolution to the map.
- **Read the full protocol.** The Getting Started guide simplifies some details. The [Inversion Protocol v2.0](../protocol/inversion-protocol-v2.0.md) contains the complete specification, including the tier separation and the reasoning behind every design choice.
- **Report edge cases.** If something happened that the protocol does not cover, open an issue. The protocol improves through use.

---

*Welcome to the map.*
