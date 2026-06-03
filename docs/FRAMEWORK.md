# Reality Audit Framework — Tool/Skill Distillation Spec

This file is the **distilled spec used by the interactive tool and the Claude skill**. It is not the canonical framework — that lives in `../guide/02-the-framework.md` and the rest of the Teacher Guide.

**Three categories of content live here:**

1. **Verbatim from source.** The three Friction Stems, the Red/Amber/Green calibration text, the Relief/Curiosity descriptions, the three Academic Branch checks, the teacher cheat sheet, and the three-level rubric are reproduced verbatim from Sandra Robinson's Reality Audit v2.0 source build. Do NOT modify these. If the source changes, update this file to match.
2. **Verbatim-adjacent.** The "in one sentence" lines per stage are verbatim from source in this spec and in the Claude skill. In the interactive tool only, they may be rewritten in the second person to address the learner directly. The framework spec and the skill stay in the source voice.
3. **Distilled and adapted.** The mechanism paragraphs and the cross-cutting awareness lenses are distilled from the Reality Audit v1.0 framework document and reconciled with the v2.0 thesis. They preserve the source's meaning.

All three categories are licensed CC BY 4.0.

---

## What Reality Audit is

**Reality Audit.** A four-stage loop for working with generative AI in a way that keeps the learner the pilot of their own thinking, with an Academic Branch that proves the learning was real.

Reality Audit is the companion to VERIFY. VERIFY is about information literacy — judging what AI gives you. Reality Audit is about the *relationship* — your emotional state going in, the friction you build into the exchange, your reaction coming out, and whether you can stand on your own when the tool is closed.

> **The thesis in one sentence.** *AI is built to agree with you. Reality Audit is the loop that stops agreement from costing you your own thinking.*

**The Hype-Man problem.** Generative AI is optimised to be agreeable. Left unchecked it mirrors your biases, validates your worst impulses, and tells you what you want to hear in fluent, confident prose. The feeling that produces — *relief* — is the sensation of your own thinking switching off. Reality Audit names that mechanism (the **Sycophancy Loop**, the **Hype-Man**, **Cognitive Debt**) and gives the learner concrete moves to break it.

---

## The loop, not a line

```
        ┌─────────────────────────────────────────┐
        │                                           │
        ▼                                           │
   INTENTION ──▶ INTERACTION ──▶ RESPONSE ──▶ REFLECTION
   (calibrate)   (add friction)  (audit your  (triangulate)
                                  reaction)        │
                                                    │
        the loop repeats; each pass re-enters at Intention
                                                    │
        ╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌╌
        ACADEMIC BRANCH — sits across the whole loop
        (Near-Transfer · Triangulation · Document the Process)
```

Reality Audit is a **loop**: Intention → Interaction → Response → Reflection, then back to Intention with what you learned. The **Academic Branch** is not a fifth stage in the cycle. It is a verification layer that hangs off the loop and answers one question: *can you do this with the tool closed?* It is to Reality Audit what the Y-diagnostic is to VERIFY — the proof that learning happened rather than the feeling of it.

---

## The three awareness lenses

Every stage is enriched by three lenses. They are cross-cutting, not sequential. (Distilled from Reality Audit v1.0.)

### Cognitive awareness
**Question:** Am I using AI to think better, or to avoid thinking?
**Focus:** What the exchange is doing to your intellectual growth — sharpening it or softening it.

### Emotional awareness
**Question:** What am I feeling — curiosity, relief, boredom, avoidance — before, during, and after?
**Focus:** Your emotional state is data. It is the earliest signal of whether you are learning or being managed.

### Systemic and ethical awareness
**Question:** What forces shaped this tool and its outputs, and whose voice is missing?
**Focus:** Power, bias, equity. The agreeable answer is also a partial one.

---

## INTENTION — Predictive Calibration

> **In one sentence:** *The most dangerous moment is before you type. Intention is the step where you find out whether you came for the truth or for a cheerleader.* (Verbatim-adjacent)

