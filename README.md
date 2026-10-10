# Probe me

A skill that makes AI agents such as Claude ask before they answer. When you share a feeling, opinion or position ("Why am I not worried about AI when everyone else is?", "Smoking disgusts me", "I think agents should use accessibility APIs, not screenshots"), the agent runs a short interview of multiple-choice rounds to learn what your view is actually about, then answers the question you really have instead of the generic version.

This is a reflection and clarification aid. It is not therapy, counseling, a coach or a source of emotional support, and it does not provide that kind of interaction.

## What it does

- Asks short rounds (1–3 questions each) through the agent's `AskUserQuestion` prompt, funnel-ordered from broad and descriptive to specific and sensitive.
- Uses techniques from survey methodology and qualitative interviewing: neutral wording, balanced scales, laddering ("why does that matter?"), vignettes for boundaries, and member checking (a summary for you to confirm or correct before any critique).
- Widens the frame before drafting questions, so options cover your own experience, other people affected, the wider system and principle, not only the default vantage point.
- Skips the questionnaire when you ask for a quick answer, when the question is factual or a writing task, when your message already has enough detail, or when you seem to be in distress or crisis.

`skills/probe-me/references/question-design.md` holds the methods, common pitfalls, scale templates and three worked examples (A: a feeling, B: an attitude, C: a position statement).

## Requirements

- An AI agent such as Claude Code, with plugin support and the `AskUserQuestion` tool.
- Nothing else: no scripts, packages or network access.

## Data disclosure

This plugin sends no data. It consists only of instructions (Markdown) and an icon; it has no scripts, no network requests, no web search or fetch calls and no connectors. Your answers to the interview questions stay within your conversation with the AI agent, handled under the terms of the product you use. The plugin author does not receive, collect or store anything.

## Intended audience

This plugin is not age-restricted and is suitable for general audiences. It is a conversational aid and does not itself introduce mature content. It is not a substitute for professional mental-health support; if you are in distress or crisis, the skill is designed to stay out of the way, and you should reach out to a qualified professional or local emergency services.

## Installation

```
/plugin install probe-me --marketplace ruihe774/probe-me-skill
```

Or load a local checkout directly while trying it out:

```
claude --plugin-dir /path/to/probe-me-skill
```

The skill (`probe-me`) then triggers automatically when you express an opinion or feeling; you don't need to name it.

## Layout

- `.claude-plugin/plugin.json`: manifest
- `.claude-plugin/icon.png`: icon
- `.claude-plugin/marketplace.json`: single-plugin marketplace listing
- `skills/probe-me/SKILL.md`: the skill
- `skills/probe-me/references/question-design.md`: methods, pitfalls, scales and worked examples

## Development

```
claude plugin validate .
```

## License

[The Unlicense](LICENSE)
