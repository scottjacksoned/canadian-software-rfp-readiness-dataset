---
language:
  - en
pretty_name: Canadian Software Procurement Notice Dataset
tags:
  - tabular
  - procurement
  - software-development
  - canada
  - rfp
size_categories:
  - n<1K
license: other
license_name: open-government-licence-canada-2.0
license_link: https://open.canada.ca/en/open-government-licence-canada
configs:
  - config_name: default
    data_files:
      - split: train
        path: qualified-notices.csv
---

# Canadian Software Procurement Notice Dataset

This tabular dataset contains 136 Canadian public software procurement notices selected through a documented rule-based classifier and complete review of all lower-confidence candidates.

## Dataset Summary

Essential Designs parsed 16,203 official CanadaBuys tender-notice rows across three fiscal years and deduplicated amendments by notice reference. The classifier produced 167 candidates. Ninety-nine qualified automatically, all 68 lower-confidence candidates were reviewed, and 37 of those were retained. The released dataset contains 136 notices with no record-count cap.

Of the 136 released notices, 109 are identified as a Request for Proposal or an RFP against a supply arrangement.

## Intended Uses

- Inspect public software procurement language
- Reproduce the published aggregate counts
- Explore project categories and notice types
- Test transparent text classification approaches
- Support research into software RFP planning inputs

## Limitations

Requirement flags use explicit keyword patterns against public English title, classification, and notice-description fields. Attachments were not parsed. Missing flags do not prove that requirements were absent.

The release is complete for the documented method, but it is not statistically representative of all Canadian procurement or private-sector software projects.

## Privacy

Contact names, email addresses, phone numbers, and street addresses are excluded.

## Source And Licence

Contains information licensed under the Open Government Licence - Canada:

https://open.canada.ca/en/open-government-licence-canada

This derivative release does not suggest Government of Canada endorsement.

## Canonical Resource

The interactive Software RFP Checklist & Readiness Checker, current methodology, and latest downloads are maintained at:

https://www.essentialdesigns.net/tools/software-project-readiness

## Citation

Essential Designs. (2026). Canadian Software Procurement Notice Dataset (Version 1.0.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.22151691
