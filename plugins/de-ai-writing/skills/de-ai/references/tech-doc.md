# Technical Documentation

Use these rules for READMEs, API references, tutorials, user guides, and project wikis in English or Chinese. Match the expected knowledge of the intended reader.

**Primary dimensions:** Formulaic expression and directness. Give secondary attention to logical coherence, sentence complexity, and term consistency; flag transition or vocabulary issues when they affect a reader's task.

## Detect Documentation-Specific AI Flavor

Flag patterns when they replace usable information:

- Marketing language such as “seamless,” “powerful and flexible,” “revolutionize,” “赋能,” or “极致” without a specific capability or measurement.
- Tutorial preambles that delay the first actionable step.
- Repeated “simply,” “just,” “只需,” or “轻松” that understates prerequisites or failure cases.
- Claims such as “robust,” “scalable,” “production-ready,” or “企业级” without evidence.
- Emoji clusters, slogan-like headings, or feature bullets that make every capability sound equally important.
- Paragraphs that repeatedly restate what the next code block already shows.

Treat each word as context-dependent. “Scalable” is useful when the document defines the tested scale.

## Prioritize Reader Tasks

- Lead procedural sections with the goal, prerequisite, or command the reader needs.
- State versions, file paths, configuration keys, defaults, units, return types, and error behavior precisely.
- Use imperative instructions when telling the reader what to do.
- Use prose for explanation and bullets or tables for reference material.
- Explain a concept before a command only when the command cannot be used safely without it.
- Keep warnings and notes when they prevent misuse; remove only empty announcements.

## Prefer Concrete Vocabulary

| Vague Pattern | Prefer |
|---|---|
| “leverage” / “utilize” | “use,” “call,” or the exact operation |
| “facilitate” | Name what becomes possible |
| “perform an analysis” | “analyze” |
| “provide functionality for” | Name the feature or behavior |
| “实现闭环” | Describe the actual feedback or end-to-end process |
| “大幅提升性能” | Give the metric and test conditions if available |

Do not simplify established API, protocol, or domain terminology.

## Check Structure and Completeness

- Verify that prerequisites appear before the steps that require them.
- Keep code, output, and explanation synchronized.
- Ensure examples use current names and consistent placeholders.
- Separate quick-start instructions from conceptual explanation when both are needed.
- Quote exact error messages and state the conditions that trigger them.
- Avoid adding performance numbers, compatibility claims, or security assurances not present in the source.

## Preserve Technical Integrity

- Keep code blocks, commands, flags, paths, config keys, API names, versions, and error messages unchanged unless they are the edit target.
- Do not remove caveats, security warnings, or compatibility limits merely to make prose shorter.
- Do not make documentation promotional or artificially casual.
