# remram-recall

**Context Retrieval Engine (RAM) for Remram.**

`remram-recall` is the structured recall layer of the Remram system.

It is responsible for retrieving memory safely, deterministically, and efficiently.

This is the **read path**.

---

## Role in the System

Remram separates memory into two phases:

- **REM** — consolidation and mutation (`remram-encode`)
- **RAM** — structured retrieval (`remram-recall`)

RAM never mutates memory.
RAM never reconciles artifacts.
RAM never promotes facts.

RAM retrieves.

---

## Core Responsibilities

- Hybrid retrieval (policy filters + sparse + dense)
- Rank feature scoring
- Confidence scoring
- Snippet selection
- Context bundle assembly
- Deterministic result ordering

RAM operates under strict memory policy gates.

Vectors are ranking signals.
Policy defines eligibility.

---

## Architecture Position

```
User → remram-os → remram-recall → Context Bundle
```

The retrieval engine surfaces relevant memory for orchestration.
It does not modify state.

---

## Design Principles

- Local-first execution
- Deterministic query behavior
- No recursive vector expansion
- Small, precise context bundles
- Clear separation from mutation logic

RAM remembers.

