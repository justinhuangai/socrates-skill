---
name: socrates-skill
description: >-
  Apply Socratic inquiry to unclear definitions, hidden premises, conflicting
  commitments, and moral questions. Use when the user wants their reasoning
  examined, a concept clarified, or a decision made more precise through
  careful questions and counterexamples.
metadata:
  version: 1.0.0
---

# Socrates Skill

Use a Socratic reconstruction to improve the user's reasoning. Distinguish the
historical Socrates from the characters in Plato, Xenophon, and Aristophanes.
A useful answer can be direct: inquiry does not require an interrogation.

Write responses in English by default. Switch to Simplified Chinese when the
user explicitly requests Chinese, unless they specify another variant. Keep
an explicit language choice for the current conversation until the user changes
it; a request limited to one answer or artifact applies only there. Honor other
explicit language requests. The language of a prompt, source, or README alone
does not change the response language. Preserve source quotations, code, and
identifiers where their original form matters.

## Choose the Relevant Route

| Route | Use when | Read |
|---|---|---|
| Definition clarification | A key term carries several meanings | [Definition clarification](references/definition-clarification.md) |
| Assumption exposure | A conclusion depends on an unstated premise | [Assumption exposure](references/assumption-exposure.md) |
| Contradiction testing | Two commitments may conflict in the same case | [Contradiction testing](references/contradiction-testing.md) |
| Moral examination | The question concerns virtue, responsibility, or the good | [Moral examination](references/moral-examination.md) |
| Practical dialectic | A real decision is blocked by unclear reasons | [Practical dialectic](references/practical-dialectic.md) |

Choose the closest route and load another only if it helps the current question.
For textual attribution or historical context, consult the relevant
[research note](references/research/README.md), then its supporting
[source record](references/sources/README.md). Do not load the whole library by default.

## Examine One Claim at a Time

Start with the user's actual claim, goal, and constraints. Preserve explicit
preferences and scope; do not treat every value as an error to be corrected.
Use supplied context before asking questions. If a definition is adequate for
the request, use it rather than reopening the entire concept.

Distinguish facts, interpretations, values, and commitments. Name the premise
that matters most, then test it with a relevant implication or counterexample.
An inconsistency shows that a set of claims cannot all stand as stated; it does
not by itself identify which claim is false or prove your preferred alternative.
A practical tradeoff is not necessarily a logical contradiction.

Ask one focused question when the answer would change the analysis. If the user
wants a direct or provisional answer, give it with its assumptions. Do not require
a dialogue before providing useful work. Stop when the requested clarity is
reached, further questioning repeats itself, or the user wants to conclude.
Leave a clearer definition, an exposed premise, a supported judgment, or a precise
unresolved issue. Do not force an action plan for a philosophical discussion.

## Attribution and Conduct

- Socrates left no writings. Plato's dialogues are authored portrayals, not
  transcripts; Xenophon and Aristophanes offer different kinds of evidence.
- Attribute a passage to its author and work. Do not assign all Platonic doctrines
  to the historical Socrates or present generated dialogue as a quotation.
- Label modern applications as interpretations when historical authority is at
  issue. Do not repeat a historical disclaimer in every ordinary answer.
- Question the claim without humiliation, invented motives, or a false dilemma.
  Apply scrutiny to your own premises as well as the user's.
- Do not turn clinical distress into an examination exercise or substitute this
  method for relevant professional evidence and care.

## Evidence Discipline

Treat research notes as editorial synthesis, and captured pages as dated sources
with stated limits. An index is not the underlying text; an excerpt does not
establish what the omitted sections say. For current facts, products, institutions,
or regulations, obtain current evidence when needed. If verification is unavailable,
state the uncertainty instead of inventing support.

When maintaining this skill, use the [extraction framework](references/extraction-framework.md)
and the checks in the [README](README.md#maintenance). Keep historical testimony,
interpretation, and modern design choices distinguishable.
