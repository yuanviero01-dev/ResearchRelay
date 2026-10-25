# Search a small set of local project notes

**Archive ID:** EXAMPLE-NOTE-WALKTHROUGH-001  
**Created / updated:** 2026-10-25  
**Version:** v01  
**Status:** Exploring  
**Owner:** Fictional design-team researcher  
**Tags:** local-search, project-notes, retrieval, beginner-learning

This is an illustrative fixture. The people, note, and design choices are fictional. No repository has been selected, installed, or tested. All outputs below are expected examples, not recorded AI results.

## Start here

- **Idea:** Test whether local note search can help retrieve project decisions with correct source references.
- **Current state:** The first learning action is READY: the sample note is included below. Chat access is CHECK FIRST; repository execution is BLOCKED because no candidate has been selected.
- **Main unknown:** Whether a candidate repo can retrieve the correct passage and preserve its source reference.
- **First action:** Read the sample note in section 5 and identify the decision sentence.
- **Restart trigger:** Continue the learning exercise when a usable text chat is available; consider a repository test after selecting and inspecting a candidate.

READY means the stated next action has what it needs. CHECK FIRST means a prerequisite is unknown. BLOCKED means a known missing requirement prevents that stage. DONE would mean an action and its observable check were completed; no step is marked DONE here.

## A. Context and intended use

### 1. Topic and summary

Explore local search over project notes. The expected benefit is faster retrieval of a decision with a correct source reference. A single-note learning exercise first teaches input, output, checking, and handoff. It does not test indexing or retrieval software. There are no measured performance results.

### 2. Background and relevance

The fictional team searches notes manually and sometimes repeats discussions. The reader is new to operating AI workflows. A small example can explain the process before software setup. Actual hardware, engineering time, and coding-assistant access are unknown.

### 3. LinkRepo and source snapshot

**Repository name / URL:** Not supplied.  
**Proposed role:** Local indexing and retrieval component.  
**Revision / access date:** Not applicable; no repo was accessed for this fixture.  
**License / documentation:** Not verified.  
**Evidence status:** The operating workflow is proposed. No repository-specific instruction is presented as runnable.

### 4. Description: future use context

A team member would search when recalling a project decision. Approved notes and a question would be the inputs. A candidate component would return passages with source references. The reader would verify those passages before using them. Integration with the team's usual note tool is outside the first test.

**In plain language:** You give the tool notes and a question. It tries to find the relevant words. You compare its answer with the original note before trusting it. The proposed repo would add searching across stored notes; ordinary chat over one pasted note does not demonstrate that capability.

**Terms used here:**

- **Repository:** A published collection of project files; opening its page does not run its software.
- **Index:** A prepared representation of the notes that a search component can use.
- **Retrieval:** Finding relevant stored content for a question.
- **Source reference:** A filename, note ID, or location that lets you check where an answer came from.
- **Baseline:** A comparison result produced before testing the candidate on the same task.

## B. Proposed approach and feasibility

### 5. Workflow

**Technical operating workflow, proposed:**

1. Collect approved notes and preserve stable source IDs.
2. Index them with a selected component after verifying supported formats and setup.
3. Submit questions whose answers are known in the sample.
4. Retrieve passages with source references.
5. Compare each result with the originals and store errors as well as successes.

The input to each retrieval query is the indexed note collection plus a question. The output is a passage/reference pair for evaluation. Format support, indexing behavior, and integration remain unknown. Missing references or incorrect passages count as failures, not successful retrieval.

#### Beginner walkthrough: manual learning exercise

This is a rehearsal in ordinary text chat using fictional data. It teaches the handoff and verification process. It does not install, invoke, or validate a repository or plugin.

**Sample note provided with this fixture:**

```text
Note ID: N1
Project: Courtyard Study
At the review on 12 October, the team chose shaded benches for the west edge.
Reason: afternoon heat made the existing seating uncomfortable.
No budget or supplier was selected.
```

**Step 1. Read the sample note. Readiness: READY.**

- **Where:** This Markdown document, in any reader.
- **Do this:** Read the sample note and identify the decision sentence.
- **You should see / check:** The sentence says the team chose shaded benches for the west edge. It does not name a supplier or budget.
- **If different:** If your sample differs, use the supplied fixture first. Do not mix it with real project notes for this exercise.
- **Keep / pass next:** Keep Note ID N1 and the full note. Step 2 needs the original wording, not a summary.

**Step 2. Ask for an extraction. Readiness: CHECK FIRST until ordinary text chat is available.**

- **Where:** The message box of an AI text chat you can already use. This is not a terminal or plugin-command interface.
- **Do this:** Paste the complete practice prompt below as one message.
- **You should see / check:** An answer containing a decision, reason, exact quote, and source ID. A fluent answer without a matching quote is insufficient.
- **If different:** If no chat is available, keep the manual result and pause this step. If the answer lacks a quote, ask it to copy the exact supporting sentence from N1. Do not add invented sources.
- **Keep / pass next:** Copy the answer and the original note together into a temporary working note. Step 3 compares them.

**Practice prompt, with complete fictional input:**

```text
Use only the note below. Identify the decision and its reason.
Return four fields: Decision, Reason, Exact supporting quote, Source ID.
If a requested fact is absent, write "Not stated". Do not invent facts.

Note ID: N1
Project: Courtyard Study
At the review on 12 October, the team chose shaded benches for the west edge.
Reason: afternoon heat made the existing seating uncomfortable.
No budget or supplier was selected.
```

