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

Entries follow this two-line shape, and new entries must match it:

```markdown
- **[Name](url)** — One sentence on what it is and why it matters.
  *Modalities:* comma-separated list · *Access:* Open | Registration | Application
```

Access levels are defined in the README's "How to Read the Entries" section:
**Open** (direct download), **Registration** (free account or click-through
terms), **Application** (formal request, data use agreement or review).

Entries are ordered alphabetically within each section.

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
