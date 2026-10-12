---
name: citation-management-offline
description: Organize and check locally supplied academic references, author-year citations, BibTeX or RIS records, and subsection bibliographies for Chinese or English manuscripts. Use for local deduplication, field completeness, citation-reference correspondence, and preparing EndNote handoff. Does not discover literature or verify publications online.
---

# Offline Citation Management

Work only with the manuscript and bibliographic records supplied or already available locally. Keep verified bibliographic facts intact. State which checks are structural and which require reading original publications.

## Workflow

1. Identify the requested scope and output format. For Chinese papers, preserve author-year parenthetical citations and the requested journal style. Keep references organized by subsection, plus a deduplicated master set when requested.
2. Match in-text authors and years against the bibliography. List missing references, uncited entries, inconsistent years, and ambiguous same-author same-year records. Distinguish results from the user's study from explanations requiring external literature.
3. Check available author, title, year, journal, volume, page or article number, and DOI fields. Preserve missing fields as unresolved. Never invent missing metadata or claim that a structurally valid DOI proves authenticity.
4. Identify duplicates by normalized DOI first, then title and author-year. Flag conflicting metadata before merging. Preserve the most complete verified record.
5. Use the bundled formatter for supplied BibTeX files. It requires only Python's standard library. Write a new output file by default:

```bash
python scripts/format_bibtex.py references.bib --output cleaned.bib --deduplicate --sort year
```

6. When RIS is requested, preserve full author names as separate AU fields, publication year, title, journal, DOI, and applicable bibliographic fields. Mark the beginning and ending of each record with TY and ER. Check record count and citation coverage; do not claim that ordinary Word text contains EndNote fields.
7. Report edits and unresolved bibliographic conflicts briefly. If publication authenticity or claim support remains unverified, identify that gap for a separate literature-checking task.

## Scope

The bundled scripts read and write explicitly selected local bibliography files. They make no network calls and read no credentials. Offline checks do not establish source quality, authenticity, or whether a paper supports a scientific claim.

Keep manuscript editing within the user's scope. Do not rewrite scientific conclusions while fixing citations. Pair Word changes with the documents skill when requested.

## Attribution

The BibTeX parser and formatter are retained from K-Dense Inc. under MIT. See LICENSE.md and references/upstream-source.json for origin and the pinned source revision. The workflow above is an adaptation for local use.
