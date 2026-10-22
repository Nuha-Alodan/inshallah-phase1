# Inshallah Project: Phase 2 (D2.1 to D2.4)

This folder contains the Phase 2 code, the 1,000-row annotation sample, the manual check sheets, the report tables and the corpus report.

## Deliverables

| Item | File |
|---|---|
| D2.1 Master collection (479,942 rows, 11 columns) | `D2.1_master_collection.csv` and `D2.1_provenance.csv`, shared at https://drive.google.com/file/d/1wJbdsxksV2r_piTCvYuox2JU4MDstBob/view?usp=drive_link (396 MB, too large for GitHub) |
| D2.2 Annotation sample (1,000 rows, 14 columns) | `data/D2.2_annotation_sample.csv`, with `data/D2.2_sampling_weights.csv` |
| D2.3 Corpus report (6 pages) | `D2.3_Corpus_Report.pdf` and `.docx` |
| D2.4 Code and README | `code/inshallah_phase1_phase2_colab.ipynb` (clean) and `code/inshallah_phase1_phase2_executed.ipynb` (with outputs); this README |

Other folders: `manual/` holds the reviewed sheets the notebook reads (50-row check, 100-row check, rare candidates, metadata corrections, stratum evidence, quotation check). `reports/phase2/` holds every table used in the report and `run_manifest.json` (source hashes and package versions).

## Where to place the files

The notebook downloads the sources itself. To reuse files you already have, place them under the project folder as follows:

| File | Folder |
|---|---|
| SFC-mini `0.txt` … `62.txt` | `data/raw/sfc_mini/` |
| Gulf tweets `arab_gen_twitter.csv` | `data/raw/gulf_tweets/` |
| SADA `train.csv`, `valid.csv`, `test.csv` | `data/raw/sada/` |
| Tanzil `quran-simple-clean.txt` | `data/raw/tanzil/` |
| All files from `manual/` in this folder | `manual/` |

## How to reproduce D2.2

1. Open https://colab.research.google.com, choose *File → Upload notebook* and select `code/inshallah_phase1_phase2_colab.ipynb`.
2. The notebook saves its work in Google Drive (`MyDrive/inshallah_project`). If Drive does not mount, set `USE_DRIVE = False` in cell A4; the folder is then `/content/inshallah_project`.
3. Copy all files from `manual/` into the `manual/` folder of that project folder before running Step 4.
4. For SADA, add `KAGGLE_USERNAME` and `KAGGLE_KEY` in the 🔑 Secrets panel.
5. Choose *Runtime → Run all*. If package installation asks for a restart, restart and run all again.
6. The cells run in this order: setup and CAMeL Tools; source download (SFC-mini, Gulf tweets, SADA version 23, Tanzil); extraction; cleaning and duplicate removal; Step 4 (11 columns and quotation flags); Step 5 (50-row check); Step 6 (100-row check); Step 7 (sampling); automatic checks; Step 8 (report numbers); download.

With the same sources, manual sheets and seed 2026, the notebook writes `D2.1_master_collection.csv`, `D2.1_provenance.csv`, `D2.2_annotation_sample.csv`, `D2.2_sampling_weights.csv` and the tables in `reports/phase2/`.

## Expected numbers

| Source | Found | After duplicates | After all filters (D2.1) | In D2.2 |
|---|---|---|---|---|
| SFC-mini | 519,971 | 508,010 | 469,943 | 300 |
| SADA | 9,655 | 9,627 | 9,114 | 350 |
| Gulf tweets | 1,036 | 926 | 885 | 350 |
| Total | 530,662 | 518,563 | 479,942 | 1,000 |

## Data and licences

The raw corpora are not included; the notebook downloads them. SFC-mini: CC BY-NC 4.0. Gulf Arabic Tweets 2018–2020: CC BY 4.0. SADA: CC BY-NC-SA 4.0. Tanzil: CC BY 3.0 with verbatim-copying terms. `original_text` keeps the source text unchanged. See `ATTRIBUTION.md`.
