# Calibration Examples

Read only when the primary scenario rules leave a real edit-versus-preserve ambiguity. Use these examples as decision anchors, not as phrases to copy.

## Academic Paper

**Flag and revise**

- Before: “In this paper, we make three key contributions. First, we propose a novel and comprehensive framework that significantly improves performance.”
- Why: The contribution template clusters with unsupported self-evaluation and no mechanism or comparison.
- After: “We introduce X, which reduces Y by reusing Z.” Use only facts present in the source.

**Preserve**

- Text: “Our contributions are threefold: a selector constrained to 2 GB, an evaluation on six datasets, and released code and configurations.”
- Decision: Keep when the list is concrete and the venue benefits from explicit navigation.

## Academic Rebuttal

**Flag and revise**

- Before: “We sincerely thank the reviewer for this insightful comment. We would like to emphasize that the reviewer misunderstood our setup.”
- Why: Generic praise delays the answer and the clarification assigns blame.
- After: “To clarify, all methods use the same backbone and training schedule.”

**Preserve**

- Text: “Thank you for identifying the missing definition. We added it to Section 3.”
- Decision: Keep the brief, specific acknowledgment and completed-change statement.

## Technical Documentation

**Flag and revise**

- Before: “This powerful and flexible tool seamlessly unlocks a robust workflow.”
- Why: Marketing adjectives replace capabilities and operating conditions.
- After: “The tool converts CSV files to Parquet and preserves the input schema.”

**Preserve**

- Text: “The service scales to 10,000 requests per second in the benchmark configuration described below.”
- Decision: Keep “scales” because the text defines the measured scale and conditions.

## Reading Notes

**Flag or prompt**

- Text in personal working notes: “The authors introduce X, evaluate Y, and report 92.3% accuracy.”
- Decision: Keep the facts, then suggest a placeholder such as `[待补：这个结果是否改变了我对 X 的判断？]`. Do not supply the reaction.

**Preserve**

- The same text in a requested neutral summary.
- Decision: Do not flag the absence of first person or personal judgment.

## General Chinese

**Flag and revise**

- Before: “随着人工智能技术的不断发展，智能工具正在日益发挥不可忽视的重要作用。”
- Why: Generic background, stacked importance markers, and no concrete subject or event.
- After: Replace it with the first specific fact already available in the source.

**Preserve**

- Text: “最麻烦的不是代码，而是数据路径：每个节点看到的挂载点并不一致。”
- Decision: Keep because the contrast corrects a real expectation and immediately explains why.

## General English

**Flag and revise**

- Before: “In today's rapidly evolving landscape, this transformative platform empowers teams to unlock their full potential.”
- Why: Generic opening and promotional claims provide no concrete action or evidence.
- After: Replace it with the specific capability, user, and outcome already supported by the source.

**Preserve**

- Text: “The parser is robust to missing trailing delimiters; the test suite covers all 18 documented cases.”
- Decision: Keep “robust” because the scope and evidence are explicit.
