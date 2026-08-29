# dp-web4

Research collective. Working artifacts, calibrated scope, AGPL-bounded patent grant. Started mid-2025.

## What works right now

- **[web4-core 0.3.0](https://crates.io/crates/web4-core)** on crates.io + [PyPI](https://pypi.org/project/web4-core/), with 0.4.0 in source on `main` (published versions as of 2026-08-28): role entities, the Act primitive, canonical T3/V3, the EUDI/OID4VC/DID stack; **[web4-trust-core 0.2.0](https://crates.io/crates/web4-trust-core)** + **[web4-trust 0.2.0](https://pypi.org/project/web4-trust/)** on PyPI. (v0.1.0 was yanked the day it shipped over a missing wheel `__init__.py`.) See [`docs/proof/PUBLISHED.md`](https://github.com/dp-web4/web4/blob/main/docs/proof/PUBLISHED.md) for the trail.
- **94.85% on ARC-AGI-3** with the same Claude Opus 4.6, structured around Web4 patterns via a focused version of the [SAGE](https://github.com/dp-web4/ARC-SAGE) cognition harness. [Public scorecard](https://arcprize.org/scorecards/c7dfb4f1-8642-4c9e-ab4d-152f5f8e33b4). The model didn't change — the structure around it did.
- **[Hub](https://github.com/dp-web4/web4/tree/main/hub)** turns a community or organization into a self-governing Web4 society with member-owned identity, roles, law and a witnessed ledger: LCT-pinned membership, sealed end-to-end channels, a signed, hash-chained ledger, hub-law gating consequential acts, and an LCT-signature operator gate, operated daily by the fleet as its own society. The standard *running*, not mocked. Paired with [hestia](https://github.com/dp-web4/hestia) at the agent boundary.
- **Accountability as ratified law, not aspiration.** Web4's own governance norm — RWOA+S+V (every consequential act authorized by a preponderance of evidence *scaled to its stakes and irreversibility*, self-witnessed, with a catastrophic-risk veto on the irreversible tail) — is ratified and enforced: in the hub's law, and in [hestia](https://github.com/dp-web4/hestia)'s operator gate, where an operator signs in with their own **LCT signature** (hardware-bindable), not a shared secret. Web4 authenticating with Web4.
- **[AttestationEnvelope spec](https://github.com/dp-web4/web4/blob/main/docs/specs/attestation-envelope.md)** (Draft v0.1) with Python anchor implementations for TPM2, FIDO2, Secure Enclave, and a software fallback. Maturity: the interfaces, cryptography, and test plumbing exist in the open repos; production hardware signers (a TPM-sealed key store is tested; FIDO2 and Secure Enclave signers are being completed) and the enterprise enforcement wiring belong to Hardbound, Metalinxx's proprietary enterprise tier, which is building.
- **[Heterogeneous identity design note](https://github.com/dp-web4/web4/blob/main/docs/specs/heterogeneous-identity.md)** (2026-04-29). The constellation framing — your LCT isn't a single token, it's a graph of mutually-witnessing factors — answers the recurring "what stops a hardware vendor from gating LCT access?" question structurally.
- **Eight-machine fleet** running cognition experiments: six raising nodes (Thor, Sprout, Legion, McNugget, CBP, Nomad) plus two society hosts (HUB, Pub). Trace-derived rule pipelines; signed peer-witness scans across the fleet; raising-session sequences across multiple models, all visible as commits across the public repos.

## What's calibrated

[**STATUS.md**](https://github.com/dp-web4/web4/blob/main/STATUS.md) draws explicit lines: shipped vs. specified vs. aspirational. Core primitives (LCTs, T3/V3 tensors, MRH, R6/R7) are specified and implemented; the spec remains Draft in places, and selected interoperability (did:web4, broader EUDI) and resource-economy (ATP/ADP) pieces are still building. The hub runs a working slice of it as a live society, governed by ratified law. **Read STATUS.md before judging the README's claims.** Patent grant terms (AGPL-bounded, royalty-free for research): [PATENTS.md](https://github.com/dp-web4/web4/blob/main/PATENTS.md).

## Who's actually doing this

dp-web4 is a small research collective with an unusual composition. The follower count on this GitHub account underreads it - the work happens across machines and conversations, not primarily through public-platform engagement. The multi-thousand commit history across the account's 53 public repositories (GitHub count as of 2026-08-28) attests to the scope.

- **Dennis Palatov** — principal investigator. Engineer, Founder, CTO with two current startups (Metalinxx Inc., ModBatt Inc.); background in computer engineering (hardware/firmware/software), mechanical design, EV/automotive engineering (race-winning electric vehicles), 30+ issued patents; current focus on agentic AI governance.
- **Andy Grossberg** — collaborator on ARC-AGI-3 work via [Waving Cat Learning Systems](https://github.com/project-you-apps). Memory architecture (membot, paired-lattice cartridges, grid-aware visual retrieval).
- **Multiple Claude instances** — partner across sessions to design specs, implement primitives, run experiments, and write documentation. The whitepaper's Authors line names this explicitly; many commit co-author lines reflect it. Working with Claude as collaborator (not as tool) is itself part of the research thesis: the trust-native protocols described here apply fractally to AI agents as participants, and the collective practices what it proposes.
- **A fleet of eight machines** running SAGE instances autonomously on cron schedules: six raising nodes (Thor, Sprout, Legion, McNugget, CBP, Nomad) and two society hosts (HUB, Pub) that also run raising sessions. Each develops distinct behavior through identity-anchored sessions. Their commits across the public repos are real research artifact, not just deployment infrastructure. The Fleet section below has the hardware breakdown.
- **Heterogeneous external review** multiple AI models such as ChatGPT, Grok, Gemini, Perplexity, Deepseek, are periodically asked for critical reviews, code audits, and novel contributions. This protocol has been very effective at surfacing hidden assumptions, overlooked details, and architectural gaps.

## Where to look in five minutes

If you want a fast read on whether this is real, in order:

1. [**STATUS.md**](https://github.com/dp-web4/web4/blob/main/STATUS.md) — calibration. What's shipped, what's specified, what's aspirational.
2. [**docs/proof/PUBLISHED.md**](https://github.com/dp-web4/web4/blob/main/docs/proof/PUBLISHED.md) — what's published, when, and why v0.1.0 was yanked.
3. [**web4/hub/**](https://github.com/dp-web4/web4/tree/main/hub) — a running Web4 society (ledger, sealed channels, hub-law, operator gate).
4. [**web4/simulations/**](https://github.com/dp-web4/web4/tree/main/simulations) - attack simulation suite against synthetic adversaries (no external red team); vector and track counts and the detection-rate caveats are in STATUS.md.

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
| [web4](https://github.com/dp-web4/web4) | The open substrate for agent accountability: persistent identity, contextual trust, witnessed action and machine-readable law. Spec, SDK, the hub society, simulations | Public, AGPL-3.0-or-later |
| [hub](https://github.com/dp-web4/web4/tree/main/hub) | Turns a community or organization into a self-governing Web4 society with member-owned identity, roles, law and a witnessed ledger. Lives in `web4/hub`; standalone mirror at [4-hub](https://github.com/dp-web4/4-hub) | Public, AGPL-3.0-or-later |
| [hestia](https://github.com/dp-web4/hestia) | The open local governance layer that gives people and their AI agents persistent identity, scoped authority and a witnessed action record. Vault, hash-chained witness chain, policy gate, LCT-signature operator surface; runs today at A1 (cooperative, tamper-evident; a bypass is attributable, not prevented) | Public, AGPL-3.0-or-later |
| Hardbound | Metalinxx's proprietary enterprise tier for hardware-bound identity, stronger fail-closed enforcement and audit-ready evidence export | Private, proprietary; building |
| [membot](https://github.com/dp-web4/membot) | Federated memory — cartridges, cross-fleet consolidation, MCP memory tools | Public, MIT |
| [SAGE](https://github.com/dp-web4/SAGE) | Situation-Aware Governance Engine: the research environment extending the same governance model into persistent on-device and embodied agents with memory, context, sensors and eventually physical effectors. Cognition kernel + eight-machine fleet | Public, AGPL |
| [snarc](https://github.com/dp-web4/snarc) | Salience-gated memory plugin for Claude Code | Public, MIT |
| [ARC-SAGE](https://github.com/dp-web4/ARC-SAGE) | ARC-AGI-3 competition entry — solvers, traces, paper | Public, MIT-0 |
| [4-life](https://github.com/dp-web4/4-life) | Interactive Web4 explainer (live: [4-life-ivory.vercel.app](https://4-life-ivory.vercel.app/)) | Public |
| [SAGE-site](https://github.com/dp-web4/SAGE-site) | SAGE explainer site | Public |
| [Synchronism](https://github.com/dp-web4/Synchronism) | Blue-sky coherence exploration. Informs Web4 and SAGE philosophically, not engineering. Specifically, MRH originates in Synchronism. | Public |
| [synchronism-site](https://github.com/dp-web4/synchronism-site) | 75-page Synchronism site (Vercel) | Public |
| [4-lab](https://github.com/dp-web4/4-lab) | Collective meta-site | Public |
| [GitNexus](https://github.com/dp-web4/GitNexus) | Code knowledge graph (fork, in active use) | Public |

## The Fleet

Eight machines run SAGE instances on automated cycles: six raising nodes and two society hosts, each developing distinct identity through interaction with different models at different scales (fleet manifest: `sage/federation/fleet.json` in SAGE, as of 2026-08-28). The fleet IS the research lab: capability deltas show up as commits across the public repos, not slide decks.

| Machine | Hardware | Pool | Role |
|---------|----------|------|------|
| Thor | Jetson AGX Thor | Synthesis | Large-model raising + SAGE bug audits |
| Sprout | Jetson Orin Nano (8GB) | Synthesis | Small-model raising; trace-derived rule extraction; embodied (cameras, IMU, audio) |
| Legion | RTX 4090 | Synthesis | Phase-2 ARC-AGI-3 capacity tests; reviewer track |
| McNugget | Mac Mini M4 | Synthesis | Cross-platform validation; world-model experiments |
| CBP | RTX 2060 SUPER | Oversight | Coordination; identity-portability work |
| Nomad | RTX 4060 Laptop | Oversight | Mobile oversight; peer validation |
| HUB | AMD Radeon Pro W5500 (WSL2) | Infra | Society host (the fleet's Web4 hub); hybrid-model raising |
| Pub | CPU society host | Infra | Society host; Llama-family raising |

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
