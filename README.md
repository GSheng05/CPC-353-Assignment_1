# CPC353 Assignment 1: Code-Switching Analysis

This project examines English-Malay code-switching and sentiment in Ayam Gepuk restaurant reviews. The final workflow is `Notebooks/Complete_Analysis.ipynb`.

## Run the analysis

1. Install `pandas`, `openpyxl`, `matplotlib`, and a Jupyter Python kernel.
2. Open `Notebooks/Complete_Analysis.ipynb` from the repository root or `Notebooks/`.
3. Restart the kernel and run all cells in order.
4. Inspect the validation flags, tables and figures under `Outputs/`.

The notebook performs retained-data checks, exploratory bigram/trigram extraction, keyword concordance, reviewed evidence validation, sentiment distributions and contextual interpretation. It uses manual sentiment labels; it does not train a classifier.

## Required inputs: preserve these files

- `Data/CPC 353 Dataset.xlsx`: source reviews and annotations.
- `Outputs/Tables/focused_concordance_review.xlsx`: focused concordance decisions.
- `Outputs/Tables/selected_evidence_review.xlsx`: selected evidence and lexicon decisions.
- `Outputs/Tables/integrated_discussion_evidence.csv`: supplementary discussion passages.

These files are read-only inputs even though three are stored under `Outputs/`. Hash checks verify that execution leaves them unchanged. Missing or incompatible review decisions stop execution; they are not automatically recreated or accepted. Other calculated CSV tables and figures are regenerated.

## Analysis conventions

- A review with both intra- and inter-sentential switching receives an intra-sentential primary label.
- Food names alone do not establish switching.
- Whole-review sentiment is distinct from passage-level evaluation. Neutral includes mixed evaluations under the annotation conventions.
- Within-group sentiment percentages use the number of reviews in that switching group as the denominator.
- Keyword hits and recurring phrases are not automatically confirmed switching events.
- Purposively selected examples illustrate contextual functions without estimating the frequency of every function.

The retained corpus contains 197 reviews. Historical collection/removal totals remain unresolved: the reported 275 and approximately 300 must be reconciled with original collection records. Keep `cleaning_history.csv` and the provenance/check outputs until this is resolved. Supplementary recurring-expression interpretations remain pending review.

## Collection and supporting evidence

`Food-Review-Scrapper/` retains the review collector, browser and SerpAPI adapters, filtering resources, requirements, tests, collection documentation and licence. Follow its [README](Food-Review-Scrapper/README.md) for collection. Existing raw collection folders must be preserved locally; analysis does not recollect or overwrite them.

`Outputs/Tables/inter_sentential_cases.xlsx` and `selected_analysis_checklist.csv` remain supporting records. `combined_verification.json` describes a historical verification run, not the current notebook version.

## Archived development files

`Archive/Notebooks/` preserves the four earlier standalone notebooks. They are historical references and are not required by the final workflow. Their original relative paths may need adjustment if reused.

`Archive/Food-Review-Scrapper/` preserves the unrelated generic website crawler and its original environment files. Run it from that directory if needed; it is not part of the review analysis or collection workflow.

Local report drafts and review notes under `docs/` remain excluded from Git.
