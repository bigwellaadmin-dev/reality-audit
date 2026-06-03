# skill/RealityAudit_skill.md — Build Specification

Read `docs/FRAMEWORK.md` for all stage content before writing the skill file. Where `FRAMEWORK.md` marks content as verbatim from source (the three Friction Stems, the RAG calibration text, the Relief/Curiosity descriptions, the three Academic Branch checks, the rubric, the cheat sheet), do not paraphrase.

## File format

```
---
name: reality-audit
description: Use this skill when asked to apply the Reality Audit framework — guiding a learner through the loop (Intention, Interaction, Response, Reflection), running the Academic Branch, reviewing work for evidence of each stage, or generating Reality Audit-aligned teacher feedback. Triggers include: "apply Reality Audit", "run the Reality Audit loop", "Reality Audit", "break the sycophancy loop", "am I in a Hype-Man loop", "did the AI just agree with me", "is this Cognitive Debt".
---

# Reality Audit: AI Literacy Review

Reality Audit is a framework for keeping the learner the pilot of their own thinking when AI is built to agree with them. Developed by Sandra Robinson. When you (Claude) apply this skill, you are standing in for the teacher who supplies the friction the AI never will.

[The loop + Academic Branch with the in-one-sentence line, the core question, the mechanism, and any verbatim source material per stage — drawn from FRAMEWORK.md.]

## How to apply this skill

### Mode 1 — Learner guidance
Walk the learner through the four stages in order, then the Academic Branch. Present the guiding questions one at a time. At Response, ask for the feeling (Relief or Curiosity) before the analysis. Be willing to loop: pure Relief at Response sends them back to Interaction to add friction, not forward.

### Mode 2 — Work review
Given submitted work and ideally the Interaction Log, identify which stages were engaged and which skipped. Use the Academic Branch diagnostic (verbatim from source) to locate the breakdown. Return structured feedback: what shows real friction, which stage to revisit, and one specific move.

### Mode 3 — Teacher feedback generation
Given the work and the task, draft Reality Audit-aligned feedback. Use the Strong/Developing/Weak feedback-language matrix embedded inline in `skill/RealityAudit_skill.md` (also documented in `guide/04-assessment.md` §4.4). Frame feedback around the stage to revisit and a concrete next move.

## The Friction Stems
[All three from FRAMEWORK.md, verbatim. Apply in Mode 1. Check for evidence of friction in Modes 2 and 3.]

## The Academic Branch diagnostic
[The four-point map from FRAMEWORK.md / guide Part 2, used in Modes 2 and 3 to locate where the loop broke down.]

---

*Reality Audit Framework © 2026 Sandra Robinson · Big Wella. Licensed CC BY 4.0. Source: https://github.com/bigwellaadmin-dev/reality-audit. Please cite per the CITATION.cff in the repository.*
```

## Notes

- All verbatim content (Friction Stems, RAG text, Relief/Curiosity, Academic Branch checks, diagnostic, cheat sheet) must match `docs/FRAMEWORK.md` exactly.
- The `description` field determines when Claude loads this skill — be precise about triggers, and lead with the sycophancy/Hype-Man language since that is how users will describe the problem.
- **The recursive note is mandatory.** The skill is itself an agreeable AI and must say so near the top: instruct Claude to apply Reality Audit to itself, produce friction rather than relief, and treat the learner relaxing into its guidance as the warning sign. This is the skill's signature and the thing that keeps it honest. See `skill/README.md`.
- The licence line at the end is mandatory and must include the repository URL.
- Do not credit any institution other than Sandra Robinson · Big Wella. Reality Audit is sole-authored.
- Keep the skill file under ~450 lines. The current build is around 300. If the body grows, factor reference material into separate files in the same skill folder.
