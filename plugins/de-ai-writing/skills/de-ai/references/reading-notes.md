# Reading Notes

Use these rules for paper notes, book notes, literature summaries, and study notes in Chinese or English.

**Primary dimensions:** Formulaic expression and directness. Give secondary attention to vocabulary naturalness and term consistency; flag logic, transitions, or sentence complexity only when they clearly reduce the notes' usefulness.

## Determine the Note's Function

Infer whether the notes are:

- **Personal working notes:** prioritize reactions, uncertainty, connections, and reminders.
- **Shared research notes:** prioritize traceable claims, concrete evidence, and concise evaluation.
- **Neutral summaries:** prioritize faithful coverage; do not force first-person commentary.
- **Study guides:** prioritize explanation, retrieval cues, and conceptual structure.

Do not treat the absence of “I” or “我” as an AI signal by itself.

## Detect Note-Specific Pattern Clusters

Flag combinations such as:

- Every paper uses the same Background–Method–Experiments–Conclusion template regardless of its actual contribution.
- A chronological “first, then, finally” summary hides the main result or idea.
- Every paragraph follows “the authors do X; results show Y” with no selection or hierarchy.
- Metrics are copied without baselines, conditions, or an explanation of why they matter.
- The notes sound completely certain about difficult material while skipping unresolved derivations or assumptions.
- Repeated “值得注意的是,” “总体而言,” “Specifically,” or “Overall” substitutes for real organization.

Pure description is appropriate for a neutral summary. Flag it only when the user expects critical or personal notes.

## Improve Usefulness Without Inventing a Voice

- Lead with the contribution, theorem, dataset, mechanism, or result most relevant to the note's purpose.
- Record concrete numbers, conditions, comparison points, and limitations.
- Mark uncertainty when the source or the user's notes already indicate it.
- Preserve the difference between the paper's claim and the note author's judgment.
- For personal working notes, flag sections that remain purely descriptive when a reaction, uncertainty, or connection would make them more useful. Suggest a prompt such as `[待确认：这里是否认可作者的假设？]`; do not invent the reader's answer.
- For neutral summaries, do not require or manufacture personal opinions.

## Check Vocabulary

Treat the following as weak signals when they occur without concrete content:

| Pattern | Improve By |
|---|---|
| “深入剖析” / “系统性梳理” | Name what was analyzed or how items were organized |
| “从宏观到微观” | Describe the actual sequence |
| “核心在于” / “本质上” | State the mechanism directly |
| “It is interesting to note that” | State what is surprising and why |
| “opens exciting avenues” | Name the specific follow-up question |
| “clearly demonstrates” | State what the evidence supports |

Keep these phrases when they are specific and not repeated.

## Preserve Source Fidelity

- Do not invent criticisms, reactions, uncertainties, connections, or numerical context.
- Keep quotations distinct from paraphrases.
- Preserve page, section, figure, and citation references.
- Mark unsupported interpretations as the note author's interpretation.
- Do not turn a partial reading into a claim about the entire work.
