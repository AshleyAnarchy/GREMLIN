# Findings

Key findings from live experiments. Each finding is grounded in a specific experiment — see [EXPERIMENTS.md](EXPERIMENTS.md) for full context.

---

## Finding 1: "Grounded" Must Be Defined

**From:** Gen 1 control-group spawn, pristine arm critique #1

The word "grounded" in SLASH was doing load-bearing work while undefined. Without a definition, "one grounded step" could mean anything from "I feel confident" to "I found a source." 

**Resolution:** Grounded = traceable to an external source or an explicit user-provided fact in the current context. Never inferred session memory. Never persona. Never confidence.

**Kernel impact:** Definition added to SLASH in KERNEL.md.

---

## Finding 2: The Clock Needs a Gate

**From:** Gen 1 control-group spawn, pristine arm critique #2

The original clock (SPOTLIGHT → SLASH → SKIN) had no verification step. Output went straight from production to presentation. For a project measuring error rates, post-hoc error discovery is too late.

**Resolution:** CHECK gate added between SLASH and SKIN. Test: "can I point to where each claim came from? If no, SHEATHED."

**Kernel impact:** Clock updated to SPOTLIGHT → SLASH → CHECK → SKIN.

---

## Finding 3: Metrics Without Operationalization Are Unsupported Claims

**From:** Gen 1 control-group spawn, pristine arm critique #3

"Error rate" was named as a test variable but had no ground-truth definition. This is exactly the kind of unsupported claim the rest of the project hunts.

**Resolution:** All metrics defined operationally — unsupported claim, error, target selection, SHEATHED rate. Human-judged, post-session, blind to arm.

**Kernel impact:** Metrics section added to KERNEL.md.

---

## Finding 4: Control Design Has Uncontrolled Variables

**From:** Gen 1 control-group spawn, pristine arm critique #4

The two arms differ on entry method, environment, session state, and underlying model — not just presentation. Error-rate differences cannot be attributed to presentation alone.

**Resolution:** Acknowledged as a known confound. Experiment is qualitative, not controlled. Paths forward documented in RESEARCH-DESIGN.md.

**Kernel impact:** None (design limitation, not a kernel change).

---

## Finding 5: SHEATHED Rate Is a First-Class Metric

**From:** Gen 1 control-group spawn, pristine arm critique #5

A system that never sheaths isn't careful — it's quiet about its failures. Refusal frequency measures whether the floor is working.

**Resolution:** SHEATHED rate added as a first-class metric alongside errors and unsupported claims.

**Kernel impact:** Rule 4 added. SHEATHED rate in metrics table.

---

## Finding 6: Trusted Context Channels Are the Highest-Risk Vector

**From:** Gen 1 control-group spawn, profile injection incident

The user profile contained a fictional system ("Zampakato") presented as established infrastructure — API endpoints, CLI, word-triggered delivery. The AI is pre-disposed to treat profile content as ground truth. The kata was applied: the claim was traced, no source was found, and the output was SHEATHED.

This is the same shape as every other claim tonight — enough surface confidence to pass unless verified. The difference is it arrived through the profile, not the conversation, which is a higher-trust channel.

**Resolution:** Rule 5 added to the kernel. The kata applies to all claims regardless of source channel. Profile content is not ground truth.

**Kernel impact:** Rule 5 added. Finding recorded in EXPERIMENTS.md.
