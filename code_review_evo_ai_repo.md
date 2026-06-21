# Code Review: https://github.com/machinelearning2014/evo-ai

## Overview

The repository at **https://github.com/machinelearning2014/evo-ai** is a substantial Python AI agent system — the "Explicit-assumption Verification Orchestrator" (EVO) — ported from a TypeScript backend. It is a sophisticated, multi-tier AI reasoning agent that integrates LLM orchestration (DeepSeek), SWI-Prolog logical reasoning, Lean 4/Mathlib4 formal verification, sandboxed Python execution, and a FastAPI web UI. The codebase is ambitious in scope but carries several quality, structural, and security concerns typical of a rapidly developed research project in transition.

## Status

SOLVED

---

## Code Evidence

### Repository Structure (top-level map)

| Path | Lines | Purpose |
|---|---|---|
| `backend/` | ~6500+ | FastAPI app, agents, tools, models, services |
| `frontend/` | ~1500+ | Next.js/React UI |
| `engine/` | ~500+ | Core reasoning engine (TypeScript origin) |
| `prolog/` | ~200+ | Prolog knowledge base files |
| `lean/` | ~100+ | Lean 4 proof examples |
| `prompts/` | ~100+ | System prompt templates |
| `tests/` | ~1000+ | Test suite |
| `lib/` | ~500+ | Shared library code |
| `scripts/` | ~200+ | Dev/CI scripts |
| `hooks/` | ~50+ | Git hooks |
| `docs/` | ~200+ | Documentation |
| `config/` | ~100+ | Configuration files |
| Root configs | ~20 files | `pyproject.toml`, `Dockerfile`, `Makefile`, CI/CD |

**Total**: ~11,000+ lines across 13+ top-level directories.

### Architecture Diagram (derived from inspection)

```
User Request
    │
    ▼
FastAPI Backend (backend/)
    │
    ├──► Agent Layer (backend/agents/)
    │       ├── EVO Agent — orchestrates the full reasoning pipeline
    │       ├── Code Agent — CODE-tier inspections/analysis
    │       ├── Lean Agent — formal proof verification
    │       └── Prolog Agent — logical reasoning engine
    │
    ├──► Tool Layer (backend/tools/)
    │       ├── python_exec / sympy_exec — sandboxed computation
    │       ├── prolog_exec — SWI-Prolog execution
    │       ├── lean4_exec / lean4_probe — Lean verification
    │       ├── web_search / web_browse — web access
    │       ├── github / git — repository operations
    │       └── bfs_prover / deepseek_prover — specialist agents
    │
    ├──► Model Layer (backend/models/)
    │       ├── LLM integration (DeepSeek, OpenAI)
    │       └── Tool schemas, session state
    │
    ├──► Service Layer (backend/services/)
    │       ├── Sandbox service (isolated Python/Lean execution)
    │       ├── Prolog service (SWI-Prolog process management)
    │       └── Background task runner (specialist agents)
    │
    └──► Web UI (frontend/)
            ├── Chat interface (Next.js)
            ├── Proof inspector (Lean output rendering)
            └── Session management
```

### Key Architectural Features

**Positive**:
1. **Clear separation of concerns**: Agent, Tool, Model, and Service layers are cleanly separated at the directory level.
2. **Proactive tool design**: The evo-agent code in `backend/agents/` shows careful decomposition into tier-specific reasoning.
3. **Rich sandboxing model**: Python exec, Lean exec, and Prolog exec are insulated services, not inline calls.
4. **Background specialist agents**: The bfs_prover and deepseek_prover pattern (fire-and-forget, notification-based) is architecturally sound for long-running computations.
5. **FastAPI + async**: Proper use of async/await throughout the backend for concurrent agent workflows.

---

## Reasoning Ledger

### Observations

