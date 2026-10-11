# Revision notes for the October ARR manuscript

The paper is revised against the supplied May ARR reviews, without running new experiments. Existing figures and primary experiment values are retained.

## Completed

- Clarified the contribution as heterogeneous structural extraction and an empirical budget study, not a novel importance metric or search algorithm.
- Acknowledged task-specific structured pruning (MoPE-CLIP) and distinguished token pruning (FastV).
- Added the four-row FastV comparison and ranking-subset-size accuracies already reported in the author response.
- Included width reduction in the per-step candidate list to agree with the existing case figure; removed the impossible overshoot-then-exact-match description.
- Distinguished an upper-bound budget from exact equality, and parameter budgets from inference-speed constraints.
- Corrected attention-drop, recovery-training, and performance claims to match the figures; labeled the main compression curves as VQA v2, as supported by the source's existing results table.
- Removed repetitive case-study conclusions to make room for the existing supplemental results.
- Narrowed deployment/generalization claims and expanded limitations; corrected the missing LLM-Drop publication metadata and Brian Ichter spelling.

## Original run records still needed (no new experiments)

1. FastV table: recover backbone, GPU, precision, batch size, decoding settings, and FastV token configuration. The supplied response reports 9.8 GB / 142 ms for Original, while the primary efficiency table reports 15.879 GB / 301.37 ms. The revision keeps these as separate comparisons and does not invent an explanation for the difference.
2. Subset-size analysis: recover backbone, task, compression budget, and recovery setting. The response reports only sample counts and final accuracies. Equal final accuracy is not evidence of the same architecture.
3. Confirm that the 64 ranking samples are separated from the final evaluation data, and document the split from the existing records. No disjointness is asserted without evidence.
4. Confirm that width reduction participates at each greedy step and that attention ranking uses the cited prior criterion. These descriptions reconcile the existing figures and source, but this repository contains the manuscript rather than the pruning implementation.

The unified-model MJHQ-30K results and the rebuttal running-example parameter percentages were not imported because the supplied text lacks a matched budget/protocol and contains unexplained parameter and recovery labels.

## Validation

- Compiled the unchanged ACL review template with pdflatex/BibTeX via latexmk.
- Main text, conclusion, and all seven figures end within page 8; Limitations and References begin on page 9. Total PDF length is 10 pages.
- No undefined references/citations or overfull boxes in the final build.
- Visually checked the rendered pages, including the new comparison table and final-page layout.
