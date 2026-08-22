# DEAP Profile: Backend API

> **Repository Role:** `PROFILE_REPOSITORY`  
> **Profile Name:** `backend-api`  
> **Primary Technology Profiles:** `Python / FastAPI / REST API` | `Backend Services`  
> **Target Regulatory Frameworks:** `DO-178C` | `SysML v2 Interface Architecture`  

---

## 1. System Overview

This repository provides the official **Backend API Profile** for the **Digital Engineering Agent Platform (DEAP)**.

### 1.1 Primary Commercial Toolchain Integration Context

This platform explicitly declares **MATLAB / Simulink / Stateflow / Embedded Coder** as the Primary Tier-1 Commercial Toolchain Integration Context (Model-Based Design, Control Law Synthesis, DO-178C C/SPARK Ada code generation).

---

## 2. Pipeline Structure & Governance

- `.agents/` & `AGENTS.md`: Agent behavior rules, role boundaries, and subagent dispatch protocols.
- `CLAUDE.md`: Claude Code guidelines and verification gates.
- `rules/`: Profile and platform engineering rules (`backend-api-discipline.md`, `latex-katex-integrity.md`).
- `schema/`: Contract definitions, specification schemas, and SysML v2 models.
- `scripts/`: Modular installer (`install_pipeline.sh`, `install_pipeline.py`) and downstream verifiers (`verify_downstream_baseline.py`).
- `tests/`: Automated baseline verification and runtime integrity test suites.

---

## 3. Installation & Usage

To install this profile into a downstream repository:

```bash
./scripts/install_pipeline.sh /path/to/downstream/project
```

---

## 4. Verification & Quality Gates

Execute baseline and governance verification:

```bash
# Run baseline tests
python3 -m pytest tests/

# Run downstream conformance gate
python3 scripts/verify_downstream_baseline.py --no-domain
```