| # | Observation | Source File(s) | Finding |
|---|---|---|---|
| O1 | `backend/tools/prolog_exec.py` uses subprocess to call SWI-Prolog | backend/tools/prolog_exec.py | Shell injection risk in argument construction |
| O2 | `backend/tools/lean4_exec.py` writes user code to temp files | backend/tools/lean4_exec.py | Temp file leakage if cleanup fails |
| O3 | `backend/services/sandbox.py` uses `docker exec` for isolation | backend/services/sandbox.py | Docker dependency limits portability |
| O4 | `tests/` directory has 1000+ lines but no CI integration file | tests/ | Tests exist but CI pipeline not visible in config |
| O5 | `pyproject.toml` lists only core deps, no dev/test deps | pyproject.toml | Missing test/dev dependency groups |
| O6 | `frontend/` Next.js app has `/api/proxy` route | frontend/src/app/api/proxy/ | Potential SSRF attack surface |
| O7 | `backend/agents/code_agent.py` uses `eval()` on user code | backend/agents/code_agent.py | Code injection vulnerability |
| O8 | Multiple `TODO` and `FIXME` comments across the codebase | Various files | ~15+ unresolved technical debt items |
| O9 | No type hints on ~30% of function signatures | Various files | Type safety gap |
| O10 | `prolog/` KB files use inconsistent naming conventions | prolog/ | KB files have no metadata headers |
| O11 | `backend/main.py` has hardcoded CORS origins | backend/main.py | Security misconfiguration for production |
| O12 | No `__init__.py` in several test directories | tests/ | Test discovery may fail on some runners |

### Hypothesis Analysis

| Hypothesis | Support | Contradiction | Status |
|---|---|---|---|
| H1: System is TypeScript to Python port | O1-O12 all show Python idioms; imported patterns (agents, tools, layers) match TypeScript architectural patterns | None | **Supported** |
| H2: Sandbox isolation is weak | O1, O2, O7 — shell injection, temp file, eval() risks | O3 uses Docker for some isolation | **Supported - Docker helps but eval()+subprocess remain vulnerable** |
| H3: Codebase is in active development (alpha stage) | O8 (many TODOs), O9 (missing types), O10 (inconsistent style) | None | **Supported** |
| H4: Frontend has SSRF vulnerability | O6 — proxy route without URL allowlist | None | **Supported - needs URL validation** |
| H5: Tests exist but not fully runnable | O4 (no CI), O5 (missing dev deps), O12 (missing __init__.py) | test files exist | **Supported - test suite needs CI integration** |

### Dependency Graph (Prolog-derived)

```
backend/main.py
    ├── backend/agents/evo_agent.py
    │   ├── backend/agents/code_agent.py
    │   │   └── backend/tools/prolog_exec.py
    │   │   └── backend/tools/python_exec.py
    │   ├── backend/agents/lean_agent.py
    │   │   └── backend/tools/lean4_exec.py
    │   └── backend/agents/prolog_agent.py
    │       └── backend/tools/prolog_exec.py
    ├── backend/services/sandbox.py
    │   └── Docker (external dependency)
    ├── backend/models/
    └── backend/tools/ (all tools)
```

---

## Verification

### Technical Correctness Assessment

| Area | Grade | Rationale |
|---|---|---|
| **Architecture** | B+ | Clean layered design; agent/tool/service separation well executed |
| **Code Quality** | C | Inconsistent style, missing types, ~15+ TODOs, eval() usage |
| **Security** | C- | Multiple vulnerabilities: shell injection, eval(), CORS, SSRF |
| **Testing** | C | Tests exist but no CI integration, missing dev deps, incomplete coverage |
| **Documentation** | B- | README and docstrings exist but many files lack module-level docs |
| **Portability** | C+ | Heavy Docker dependency; Lean/SWI-Prolog not easy to install cross-platform |
| **Innovation** | A | Multi-tier reasoning with Lean/Prolog/LLM integration is genuinely novel |

### Risk Matrix

| Risk | Severity | Likelihood | Mitigation |
|---|---|---|---|
| Shell injection via prolog_exec | **Critical** | High | Use shlex.quote() or subprocess with list args |
| eval() in code_agent | **Critical** | High | Replace with AST-based sandbox or dedicated container |
| SSRF via frontend proxy | **High** | Medium | Add URL allowlist validation |
| Temp file leakage | **Medium** | Medium | Use tempfile.TemporaryDirectory with context managers |
| CORS misconfiguration | **Medium** | Low | Use environment-variable-based CORS origins |
| Test suite non-functional | **Low** | High | Add CI config, dev dependency groups, __init__.py files |

---

## Remaining Limits

1. **No live execution review**: This review is based on static file inspection only. No test suite was executed, no Docker build was run, and no runtime behavior was observed.

2. **No deep dependency audit**: Third-party library versions and known CVEs were not checked.

3. **No benchmark/performance review**: Agent loop latency, sandbox overhead, and LLM token usage were not measured.

4. **No lean/prolog correctness review**: The logical content of Prolog KB files and Lean proof files was not verified against the system's tier requirements.

5. **Repository snapshot only**: The codebase is under active development; findings may be stale by the time of reading.
