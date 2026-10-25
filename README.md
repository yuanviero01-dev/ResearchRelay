# ResearchRelay

Skill identifier: `research-relay`.

Explore GitHub repositories, learn how an AI workflow fits your needs, and preserve your reasoning in one restartable Markdown archive.

Bring your background and an initial repository link. Brainstorm a practical use, discover complementary repositories when needed, and ask to archive when you want a complete research record.

## What it does

- Connects repository capabilities to your goals, tools, and constraints.
- Finds relevant repositories for the next workflow step and explains how their inputs and outputs could connect.
- Separates source evidence, untested claims, proposed integrations, and user decisions.
- Keeps technical detail alongside simple guidance about where to act, what to provide, what to check, and what to do next.
- Produces one Markdown archive with context, decisions, experiments, sources, and a ready-to-use resume prompt.

The communication style emphasizes clear next actions, manageable steps, and a parking lot for side ideas. It adapts ADHD-friendly communication preferences without assuming a diagnosis. English is the default; explicitly request another language when needed.

## Quick start

1. Load the skill using a supported method below.
2. Provide your background, goal, constraints, and initial GitHub link or links file.
3. Brainstorm. Ask for additional repositories when you need help with the next step.
4. Say **Archive this idea** to save the discussion as a complete Markdown document.

```text
Use research-relay.
My background: I work with a small design team.
My goal: find project decisions in our existing notes.
My constraints: keep project notes local and start with a small experiment.
Repository: paste your GitHub repository URL here.

Assess relevance and brainstorm first. I am new to operating AI tools.
Explain where to act, what input to provide, and how to check the result.
Keep the technical detail. Wait to archive until I ask.
```

## Find repositories for the next step

```text
Find relevant repositories using the GitHub links I supplied earlier
and the workflow we are discussing. Explain each candidate's role,
how its inputs connect to the original repository's outputs,
required setup, and what remains unverified.
Recommend one small next check. Continue brainstorming for now.
```

The assistant uses the initial repositories as references and looks for the missing capability. Candidates are identified as complements, replacement alternatives, or learning references. It explains format conversions, source preservation, prerequisites, and important uncertainties. Keeping the original repository alone is a valid recommendation when it already meets the need.

Search is focused on the next decision. Live discovery requires browsing or repository tools in the host platform. If access is unavailable, the assistant can inspect supplied documents or prepare clearly labeled search queries. A relevant candidate is not automatically a working integration.

## Load the skill

Copy the folder named `research-relay` into one supported location. `SKILL.md` belongs directly inside that folder.

| Host | Project-local location | Personal location |
| --- | --- | --- |
| Codex | `.agents/skills/research-relay/` | `~/.agents/skills/research-relay/` |
| Claude Code | `.claude/skills/research-relay/` | `~/.claude/skills/research-relay/` |

In Claude Code, invoke `/research-relay`. In Codex, ask to use `research-relay` or select it through the client's skill interface. For host-specific details, see the [OpenAI skill documentation](https://learn.chatgpt.com/docs/build-skills) and [Claude Code skill documentation](https://code.claude.com/docs/en/skills).

For another assistant, supply `SKILL.md` through its supported instruction workflow. Uploading it to an ordinary chat does not necessarily install a persistent skill or grant tools. Keep the MIT license and attribution when redistributing the file or package.

## Archive contents

Each archive includes identity metadata, a short **Start here** block, and 14 numbered sections:

| Group | Sections |
| --- | --- |
| Context and intended use | 1. Topic and summary; 2. Background and relevance; 3. LinkRepo and source snapshot; 4. Description: future use context |
| Proposed approach and feasibility | 5. Workflow; 6. Scope and deliverables; 7. Hypotheses and research questions; 8. Requirements and dependencies; 9. Risks and limitations |
| Decisions and experiments | 10. Decisions, alternatives, and parking lot; 11. First experiment and success criteria |
| Restart and traceability | 12. Restart trigger and first action; 13. Resume packet; 14. Sources and change history |

Beginner guidance appears inside the relevant sections. It explains **Where**, **Do this**, **You should see / check**, **If different**, and **Keep / pass next**, while preserving technical terms, prerequisites, evidence, and limitations.

| Readiness | Meaning |
| --- | --- |
| READY | Known prerequisites allow the stated next step; correctness is not proven |
| CHECK FIRST | A prerequisite or instruction needs verification |
| BLOCKED | A known missing requirement prevents that step |
| DONE | The action was performed and its observable check was met |

Future checkpoints say **Done when...**. Readiness is separate from evidence and agreement.

Archive filename pattern: `YYYY-MM-DD_short-topic_v01.md`. The suffix tracks revisions of an individual research archive. See the [fictional example archive](examples/local-note-search.md) for a complete learning exercise.

## Resume your research

Attach your saved archive and use:

```text
Use research-relay. Read the attached archive, restore its context and
current decision, and help me take the first restart action.
Check sources that may have changed and identify outdated assumptions.
```

The assistant retains component roles, unresolved prerequisites, and historical results instead of treating earlier assumptions as newly verified facts.

Use `normal mode` to disable the special communication style for the current workflow. This keeps the archive structure and beginner companion. Ask for a technical-only archive explicitly if you want to omit the beginner companion.

## Scope and requirements

This is an instruction skill. It has no runtime dependencies of its own; browsing, repository access, file creation, and execution capabilities depend on the host. It does not supply cross-platform memory, automatic reminders, or background monitoring. Attach the archive when moving to another conversation or platform.

Repository analysis and discovery do not themselves install or run software. Archiving produces one Markdown file per agreed topic and does not publish it. If file creation is unavailable, the assistant provides the complete Markdown for you to save. Store personal research records outside the public skill repository.

## Package contents

```text
research-relay/
  SKILL.md
  README.md
  LICENSE
  THIRD_PARTY_NOTICES.md
  CONTRIBUTING.md
  .gitignore
  examples/
    local-note-search.md
```

`SKILL.md` contains the complete runtime instructions. The remaining files provide usage guidance, a fictional example, and redistribution information.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for focused changes and behavior checks. Use fictional examples when reporting problems and describe observed behavior without including private research context.

## License and credit

MIT. The communication layer adapts [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd), by Ayoub Ghriss. See [LICENSE](LICENSE) and [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
