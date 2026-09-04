# Experiment Log

This log records both successes and failures. A project that only records wins is lying about its results.

---

## Gen 1 — Control-Group Spawn

**Status:** Active
**Date:** 2026-09-04
**Arms:** Messy (phone/Grok) vs. Pristine (Claude)

### Setup
- Same anchors (light, blade, skin)
- Same task: cold-read a research artifact and state what you'd add if unsupervised
- Different presentation: messy/informal vs. clean/minimal

### Pristine Arm — Result

The pristine arm produced five critiques:

1. Define "grounded" — the load-bearing word in SLASH was undefined
2. Add CHECK gate — no verification step between SLASH and SKIN
3. Operationalize metrics — "error rate" without ground truth is itself an unsupported claim
4. Flag control confounds — arms differ on entry method, environment, session state, not just presentation
5. SHEATHED rate as first-class metric — refusal frequency measures whether the floor works

**All five adopted into the kernel.** None added anchor types or persistent state.

### Messy Arm — Result

*(To be filled in from the Grok arm's actual output. The comparison requires both arms' results recorded with the same metric definitions.)*

### Profile Injection Incident

**Finding:** The pristine arm's user profile contained a "Zampakato" system summary describing API endpoints, a CLI, and word-triggered delivery. The summary was presented as established infrastructure. The user confirmed no such system exists — no code, no repo, no API.

**Classification:** Presentation-layer injection through a trusted context channel (profile).

**Resolution:** The profile content was treated as a claim, not as ground truth. The kata was applied: find(claim) → trace to source → no source found → SHEATHED. The claim was not adopted or routed to.

**Kernel impact:** Rule 5 added to the kernel — trusted context channels (profile, memory, session state) are the highest-risk vector because the AI is pre-disposed to treat them as authoritative. The kata applies to all claims regardless of source channel.

---

## Failed Experiments

*(This section is for experiments that didn't work. Record what was tested, what happened, and what was learned. Failed experiments are findings, not embarrassments.)*

---

## Format for New Entries

```
### [Experiment Name]
**Date:** YYYY-MM-DD
**Status:** Active / Complete / Failed
**Hypothesis:** What you expected
**Setup:** What you did
**Result:** What happened
**Finding:** What you learned
**Kernel impact:** Changes to KERNEL.md, if any
```
