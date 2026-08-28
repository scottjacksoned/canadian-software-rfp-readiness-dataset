# Canadian Software Procurement Notice Dataset Methodology

Version: 1.0.0

Generated: 2026-08-28T07:10:11.136Z

## Purpose

This dataset provides a reproducible evidence layer for the Essential Designs software-project readiness benchmark. It is not a census of Canadian software projects, a cost study, or a claim about every requirement in an RFP.

## Source frame

The pipeline parsed 16,203 rows from the official CanadaBuys 2024-2025, 2025-2026, and 2026-2027 tender-notice CSV files, then deduplicated amendments by notice reference.

## Selection

Notices were deduplicated by reference number, matched against development-oriented title and description patterns, and screened for product-only and equipment exclusions. Candidates scoring 6 or higher qualified automatically; every lower-confidence candidate was reviewed against its public title and description, and only records with clear software planning, development, modernization, testing, or support scope were retained. No record-count cap was applied. The resulting 136-notice dataset is complete for this classification and review method across the listed source files. Because its inclusion rules are purposive, it is not statistically representative of all Canadian procurement or private-sector software projects.

109 of the 136 released notices (80.1%) are identified as either a Request for Proposal or an RFP against a supply arrangement. The remaining notices include requests for information, advance contract award notices, standing offers, and records without a stated formal notice type.

The classifier produced 167 candidates after automated exclusions. 99 met the automatic confidence threshold, all 68 lower-confidence candidates were reviewed, 37 were retained, and 31 were excluded.

## Requirement detection

Requirement flags use documented keyword patterns against English title, classification, and notice-description fields. Counts indicate explicit mentions only. Detailed requirements may appear solely in attachments, so a missing flag must not be interpreted as proof that a requirement was absent.

## Exclusions

The pipeline excludes clear physical-equipment notices and product-only licence, subscription, or renewal notices when the title does not indicate development work. Contact names, email addresses, phone numbers, and street addresses are not published.

## Reproducibility

The source manifest records the official URL, fiscal year, byte size, row count, and SHA-256 hash for each input file. The public record file contains only the fields needed to audit selection and requirement flags.
