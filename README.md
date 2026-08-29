# Canadian Software Procurement Notice Dataset

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22151691.svg)](https://doi.org/10.5281/zenodo.22151691)

An auditable dataset of 136 Canadian public software procurement notices, released by Essential Designs as the evidence layer for the [Software RFP Checklist & Readiness Checker](https://www.essentialdesigns.net/tools/software-project-readiness).

## Snapshot

- 16,203 official CanadaBuys source rows parsed
- 16,202 notices after amendment deduplication
- 167 classifier candidates after automated exclusions
- 99 notices qualified automatically
- 68 lower-confidence candidates reviewed
- 37 notices retained after review
- 136 notices in the complete qualified release
- 109 formal RFPs, or 80.1% of the release
- Notice dates from 2024-04-11 through 2026-08-07

No record-count cap was applied.

## Files

- `qualified-notices.csv`: public tabular release
- `qualified-notices.json`: public JSON release
- `benchmark-summary.json`: aggregate counts, categories, notice types, and requirement signals
- `source-manifest.json`: official source URLs, row counts, file sizes, and SHA-256 hashes
- `methodology.md`: selection, interpretation, exclusions, and reproducibility notes
- `DATA_DICTIONARY.md`: field definitions, types, values, and interpretation guidance
- `CITATION.cff`: machine-readable citation metadata
- `.zenodo.json`: Zenodo release metadata
- `dataset-metadata.json`: Kaggle-ready dataset metadata
- `LICENSE-DATA.md`: source attribution and reuse terms
- `CHECKSUMS.sha256`: SHA-256 checksums for the release files

## Selection Method

The pipeline parsed official CanadaBuys tender-notice CSV files for fiscal years 2024-2025, 2025-2026, and 2026-2027. It retained the newest amendment for each reference, matched development-oriented title and description signals, and screened out clear equipment and product-only licence, subscription, or renewal notices.

Candidates scoring 6 or higher qualified automatically. Every lower-confidence candidate was reviewed against its public title and description. Only records with clear software planning, development, modernization, testing, or support scope were retained.

## Interpretation

Requirement flags indicate explicit text matches in published title and description fields. Procurement attachments were not parsed. A missing flag must not be interpreted as proof that a requirement was absent.

The release is complete for the documented classifier and review method. It is not statistically representative of all Canadian procurement or private-sector software projects, and it should not be used as a software cost benchmark.

## Leading Explicit Signals

| Signal | Notices | Percent |
| --- | ---: | ---: |
| Support and maintenance | 38 | 27.9% |
| QA and testing | 31 | 22.8% |
| Bilingual delivery | 30 | 22.1% |
| Integrations and APIs | 22 | 16.2% |
| Security | 21 | 15.4% |
| Accessibility | 18 | 13.2% |
| Cloud | 18 | 13.2% |

## Privacy

The public release excludes contact names, email addresses, phone numbers, and street addresses. Each record retains only the fields needed to audit classification and follow its public notice URL.

## Source And Licence

Contains information licensed under the [Open Government Licence - Canada](https://open.canada.ca/en/open-government-licence-canada).

The source information is provided without any suggestion of official status or Government of Canada endorsement. Essential Designs' classification, documentation, and readiness tool are independent derivative work.

## Citation

Essential Designs. (2026). *Canadian Software Procurement Notice Dataset* (Version 1.0.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.22151691

## Release Repository

The versioned release source is maintained at:

https://github.com/scottjacksoned/canadian-software-rfp-readiness-dataset

## Canonical Resource

Use the interactive checker, inspect all 136 public records, and download the latest artifacts at:

https://www.essentialdesigns.net/tools/software-project-readiness
