# Changelog

All notable changes to this project are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

Framework content changes are noted distinctly from tool / skill / repo-infrastructure changes. The framework text in `guide/` is canonical. Any change to it is treated as a breaking change to the citable artefact and triggers at least a minor version bump.

## [1.0.0] - 2026-06-03

Initial public release.

### Added

- **Teacher Guide** (`guide/`) — five parts plus appendix: the Hype-Man problem and its three-dimensional cost, the loop in depth, Reality Audit in practice with four worked examples, assessment and accountability, and the research foundation.
- **Claude skill** (`skill/RealityAudit_skill.md`) — three application modes (learner guidance, work review, teacher feedback), the loop and Academic Branch with diagnostic, the Strong/Developing/Weak feedback matrix, and the recursive-honesty instruction to produce friction rather than relief.
- **Skill README** (`skill/README.md`) — the recursive-honesty note on using an agreeable AI to teach distrust of agreeable AIs.
- **Interactive tool** (`tool/index.html`) — single-file, no-backend, no-telemetry walk-through of the loop: RAG calibration, copyable Friction Stems, the Relief/Curiosity audit, the Reflection checklist, the Academic Branch and self-rubric, and Reality Audit Log export. Self-hosted fonts, WCAG 2.1 AA, CSP-locked, `textContent`-only rendering.
- **Rubrics** (`rubrics/`) — A–E (QCAA-aligned) and four-level, assessing the loop rather than the polish.
- **Build specs** (`docs/`) — `FRAMEWORK.md` (canonical distillation, marking verbatim vs distilled content), `SKILL_SPEC.md`, `TOOL_SPEC.md`.
- **Repository infrastructure** — CC BY 4.0 `LICENSE`, machine-readable `CITATION.cff`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, issue and PR templates, and CI (citation + link validation, CodeQL, OpenSSF Scorecard, Dependabot, Pages deploy).
