# Data Dictionary

This dictionary describes the columns in `qualified-notices.csv`. The JSON release contains the same records and fields.

## Record Fields

| Field | Type | Description |
| --- | --- | --- |
| `reference` | string | Stable CanadaBuys tender-notice reference retained after amendment deduplication. |
| `title` | string | Public English notice title. |
| `publication_date` | date | Notice publication date in `YYYY-MM-DD` format. |
| `fiscal_year` | string | CanadaBuys source-file fiscal year: `2024-2025`, `2025-2026`, or `2026-2027`. |
| `contracting_entity` | string | Public contracting organization named by CanadaBuys. |
| `project_category` | category | Derived category: `Custom application development`, `Modernization and upgrades`, `Web and digital services`, `Development and support`, or `AI and automation`. |
| `notice_type` | category | Public notice type. A blank value means the source did not state a formal type. |
| `notice_status` | category | Public status at collection time: `Expired` or `Cancelled`. |
| `notice_url` | URL | Public CanadaBuys notice page. |
| `classifier_confidence` | integer | Rule-based inclusion score. Scores of 6 or higher qualified automatically; lower-confidence candidates were manually reviewed. This is not a probability. |
| `matched_signals` | string list | Classifier text signals separated by ` | `. |

## Requirement-Mention Fields

Every `mentions_*` field is a `yes` or `no` string. `yes` means an explicit keyword pattern appeared in the public English title, classification, or notice description. `no` does not prove that the requirement was absent because procurement attachments were not parsed.

| Field | Signal represented |
| --- | --- |
| `mentions_security` | Security |
| `mentions_privacy` | Privacy |
| `mentions_accessibility` | Accessibility |
| `mentions_integration` | Integrations or APIs |
| `mentions_data-migration` | Data migration |
| `mentions_cloud` | Cloud delivery or infrastructure |
| `mentions_bilingual` | Bilingual delivery |
| `mentions_qa-testing` | Quality assurance or testing |
| `mentions_support` | Support or maintenance |
| `mentions_agile` | Agile delivery |
| `mentions_ux` | User experience |
| `mentions_ai` | AI or automation |
| `mentions_mobile` | Mobile delivery |
| `mentions_devops` | DevOps or release automation |
| `mentions_training` | Training or knowledge transfer |
| `mentions_open-source` | Open-source requirements |

## Missing And Excluded Data

Blank `notice_type` values mean the public source did not state a formal type. Contact names, email addresses, phone numbers, and street addresses are deliberately excluded. The dataset does not include tender attachments or full notice descriptions.
