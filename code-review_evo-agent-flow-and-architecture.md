# Code Review: EVO Agent Flow and Architecture

**Repository:** github.com/machinelearning2014/evo-ai
**Date:** June 20, 2026
**Reviewer:** EVO (self-review)

---

## Overview

This document captures the code review and architectural analysis of the EVO AI repository. The review covered:

1. **EvoAgent end-to-end flow** for all six tiers (LITE, COMPUTE, MATHS, CODE, REASON, PROVE)
2. **System architecture** — the orchestration layer, tool registry, memory system, and Prolog/Lean integration
3. **Groundedness auditing** — the verification system that ensures every conclusion has tool-grounded evidence

---

## EvoAgent Flow by Tier

### LITE Tier (Fact Lookup / Simple Computation)

```
Entry → Tier Router determines LITE
  → Internal knowledge check (preferred)
  → web_search / python_exec fallback
  → Mini-KB validation (Prolog: observations → supports → conclusion → assumptions)
  → Consistency check
  → Answer with sources, assumptions, limitations
```

**Key files:** `l2_triage.py` (routing), `base_agent_iterator.py` (execution loop)

### COMPUTE Tier (Numerical / Symbolic Computation)

```
Entry → Tier Router determines COMPUTE
  → Prolog SETUP (problem_spec, spec_requirements)
  → python_exec / sympy_exec computation
  → Verification claims (computation_check, verified_value)
  → Spec requirement fulfillment check
  → Answer with computation summary
```

**Key files:** `c2_compute.py`, `c3_validate.py`

### MATHS Tier (Mathematical Derivation / Proof)

```
Entry → Tier Router determines MATHS
  → maths_problem stage=start (problem, target, complexity)
  → maths_problem stage=model (definitions, variables, constraints)
  → maths_problem stage=explore (optional python/SymPy exploration)
  → maths_problem stage=derive (claims, lemmas, case splits, evidence)
  → maths_problem stage=verify_step / verify_final
  → Answer with mathematical argument
```

**Key files:** `m1_model.py`, `m2_explore.py`, `m3_derive.py`, `m4_verify.py`, `maths_problem.py` (stage controller)

### CODE Tier (Source / Repository / Security)

```
Entry → Tier Router determines CODE
  → git clone + inspection (log, grep, show, status)
  → GitHub API reads (list_dir, read_file)
  → Prolog fact mapping (source_file, calls, imports, config_sets)
  → Reasoning ledger (observations → hypotheses → support/contradiction)
  → Optional verification (test/build)
  → Answer with code evidence and reasoning ledger
```

**Key files:** `k1_inspect.py`, `k2_analyze.py`, `k4_verify.py`

### REASON Tier (Logical Reasoning)

```
Entry → Tier Router determines REASON
  → Prolog SETUP (R1): observations, rules, assumptions, harness (prove/2, inconsistent/0)
  → Prolog DERIVE (R2): setof(Answer-Proof, prove/2, Results)
  → Prolog CONSISTENCY (R3): query inconsistent/0
  → Assumption-DEPENDENCE TEST (R4): retract/reassert each assumption
  → CAPABILITY LOOP (if need_capability/2 emitted)
  → VALIDATE (R5): spec_requirement fulfillment
  → Answer with derivation, classification, validation
```

**Key files:** `r1_setup.py`, `r2_derive.py`, `r3_consistency.py`, `r4_dependence.py`, `r5_validate.py`

### PROVE Tier (Formal Proof)

```
Entry → Tier Router determines PROVE
  → ProveProblem stage=start
  → Prolog SETUP (theorem_statement, proof_strategy)
  → python_exec EXPLORE (pattern discovery)
  → BUILD & VERIFY (parallel):
      → lean4_builder (auto proof building)
      → deepseek_prover (proof strategy)
      → bfs_prover (tactic-level generation)
      → Manual loop (lean4_probe → fix → close → probe)
  → ProveProblem stage=prove_ready
  → lean4_exec final verification
  → ProveProblem stage=verify_final
  → MATHS fallback if formal verification infeasible
  → Answer with formal proof (or mathematical fallback)
```

**Key files:** `p2_explore.py`, `p3_build.py`, `p4_verify.py`, `prove_problem.py` (stage controller)

---

## System Architecture (Key Files)

| File | Size | Purpose |
|------|------|---------|
| `evo_agent.py` | 289KB / 6424 lines | Central orchestration hub — WebSocket server, tool dispatch, tier routing, LLM integration |
| `base_agent_iterator.py` | 143KB | Execution loop, tool invocation, message dispatch |
| `l2_triage.py` | 37KB | Tier classification based on user intent |
| `r1_setup.py` | 12KB | Prolog KB construction for REASON tier |
| `r4_dependence.py` | 12KB | Assumption-dependence testing |
| `m4_verify.py` | 16KB | MATHS verification finalization |
| `p3_build.py` | 29KB | PROVE build loop with Lean integration |
| `maths_problem.py` | 16KB | MATHS stage controller |
| `prove_problem.py` | 14KB | PROVE stage controller |
| `groundedness.py` | 38KB | Audit system — verifies every claim has tool-grounded evidence |

---

## Key Architectural Insights

1. **Orchestration is the architecture** — The system is not a monolithic agent but a disciplined orchestration engine that routes to specialized sub-systems (Prolog, Lean, Python) with explicit state management.

2. **Assumption tracking is first-class** — Every tier represents assumptions explicitly. The REASON tier tests conclusion robustness by retracting each assumption. This is unique.

3. **Groundedness auditing** — The `groundedness.py` system (38KB) enforces that every conclusion in the final answer corresponds to a tool output. Claims without evidence are flagged and suppressed.

4. **Stage controllers** — `maths_problem.py` and `prove_problem.py` act as finite state machines that gate the SOLVED status until required evidence is recorded. This prevents premature conclusions.

5. **Parallel specialist architecture** — The PROVE tier launches `lean4_builder`, `deepseek_prover`, and `bfs_prover` in background while the main thread continues manual proof work. Notifications are handled as synthetic messages.

---

## Observations

- The system is genuinely self-referential — it is an AI agent whose position paper argues that system-level orchestration IS intelligence
- The codebase is large (289KB core file) and would benefit from modularization
- The design philosophy of "explicit assumptions" and "groundedness auditing" is consistent throughout
- The Lean integration for formal proof is the most sophisticated component
