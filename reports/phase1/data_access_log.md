# D1.3 Data access log

| Source | Link | Licence | Files | Records | Revision | Accessed (UTC) | Status |
|---|---|---|---|---|---|---|---|
| SFC-mini | https://huggingface.co/datasets/faisalq/SFC-mini | CC BY-NC 4.0 | 63 txt files | 8,866,859 posts | cae145d64190 | 2026-10-09 07:23 | downloaded |
| Gulf Arabic Tweets 2018–2020 | https://huggingface.co/datasets/AhmedSSabir/Gulf-Arabic-Tweets-2018-2020 | CC BY 4.0 | arab_gen_twitter.csv | 108,052 tweets | b549bc3dc6e2 | 2026-10-09 07:23 | downloaded |
| SADA (text fields only) | https://www.kaggle.com/datasets/sdaiancai/sada2022 | CC BY-NC-SA 4.0 | train.csv, valid.csv, test.csv | 253,166 segments | Kaggle version 23 | 2026-10-09 07:23 | downloaded |

**Downloaded:** all three sources. **Requested:** none; all three are public downloads (SADA needs a free Kaggle account).

Notes: SFC-mini has one post per non-empty line. The Gulf tweets were already cleaned by the dataset authors (no URLs, user names or diacritics). For SADA we used only the text column GroundTruthText; the audio was not downloaded.

## Extraction prototype results

Occurrences of the formula found by `inshallah_phase1_colab.ipynb`, before removing duplicates (see `prototype_variant_counts.csv`).

| Source | Occurrences | Different spellings |
|---|---|---|
| SFC-mini | 519,971 | 1,175 |
| SADA | 9,655 | 32 |
| Gulf tweets | 1,036 | 15 |
| **Total** | **530,662** | **1,222** |

## What can be released

SFC-mini (NC) and SADA (NC-SA) do not allow commercial use, and SADA requires the same licence for derived data. Any release of annotated data should therefore be non-commercial and use the SADA terms, or contain only IDs and labels.
