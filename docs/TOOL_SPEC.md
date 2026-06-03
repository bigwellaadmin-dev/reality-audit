# tool/index.html — Build Specification

Read `docs/FRAMEWORK.md` for all stage content before building. All step text comes from `FRAMEWORK.md` — do not invent.

## Positioning

The tool is a **student companion**, not a self-management tool. The student opens it alongside their AI work (chat window, document, printout) and walks the loop: calibrate, force friction, audit their reaction, triangulate, then prove the learning. The tool **does not capture or store the AI output**; it provides the structure, the Friction Stems to copy, and the reflection prompts.

The teacher's role is to review the **Reality Audit Log** the tool exports and to have the conversations the guide describes — especially the Reflection (Difficult Human) and the Academic Branch (Near-Transfer) checks, which happen with people and blank pages, not in the tool. "Teacher present" means present in the review and the friction that follows the log, not present in the tool itself.

The framework states it plainly (Guide, Part 1, §1.3): Reality Audit is *a teaching framework that requires a teacher who is present and willing to be the friction.*

## Structure: a five-screen wizard

A linear wizard with a phase indicator. The four loop stages, then the Academic Branch.

1. **Intention** — Predictive Calibration
2. **Interaction** — The Friction Protocol
3. **Response** — The Fluency Audit
4. **Reflection** — Social Triangulation
5. **Academic Branch** — Prove You Learned It

Next is always enabled; nothing is locked. A "Start over" reset returns to stage 1 and clears state.

## Splash screen

- "Reality Audit" large in `--font-display`.
- Subheading: *"The Reality Audit."*
- Tagline (verbatim): *"AI is built to agree with you. Walk the loop so it sharpens your thinking instead of softening it."*
- Single CTA: "Begin".
- Small attribution: *"Sandra Robinson"* in uppercase tracking.
- A quieter link: *"Read the Teacher Guide →"* to `https://github.com/bigwellaadmin-dev/reality-audit`.

## Per-stage screen

1. Stage name + subtitle (e.g. "Intention — Predictive Calibration"), large, `--font-display`, in `--color-{stage}`.
2. **In-one-sentence line** (verbatim from `FRAMEWORK.md`, italic, accent colour). The tool may render it in the second person.
3. The **core question** in a highlighted callout (`"Am I here for the truth, or for a cheerleader?"`).
4. A **"The Hype-Man Trap"** warning callout per stage (verbatim trap text from source).
5. Stage-specific interactive element (below).
6. Guiding-question textareas — not required, no submit.
7. Back / Next.

## Stage-specific interactions

- **Intention — RAG selector.** Three selectable cards: RED / AMBER / GREEN, each with its description (verbatim). Selecting one reveals its guidance text below. Single-select; selection preserved within the session.
- **Interaction — copyable Friction Stems.** The three stems (verbatim) as cards, each with a copy button. `navigator.clipboard.writeText()` with the file:// fallback (see Export).
- **Response — Relief vs Curiosity.** Two selectable cards (verbatim descriptions). Selecting Relief surfaces a gentle prompt to go back and add friction; selecting Curiosity confirms the signal. Single-select.
- **Reflection — action checklist.** Three toggleable items (share with a Difficult Human; ask "is the bot just being a Hype Man?"; if they disagree, explore why before accepting either view). Toggling preserves state.
- **Academic Branch — the three checks + self-rubric.** The three checks (verbatim) as cards. Below them, the three-level self-assessment rubric (Emerging / Proficient / Advanced, verbatim outcomes) for the student to locate themselves. Then the export controls.

## Export — the Reality Audit Log

"Export Reality Audit Log" button at the end of the Academic Branch:

- Generates plain text: `Reality Audit Log — DD/MM/YYYY HH:mm` followed by each stage, the RAG state chosen, the Friction Stems used, the Relief/Curiosity reaction, the Reflection checklist state, and every guiding-question response.
- Australian locale date (DD/MM/YYYY), 24-hour time.
- Attempts `navigator.clipboard.writeText()`. On rejection (file://, blocked permission), falls back to selecting text in a hidden `<textarea>` with a "Copy with ⌘C / Ctrl-C" prompt.
- Success confirmation: *"Copied — paste into your LMS or email to your teacher."*
- Secondary "Print" button → `window.print()` with the print stylesheet.

## State management

All state in a single in-memory JS object. No persistence of any kind. Page refresh intentionally resets. A banner near export reads: *"Your responses are not saved — export before closing."*

## Rendering contract

Iterate stored values and assign via `textContent` only. Never `innerHTML`. Removing the HTML-parsing path is what protects against XSS — there is no untrusted-HTML hop to sanitise because there is no HTML hop at all.

## Brand tokens

- Accent palette from the v2 build: orange (Intention), cyan (Interaction), violet (Response), magenta (Reflection), teal (Academic Branch). Each must pass WCAG AA (≥ 4.5:1) against its background for any text it carries.
- Fonts self-hosted in `tool/fonts/` (display + body), bundled under the SIL Open Font Licence. No third-party network requests.
- Favicon set is bundled in `tool/` alongside the fonts.

## Transitions

200ms ease, opacity fade only. No transforms on stage changes.

```css
@media (prefers-reduced-motion: reduce) {
  * { transition: none !important; animation: none !important; }
}
```

## Accessibility checklist

- [ ] All inputs, toggles, and buttons reachable by Tab
- [ ] Enter/Space activates buttons and toggles
- [ ] `aria-label` on icon buttons and selectable cards
- [ ] `aria-live="polite"` on the stage region (announces stage changes)
- [ ] Focus ring always visible — never `outline: none` without a replacement
- [ ] Colour + text/icon together for all state (selected RAG, completed stage) — never colour alone
- [ ] Contrast ≥ 4.5:1 for all body text
- [ ] `prefers-reduced-motion` honoured
- [ ] `<noscript>` block explains the tool needs JS and links to the Teacher Guide

## Content Security Policy

Single-file, inlined styles and JS, self-hosted fonts, no third-party origins:

```
default-src 'none'; style-src 'self' 'unsafe-inline'; font-src 'self'; script-src 'unsafe-inline'; img-src 'self' data:; connect-src 'none'; frame-ancestors *; base-uri 'none'; form-action 'none';
```

`frame-ancestors *` permits LMS embedding (Moodle, Canvas).

## Print stylesheet

- Hide header, stage navigation, export controls.
- Show all five stages and responses in full, linear order.
- Title at top: `Reality Audit Log — DD/MM/YYYY HH:mm`.
- Black text on white, no background colours.
- Page breaks between stages where natural.
