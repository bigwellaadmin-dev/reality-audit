# Contributing to Reality Audit

Thank you for thinking about contributing. Reality Audit is an open educational framework, and the most valuable contributions are not always code.

## What this project welcomes

In rough order of usefulness:

1. **Classroom-tested feedback.** You used Reality Audit with real students. Something landed, something did not. Tell us. Use the [Classroom feedback issue template](.github/ISSUE_TEMPLATE/classroom-feedback.md). This is the single most useful kind of contribution.
2. **Translations and adaptations** for other education systems. The framework is written for an Australian secondary context but the cognitive and emotional principles apply anywhere. Open an issue first to discuss scope.
3. **Bug or accessibility fixes** to the interactive tool or the Claude skill.
4. **Improvements to the build specs** in `docs/`.
5. **Documentation improvements** to the README, the guide files, or the rubrics.

## What needs careful discussion before a PR

The **framework text itself** is canonical. That includes:

- The four loop stages (Intention, Interaction, Response, Reflection) and their definitions
- The Academic Branch and its three checks
- The three Friction Stems (verbatim from the source)
- The Red/Amber/Green calibration text (verbatim)
- The Relief/Curiosity descriptions (verbatim)
- The Academic Branch diagnostic
- The "in one sentence" lines per stage
- The rubric criteria and the teacher cheat sheet

These are the published intellectual work of Sandra Robinson, and changes need to be discussed first. Open an issue with the proposed change, your reasoning, and any classroom evidence before opening a PR.

The **distilled tool wording** (the plain-language guiding questions) is more open to revision because it was adapted for accessibility and is not verbatim from source. PRs welcome.

## Style and tone

Match the existing voice where you can. It is direct, treats the reader as intelligent, names limits honestly, and uses the "It is not X. It is Y." pattern when correcting a misreading. It produces friction, not reassurance. No hedging, no qualifying language, no marketing voice.

## How to open a good issue

- Use one of the [issue templates](.github/ISSUE_TEMPLATE/)
- Be specific about year level, subject, task, and what happened
- Quote any wording you are responding to so the maintainer can find it
- For tool bugs, include browser version and steps to reproduce

## How to open a good pull request

- Use the [pull request template](.github/PULL_REQUEST_TEMPLATE.md)
- Keep PRs focused on one change at a time
- For tool changes, manually test in Chrome, Firefox, and Safari
- For skill changes, test in a Claude project
- Confirm the framework text is unchanged unless previously discussed
- Match the existing code style and indentation

## Repo structure

```
reality-audit/
├── README.md              Public landing page
├── LICENSE                CC BY 4.0
├── CITATION.cff           Machine-readable citation
├── CHANGELOG.md           Release history
├── CONTRIBUTING.md        This file
├── CODE_OF_CONDUCT.md     Contributor Covenant 2.1
├── SECURITY.md            Security reporting
├── .github/               Issue and PR templates, CI workflows
├── guide/                 Teacher Guide (Parts 1 to 4 plus Appendix)
├── skill/                 Claude SKILL.md file plus skill README
├── tool/                  Single-file interactive HTML companion
├── rubrics/               A to E and four-level rubrics
├── docs/                  Build specs (FRAMEWORK, TOOL_SPEC, SKILL_SPEC)
└── assets/                Screenshots and images
```

## Code of Conduct

All contributors are expected to follow the [Code of Conduct](CODE_OF_CONDUCT.md). In short: respectful, no harassment, focus on what is best for the community.

## Licence

By contributing, you agree that your contribution will be licensed under the same CC BY 4.0 licence as the rest of the project.
