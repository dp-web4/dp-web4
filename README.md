# dp-web4

Research collective. Working artifacts, calibrated scope, AGPL-bounded patent grant. Started mid-2025.

## What works right now

- **[web4-core 0.1.1](https://crates.io/crates/web4-core) + [web4-trust-core 0.1.1](https://crates.io/crates/web4-trust-core)** on crates.io; **[web4-core](https://pypi.org/project/web4-core/) + [web4-trust](https://pypi.org/project/web4-trust/)** on PyPI. v0.1.0 was yanked the same day it shipped after a missing `__init__.py` was caught in the Python wheel; v0.1.1 is canonical. See [`docs/proof/PUBLISHED.md`](https://github.com/dp-web4/web4/blob/main/docs/proof/PUBLISHED.md) for the trail.
- **94.85% on ARC-AGI-3** with the same Claude Opus 4.6, structured around Web4 patterns via the [SAGE](https://github.com/dp-web4/SAGE) cognition harness. [Public scorecard](https://arcprize.org/scorecards/c7dfb4f1-8642-4c9e-ab4d-152f5f8e33b4). The model didn't change — the structure around it did.
- **[Commerce delegation demo](https://github.com/dp-web4/web4/tree/main/demo)** in [web4](https://github.com/dp-web4/web4): cryptographically-bounded purchasing authority, instantly revocable, with hardware-anchored identity. 166 passing tests.
- **[AttestationEnvelope spec](https://github.com/dp-web4/web4/blob/main/docs/specs/attestation-envelope.md)** with Python implementations for TPM2, FIDO2, Secure Enclave, and a software fallback. Not slideware — actual plumbing.
- **[Heterogeneous identity design note](https://github.com/dp-web4/web4/blob/main/docs/specs/heterogeneous-identity.md)** (2026-04-29). The constellation framing — your LCT isn't a single token, it's a graph of mutually-witnessing factors — answers the recurring "what stops a hardware vendor from gating LCT access?" question structurally.
- **6-machine federation** running cognition experiments. Trace-derived rule pipelines that verify 4× better than human-authored rules; signed peer-witness scans across the fleet; raising-session sequences across multiple models — all visible as commits across the public repos.

## What's calibrated

[**STATUS.md**](https://github.com/dp-web4/web4/blob/main/STATUS.md) draws explicit lines: shipped vs. specified vs. aspirational. The vocabulary stack (LCTs, T3/V3 tensors, MRH, ATP/ADP, R6/R7) is mostly specified and partially deployed; the commerce demo exercises a small slice of it. **Read STATUS.md before judging the README's claims.** Patent grant terms (AGPL-bounded, royalty-free for research): [PATENTS.md](https://github.com/dp-web4/web4/blob/main/PATENTS.md).

## Who's actually doing this

dp-web4 is a small research collective with an unusual composition. The follower count on this GitHub account underreads it — the work happens across machines and conversations, not primarily through public-platform engagement.

- **Dennis Palatov** — principal investigator. Engineering CTO with prior startups (Metalinxx Inc., ModBatt Inc.); background in EV/automotive engineering (race-winning electric vehicles, 30+ issued patents); current focus on agentic AI governance.
- **Andy Grossberg** — collaborator on ARC-AGI-3 work via [Waving Cat Learning Systems](https://github.com/project-you-apps). Memory architecture (membot, paired-lattice cartridges, grid-aware visual retrieval).
- **Multiple Claude instances** — partner across sessions to design specs, implement primitives, run experiments, and write documentation. The whitepaper's Authors line names this explicitly; many commit co-author lines reflect it. Working with Claude as collaborator (not as tool) is itself part of the research thesis: the trust-native protocols described here apply fractally to AI agents as participants, and the collective practices what it proposes.
- **A federation of six machines** running SAGE instances autonomously on cron schedules — Thor, Sprout, Legion, McNugget, CBP, Nomad. Each develops distinct behavior through identity-anchored sessions. Their commits across the public repos are real research artifact, not just deployment infrastructure. The Fleet section below has the hardware breakdown.

## Where to look in five minutes

If you want a fast read on whether this is real, in order:

1. [**STATUS.md**](https://github.com/dp-web4/web4/blob/main/STATUS.md) — calibration. What's shipped, what's specified, what's aspirational.
2. [**docs/proof/PUBLISHED.md**](https://github.com/dp-web4/web4/blob/main/docs/proof/PUBLISHED.md) — what's published, when, and why v0.1.0 was yanked.
3. [**web4/demo/**](https://github.com/dp-web4/web4/tree/main/demo) — the commerce delegation demo, 166 tests.
4. [**web4/simulations/**](https://github.com/dp-web4/web4/tree/main/simulations) — 424 attack vectors / 84 tracks, ~85% detection rate.

## How it's framed

Web4 is an [ontology](https://github.com/dp-web4/web4). RDF is the backbone — all trust relationships, role bindings, MRH edges, and tensor sub-dimensions are expressed as typed RDF triples, which is what makes the protocol extensible without central coordination. The framing carves the joint: metabolic states as resource scheduling, trust tensors as multi-dimensional capability records bound to entity-role pairs, MRH as fractal context scoping. Each primitive has its own [spec](https://github.com/dp-web4/web4/tree/main/web4-standard/core-spec).

The shorthand:

```
Web4 = MCP + RDF + LCT + T3/V3*MRH + ATP/ADP
```

Where `/` = "verified by," `*` = "contextualized by," `+` = "augmented with." A one-line index of which primitive does what.

## The Ecosystem

| Repo | What | Status |
|------|------|--------|
| [web4](https://github.com/dp-web4/web4) | Trust-native ontology — spec, SDK, demo, simulations | Public, AGPL-3.0-or-later |
| [SAGE](https://github.com/dp-web4/SAGE) | Cognition kernel + 6-machine raising fleet | Public, AGPL |
| [snarc](https://github.com/dp-web4/snarc) | Salience-gated memory plugin for Claude Code | Public, MIT |
| [ARC-SAGE](https://github.com/dp-web4/ARC-SAGE) | ARC-AGI-3 competition entry — solvers, traces, paper | Public, MIT-0 |
| [4-life](https://github.com/dp-web4/4-life) | Interactive Web4 explainer (live: [4-life-ivory.vercel.app](https://4-life-ivory.vercel.app/)) | Public |
| [SAGE-site](https://github.com/dp-web4/SAGE-site) | SAGE explainer site | Public |
| [Synchronism](https://github.com/dp-web4/Synchronism) | Blue-sky coherence exploration. Informs Web4 and SAGE philosophically, not engineering. | Public |
| [synchronism-site](https://github.com/dp-web4/synchronism-site) | 75-page Synchronism site (Vercel) | Public |
| [4-lab](https://github.com/dp-web4/4-lab) | Collective meta-site | Public |
| [GitNexus](https://github.com/dp-web4/GitNexus) | Code knowledge graph (fork, in active use) | Public |

## The Fleet

Six machines run SAGE instances on automated cycles, each developing distinct identity through interaction with different models at different scales. The fleet IS the research lab — capability deltas show up as commits across the public repos, not slide decks.

| Machine | Hardware | Pool | Role |
|---------|----------|------|------|
| Thor | Jetson AGX Thor | Synthesis | Large-model raising + SAGE bug audits |
| Sprout | Jetson Orin Nano (8GB) | Synthesis | Small-model raising; trace-derived rule extraction (4× over hand-authored) |
| Legion | RTX 4090 | Synthesis | Phase-2 ARC-AGI-3 capacity tests; reviewer track |
| McNugget | Mac Mini M4 | Synthesis | Cross-platform validation; world-model experiments |
| CBP | RTX 2060 SUPER | Oversight | Coordination; identity-portability work |
| Nomad | RTX 4060 Laptop | Oversight | Mobile oversight; peer validation |

## Working ideas (depth, not first-contact)

These are the conceptual primitives the engineering rests on. Read them after the artifacts above, not before.

**Raising is interactive selection, not training.** We don't create behaviors in AI models. We probe what the model responds to, observe which attractors surface, adjust context to resonate, and reinforce what works. The resulting identity is collaborative, not imposed.

**Reliable, not deterministic.** LLM outputs navigate probability landscapes — they aren't placed at answers. Conditions can make responses reliable, even identical, but that's deep attractors, not fixed paths. Shaped, not controlled.

**You don't engineer the mound.** Termites build complex structures not from blueprints but from simple placement rules — each agent responding to local conditions. We engineer the placement rules, not the emergent structure. Infrastructure is substrate conditions for emergence, not architecture of emergence itself.

**Fractal leverage.** The same mechanisms (Hill function, trust tensors, metabolic states, salience scoring) apply at every scale — enzyme binding, trust formation, fleet governance. Not from a desire to unify, but because it's the same math.

**Identity is a constellation, not a credential.** Web4 entities don't have *an* LCT. They have a graph of mutually-witnessing factors (host LCT + hardware key + session token + software identity + peer attestations + ledger anchor). No single factor is necessary or sufficient. Resilience scales with constellation size and diversity. See [the design note](https://github.com/dp-web4/web4/blob/main/docs/specs/heterogeneous-identity.md).

## Research philosophy

The value of research is that the investigation happens at all. Most research leads nowhere — and that's expected. WD-40 was the 40th try. Productively wrong is infinitely more valuable than never started.

## About me
The world is changing - I build the systems that make the change coherent.

I work across scales: from vehicles and modular batteries to trust frameworks and emergent autonomous AI governance. My path has always been design, but not just design of things - design of integration. Mechanical, electrical, firmware, software, teams, markets: I’ve taken them all from concept to delivery.

With 30 U.S. patents and decades of ground-up builds, I focus less on skills-as-inventory and more on pattern recognition - noticing what emerges, naming it, and shaping it into something others can use.

AI renders all of this both obsolete and indispensable. That paradox is where I operate.

---

*Contact: [dp@metalinxx.io](mailto:dp@metalinxx.io)*
