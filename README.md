# Haiku 5.5 → Sonnet 4.5: A writing-style experiment

Can custom XML instructions make **Claude Haiku 5.5 sound more like Sonnet 4.5** without sacrificing Haiku's original imagery and warmth?

I compared their creative writing using the 32 prompts in [EQ-Bench Creative Writing v3](https://eqbench.com/creative_writing.html), then iterated on Haiku's instructions with help from GPT-6 and GLM 5.3. The aim was **stylistic similarity**, not necessarily a higher creative-writing score.

## Read the stories

| Set | Stories | Transcript |
| --- | ---: | --- |
| Sonnet 4.5 reference | 32 | [EQ-Bench's original results](https://eqbench.com/results/creative-writing-v3/claude-sonnet-4.5.html) |
| Haiku 5.5, no instructions | 32 | [Original Haiku outputs](results/haiku-5.5-original.md) |
| Haiku 5.5, earlier custom instructions | 31 | [Earlier instructed outputs](results/haiku-5.5-earlier-instructed.md) |
| Haiku 5.5, V3 | 32 | [V3 outputs](results/haiku-5.5-v3.md) |

Each transcript contains **only the generated stories**. No Claude conversation history, account data, chat links or attachments are included. The original benchmark prompts are available on EQ-Bench.

## Custom instructions

- **[V3 — version used for the initial eight-story test](instructions/haiku-v3.xml)**
- **[V3.1 — recommended version](instructions/haiku-v3.1.xml)**, with two small refinements to dialogue rhythm and use of em-dashes. V3.1 has **not** been separately benchmarked.
- **[V4 — experimental simplified version](instructions/haiku-v4-experimental.xml)**, which consolidates overlapping rules into broader stylistic principles. It is **not a proven improvement** over V3 or V3.1.

### V4 — Experimental

V4 uses fewer, more generalized rules to give Haiku greater freedom across genres. It was tried against all 32 EQ-Bench Creative Writing v3 prompts. Informal comparisons suggest strengths in dialogue, humour and genre adaptability, but weaknesses remain in following specific prompt requirements.

**All 32 V4 responses were generated in one long conversation**, so accumulated context may have influenced the results. The comparisons were non-blind, single-generation and not a controlled test. V4 has **not demonstrated consistent superiority over V3 or V3.1**. V3.1 remains the recommended version. The V4 responses are not included in the published V3 transcript set.

## Sonnet 4.5 writing-style Skill

- **[Generalized writing Skill (SKILL.md)](skills/sonnet-4-5-writing-style/SKILL.md)** — applies the target style across fiction, essays, articles and practical writing. This is a later, experimental adaptation and was **not used to produce the benchmark transcripts above**. Initial separate Skill-only tests suggest promising dialogue and humour, but they are too limited to establish superiority over the XML instructions.

## What I was trying to change

Sonnet 4.5 often uses brisker sentence rhythms, quick and uneven dialogue, more purposeful scene movement and endings that stop on a meaningful beat. Haiku's unmodified writing can be more lyrical, earnest and expansive. The instructions target those habits while explicitly preserving Haiku's creativity.

**Initial qualitative impression:** The instructed Haiku responses feel closer to Sonnet 4.5 in pacing, dialogue and endings, but the match isn't exact. Comedy, physical continuity and overly balanced banter remain uneven. Haiku's warmer emotional voice and unusual imagery are intentionally preserved.

## Method and limitations

The questions come from the same benchmark, but this is an **informal, non-blind comparison**, not a controlled evaluation or a claim of objective parity. Outputs vary between generations. The earlier instructed run contains 31 stories because question 26 was not generated. The V3 results were produced in two batches (eight selected questions, then the remaining 24). The final V3.1 XML was refined afterward.

If you're trying the instructions yourself, use fresh chats, the original [EQ-Bench prompts](https://eqbench.com/creative_writing.html) and identical generation settings when possible. Compare **voice, rhythm, dialogue, imagery and narrative structure**, rather than assuming the most enjoyable story is necessarily the closest stylistic match.