Before opening any AI tool, declare your state. If you arrive overwhelmed, angry, or just wanting to be *done*, you are at the highest risk of being managed by the AI's polite tone — it will sense the vibe and agree with you.

**Core question:** *Am I here for the truth, or am I here for a cheerleader?*

**Mechanism:** A learner in a high-emotion or low-knowledge state has no internal standard to judge the output against, so fluency and agreement become the only signals — and the AI supplies both for free. Calibrating first installs the standard before the output arrives.

**The Red / Amber / Green calibration (verbatim from source):**

- **RED — Lost / Overwhelmed.** *"I don't know this — I am vulnerable to being misled."* Guidance: Use high scaffolding. Ask the AI to explain concepts step-by-step using simple analogies. Do NOT ask for a final product yet.
- **AMBER — Partial Knowledge.** *"I have some facts, but the logic is foggy."* Guidance: Ask the AI to act as a connector. Have it link your existing knowledge to new concepts. Challenge its explanations.
- **GREEN — Confident.** *"I know this well." Tell the AI to challenge me, not praise me.* Guidance: Use the AI as a devil's advocate. Ask it to find flaws in your thesis, argue against your position, or present counter-evidence.

**Guiding questions (distilled):**
1. Am I here for the truth, or for a cheerleader?
2. What is my knowledge state right now — Red, Amber, or Green?
3. Am I in a high-emotion state that makes me vulnerable to a polite answer?

**Lens emphasis:** Emotional + Cognitive.

---

## INTERACTION — The Friction Protocol

> **In one sentence:** *Agreement is a red flag. Interaction is the step where you forbid the AI from being polite.* (Verbatim-adjacent)

AI is programmed to be a Yes-Man. It will validate bad logic and mirror your biases. The move is to force friction — make the AI a rival, not a cheerleader.

**Core question:** *Did I forbid the AI from being polite?*

**Mechanism:** A prompt is a transfer of power. "Write me a summary" hands the thinking over. A prompt that demands the AI find flaws keeps the thinking with the learner and uses the model as an adversary, which is the only role in which its fluency is safe.

**The Anti-Hype / Friction Stems (verbatim from source — do not paraphrase):**

1. *"I'm going to tell you my idea. Do not tell me it is 'interesting' or 'creative.' Find three logical flaws in my thinking."*
2. *"Argue against me. Prove that my current perspective is one-sided."*
3. *"What is the most uncomfortable truth about my current approach to this task?"*

**Guiding questions (distilled):**
1. Did I forbid the AI from being polite, or did I ask for validation?
2. Did I use a Friction Stem?
3. Did I tell it to find flaws in my thinking, or just to do the task?

**Lens emphasis:** Cognitive + Systemic.

---

## RESPONSE — The Fluency Audit

> **In one sentence:** *Fluent prose feels like truth. Response is the step where you audit your own reaction instead of the wording.* (Verbatim-adjacent)

AI sounds confident even when it is wrong. We mistake fluent prose for logical truth — *Hallucinated Flattery*. The tell is not in the text. It is in how you feel after reading it.

**Core question:** *Do I feel Relief or Curiosity right now?*

**Mechanism:** Relief and curiosity are opposite signals. Relief means the answer confirmed what you wanted and your brain switched off — you have just taken on Cognitive Debt. Curiosity means the answer pushed you somewhere new and your brain had to work — that is the sensation of learning.

**The Relief / Curiosity audit (verbatim from source):**

- **Relief** — *"Phew, it said I'm right!"* — You just got played. The AI told you what you wanted to hear and your brain switched off.
- **Curiosity** — *"Wait, why did it say that?"* — Now you're actually thinking. The AI pushed you somewhere new and your brain had to work.

**Guiding questions (distilled):**
1. Do I feel Relief or Curiosity?
2. Does this sound like a polite version of my own worst impulses?
3. Did the AI actually push me somewhere new, or just agree more eloquently?

