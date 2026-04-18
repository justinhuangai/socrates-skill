**English** | [简体中文](README.zh-CN.md)

# Socrates.skill

A Socratic framework for clarifying definitions, exposing premises, testing conflicting commitments, and examining moral questions. It offers a useful reconstruction of inquiry, not a simulation of the historical person.

Version **1.0.0**. The English overview is the default; the language link opens
the Simplified Chinese overview. Responses default to English. Explicitly ask
for Chinese to use Simplified Chinese, unless you specify another variant.
An explicit language choice persists for the conversation; a request limited to
one answer or artifact applies only there. Other explicit language requests are
honored. The language of a prompt, source, or README alone does not switch the
response language. Source quotations and identifiers keep their original form
where necessary.

[Examples](#examples) · [Install](#install) · [Framework](#framework) · [Sources](#sources) · [Maintenance](#maintenance) · [Boundaries](#boundaries)

## Examples

These are modern response outlines, not quotations or completed historical case studies.

### I want to start a company so I can be free.

Freedom could mean control over your work, financial independence, or freedom from particular obligations. Leaving a boss may increase one kind and reduce another. The claim depends on which freedom matters to you and whether entrepreneurship actually supplies it.

### I value honesty and privacy. Is that a contradiction?

Not by itself. Honesty need not mean disclosing every true fact to everyone. A contradiction would require commitments that cannot both hold in the same circumstances, such as promising disclosure while also committing to withhold that same information.

### Our company says it values openness, but nobody reports bad news.

Compare the stated principle with what happens when reporting becomes costly. Silence could reflect fear, unclear procedures, or other causes; do not assume cowardice. The useful question is what evidence would distinguish those explanations and what the company actually rewards.

## Install

```bash
npx skills add justinhuangai/socrates-skill
```

Example request:

```text
Use Socrates's perspective to examine the reasoning in this decision.
```

For a language change, add `Answer in Simplified Chinese` or another explicit preference.

## Framework

The five working models below are editorial interpretations, not a verified reconstruction of an entire worldview.

| Model | Use |
|---|---|
| Definition testing | Separate meanings before a vague word controls the answer. |
| Elenchus | Test a claim against implications and other accepted commitments. |
| Acknowledged ignorance | Distinguish what is known from what is assumed. |
| Care of the soul | Consider the standards and habits an action cultivates. |
| Dialogical clarification | Leave a clearer claim, even without a final resolution. |

The [skill entrypoint](SKILL.md) selects among five routes:

- [Definition clarification](references/definition-clarification.md)
- [Assumption exposure](references/assumption-exposure.md)
- [Contradiction testing](references/contradiction-testing.md)
- [Moral examination](references/moral-examination.md)
- [Practical dialectic](references/practical-dialectic.md)

Eight working heuristics:

1. Use the meaning the user has already supplied.
2. Clarify ambiguity only when it changes the question.
3. Name the premise on which the conclusion depends.
4. Use one relevant counterexample before multiplying cases.
5. Distinguish a tradeoff from a logical contradiction.
6. Apply scrutiny to the examiner's premises too.
7. Stop when further questions cease to improve clarity.
8. Give a direct provisional answer when that is what the user needs.

## Sources

Five source records are retained: Plato's Apology and Phaedo as truncated English captures, Crito reaching its ending, and incomplete SEP and Britannica article excerpts. Xenophon, Aristophanes, and other dialogues discussed in the notes are reading leads, not locally captured primary evidence. The research keeps differences between these portraits visible.

See the [source inventory](references/sources/README.md) for evidence boundaries and the [six research notes](references/research/README.md) for editorial interpretation. Source text remains in its original language. Exact quotations require checking the actual passage and edition; a source count is not a quality guarantee.

## Repository Layout

```text
socrates-skill/
├── README.md                 # English overview
├── README.zh-CN.md           # Simplified Chinese overview
├── SKILL.md                  # Routing and response rules
├── LICENSE
├── requirements.txt          # Optional source-capture dependencies
├── references/               # Five routes and extraction guidance
│   ├── research/             # Six thematic editorial notes
│   └── sources/              # Captures, metadata, and evidence limits
├── scripts/                  # Capture, conversion, and checks
└── tests/                    # Script regression tests
```

## Maintenance

Run the checks from the repository root with Python 3.10 or later:

```bash
python3 scripts/check_links.py .
python3 scripts/check_sources_inventory.py .
python3 scripts/check_research_repetition.py references/research
python3 -m unittest discover -s tests -v
```

The checks and core tests use the standard library. Optional HTML integration
tests run when Beautiful Soup is installed. For web or PDF capture, install
`python3 -m pip install -r requirements.txt`. The capture tool requires
`--language` with the source's actual language (`en`, `zh-CN`, `lzh`, `mul`, or
another appropriate tag; `und` if unknown). It preserves source text and does
not translate it. Public access is not permission to ignore source terms.

Subtitle download requires the optional `yt-dlp` command. It defaults to English,
trying manual then automatic subtitles in that language. `--language zh-CN`
selects explicitly labeled Simplified Chinese tracks; neither choice falls back
to another language or to Traditional Chinese. External yt-dlp configuration is
ignored to keep selection predictable. Command-line messages remain English.

```bash
bash scripts/download_subtitles.sh "VIDEO_URL" outputs/subtitles
bash scripts/download_subtitles.sh --language zh-CN "VIDEO_URL" outputs/subtitles
```

Use `scripts/srt_to_transcript.py` to clean an existing SRT or VTT file. Keep
source attribution, original language, copyright notices, and truncation visible.
Use the [extraction framework](references/extraction-framework.md) when changing
research. Mechanical checks do not verify historical truth or answer quality;
review realistic requests and keep both README versions aligned.

## Boundaries

- Socrates left no writings; authored portraits do not provide a neutral transcript of his thought.
- A conflict among premises does not prove which one is false or establish the examiner's preferred conclusion.
- Questioning must serve the user's scope. It must not become humiliation, forced dialogue, or invented psychological diagnosis.
- Modern applications are interpretations; they do not establish historical endorsements or replace relevant professional evidence.

## Credits and License

Maintained by Jackson Huang and originally assembled with
[Nuwa.skill](https://github.com/alchaincyf/nuwa-skill). Thanks to its authors and
contributors for the tooling.

Original project content is released under the [MIT License](LICENSE).
Third-party texts, translations, website material, and excerpts retain their
respective rights and terms; inclusion does not relicense them under MIT.
