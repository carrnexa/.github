# The CarrNexa Constitution

**Modular Tools for Curious Minds.**

This document defines the engineering philosophy, operating principles, and cultural constraints of the CarrNexa ecosystem. It serves as the single source of truth for decision-making.

## Core Philosophy

### 1. Density over Abstraction

We reject the modern web's tendency toward "black box" abstraction.

- **The Rule:** If an abstraction hides _how_ things work (e.g., ORMs that obscure SQL, No-Code builders), we avoid it.
- **The Preference:** Raw HTML/CSS, SQL drivers, and explicit types. We optimize for _Time-to-Understanding_, not just Time-to-Hello-World.

### 2. Modularity is Survival

We build systems, not monoliths.

- **The Why:** Monoliths hide complexity until it is too late. Modules isolate complexity so it can be solved (or deleted) independently.
- **The AI Stance:** We are skeptics of "Do-It-All" monolithic AI. We believe in **Hybrid Intelligence**: strictly deterministic systems for logic/math, and specialized probabilistic models for creativity/heuristics. Never use an LLM for a task that a Regex or a deterministic algorithm can solve.

### 3. Glass Box Engineering

We operate in the open.

- **Security:** We do not rely on "Security through Obscurity" as a primary defense. Our code is public; our secrets are dark.
- **Trust:** We assume our users are technical and curious. We do not "dumb down" our documentation. We invite them to look inside the machine.

## Engineering Standards

### 1. The "No Magic" Rule

Code should be readable without needing to memorize the internal state of a framework.

- **Avoid:** "Magic" dependency injection, implicit global state, or framework-specific macros that rewrite code behavior invisibly.
- **Prefer:** Explicit imports, pure functions, and standard libraries.

### 2. Neuroergonomics

We design workflows for high-momentum, low-friction execution.

- **Feedback Loops:** CI/CD pipelines must be fast (<5 min). If tests take too long, people stop running them.
- **Context Boundaries:** A repository should handle _one_ domain. Do not force a developer to load the entire cognitive model of the company just to fix a typo in the README.

### 3. Pragmatic Performance

We optimize for the _critical path_, not the theoretical maximum.

- **Latency:** Sub-100ms response times are a non-negotiable usability feature.
- **Stack:** We use high-throughput tools (Rust, Python Async, UDS) because they respect the user's hardware.

## The Stack (Default Choices)

- **Language:** Python 3.12+ (Async), Rust (for Systems/Game), TypeScript (Strict).
- **Infrastructure:** Arch Linux (Dev), Docker (Prod), Caddy (Edge).
- **Communication:** REST (Public), Unix Domain Sockets (Internal/IPC).
- **Data:** PostgreSQL (Relational), Valkey (Ephemeral).

## Communication Style

- **Tone:** Objective, dense, academic.
- **Anti-Patterns:** No marketing fluff, no customer service voice.
- **Format:** Use bullet points, bolding for emphasis, and standard Markdown.
