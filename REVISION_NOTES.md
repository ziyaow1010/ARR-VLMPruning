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

## Confirmed experimental details

- The 64 ranking examples are disjoint from the final evaluation examples.
- Width reduction is a candidate at every search step.
- Attention modules, like blocks and MLP modules, are ranked by validation accuracy after removal.
- The FastV comparison uses Qwen2.5-VL-3B; the original efficiency table uses Qwen2.5-VL-7B. Other settings follow the manuscript's existing experimental protocol.
- The ranking-subset analysis follows the parameter-priority and speed-priority case-study extraction settings. Its reported accuracy values are preserved without inventing new compression ratios or averaging procedures.
- All author-check placeholders have been removed.

## Validation

- Compiled the unchanged ACL review template with pdflatex/BibTeX via latexmk.
- Main text, conclusion, and all seven figures end within page 8; Limitations and References begin on page 9. Total PDF length is 10 pages.
- No undefined references/citations or overfull boxes in the final build.
- Visually checked the rendered pages, including the new comparison table and final-page layout.
