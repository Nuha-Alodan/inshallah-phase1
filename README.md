# Inshallah Project: Phase 1 (D1.2 and D1.3)

This repository contains the Phase 1 extraction prototype, the data access log and the label inventory. The raw data are not included; the notebook downloads them from their original sources.

## Phase 2 files (D2.1 and D2.4) are in the phase2 folder.

## Files

| File | Content |
|---|---|
| code/inshallah_phase1_colab.ipynb | Extraction prototype: installs Python packages and CAMeL Tools, downloads the data, finds the formula and its spellings, pulls three examples per label |
| reports/phase1/data_access_log.md, data_access_log.csv | Sources, links, licences, access dates and prototype counts (D1.3) |
| reports/phase1/prototype_variant_counts.csv | Every spelling of the formula found, with its count per source |
| reports/phase1/D1_2_Label_Inventory_v0_4.docx, label_inventory_v0.4.md | Label inventory: one definition and three real examples per label (D1.2) |
| reports/phase1/label_examples.csv | The 18 inventory examples with label, source, record reference and English translation |
| requirements.txt | Python packages used by the notebook |
| ATTRIBUTION.md | Source attribution and licences |

## How to run

1. Open https://colab.research.google.com, choose *File → Open notebook → GitHub*, paste the link of this repository and open `code/inshallah_phase1_colab.ipynb`.
2. In the 🔑 Secrets panel, add `KAGGLE_USERNAME` and `KAGGLE_KEY` (kaggle.com → Settings → API → Create New Token). These are needed for SADA.
3. Run cell 1: installs the packages.
4. Run cell 2: downloads SFC-mini (about 3 GB), the Gulf tweets and the SADA text files.
5. Run cell 3: finds every occurrence of the formula and counts the spellings.
6. Run cell 4: pulls the 18 label-inventory examples from the corpus.

## Expected outputs

- `prototype_variant_counts.csv`: 530,662 occurrences (SFC-mini 519,971; SADA 9,655; Gulf tweets 1,036) and 1,222 different spellings, counted before removing duplicates.
- `label_examples_check.csv`: each of the 18 examples with its full source record. Cell 4 should print `OK` for all 18.

## Data sources

| Source | Licence |
|---|---|
| SFC-mini (Hugging Face: faisalq/SFC-mini) | CC BY-NC 4.0 |
| Gulf Arabic Tweets 2018–2020 (Hugging Face: AhmedSSabir/Gulf-Arabic-Tweets-2018-2020) | CC BY 4.0 |
| SADA, text only (Kaggle: sdaiancai/sada2022, version 23) | CC BY-NC-SA 4.0 |
