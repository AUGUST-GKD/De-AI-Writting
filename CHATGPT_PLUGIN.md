# ChatGPT Desktop Plugin

This repository includes a **skills-only ChatGPT plugin** for **De-AI Writing**. It does not require an MCP server, external API, or external account because the workflow is fully instruction-based.

The manifest is named `.codex-plugin/plugin.json` because that is the current OpenAI plugin package format shared by ChatGPT and Codex. The name of the folder does **not** mean the plugin is Codex-only.

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

The original root-level `SKILL.md`, `references/`, and `agents/openai.yaml` are retained for compatibility with the existing Codex skill installation flow. The ChatGPT plugin uses the mirrored bundle under `plugins/de-ai-writing/skills/de-ai/`.

## Install in ChatGPT Desktop without Codex CLI

### Option A: repo-scoped marketplace

1. Clone this repository and check out the plugin branch while testing:

```bash
git clone -b chatgpt-plugin https://github.com/AUGUST-GKD/De-AI-Writting.git
```

2. Open the repository as a local project/workspace in the ChatGPT desktop app. The repository already contains:

```text
.agents/plugins/marketplace.json
```

3. Restart ChatGPT Desktop.
4. Open **Plugins** in ChatGPT Desktop.
5. Select the **De-AI Writing** local marketplace source.
6. Install **De-AI Writing**.
7. Start a new ChatGPT conversation with the plugin enabled, or invoke it with an `@` mention when available.

### Option B: personal marketplace

Use this if you want De-AI Writing available independently of a particular repository.

1. Copy the plugin into your personal plugin directory:

```bash
mkdir -p ~/.codex/plugins ~/.agents/plugins
cp -R ./De-AI-Writting/plugins/de-ai-writing ~/.codex/plugins/de-ai-writing
```

2. Create or merge the following entry into `~/.agents/plugins/marketplace.json`:

```json
{
  "name": "personal-plugins",
  "interface": {
    "displayName": "Personal Plugins"
  },
  "plugins": [
    {
      "name": "de-ai-writing",
      "source": {
        "source": "local",
        "path": "./.codex/plugins/de-ai-writing"
      },
      "policy": {
        "installation": "AVAILABLE",
        "authentication": "ON_INSTALL"
      },
      "category": "Productivity"
    }
  ]
}
```

3. Restart ChatGPT Desktop.
4. Open **Plugins**, choose **Personal Plugins**, and install **De-AI Writing**.

ChatGPT installs the plugin into its local plugin cache and lets you enable or disable it from the desktop app.

## Optional CLI shortcut

The `codex plugin marketplace add ...` command is only a shortcut for registering a marketplace source. It is **not required** to use the plugin in ChatGPT Desktop.

## Use in ChatGPT

After installation, try prompts such as:

```text
Use De-AI Writing to audit this abstract for AI-flavored writing.

Use De-AI Writing to rewrite this reviewer response while preserving every factual claim and citation.

使用 De-AI Writing 检查并修改这段中文，保留原意和术语，降低 AI 味。
```

You can also mention the installed plugin with `@De-AI Writing` when the ChatGPT surface exposes plugin mentions.

## Availability note

Plugin and skill availability depends on your ChatGPT plan, desktop version, region, and workspace policy. If the local marketplace or Skills capability does not appear in ChatGPT Desktop, update the app first and check whether your account/workspace has plugin and skill access enabled.

## Public publishing

OpenAI supports skills-only plugin submissions. To publish this plugin to the universal Plugins Directory, create a skills-only plugin submission and provide the required publisher metadata, listing assets, legal/support URLs, starter prompts, and evaluation cases.
