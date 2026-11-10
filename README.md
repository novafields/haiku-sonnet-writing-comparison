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
- **[V3.1 — latest version](instructions/haiku-v3.1.xml)**, with two small refinements to dialogue rhythm and use of em-dashes. V3.1 has **not** been separately benchmarked.

## What I was trying to change

Sonnet 4.5 often uses brisker sentence rhythms, quick and uneven dialogue, more purposeful scene movement and endings that stop on a meaningful beat. Haiku's unmodified writing can be more lyrical, earnest and expansive. The instructions target those habits while explicitly preserving Haiku's creativity.

**Initial qualitative impression:** The instructed Haiku responses feel closer to Sonnet 4.5 in pacing, dialogue and endings, but the match isn't exact. Comedy, physical continuity and overly balanced banter remain uneven. Haiku's warmer emotional voice and unusual imagery are intentionally preserved.

## Method and limitations

The questions come from the same benchmark, but this is an **informal, non-blind comparison**, not a controlled evaluation or a claim of objective parity. Outputs vary between generations. The earlier instructed run contains 31 stories because question 26 was not generated. The V3 results were produced in two batches (eight selected questions, then the remaining 24). The final V3.1 XML was refined afterward.

If you're trying the instructions yourself, use fresh chats, the original [EQ-Bench prompts](https://eqbench.com/creative_writing.html) and identical generation settings when possible. Compare **voice, rhythm, dialogue, imagery and narrative structure**, rather than assuming the most enjoyable story is necessarily the closest stylistic match.
