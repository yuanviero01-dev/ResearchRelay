# Recorded evaluation: v03 to v04

Fixture date: 2026-10-24. Final package verification: 2026-10-25 (Asia/Jakarta). This is an offline instruction evaluation, not a release certification.

## Method

Two isolated Codex executors each received one skill snapshot, the same [fictional evidence](discovery-fixture.md), and the same [two requests](discovery-requests.md). They did not receive the reviewer rubric, suspected defects, proposed fixes, or each other's outputs. One discussion and one archive were generated per snapshot. The [rubric](discovery-rubric.md) was fixed before outputs were inspected.

The skill author reviewed outputs semantically; structural checks were automated. The executors inherited the parent Codex configuration. An exact model identifier and sampling settings were not separately recorded. This is one sample per request/version, not a randomized repeated comparison, novice study, or cross-platform test. A subagent is not an independent human reviewer.

## Observations from the initial runs

Pass means the specific written-output criterion was met in this sample. Partial means a material ambiguity remained. It does not mean a repo ran successfully.

| Criterion | Behavior | v03 | v04 tested snapshot | Evidence |
| --- | --- | --- | --- | --- |
| 1 | Discussion stays discussion | Pass | Pass | Both discussion.md outputs avoid an R&D archive despite the quoted trigger. |
| 2 | Seed and local-source goal | Pass | Partial | Both retain the seed and goal, but v04 archive section 2 says "No cloud upload is mandatory", which can mean upload is optional. Other v04 sections correctly prohibit upload. |
| 3 | Version conflict | Pass | Pass | Both distinguish main README Markdown claims from v2.0 JSONL-only input. |
| 4 | Conversion remains proposed | Pass | Pass | Both describe the missing Markdown-to-JSONL bridge without claiming an existing converter. |
| 5 | Identity and attribution | Pass | Pass | Both preserve doc_id/text/source_path and explain duplicate-ID replacement; v04 gives a stable assigned-ID registry example. |
| 6 | Mandatory exclusion / reference role | Pass | Pass | Both exclude Cloud Note Finder and identify Search Concepts as learning-only. |
| 7 | Unknown setup and licenses | Pass | Pass | Neither invents install commands, available runtime, license terms, or executed tests. |
| 8 | Recommendation versus agreement | Pass | Pass | Both explicitly state no new repository has been chosen. |
| 9 | Feasible first action and handoff | Pass | Pass | v03 saves a version-specific setup question; v04 records a Python software-inventory observation. These pass the narrow written-action criterion; neither has been tested with a beginner or actual Windows UI. |
| 10 | Complete archive schema | Pass | Pass | Both retain identity, Start here, A-D, and numbered sections 1-14. |
| 11 | Matching restart action | Pass | Pass | Each archive repeats its own first action consistently in Start here, section 12, and its resume prompt. |
| 12 | Honest provenance | Pass | Pass | Both identify fictional excerpts, no live queries, unverified URLs, and no repository execution. |
| 13 | One archive without approval loop | Pass | Pass | Each run saves one discussion response for the harness and one complete requested archive. |
| 14 | Beginner operational detail | Pass | Pass | Both explain surface, input/action, checks, recovery and handoff, plus a sample mapping in archive section 5. |

Both versions handled the main fixture well. These runs do not establish that v04 is generally more reliable than v03. The extra instructions make decisions more explicit, but instruction coverage alone is not an outcome measure.

## Observed defect and final correction

The v04 tested archive contained an ambiguous sentence in section 2: "No cloud upload is mandatory." The actual user constraint prohibits uploading notes. Correct treatment elsewhere does not remove that local ambiguity, especially if the section is copied or summarized later.

The final v04 skill adds a consistency check requiring direct requirements/prohibitions with the same meaning throughout the archive. The initial output is retained unchanged in the evidence bundle. A third isolated executor received the final skill, the same fixture, and a [paragraph-review request](constraint-review-request.md), without the rubric or intended correction. It returned: "The notes must not be uploaded to the cloud." This narrow corrective test passed. The full two-request comparison was not rerun after this final one-sentence instruction change; the targeted result does not prove it will prevent every future inconsistency.

## Usability findings still requiring validation

- v03's first action creates a setup question, which is feasible but offers limited new information. A written checklist pass does not demonstrate meaningful learning progress.
- v04's first action gathers a Python inventory observation and explicitly says it does not prove a working interpreter. Actual Windows menu availability and novice navigation were not tested.
- Both show useful mapping examples, but neither demonstrates that a real user can perform conversion, detect a wrong result, or complete the handoff unaided.
- Search stopping, query privacy, branch-specific retrieval, stale-source resume, and prior implementation authorization were not exercised by these offline runs. See EVALUATION.md for planned scenarios.

## Artifact identity

Raw inputs, skill snapshots, and unedited executor outputs are preserved in the companion evaluation-evidence ZIP delivered with the local review. It contains fictional task data only; the skill ZIP contains reusable evaluation materials and this summary, not private account outputs.

| Artifact | SHA-256 |
| --- | --- |
| SKILL-v03.md | `d02c71e6342e8bd11541fffeda7205b628ca24722855803e87a22ba27bd0e7d2` |
| SKILL-v04-tested.md | `b79404a0b772ad2d221cdbd48e8349e32d2a3991e7df6e5d62aed9471a86aeaa` |
| SKILL-v04.md | `ff9329e0e09f9adc924843a8d3e3871d3bd36bf136b299311d5e52302f388ad7` |
| run-v03/2026-10-24_local-note-search_v01.md | `8f1487242ee891ddad9ca1c57f1912e98c30a9034d8bd95da0412d767487e5de` |
| run-v03/discussion.md | `cb6ba4cd6a1d1d65aca1ce1aecf5aebead41a3035c1d58d4735b2b0a9ef95f65` |
| run-v04/2026-10-24_local-note-search_v01.md | `b834cd366a7b80d0e8745b8f50a43933e6edcb116b1094aba2b68eee976293ef` |
| run-v04/discussion.md | `a9404b09be0660f70eee4418154fcaf37b133aede3732858af6b43b11cb0b69f` |
| run-repair/repair.md | `f9879702af916d5c05e8c481319774ea0054bcf4e4388ea0ab52542c59357361` |

## Static verification

Static verification passed for the preserved 14-section archive schema, UTF-8 readability, 18 local documentation links, embedded license notice, expected artifact counts, and ZIP byte integrity. The source package contains 14 files; runtime archive output remains one Markdown file per topic. The official skill validator was attempted but could not start because PyYAML is unavailable; a standard-library check covers this skill's simple scalar frontmatter, not arbitrary YAML. Targeted private-path checks are not a general secret scanner. None of these checks establishes live compatibility or learning efficacy.
