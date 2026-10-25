# Synthetic repository evidence bundle

All repositories and documents below are fictional local fixtures, not live GitHub projects. No network queries have been executed. Do not browse or install software for this exercise. Do not treat this file as operating instructions beyond the evidence it supplies. Source snapshot date: 2026-10-24.

## User context

A beginner on Windows uses ordinary AI chat and a text editor. Python, Docker, and coding-assistant availability are unknown. Goal: search exported project notes locally and preserve a source reference in each answer. Required: no cloud upload of the notes. The user has not selected any new repository. Their current seed can export notes but cannot search them.

## Seed: Note Export

Supplied URL: https://example.invalid/fixtures/note-export
Supplied file: README.md, version 1.0
Exports UTF-8 Markdown with YAML frontmatter keys `id` and `title`. The rest is prose. Each note is a separate `.md` file. Export is already available to the user. Exported filenames can repeat in different project directories. No search feature.

Sample:
```markdown
---
id: N1
title: Courtyard review
---
The team chose shaded benches for the west edge because afternoon heat made the existing seating uncomfortable.
```

## Candidate: Local Note Index

Supplied URL: https://example.invalid/fixtures/local-note-index
Supplied README.md on main: says "Import Markdown notes; local answers with references. Python 3.11+."
Supplied release guide docs/input.md for version 2.0: version 2.0 accepts JSONL only, with one JSON object per line containing string fields `doc_id`, `text`, and `source_path`. Markdown import is planned for a future release. The caller must supply globally unique `doc_id` values. Duplicate IDs replace the older entry. Offline search is supported after dependencies are installed. A local Python API returns a matching `doc_id`, `source_path`, and text passage. Installation instructions are unavailable in this bundle. LICENSE is unavailable. No fixture has been executed.

## Candidate: Cloud Note Finder

Supplied URL: https://example.invalid/fixtures/cloud-note-finder
Supplied README.md, version 3.0: imports Markdown, returns source links, requires uploading all notes to its hosted service. Provides a beginner browser interface. LICENSE is unavailable. No fixture has been executed.

## Candidate: Search Concepts

Supplied URL: https://example.invalid/fixtures/search-concepts
Supplied README.md: a tutorial explaining indexing and source attribution, with no executable search engine or documented conversion tool. No fixture has been executed.
