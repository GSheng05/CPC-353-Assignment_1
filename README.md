# CPC353 Assignment 1: Code-Switching Analysis

## Project overview

This project studies English–Malay code-switching in Ayam Gepuk restaurant reviews. The concordance analysis examines switching patterns and their use in context. The sentiment analysis examines sentiment and its relationship with switching types.

The annotated dataset version previously reviewed contained **197 real Google reviews**: 144 code-switched, 36 English, and 17 Malay. The 144 code-switched reviews had 139 intra-sentential and 5 inter-sentential primary labels. Recheck these counts against the dataset used for the final analysis.

## Concordance analysis

- Loaded the annotated dataset while preserving review text, source information, and existing labels.
- Checked for missing values, duplicate IDs, and exact duplicate review texts.
- Summarized language classifications and primary switching labels.
- Generated keyword-in-context (KWIC) concordances and counted occurrences and distinct reviews for selected search terms.
- Prepared a qualitative analysis of six selected intra-sentential passages and the five inter-sentential-labelled reviews, along with a small bilingual lexicon and selected quotations.
- Produced tables and a figure for the group report.

The 27 Python code cells were executed successfully in a separate validation copy at commit fdbfc02. Checked focused summaries and selected-evidence outputs reproduced the saved results after accounting for CRLF/LF line-ending differences. This validates execution and output consistency, not independent agreement with every qualitative decision.

## Analysis conventions

- When a review contains both intra- and inter-sentential switching, its primary label is intra-sentential.
- Sentence-ending punctuation and line breaks mark boundaries. A language change across a boundary is needed to identify inter-sentential switching.
- Food and dish names alone are not treated as switching evidence.
- Reviews from delivery riders about restaurant service are included.
- Existing sentiment labels and annotation notes are retained unchanged.

Primary-label counts describe review classifications, not every switching event. Keyword frequencies count search hits, not automatically confirmed switching patterns. Detailed interpretations use purposively selected examples and do not estimate the frequency of every pattern in the corpus.

## Repository layout

```text
Data/
  CPC 353 Dataset.xlsx              # Annotated source dataset
Notebooks/
  Concordance_Analysis.ipynb        # Concordance analysis notebook
Outputs/
  Tables/                           # Calculated and reviewed tables
  Figures/                          # Analysis figures
```

The source workbook is read-only for this workflow. Save derived results separately and preserve manually reviewed workbooks when rerunning cells.

## Outputs for sentiment analysis

The following files were present in the repository when it was checked:

| File under `Outputs/Tables/` | Use |
| --- | --- |
| `language_distribution.csv` | Overall language categories and counts. |
| `primary_switching_distribution.csv` | Distribution of primary switching labels within the code-switched subset. |
| `keyword_search_summary.csv` | Keyword occurrence and distinct-review counts. |
| `kwic_all_hits.csv` | Search hits, context, review IDs, and existing labels. |
| `search_register.csv` | Search terms and included forms. |
| `data_review_flags.csv` | Data-quality flags; check the latest version after rerunning. |

The repository includes reviewed selected evidence, pattern summaries, all five inter-sentential cases, a six-entry bilingual lexicon and eight selected quotations. Focused concordance outputs cover 34 hits for repeat and portion; 26 were marked Confirmed and eight No local switching.

## Connecting concordance and sentiment analysis

1. Use the same final dataset, review IDs, and primary switching labels as the concordance analysis.
2. Retain the existing Positive, Negative, and Neutral sentiment labels and annotation notes.
3. Compare sentiment across the existing switching categories and clearly state the denominator for each comparison.
4. Use the concordance examples and quotations to discuss how specific switching patterns occur in evaluative contexts.
5. Treat the five inter-sentential-labelled reviews as a small group. Avoid broad or causal conclusions from their sentiment distribution.
6. Document the sentiment-analysis method and confirm with the group that the overall assignment covers at least two NLP techniques.
7. Agree on the selected research question, final results, and terminology before jointly writing the abstract and discussion.

## Running the notebook

1. Place the annotated workbook in `Data/` and open `Notebooks/Concordance_Analysis.ipynb` from the project.
2. Install the packages specified in the notebook: `pandas`, `openpyxl`, and `matplotlib`.
3. Confirm input/output paths and preserve any manually completed review workbooks.
4. Restart the kernel and run the notebook in order, completing the review steps where prompted.
5. Check the data-quality and validation flags, output tables, selected quotations, and figure.

Record the original collected and retained counts from the team's cleaning history. The final report must follow the assignment's IEEE manuscript requirements and be submitted in Word and PDF formats.

## Combined analysis

Open `Notebooks/Complete_Analysis.ipynb` and run the cells in order from the repository root or `Notebooks`. The Python kernel needs pandas, openpyxl and matplotlib. The notebook audits the retained dataset, extracts bigrams and trigrams, generates the concordance and sentiment results, and links selected expressions to their original context.

Keep the source workbook in `Data/` and the two reviewed Excel workbooks (`focused_concordance_review.xlsx` and `selected_evidence_review.xlsx`) and `integrated_discussion_evidence.csv` in `Outputs/Tables/`. The notebook uses these files as inputs and regenerates tables and figures under `Outputs/`. The supplementary contextual interpretations are pending team review.

The source workbook contains 197 retained reviews. Original collection and removal counts still require the collection records. The combined Python cells were verified in sequence. A Jupyter restart and run-all check is pending.
