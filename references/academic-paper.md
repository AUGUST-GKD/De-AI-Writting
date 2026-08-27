# English Academic Papers

Use these rules for English research manuscripts. Favor precision, evidence, and argument flow over conversational simplicity.

**Primary dimensions:** Formulaic expression, vocabulary naturalness, and sentence complexity. Treat logical coherence, transition naturalness, directness, and term consistency as secondary; flag them only when they clearly affect the passage.

## Calibrate Conventional Academic Phrases

Treat these expressions as weak signals rather than automatic errors:

| Pattern | Flag When | Preserve When |
|---|---|---|
| “Our contributions are threefold” | The list is generic, mechanically parallel, or repeats the abstract | The venue expects an explicit contribution list and each item is concrete |
| “Note that” / “We emphasize” | It repeatedly announces importance without adding structure | It introduces a real condition, exception, or distinction |
| “The key insight is” | The following statement is vague or merely restates the method | It names a precise mechanism that organizes the section |
| “Not X, but Y” | The contrast is artificial and Y alone is clearer | Correcting X is necessary to prevent a real misconception |
| “Specifically” / “We then” | Several paragraphs or sentences use the same opening | The sequence is genuinely procedural |
| “Importantly” / “Crucially” | Emphasis adverbs cluster or substitute for evidence | A rare use marks a real consequence |

Do not flag any one occurrence as high severity.

## Detect Stronger Pattern Clusters

Flag combinations such as:

- A generic trend opening followed by vague importance and an unsupported research gap.
- Consecutive paragraphs with the same topic-sentence template and sentence rhythm.
- Contribution bullets that repeat the same claim with different nouns.
- Self-evaluative language such as “novel,” “comprehensive,” or “significant” without a concrete comparison.
- Results described with intensifiers but without the relevant baseline, metric, condition, or uncertainty.
- Repeated meta-commentary that tells the reader how to interpret a claim instead of supporting it.

## Improve Directness Without Overclaiming

- Replace empty background with the specific technical condition that creates the problem.
- Remove defensive clarification only when the main claim remains accurate without it.
- Keep epistemic hedges such as “may,” “suggests,” and “under these assumptions” when the evidence requires them.
- Split observation, interpretation, and implication when one sentence makes their evidential status unclear.
- Keep meaningful contrasts; remove only contrasts created for rhetorical symmetry.

## Check Vocabulary and Translation Artifacts

Prefer established technical phrasing over literal or embellished wording:

| Awkward Pattern | Prefer |
|---|---|
| “point leader” | “ranks first” or the exact metric comparison |
| “point-estimate ordering” | “ranking by point estimates” |
| “gradient-based optimization-driven search” | Split the modifier chain |
| “places this problem in” | “frames this problem as” when that is the intended relation |
| A fancy verb used imprecisely | The domain-standard verb |

Treat terms such as “denotes,” “retain,” and “sound” as context-dependent. Do not replace them when they are technically correct.

## Check Academic Sentence Load

Consider revision when:

- A sentence combines data, interpretation, limitation, and implication.
- Multiple nested clauses separate the subject from its main verb.
- A long modifier stack can be expanded into a clearer relation.
- Parenthetical citations interrupt an already dense clause structure.

Use comprehension, not comma count, as the deciding test.

## Preserve Research Integrity

- Keep citations attached to the claims they support.
- Preserve equations, notation, defined terms, dataset names, metrics, and experimental conditions.
- Do not turn correlation into causation or “suggests” into “shows.”
- Do not strengthen priority claims such as “first” or “state of the art.”
- Preserve an explicit contribution list when it serves venue conventions or navigation.
- Keep limitations and uncertainty even when removing formulaic phrasing.