**Step 3. Check and retain the result. Readiness: CHECK FIRST until step 2 has an answer.**

- **Where:** The chat answer beside this document or in a plain-text editor.
- **Do this:** Compare the answer's four fields against N1.
- **You should see / check:** Decision: shaded benches on the west edge. Reason: uncomfortable seating due to afternoon heat. Quote: exact supporting words from N1. Source ID: N1. These are expected values, not a claimed model response.
- **If different:** Mark the mismatch. Request a correction using N1; if it still invents facts, save the failure and stop using that answer as evidence.
- **Keep / pass next:** Save the checked fields, original prompt, and any failure. Use them to define one known-answer query for a later repository test. Do not label this an executed repo result.

**Done when:** The answer has the correct decision, reason, exact quote, and source ID, and the reader has compared all four with N1. No completion has been observed for this example.

### 6. Scope and deliverables

The learning exercise covers one fictional note and one extraction task. The later repo experiment would cover a small approved collection. Exclude production deployment, automatic rewriting, cloud synchronization, and unsupported installation instructions. Retain the prompt, answer, source, checks, and failures. The researcher evaluates them.

### 7. Hypotheses and research questions

**Repository hypothesis:** A candidate can retrieve useful passages for questions with known answers. Evidence requires an actual candidate run, not the manual exercise.

**Learning hypothesis:** The companion may help a novice supply input, check an answer, and pass the right artifact forward. Evidence requires observing the reader; an AI-generated answer alone does not establish understanding.

**Open questions:** Supported note format, accuracy of references, missing decisions, and the setup needed for the chosen candidate.

### 8. Requirements and dependencies

**Before you start:**

| Requirement | Readiness and meaning |
| --- | --- |
| Sample note | READY: N1 is included in section 5 |
| Ordinary text chat | CHECK FIRST: availability and account access are unknown |
| Place to retain the answer | CHECK FIRST: choose an available text editor or existing working note |
| Candidate repository | BLOCKED for repo execution: none has been selected |
| Candidate setup and approved dataset | CHECK FIRST after selection; do not assume installation is complete |

No terminal, plugin, or external connector is needed for the manual note exercise. Those may be required by a future candidate and must be checked then. Costs, hardware, installation commands, and runtime duration are unestimated. Public or private service requirements must be checked before using real notes. This example contains no credentials or real project data.

### 9. Risks and limitations

Incorrect quotes can make an answer look supported; compare exact text. A single-note exercise does not test search over many files. A small collection may not represent the wider archive. Missing tool access blocks execution but does not prevent reading N1. Keep any real sensitive notes out of this public example.

## C. Decisions and experiments

### 10. Decisions, alternatives, and parking lot

**Example recommendation, not a real user agreement:** Begin with the supplied note exercise because the learner's tools are unknown and no candidate repo exists. It provides a small learning action without pretending setup is complete.

Direct repo testing is deferred until a candidate and prerequisites are verified. Building a custom integration is deferred until a real test demonstrates a gap. Cloud search and summarization remain in the parking lot. The recommendation can change when tool access and candidate evidence are available.

### 11. First experiment and success criteria

**First learning check:** Follow section 5 with N1 once chat access is confirmed. Verify the four fields and ask the reader to explain which surface they used, why the quote matters, and what is passed next.

**How to tell it worked, proposed rubric:**

- The reader selects ordinary text chat rather than treating the prompt as a shell command.
- The full note reaches the model with Source ID N1 intact.
- The reader catches missing or invented support by comparing exact words.
- The saved artifact retains the prompt, answer, source, and check outcome.
- The reader distinguishes this rehearsal from a repository execution test.

These are observable checks, not reported successes or validated measures of learning effectiveness.

**Later repository experiment:** After selecting a candidate, inspect its requirements, establish an approved sample, and compare its results with manual search on the same questions. Record correct references, missed answers, and incorrect passages. No performance baseline has been measured. Continue, adapt, or stop based on explicit criteria agreed after inspecting the candidate; a README assessment is not a speed or accuracy baseline. No timebox is set.

## D. Restart and traceability

### 12. Restart trigger and first action

**First action:** Read the sample note in section 5 and identify the decision sentence.

**Done when:** You can point to the sentence about shaded benches on the west edge. Then keep the full N1 note and confirm ordinary chat access before step 2. Candidate selection and installation are later stages, not hidden prerequisites for reading this sample. No review date or reminder is scheduled.

### 13. Resume packet

> Resume R&D from EXAMPLE-NOTE-WALKTHROUGH-001, Search a small set of local project notes, v01. This is a fictional scenario for a beginner. The goal is to learn input, output, checking, and handoff before evaluating local note-search software. No repository is selected. The proposed first path is a manual chat exercise, not plugin execution. Reading the included note is READY; chat access is CHECK FIRST and repository execution is BLOCKED. First, read the sample note in section 5 and identify the decision sentence. Confirm chat access before continuing the exercise. Preserve technical detail, use simple operational explanations, and check candidate requirements before any later repo test.

Attach this Markdown file when opening a new conversation.

### 14. Sources and change history

No external repo claims support this fictional example. N1 is synthetic data written for the learning exercise. Expected outputs are derived directly from that note and are not actual AI responses.

- 2026-10-25: Created this standalone fictional example. The walkthrough describes expected outputs; repository operation and learner outcomes have not been tested.
