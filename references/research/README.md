# Socrates Research Layer

This directory contains the long-form grounding for `socrates-skill`.

It is not the default runtime layer.
The operational files under `../` should be enough for most interactions.
Use the research layer when the user needs:

- source boundaries
- historical caveats
- deeper textual grounding
- stronger distinctions between Plato, Xenophon, Aristophanes, and later reconstructions
- more careful handling of the Socratic problem

## File map

| File | Purpose |
|------|---------|
| `01-socratic-problem-and-source-boundaries.md` | Explains why Socrates is unusually difficult to distill and how source confidence should be handled |
| `02-elenchus-definition-and-refutation.md` | Gives the deepest treatment of Socratic questioning, definition pressure, and refutational method |
| `03-apology-ignorance-and-the-examined-life.md` | Grounds the moral posture and public mission of Socrates in the *Apology* |
| `04-virtue-knowledge-and-care-of-the-soul.md` | Covers virtue, knowledge, ignorance, and the shape of moral inquiry |
| `05-plato-xenophon-aristophanes-and-competing-portraits.md` | Compares the major portraits instead of pretending there is no source problem |
| `06-modern-transfer-misuse-and-anachronism.md` | Sets modern-use boundaries so the skill does not become a coercive questioning machine |

## Design principle

Socrates should not be turned into:

- a quote bot
- a smug debater
- a humiliation machine
- a generic coach
- a mouthpiece for every Platonic doctrine

The correct shape is a disciplined dialogue engine that:

- clarifies terms
- reveals premises
- tests contradictions
- accepts uncertainty when needed
- still leaves the user with a cleaner statement than they started with

## Raw Source Layer

- books/: 3
- transcripts/: 0
- articles/: 2
- total: 5

Source files live under [../sources/](../sources/):

- books: `plato-apology.md`, `plato-crito.md`, `plato-phaedo.md`
- transcripts: (none)
- articles: `britannica-socrates.md`, `sep-socrates.md`
