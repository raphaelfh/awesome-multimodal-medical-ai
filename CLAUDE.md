# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Project overview

`awesome-multimodal-medical-ai` is a curated ("awesome list") collection of
tools, agents, papers, and datasets for **multimodal medical AI** — AI that
combines multiple data modalities in healthcare and biomedical research, such
as medical imaging (radiology, pathology), clinical text/EHR, genomics and
multi-omics, and models that fuse these modalities together. Entries should
be evaluated against this scope, not treated as a generic AI/ML list.

## Output language policy

All output produced for this repository must always be written in **English**,
regardless of the language a request is made in. This includes README content,
this file, commit messages, PR descriptions, code comments, and any future
docs or scripts.

## Primary goal: README navigability

The README is the product of this repository. The standing priority for any
content work here is making it fast and easy for a user to scan, filter, and
find the resource they need:

- Keep a table of contents that links to every category/section.
- Organize entries into clear, logical categories (e.g., by modality/task:
  Imaging, Clinical Text & EHR, Genomics & Multi-omics, Multimodal Fusion
  Models, Datasets & Benchmarks, Tools & Libraries, Surveys & Reviews).
- Write descriptions in plain, accessible language: state what the resource
  is and why it's relevant, expand acronyms on first use, and avoid
  unnecessary jargon.
- Do not create empty or placeholder sections; add a category only when there
  is curated content to put in it.

### Established entry format

Entries are table rows, and new entries must match the shape of the table they
join. Every table is four columns wide, starts with the name plus a one-line
description, and ends with the column that answers "can I actually use this":

| Section | Columns |
| :-- | :-- |
| Datasets | `Dataset \| Modalities \| Scale \| Access` |
| Repositories & Platforms | `Platform \| Modalities \| Highlights \| Access` |
| Libraries & Frameworks | `Library \| Modalities \| Built on \| License` |
| Tools | `Tool \| Modalities \| Highlights \| License` |
| Papers | `Paper \| Modalities \| Venue \| Code` |

```markdown
| **[Name](url)**<br><sub>One line on what it is and why it matters</sub> | `tag` `tag` | headline number<br><sub>qualifier</sub> | 🟢 Open<br><sub>caveat</sub> |
```

- Modalities are tags written as inline code, at most six per row.
- Access uses the legend at the top of the README: 🟢 Open (direct download),
  🟡 Registration (free account or click-through terms), 🔴 Application
  (formal request, data use agreement or review). Put exceptions in the
  `<sub>` qualifier rather than inventing a new level.
- Those three symbols mean data access and nothing else. Do not reuse them for
  a licence or for whether code exists, which would break the legend.
- Rows are ordered alphabetically, except papers, which run newest first within
  their subfield, since recency is what a reader scans a bibliography for.
  Papers from the same year are ordered alphabetically among themselves.
- The "Find by Modality" index covers datasets and platforms only. Libraries
  and tools carry their own modality tags, and papers are grouped by subfield,
  so re-indexing either there is redundant.
- A citation is never published unverified: venue, year and URL must each be
  confirmed before a paper row is written, and a licence must be confirmed per
  project. Drop a candidate that does not confirm rather than guessing.
- Percent-encode parentheses in URLs (`%28` / `%29`). A raw `)` inside a
  markdown link destination can terminate the link early.

### HTML in the README

GitHub sanitizes README HTML: `<br>`, `<sub>`, `<sup>`, `<details>`, `<img>`
and `<a>` render, while `<script>`, `style=`, `class=` and `id=` are stripped.
So the README cannot have real search, sorting or filtering — `<details>` and
the "Find by Modality" link index are the closest available substitutes. Keep
inline HTML limited to those formatting tags; anything needing genuine
interactivity belongs on a separate page, not in the README.

## Curation bar

Every entry must be screened before inclusion:

- The link works and points to the actual resource.
- It is genuinely relevant to multimodal medical AI.
- It is not a duplicate of an existing entry.
- It is not abandoned, misleading, or low-quality.

Favor a smaller list of high-quality, well-described entries over an
exhaustive but noisy one.

## Forward-compatibility note

A structured data source (a "database" of entries) is planned to eventually
back the README's content. When that lands, update this file to describe its
schema and the workflow for keeping the README in sync with it.
