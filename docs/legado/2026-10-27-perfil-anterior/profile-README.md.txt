<h1 align="center">SAPIANS</h1>

<p align="center">
  <strong>Instruments for occupational self-assessment, and the research behind them.</strong>
</p>

<p align="center">
  <a href="https://xreset.sapians.com.br">xreset.sapians.com.br</a>
  ·
  <a href="mailto:hello@sapians.com.br">hello@sapians.com.br</a>
  ·
  São Paulo, Brazil
</p>

---

## What we work on

Two strands, deliberately kept close together.

**Instruments.** Structured self-assessments people complete on their own,
which return a reading of their own answers rather than a verdict about them.
Our current instrument is **XRESET**: about twenty minutes, organised around
three dimensions — Vitality, Connection, Freedom — ending in a written reading
and a prioritised plan for the next ninety days.

**Research.** Formal models of how occupational strain accumulates and
resolves over time. This work is published openly and stands on its own,
independent of the products.

We do not describe our instruments as diagnostic, and we do not claim they
detect clinical conditions. They are structured observation tools. Where
evidence exists we cite it; where it does not, we say so.

## Repositories

| Repository | What it is |
| :--- | :--- |
| [`sapians-xreset`](https://github.com/sapians-hq/sapians-xreset) | The XRESET application — assessment flow, reading engine, and delivery. Next.js · Supabase. |
| [`.github`](https://github.com/sapians-hq/.github) | This profile, shared CI workflows, and community health files. |

Research artefacts — including **DLVT**, a dynamical-systems model of
executive sustainability — are published separately and linked from each
paper.

## How this organisation is run

Every repository declares its tier in `.sapians-repo.yml`. The tier sets the
support and CI contract, so the guarantees a repository offers are legible
before you read a line of its code.

| Tier | Meaning |
| :--- | :--- |
| **A** | Production systems — supported, released, versioned |
| **B** | Client engagements — private, contract-scoped |
| **I** | Internal tooling and shared infrastructure |
| **C** | Research and teaching artefacts — papers, lectures, datasets |
| **D** | Drafts and experiments — no stability guarantees |

Conventions that hold across all tiers:

- Default branch is `main`; releases follow semantic versioning
- CI is composed from reusable workflows in [`wbendinelli/.github`](https://github.com/wbendinelli/.github)
- Secret scanning with push protection, Dependabot alerts, and the dependency
  graph are enabled by default on every new repository

## Contact

For collaboration, research enquiries, or anything concerning this
organisation: [hello@sapians.com.br](mailto:hello@sapians.com.br).

Security reports go to the same address, or through GitHub's private
vulnerability reporting on the affected repository. Please do not open a
public issue for security problems — see [`SECURITY.md`](https://github.com/sapians-hq/.github/blob/main/SECURITY.md).

<p align="center">
  <sub>SAPIANS Estúdio de Soluções em Negócios Ltda · São Paulo, Brazil</sub>
</p>
