# De-AI Writing

`de-ai` is a writing skill for Codex and ChatGPT. It diagnoses and reduces formulaic AI-flavored prose while preserving the author's meaning, factual claims, stance, terminology, citations, numbers, notation, formatting, and intended voice.

The skill treats AI flavor as a contextual style diagnosis. It does not claim to detect or prove AI authorship.

## What it does

- Audits text and reports only material issues.
- Rewrites text while preserving technical and factual integrity.
- Directly edits a requested file or section without expanding the scope.
- Handles academic papers, academic rebuttals, technical documentation, reading notes, and general Chinese or English writing.
- Checks logical coherence, transitions, formulaic expression, directness, vocabulary, sentence complexity, and term consistency.
- Removes avoidable defensive language and sentence-punctuation em dashes or en dashes.

## Install

### ChatGPT Desktop plugin

This repository includes a **skills-only ChatGPT plugin**. No MCP server, external API, or external account is required.

The plugin uses OpenAI's shared plugin package format, so its manifest lives at `.codex-plugin/plugin.json`; despite the folder name, the plugin is installable and usable in **ChatGPT Desktop**.

For a repo-scoped install, clone the repository, restart ChatGPT Desktop, open **Plugins**, choose the local **De-AI Writing** marketplace, and install **De-AI Writing**.

For a personal install that does not depend on keeping this repo open, copy `plugins/de-ai-writing` into `~/.codex/plugins/de-ai-writing` and add it to `~/.agents/plugins/marketplace.json`.

Full ChatGPT Desktop instructions, including the personal marketplace JSON, are in [CHATGPT_PLUGIN.md](CHATGPT_PLUGIN.md).

### Codex skill installation

The original Codex skill remains available separately.

With the Codex skill installer:

```text
$skill-installer install the de-ai skill from https://github.com/AUGUST-GKD/De-AI-Writting
```

Or manually:

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/AUGUST-GKD/De-AI-Writting.git "$HOME/.agents/skills/de-ai"
```

## Use

In ChatGPT Desktop, enable **De-AI Writing** or mention it with `@De-AI Writing` when plugin mentions are available.

Examples:

```text
Use De-AI Writing to audit this abstract for AI-flavored writing.

Use De-AI Writing to rewrite this reviewer response while preserving every factual claim and citation.

使用 De-AI Writing 检查并修改这段中文，保留原意和术语，降低 AI 味。
```

In Codex, the original skill can still be invoked with `$de-ai`.

## Operating modes

| Mode | Typical request | Result |
| --- | --- | --- |
| Audit | Check, review, or identify AI flavor | A compact diagnosis with local fixes |
| Rewrite | Rewrite, polish, or de-AI | Revised text followed by a brief change summary |
| Direct edit | Edit a named file or section | A scoped file patch and verification |
| Audit + rewrite | Check and fix | A short diagnosis followed by revised text |

## Repository structure

```text
de-ai/
  SKILL.md
  agents/
    openai.yaml
  references/
    academic-paper.md
    academic-rebuttal.md
    calibration-examples.md
    general-en.md
    general-zh.md
    reading-notes.md
    tech-doc.md
  .agents/plugins/
    marketplace.json
  plugins/de-ai-writing/
    .codex-plugin/
      plugin.json
    skills/de-ai/
      SKILL.md
      references/
```

The root-level skill remains available for the original Codex installation flow. The plugin package mirrors that skill under `plugins/de-ai-writing/skills/de-ai/` for ChatGPT plugin installation.

## License

MIT. See [LICENSE](LICENSE).
