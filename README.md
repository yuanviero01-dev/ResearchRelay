# rnd-repo-archive

Learn an open-source AI workflow and preserve the complete technical reasoning in one restartable Markdown R&D archive.

Bring your background and a repository URL. Explore how the repo could fit your work, agree on a direction, then save the reasoning and first experiment. An integrated ADHD-friendly communication layer makes the next action visible while the archive retains the full context.

## Why this skill exists

The design hypothesis is that many people want to learn AI workflows from open-source repositories but struggle to turn documentation into practical use. The skill adds simple operational explanations to the technical record: where to work, what to provide, what should happen, how to check it, and what to do next.

This is a learning objective, not a measured effectiveness claim. The beginner companion preserves technical terms, prerequisites, evidence, and caveats. It does not imply that a repo works in every AI platform or that a chat simulation runs a plugin.

## v04 improvements

This revision strengthens version-specific evidence, mandatory constraints, concrete input/output mappings, and restart history. Discovery has a default focused pass plus one refinement when needed; it stops when the next decision is supported. External queries use capability terms rather than private project details. Archive activation follows the user's intent, including negation and quoted examples.

The archive still uses one Markdown file and the same 14 sections. The skill remains self-contained in `SKILL.md`; evaluation files are optional maintainer resources. See [recorded evaluation results](evaluation/RESULTS-v04.md) for what has and has not been tested.

## What you get

- Contextual repo analysis and seed-based discovery of repositories for your next workflow step.
- Clear separation of verified facts, documentation claims, assumptions, and decisions.
- A complete `.md` archive with sources, hypotheses, experiments, and a beginner walkthrough alongside the technical record.
- Action-first discussion, explicit readiness indicators, small next actions, and a parking lot for side ideas.
- English instructions and output by default, with explicit language overrides supported.

The deliverable is Markdown only. This package has no runtime dependencies, automatic reminders, background monitoring, or cross-platform memory. Repository access and file creation depend on the host's tools and permissions.

## Quick start

1. Install using a local option below, or supply `SKILL.md` through your assistant's supported instruction workflow.
2. Provide your relevant background and a repository URL.
3. Ask to brainstorm. When needed, ask for relevant repositories using the initial links as references.
4. Say **Archive this idea** when ready.

Example prompt:

```text
Use rnd-repo-archive.
My background: I build internal tools for a small design team.
My problem: useful repository ideas get lost after brainstorming.
My constraints: a small local proof of concept before any paid service.
Repository: paste the repository URL here.
Assess its relevance and brainstorm first. I am new to operating AI tools.
When I ask to archive, keep the technical detail and add simple operational guidance.
Wait to archive until I ask.
```

To resume later:

```text
Use rnd-repo-archive. Read the attached archive, restore the current decision,
and help me take the first restart action. Check sources that may have changed.
```

Use `normal mode` to disable the communication layer for the current workflow while retaining the R&D structure. Ask to re-enable ADHD-friendly mode when wanted. This is a communication preference, not a diagnosis. Turning it off does not remove the beginner companion from an archive. Request a technical-only archive explicitly if you do not want that companion.

## Discover repositories during brainstorming

Ask in natural language, including your preferred language. For example:

```text
Find relevant repositories that could help with the next step, using the
GitHub repository links I supplied earlier as references. Tie the search to
my background and the workflow we are discussing. Explain each candidate's
role, how its inputs connect to the seed repository's outputs, prerequisites,
and what is still unverified. Recommend one small next check.
Continue brainstorming; archive when I ask.
```

If your links are in a file, attach it and identify it in the request. The assistant reuses the available links and context. It asks only when a missing goal or ambiguous seed would materially change the search.

The flow is **seed repositories → missing capability → inspected candidates → proposed connection → first validation check**. You receive a short search basis, usually two to four candidates with evidence and feasibility, and a recommendation. Each candidate is identified as a complement, replacement alternative, or learning reference. A repository can be relevant while its integration remains untested.

The beginner explanation tells you what each repository would do, what to pass between them, where to act, and how to check the result. The technical explanation retains formats, interfaces, runtime/access requirements, and unresolved dependencies. Adding a repo is optional if the existing one already meets your need.

Live discovery requires search or browsing tools in your AI platform. Without access, the assistant labels the limitation and can prepare search queries or inspect files you provide. It does not claim those queries were executed. No suitable result is an acceptable finding.

When you later say **archive**, the discovery findings become part of the same 14-section Markdown archive: LinkRepo (3), Workflow (5), Requirements (8), Decisions (10), Experiment (11), and Sources (14). The search alone does not install or run the candidates. You can explicitly request both discovery and archiving in the same prompt.

## Local installation

Copy this package into a directory named `rnd-repo-archive` at one location below. `SKILL.md` must be directly inside it. Keep the license and attribution files when redistributing the package.

