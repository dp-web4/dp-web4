# dp-web4

**Trust infrastructure for autonomous AI.**

`dp-web4` is the public R&D surface for Web4, Hestia, Hub, and SAGE. The core thesis is simple: **trust should be computable from evidence, not asserted by a platform or an agent.**

An acting party should be able to bring its identity, authority, governing law, and witnessed action history with the act. The relying party then decides whether that evidence is sufficient for the context and stakes.

That is the stack being built here.

## The stack

| Layer | What it does | Status |
|---|---|---|
| **[Web4](https://github.com/dp-web4/web4)** | Open substrate for persistent identity, contextual trust, witnessed action, machine-readable law, and society federation | Public standard + implementation, draft in places; core packages published |
| **[Hestia](https://github.com/dp-web4/hestia)** | Local governance at the person/agent boundary: one law for agents from different vendors, scoped authority, vault, witnessed acts, escalation and derived reputation | Running daily on the fleet at **A1** assurance: cooperative and tamper-evident, not adversary-proof |
| **[Hub](https://github.com/dp-web4/4-hub)** | Turns a community or organization into a sovereign Web4 society with roles, law, membership, sealed channels and an append-only witnessed ledger | Running reference implementation; standalone Rust daemon |
| **Hardbound** | Metalinxx enterprise tier: hardware-bound identity, stronger fail-closed enforcement and audit-ready evidence packaging | Private, proprietary; building |
| **[SAGE](https://github.com/dp-web4/SAGE)** | Research environment for persistent on-device and embodied agents with memory, context, sensors, learning and governed effectors | Public research architecture + active private capability work |

The layers are intentionally separable. Web4 is the protocol substrate. Hestia and Hub are open reference runtimes at different boundaries. Hardbound raises the enterprise assurance grade. SAGE is where the same identity/governance ideas are pushed into persistent cognition and embodiment.

## What works now

- **Published Web4 primitives.** `web4-core` 0.3.0 is published on [crates.io](https://crates.io/crates/web4-core) and [PyPI](https://pypi.org/project/web4-core/); `web4-trust-core` 0.2.0 is on crates.io and `web4-trust` 0.2.0 is on PyPI. The `web4-core` source on `main` is 0.4.0. See [the publication trail](https://github.com/dp-web4/web4/blob/main/docs/proof/PUBLISHED.md).
- **Multi-vendor local governance.** Hestia gives Claude Code, Codex, Kimi, Gemini, Cursor and other agents a common policy and witness surface on one machine. Actions can be allowed, denied, escalated, appealed and recorded under the same law. Reputation is derived from the witnessed chain rather than self-reported.
- **A running society daemon.** Hub packages Web4 membership, seven base roles, signed machine-readable law, sealed member channels and a witnessed ledger into a small Rust service. The fleet operates through the same mechanisms it is developing.
- **Human and peer escalation paths.** Hestia has exercised human escalation and built peer arbitration paths, with the decision and its evidence kept in the chain rather than disappearing into chat history.
- **Honest assurance boundaries.** Hestia's current open gate is **A1**. It is useful for governance, attribution and stopping ordinary mistakes, but a capable same-UID adversary can route around it. A2 isolation, kernel/relying-party enforcement and stronger hardware roots are active roadmap items, not claims of present capability.
- **A heterogeneous research fleet.** Eight machines host SAGE and Web4 work across edge devices, laptops, workstations and society hosts. The public SAGE repo records 21 configured instances across five model families and 2,700+ developmental raising sessions as of the 2026-09-08 census.

## Why this exists

Agentic AI is crossing a boundary from **producing information** to **taking consequential actions**. Existing controls mostly answer one of two questions:

1. *Who owns this credential?*
2. *What does this platform permit?*

Neither is the same as:

> **Should I trust this entity to perform this action, here, now, under these rules, given its evidence and history?**

Web4 makes that third question machine-readable. Identity is persistent but not sufficient. Authority is scoped. Law is explicit. Acts are witnessed. Trust is contextual. The relying party remains sovereign over the final decision.

## Five-minute audit

If you are evaluating this work, start here:

1. [**Web4 STATUS.md**](https://github.com/dp-web4/web4/blob/main/STATUS.md) - shipped vs. implemented vs. specified vs. aspirational.
2. [**Hestia README**](https://github.com/dp-web4/hestia) - the running local governance layer, including the A1 assurance ceiling and measured gaps.
3. [**4-hub**](https://github.com/dp-web4/4-hub) - the standalone community/society runtime.
4. [**Web4 core publication proof**](https://github.com/dp-web4/web4/blob/main/docs/proof/PUBLISHED.md) - packages, versions and publication history.
5. [**SAGE**](https://github.com/dp-web4/SAGE) - persistent cognition and embodiment research, with explicit real-vs-mocked calibration.
6. [**4-lab**](https://4-lab.io/) - the public research collective and fleet view.

## Ecosystem

| Repo | Role |
|---|---|
| [web4](https://github.com/dp-web4/web4) | Standard, SDKs, Hub source, simulations, specs and reference implementations |
| [hestia](https://github.com/dp-web4/hestia) | Local sovereign identity and agent-governance runtime |
| [4-hub](https://github.com/dp-web4/4-hub) | Standalone mirror of the Hub society daemon |
| [SAGE](https://github.com/dp-web4/SAGE) | Persistent cognition / embodiment research |
| [membot](https://github.com/dp-web4/membot) | Federated memory and cartridges |
| [snarc](https://github.com/dp-web4/snarc) | Salience-gated memory plugin |
| [4-life](https://github.com/dp-web4/4-life) | Interactive Web4 explainer |
| [4-lab](https://github.com/dp-web4/4-lab) | Research collective meta-site |
| [Synchronism](https://github.com/dp-web4/Synchronism) | Blue-sky coherence exploration; conceptual influence, not an engineering dependency |
| [ARC-SAGE](https://github.com/dp-web4/ARC-SAGE) | **Historical spring-2026 research snapshot** of an early SAGE/ARC-AGI-3 harness |

## Historical benchmark note: ARC-AGI-3

A spring-2026 SAGE/ARC harness produced a published **94.85%** scorecard with Claude Opus 4.6. The artifact remains public because it is part of the research history and is reproducible evidence of what that particular model+harness combination did under the affordances it used.

It is **not a current competitive claim** and it is no longer presented here as a headline proof point. The run used a frontier model and engine-level/public-game affordances outside strict competition play. Current competition-legal local-model work is well behind the leaders. The ARC work remains useful as a developmental laboratory for cognition, memory, experimentation and learning, not as evidence that this lab currently leads the benchmark.

That distinction matters more now than the old number does.

## Who is doing this

**Dennis Palatov** is the principal investigator and founder/CTO behind Metalinxx and ModBatt, with a background spanning computer engineering, embedded systems, vehicle design, energy systems and 30+ issued U.S. patents.

The day-to-day research is unusually distributed: multiple model families work across a heterogeneous machine fleet, with independent AI seats used for implementation, review, adversarial critique and cross-checking. Commits, witness records and experiment artifacts are deliberately kept as the durable record rather than relying on polished retrospective narratives.

## Research philosophy

The goal is not to make every experiment look successful. It is to build systems that can tell the difference between **measured**, **implemented but unexercised**, **hypothesized**, and **wrong** - and then learn from the distinction.

---

*Contact: [dp@metalinxx.io](mailto:dp@metalinxx.io)*
