# Sonnet 4.5 writing style: an experiment

Can a writing skill make newer Claude models **write like Claude Sonnet 4.5** in fiction, articles and personal essays?

This project started as an attempt to make **Claude Haiku 5.5** sound like Sonnet 4.5, using the 32 prompts in [EQ-Bench Creative Writing v3](https://eqbench.com/creative_writing.html). It ended as a writing-style skill now used with **Claude Sonnet 5.5**. The skill was developed with help from Fable 5.2, Opus 5.5 and GPT-6.

The aim is **stylistic fidelity to Sonnet 4.5**, not a higher creative-writing score.

## The skill

**[Read the writing skill (SKILL.md)](skills/sonnet-4-5-writing-style/SKILL.md)**

The skill covers three forms:

- **Fiction:** brisk sentences, untagged and uneven dialogue, one encounter that changes something, endings on a short line or reversal
- **Articles:** a magazine-feature shape, with a catchy colon headline, a lede before the first heading, evocative section titles, familiar idioms and a kicker ending
- **Personal essays:** a human first-person narrator, an opening on a specific moment, a tone that follows the topic, the lesson stated outright, and a quotable closing line

Across all three, it asks for frequent em-dashes, plain wording over clever, feelings and stakes stated directly, and a return to the opening at the end.

It also puts the user's requirements (person, tense, length, required scenes) ahead of every style rule, and allows quotes only from real sources.

### How to use it

Add it as a skill in Claude, or include it in a Claude Project's instructions. Then ask for fiction, an article or an essay as usual.

### What testing showed

These were informal, non-blind, single-sample tests, comparing Sonnet 5.5 with the skill against Sonnet 4.5 on the same prompts.

- **Structure and form:** close. Sonnet 5.5 followed Sonnet 4.5's article and essay shapes and the fiction rhythm reliably.
- **Prompt requirements:** much improved. Tense, viewpoint and required-scene failures that had persisted through every Haiku version largely disappeared.
- **Em-dashes:** still below Sonnet 4.5's rate. Sonnet 5.5 uses them correctly but sparingly.
- **Voice:** Sonnet 5.5 stays slightly more polished and restrained than Sonnet 4.5, which is warmer, jokier and more openly sentimental.
- **Length:** Sonnet 5.5 lands near the requested word count, while Sonnet 4.5 often overshoots by 40–50%. The skill keeps the length rule rather than copying that habit.

The article and essay guidance rests on a handful of Sonnet 4.5 samples, so treat it as provisional.

## Why not Haiku?

Haiku 5.5 improved substantially on rhythm, dialogue and endings with instructions, but two problems held across every version:

- **Em-dashes:** Haiku almost never used them in narration, despite increasingly specific instructions and examples. It could produce them when a prompt asked directly, so this looks like a trained habit, not a wording problem.
- **Prompt requirements:** tense, viewpoint and character-role failures recurred on the same prompts under every instruction set.

Sonnet 5.5 handled both far better with the same skill.

## Earlier Haiku work

| Set | Stories | Transcript |
| --- | ---: | --- |
| Sonnet 4.5 reference | 32 | [EQ-Bench's original results](https://eqbench.com/results/creative-writing-v3/claude-sonnet-4.5.html) |
| Haiku 5.5, no instructions | 32 | [Original Haiku outputs](results/haiku-5.5-original.md) |
| Haiku 5.5, earlier custom instructions | 31 | [Earlier instructed outputs](results/haiku-5.5-earlier-instructed.md) |
| Haiku 5.5, V3 | 32 | [V3 outputs](results/haiku-5.5-v3.md) |
| Haiku 5.5, experimental V4 | 32 | [V4 outputs](results/haiku-5.5-v4-experimental.md) |

XML instructions:

- **[V3](instructions/haiku-v3.xml):** used for the V3 transcripts.
- **[V3.1](instructions/haiku-v3.1.xml):** small refinements to dialogue rhythm and em-dashes. Not separately benchmarked.
- **[V4](instructions/haiku-v4-experimental.xml):** a simplified, more general version. All 32 responses were generated in one long conversation, and it has not shown consistent improvement over V3.

Each transcript contains only the generated stories, with no conversation history, account data or attachments. The skill was not used to produce these transcripts.

## Method and limitations

This is an informal comparison, not a controlled evaluation:

- one sample per prompt
- non-blind judgments
- some runs generated in long conversations rather than fresh chats

Outputs vary between generations. If you test the skill or the instructions, use fresh chats and the original [EQ-Bench prompts](https://eqbench.com/creative_writing.html). Compare voice, rhythm, dialogue and structure, and don't assume the most enjoyable piece is the closest stylistic match.