| Host | Project-local directory | Personal directory |
| --- | --- | --- |
| Codex | `.agents/skills/rnd-repo-archive/` | `~/.agents/skills/rnd-repo-archive/` |
| Claude Code | `.claude/skills/rnd-repo-archive/` | `~/.claude/skills/rnd-repo-archive/` |

In Claude Code, invoke `/rnd-repo-archive`. In Codex, explicitly ask to use `rnd-repo-archive` or select it from your client's skill interface. Managed environments may restrict local discovery.

Paths checked against [OpenAI skill documentation](https://learn.chatgpt.com/docs/build-skills) and [Claude Code skill documentation](https://code.claude.com/docs/en/skills) on 2026-10-24. These are local instructions; uploading a file into an ordinary chat does not necessarily register a persistent skill. This is an instruction skill, not a marketplace plugin.

## Archive contents

Identity metadata and a five-item-or-shorter **Start here** block precede the full record:

| Group | Contents |
| --- | --- |
| Context and intended use | Topic, background, relevance, LinkRepo, source snapshot, future-use description |
| Approach and feasibility | Workflow, scope, hypotheses, requirements, risks |
| Decisions and experiments | Agreements, alternatives, parking lot, first experiment, success criteria |
| Restart and traceability | Restart trigger, first action, resume prompt, sources, change history |

The groups and 14 numbered sections are unchanged. Beginner guidance is added inside them, especially future use (4), workflow (5), prerequisites (8), the experiment (11), and restart (12-13).

### Beginner walkthrough

Each meaningful step explains **Where**, **Do this**, **You should see / check**, **If different**, and **Keep / pass next**. Technical steps remain available above the companion. Only relevant terms are defined, using simple adult language.

Readiness labels have explicit meanings:

| Indicator | Meaning |
| --- | --- |
| READY | Known prerequisites allow the next step; correctness is not yet proven |
| CHECK FIRST | A prerequisite or instruction is unverified; a named check comes first |
| BLOCKED | A known missing requirement prevents the step |
| DONE | The action was performed and its observable check was met |

A future checkpoint says **Done when...**. It is never marked completed before execution. These labels describe readiness, separately from whether a claim is verified, documented, proposed, agreed, or unknown.

Filename pattern: `YYYY-MM-DD_short-topic_v01.md`.

See the [illustrative archive](examples/2026-10-24_local-note-search_v02.md). Its scenario is fictional. It demonstrates a complete beginner chat exercise, the input-to-output handoff, and a blocked repository test without pretending the exercise executes a repo.

## Files

```text
rnd-repo-archive/
  SKILL.md
  README.md
  LICENSE
  THIRD_PARTY_NOTICES.md
  CONTRIBUTING.md
  EVALUATION.md
  .gitignore
  evaluation/
    discovery-fixture.md
    discovery-requests.md
    discovery-rubric.md
    constraint-review-request.md
    RESULTS-v04.md
  examples/
    2026-10-24_local-note-search_v01.md
    2026-10-24_local-note-search_v02.md
```

The v01 example is retained as history; v02 demonstrates the current beginner companion.

`SKILL.md` contains the full runtime instructions. Other files support distribution, attribution, examples, and maintenance; the assistant does not need to load them for every task.

## Publish on GitHub

1. Create a repository named `rnd-repo-archive` in your account.
2. Upload this package's contents so `README.md` and `SKILL.md` are at the repository root. Preserve `.gitignore` too.
3. Review the files and publish your initial commit.

Suggested description:

> Learn open-source AI workflows through complete Markdown R&D archives, beginner walkthroughs, and ADHD-friendly communication.

Suggested topics: `agent-skills`, `research`, `markdown`, `knowledge-management`, `adhd-friendly`.

Keep personal archives outside this public skill repository. `.gitignore` excludes conventional `archives/` and `private/` directories, but is not a privacy scanner. Review anything else you add before publishing.

## Validation and contributions

This is a prepared source package. Two user-supplied archive outputs were reviewed for consistency and beginner usability. They motivated stricter context/evidence handling, prerequisite gates, matching restart actions, and the beginner companion. Different recorded backgrounds mean those outputs are not a controlled account comparison.

The source package includes an offline comparison using the same fictional evidence and requests against v03 and v04. Results and limitations are recorded in [evaluation/RESULTS-v04.md](evaluation/RESULTS-v04.md). This is not a live repository integration test or a novice user study, and the skill has not been rerun in the user's two accounts. No GitHub publication or release is claimed. Private account outputs are not included in this public package.

Use [EVALUATION.md](EVALUATION.md) for behavior checks before a release and [CONTRIBUTING.md](CONTRIBUTING.md) for changes.

## License and credit

MIT. The communication layer adapts [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd), by Ayoub Ghriss. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for provenance and [LICENSE](LICENSE) for permission terms.