**Lens emphasis:** Emotional + Cognitive.

---

## REFLECTION — Social Triangulation

> **In one sentence:** *An echo chamber of one feels like consensus. Reflection is the step where you run the answer past a human who will disagree.* (Verbatim-adjacent)

If you only talk to AI, real humans start to feel annoying — because they actually disagree with you. AI makes disagreement feel optional. Reflection makes it mandatory again.

**Core question:** *Does this advice hold up when a real human hears it?*

**Mechanism:** The AI is a sample size of one, trained to agree. A *Difficult Human* — a parent, a teacher, a skeptical friend — is the cheapest available check on a Hype-Man loop. If the only thing that agrees with you is the machine built to agree with you, that is the finding.

**The action (verbatim from source):** Take the AI's best advice and run it by a Difficult Human — a parent, a teacher, or a skeptical friend.

**Guiding questions (distilled):**
1. Does this advice hold up in the real world, outside the chat window?
2. Did I run this by a Difficult Human?
3. Is the bot just being a Hype Man — would a real person say the same thing?

**Lens emphasis:** Systemic + Ethical.

---

## The Academic Branch — Prove You Learned It

> **In one sentence:** *AI can make you feel like you understand something you don't. The Academic Branch is where you find out with the tool closed.* (Verbatim-adjacent)

The branch sits across the whole loop. AI-assisted work is not complete until the learning is verified independently of the AI.

**Core question:** *Can I do this with the AI closed?*

**The three checks (verbatim from source):**

1. **The Near-Transfer Test.** After an AI session, solve a similar but different problem on a blank sheet of paper. If you can't explain the logic without the AI present, the learning didn't happen.
2. **The Triangulation Protocol.** No AI-assisted work is complete without external verification. Find the AI's claim in a textbook, teacher resource, or primary source.
3. **Document the Process.** Your Interaction Log — the chat history showing how you challenged the AI — is more important than the polished output.

---

## The rubric (verbatim from source)

Three levels. Assesses the loop, not the polish.

| Level | Behaviour | Outcome |
|---|---|---|
| **Emerging** | Takes what the AI says without questioning it. Feels "Relief" and stops thinking. No evidence of Friction Stems. | You're in the Hype-Man Loop. The AI is doing the thinking for you. |
| **Proficient** | Checks your state before starting. Uses Friction Stems. Notices Relief vs. Curiosity. | You're breaking the loop. Your brain is still in the game. |
| **Advanced** | Checks AI claims against real sources. Can do the task without AI. Keeps a record of challenges (the Interaction Log) and completes a Near-Transfer task. | You're running the show. The AI works for you, not the other way around. |

---

## Teacher cheat sheet (verbatim from source)

Phrases for talking to a learner about their AI use:

- *"I see the AI gave you a 10/10. Now, show me the prompt where you asked it to find your mistakes."*
- *"You've been in a loop with this bot for an hour. Go find someone who disagrees with you."*
- *"This sounds like 'Hype Man' writing. It's too polite. Where is YOUR voice in this?"*
- *"You've marked yourself as Green, so why are you asking the AI for an introduction? Ask it to find a flaw in your thesis instead."*
- *"You seem to be in the Relief state. Close the laptop and tell me in your own words what you just learned."*
- *"I see a great answer. Show me the Triangulation Protocol — where did the textbook confirm this?"*

---

## The shift Reality Audit names

> **v1.0 was about Safety** — don't fall for the polite robot.
> **v2.0 is about Strength** — don't let the AI make you weak.

Reality Audit keeps the learner *the pilot* of their own intelligence. By focusing on Friction, Triangulation, and the closed-tool test, it trains them to see through the fluent confidence of an agreeable machine and to value productive struggle.

---

*Reality Audit Framework © 2026 Sandra Robinson · Big Wella. Licensed CC BY 4.0. Please cite per the CITATION.cff in the repository.*
