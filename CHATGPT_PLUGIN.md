# ChatGPT Plugin

This repository includes a skills-only ChatGPT/Codex plugin package for **De-AI Writing**. It does not require an MCP server or external account because the workflow is fully instruction-based.

## Plugin layout

```text
.agents/plugins/marketplace.json
plugins/de-ai-writing/
  .codex-plugin/plugin.json
  skills/de-ai/
    SKILL.md
    references/
      academic-paper.md
      academic-rebuttal.md
      calibration-examples.md
      general-en.md
      general-zh.md
      reading-notes.md
      tech-doc.md
```

The original root-level `SKILL.md`, `references/`, and `agents/openai.yaml` are retained for compatibility with the existing Codex skill installation flow.

## Install for local use in ChatGPT

Local marketplace plugins are tested through the ChatGPT desktop app.

### Option A: add the GitHub repository as a marketplace

```bash
codex plugin marketplace add AUGUST-GKD/De-AI-Writting
```

Restart the ChatGPT desktop app, open **Plugins**, select the **De-AI Writing** marketplace source, and install **De-AI Writing**.

### Option B: use a local checkout

```bash
git clone https://github.com/AUGUST-GKD/De-AI-Writting.git
codex plugin marketplace add ./De-AI-Writting
```

Restart the ChatGPT desktop app and install the plugin from the local marketplace source.

## Use

After installation, enable or mention the plugin in ChatGPT and try prompts such as:

```text
Use De-AI Writing to audit this abstract for AI-flavored writing.

Use De-AI Writing to rewrite this reviewer response while preserving every factual claim and citation.

使用 De-AI Writing 检查并修改这段中文，保留原意和术语，降低 AI 味。
```

## Public publishing

OpenAI supports skills-only plugin submissions. To publish this plugin to the universal Plugins Directory, create a **Skills only** submission in the OpenAI Platform plugin submission portal. Public submission additionally requires verified developer/business identity, listing assets and legal/support URLs, starter prompts, and evaluation test cases.

Before submitting publicly, add the required logo, website/support URL, privacy policy, and terms of service, then upload the final skill bundle from `plugins/de-ai-writing/skills/de-ai/`.
