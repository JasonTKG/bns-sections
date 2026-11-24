# Bharatiya Nyaya Sanhita, 2023: sections, IPC correspondence and classification

**Site: [bns.govsimple.org](https://bns.govsimple.org/)** · Download: [latest release](https://github.com/JasonTKG/bns-sections/releases/latest)

Archived on Zenodo: [doi:10.5281/zenodo.24496709](https://doi.org/10.5281/zenodo.24496709) · also on [Kaggle](https://www.kaggle.com/datasets/jasontkg/bharatiya-nyaya-sanhita-2023-sections-and-ipc) and [Hugging Face](https://huggingface.co/datasets/lakerguy16/bns-sections)

The Bharatiya Nyaya Sanhita, 2023 in English as enacted, one row per section; the Indian Penal Code provisions the government's table lists against each section; and the classification of offences from the First Schedule of the Bharatiya Nagarik Suraksha Sanhita, 2023. The Act came into force on 1 July 2024, except section 106(2).

## Files

| File | Rows |
|---|---|
| `bns_sections.csv` | 358 |
| `bns_ipc_mapping.csv` | 358 |
| `bns_classification.csv` | 466 |

## Columns

**`bns_sections.csv`**

- `section`: section number, 1 to 358
- `chapter`: chapter number (Roman)
- `chapter_title`: chapter title
- `subheading`: the Gazette's centred sub-heading the section falls under, where there is one
- `heading`: section heading (the Gazette's marginal note)
- `text`: text of the section as enacted, paragraphs separated by line breaks

**`bns_ipc_mapping.csv`**

- `bns_section`: BNS section number
- `bns_heading`: section heading
- `ipc_provisions_listed_by_government_table`: the Indian Penal Code provisions the government's correspondence table lists against the section, space-separated
- `source`: URL of the table

**`bns_classification.csv`**

- `provision`: BNS section or sub-section, as the First Schedule labels it
- `offence`: offence, as the Schedule words it
- `punishment`: punishment
- `cognizable`: cognizable or non-cognizable
- `bailable`: bailable or non-bailable
- `triable_by`: court by which triable
- `status`: in force, or not in force for the entry on section 106(2)
- `source`: URL of the Gazette PDF

## Sources

| Source | URL | Terms | Retrieved |
|---|---|---|---|
| Bharatiya Nyaya Sanhita, 2023 (Act 45 of 2023), Gazette of India, Extraordinary, Part II Section 1, 25 December 2023 | https://egazette.gov.in/WriteReadData/2023/250883.pdf | Text of an Act: reproduction permitted with original matter, Copyright Act 1957 s.52(1)(q) | 2026-11-23 |
| Bharatiya Nagarik Suraksha Sanhita, 2023 (Act 46 of 2023), First Schedule, Gazette of India | https://egazette.gov.in/WriteReadData/2023/250884.pdf | As above | 2026-11-23 |
| National Crime Records Bureau, Ministry of Home Affairs, Sankalan portal: IPC and BNS correspondence table | https://www.ncrb.mha.gov.in/uploads/SankalanPortal/SectionTableBNS.html | Government of India publication; section numbers only are taken | 2026-11-23 |

## How it was checked

Every section's text is compared character by character (ignoring spacing) with the Gazette PDF, read by position so that margin notes and page headers are left out; dashes are compared separately. Every classification cell is read from the Gazette First Schedule field by field and compared in order with the site. Every mapping row is re-read from the saved NCRB pages. The checks run at every build. Where NCRB's web copy differs from the Gazette, the Gazette reading is used.

## Left out

Hindi text is not included: the Gazette PDF's Hindi text layer could not be read reliably. State amendments are not included. This is a reference copy and not legal advice; the official Gazette governs.

## Licence

Indian law does not treat the reproduction of an Act together with original matter as an infringement (Copyright Act, 1957, section 52(1)(q)); the original matter here is the tabulation, the checks and the correspondence columns. That arrangement is dedicated to the public domain under CC0 1.0 (see `LICENSE`). Cite the Gazette of India for the text.

## Maintainer

Built and maintained by [JasonTKG](https://github.com/JasonTKG); corrections and questions: open an issue.

Exported 2026-11-24 from the data the site's pages are generated from.
