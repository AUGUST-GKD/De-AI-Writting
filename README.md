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

### With the Codex skill installer

Ask Codex:

```text
$skill-installer install the de-ai skill from https://github.com/AUGUST-GKD/De-AI-Writting
```

### Manual installation

Codex loads personal skills from `$HOME/.agents/skills`:

```bash
mkdir -p "$HOME/.agents/skills"
git clone https://github.com/AUGUST-GKD/De-AI-Writting.git "$HOME/.agents/skills/de-ai"
```

Codex detects skill changes automatically. Restart Codex if the skill does not appear. See the official [Build skills documentation](https://developers.openai.com/codex/skills) for skill locations and invocation behavior.

## Use

Invoke the skill explicitly with `$de-ai`, or let Codex select it when the request matches the description in `SKILL.md`.

Examples:

```text
$de-ai audit this abstract for AI-flavored writing.

$de-ai rewrite this reviewer response while preserving every factual claim and citation.

$de-ai 检查并修改这段中文，保留原意和术语，降低 AI 味。
```

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
```

## License

MIT. See [LICENSE](LICENSE).
