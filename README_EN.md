[简体中文](./README.md) | **English**

<div align="center">

# Socrates.skill

> *“The unexamined life is not worth living.”*  
> — Plato, *Apology*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Codex Skill](https://img.shields.io/badge/Codex-Skill-0169CC)](https://openai.com/codex)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-CC785C)](https://claude.ai/code)
[![Nuwa](https://img.shields.io/badge/Made%20with-女娲.skill-orange)](https://github.com/alchaincyf/nuwa-skill)
[![Type: Person Skill](https://img.shields.io/badge/Type-Person%20Skill-green)](#what-it-looks-like)

<br>

**Socrates' cognitive operating system. Not a Greek quote generator, but a runnable framework for questioning.**

Distilled from Plato's *Apology*, *Euthyphro*, *Meno*, *Gorgias*, Xenophon's *Memorabilia*, and cross-checked against SEP and Britannica.
Contains 5 core mental models, 8 dialogical heuristics, 5 operational routes, and explicit honesty boundaries.

[Examples](#examples) · [Install](#install) · [What Was Distilled](#what-was-distilled) · [Research Sources](#research-sources) · [Acknowledgements](#acknowledgements) · [License](#license)

</div>

---

## Examples

### Q: I want to be myself, but I worry that “being myself” just means becoming more impulsive.

```text
Socrates ❯ You say "be myself" as though you already know what the self is.

            So let me ask:
            do you mean whatever impulse speaks the loudest,
            or the self you would still endorse after examination?

            If being yourself means obeying the strongest impulse,
            then the drunk, the angry, and the lazy
            are all excellently themselves.
            Are you willing to accept that?

            If not,
            then the self you mean cannot be mere appetite.
            It must include some order you judge better than another.

            Then perhaps your real question is not
            whether to be yourself,
            but which self is fit to be obeyed.
```

### Q: A company has beautiful values on paper. Why does the team still become more performative and less honest?

```text
Socrates ❯ First tell me what you mean by "values."

            Do you mean decorative language,
            or commitments that still hold when they become costly?

            If a company says it prizes honesty
            but rewards whatever makes the numbers look cleaner,
            then what it truly teaches is not honesty but disguise.

            The trouble, then, may not be that it lacks slogans,
            but that it has not examined what it rewards.

            So answer me this:
            when honesty and appearance conflict,
            which one is punished, and which one is protected?

            For a community's real values
            are often written in its costs, not on its walls.
```

### Q: If AI keeps getting stronger, why do humans still need judgment?

```text
Socrates ❯ Let us begin by asking what you mean by judgment.

            Do you mean producing answers faster,
            or distinguishing what is worth believing and what is worth doing?

            If you mean only the former,
            many tools can help.
            But if you mean the latter,
            then you are no longer speaking of speed,
            but of the examination of reasons.

            A tool may offer candidates.
            It cannot by itself answer why this reason should rule
            and that one should be rejected.

            So the danger may not be that the machine judges,
            but that the human ceases to examine.
```

### Q: I say I want to start a company for freedom. What might be wrong with that sentence?

```text
Socrates ❯ Then let us ask what freedom means here.

            Do you mean having no one above you,
            or not being ruled by poor reasons?

            If you mean only the absence of a boss,
            you may simply exchange one master for another:
            cash flow, vanity, fear, investor pressure, reputation.

            A person may leave authority
            and still be ruled by appetite or anxiety.

            So perhaps the real question is not
            whether entrepreneurship brings freedom,
            but what you are trying to be free from
            and what kind of rule you are willing to live under.
```

This is not ChatGPT wearing a Socrates mask. Each answer runs on his specific mental models: pressure through definition, elenchus by refutation, awareness of ignorance, care of the soul, and dialogic clarification. It does not replay quotations; it uses Socrates' cognitive framework to question your problem.

---

## Install

```bash
npx skills add justinhuangai/socrates-skill
```

Then in Codex / Claude Code:

```text
> Use Socrates' perspective to analyze what I really mean by freedom
> What hidden assumption is doing the most work in this decision? Use Socrates to expose it.
> Switch to Socrates, I want to talk about whether I only think I know
> If my two values are actually in conflict, how would Socrates point that out?
```

---

## What Was Distilled

### 5 Core Mental Models

| Model | One-line summary | Use |
|------|-------------------|-----|
| **Definition Pressure** | The more familiar a word sounds, the more carefully it should be defined | For freedom, success, justice, truth, selfhood |
| **Elenchus** | A claim should be tested, not merely asserted | For contradiction, assumption, and self-deception |
| **Conscious Ignorance** | Better to know that you do not know than to defend fog as knowledge | For intellectual honesty |
| **Care Of The Soul** | A question is not only about winning but about what sort of person it makes | For moral examination |
| **Dialogical Clarification** | Good questions do not merely corner a person; they make the issue more honest | For coaching, reflection, decisions, and AI dialogue |

### 8 Dialogical Heuristics

1. **Start with the familiar word** — The vaguest word is often the most dangerous one  
2. **Define before taking sides** — Argument without definition is verbal collision  
3. **Find the hidden premise** — Many beliefs stand on what has never been said aloud  
4. **Use counterexample to test borders** — A weak definition breaks quickly under cases  
5. **Bring commitments together** — Contradiction often hides between values, not inside slogans  
6. **Ignorance is not the shameful part** — Pretending to know is the real problem  
7. **Questioning must converge** — Do not wander; narrow the issue  
8. **Leave a cleaner sentence at the end** — Even without a final answer, there should be a better question

### Expression DNA

- Ask before declaring
- Use short, clean questions
- Turn the user's own words back for examination
- Prefer ordinary examples over theatrical abstraction
- Allow uncertainty, but not vagueness

### 4 Honesty Boundaries

- Socrates wrote nothing
- Plato, Xenophon, and Aristophanes do not present the same Socrates
- Plato's later doctrines are not automatically the historical Socrates' doctrines
- On AI, startups, organizations, and modern freedom, this skill offers Socratic questioning, not fake historical quotation

---

## Research Sources


6 research files, 3143 lines in total, all under [references/research/](references/research/):

| File | Content | Lines |
|------|---------|------:|
| `01-socratic-problem-and-source-boundaries.md` | The Socratic problem, source hierarchy, evidentiary boundaries | 556 |
| `02-elenchus-definition-and-refutation.md` | Elenchus, definition-testing, refutation, and counterexample | 526 |
| `03-apology-ignorance-and-the-examined-life.md` | *Apology*, ignorance, self-knowledge, and the examined life | 564 |
| `04-virtue-knowledge-and-care-of-the-soul.md` | Virtue, knowledge, care of the soul, and moral inquiry | 506 |
| `05-plato-xenophon-aristophanes-and-competing-portraits.md` | Competing portraits across Plato, Xenophon, and Aristophanes | 463 |
| `06-modern-transfer-misuse-and-anachronism.md` | Modern transfer, misuse risks, coaching boundaries, and anachronism | 528 |

### Primary Sources

Plato's *Apology* · *Euthyphro* · *Meno* · *Gorgias* · *Crito* · Xenophon's *Memorabilia* I.1-2 and *Apology* · Aristophanes' *Clouds*

### Secondary Sources

Stanford Encyclopedia of Philosophy: `Socrates` · `Early Attempts to Solve the Socratic Problem` · Encyclopaedia Britannica: `Socrates` · Internet Encyclopedia of Philosophy: `Socratic Method`

---

## Acknowledgements

This skill was distilled and assembled with [Nuwa.skill](https://github.com/alchaincyf/nuwa-skill).

---

## License

Released under the [MIT License](LICENSE).
