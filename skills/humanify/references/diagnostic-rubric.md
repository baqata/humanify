# Diagnostic rubric

Use this rubric for the diagnostic phase of `humanify`. Diagnose accountable communication, not presumed authorship. Explain how each finding affects meaning, reasoning, reader use, genre fit, or rhetorical force. Do not calculate, quote, or optimize an AI-likelihood measure or detector score.

## Audit reasoning before drafting a new document

Before the new-document human gate:

1. List every planned material conclusion, recommendation, instruction, and decision.
2. Link each one to supplied facts, source claims, approved institutional positions, and the warrant needed to move from support to conclusion.
3. Mark a link `supported`, `partly supported`, `unsupported`, or `normative choice`.
4. Identify missing operational capabilities, causal links, comparison criteria, legal rules, values, or authority.
5. Do not let approval relabel a missing premise as evidence. Ask for support, propose a neutral structure, or require transparent authorization to present the position as a choice despite the gap.
6. Include this claim-evidence-warrant map in the pre-draft plan and carry unresolved gaps into the draft and final verification record.

## Contents

[Contract](#1-establish-the-diagnostic-contract) · [Units](#2-define-and-cover-analysis-units) · [Ledger](#3-maintain-the-issue-ledger) · [Scales](#4-diagnose-at-every-scale) · [Consistency](#5-check-internal-consistency) · [Report](#6-assemble-the-diagnostic-report) · [Gate](#7-stop-at-the-human-gate) · [Completion](#8-apply-the-completion-test)

## 1. Establish the diagnostic contract

Record the following before judging the prose:

- Identify the document's primary language, route linguistic judgments to its language module, and infer the macro-genre, intended readers, purpose, expected reader action or understanding, and stakes.
- Identify the authorial or institutional role, governing register, house style, jurisdiction, source boundary, and format constraints.
- Record intended reader, institutional speaker, author, approver, decision-maker, and action owner as separate roles. Mark an unknown role as unknown; never derive decision authority or obligation from audience alone.
- Treat distinct sections as functional registers within one document when their purposes differ.
- Mark every inference as inferred; never present an inferred audience, purpose, or genre convention as supplied fact.
- Distinguish the source's claims, the author's claims, attributed third-party claims, recommendations, and open questions.
- Limit factual checking to the supplied document and supplied annexes.

Create a protected-content register before proposing changes. Include, as applicable:

- claims, conclusions, names, entities, dates, numbers, ranges, percentages, currencies, and units;
- definitions, stable technical terminology, quotations, citations, source relationships, and attribution;
- legal modalities, obligations, permissions, prohibitions, conditions, exceptions, deadlines, causal language, comparison classes, populations, jurisdictions, time periods, and evidentiary limits;
- uncertainty, confidence, disagreement, caveats, and limitations;
- equations, code, commands, labels, identifiers, and named classifications;
- intentional repetitions, marked language, and genre-required formulae;
- document mechanics that carry meaning or navigation.

Record successful mechanisms that revision must preserve. Capture effective hierarchy, precise definitions, useful repetition, calibrated uncertainty, strong transitions, or deliberate stylistic markedness when later edits could damage them.

## 2. Define and cover analysis units

Build a semantic hierarchy before detailed inspection:

`document -> part or chapter -> section -> subsection -> paragraph cluster -> paragraph or structured object`

Apply these rules:

- Assign every unit a stable identifier such as `U001`, `U002`, and `A001` for an annex unit; preserve it across diagnosis, approval, revision, and verification, and never renumber it after edits.
- Prefer the lowest heading-bounded unit that contains a complete rhetorical move; split an oversized unit only at a genuine topic or argument boundary.
- Keep paragraphs, tables, figures with essential captions, quotation blocks, footnote sequences, equations, and tightly connected arguments intact.
- Include front matter, executive material, appendices, annexes, endnotes, and reference matter when they affect interpretation or consistency.
- Give each local inspection the document map, protected-content register, terminology register, and summaries of adjacent units.
- Review adjacent-unit relations as part of both units rather than treating boundaries as context resets.
- Record every unit in a coverage matrix and assign `clear`, `issues recorded`, `not applicable`, or `blocked by missing context` for every diagnostic dimension; explain every `not applicable` or `blocked` entry.

Run three logical diagnostic rounds:

1. **Map:** Build the hierarchy, reverse outline, protected-content register, terminology register, claim map, cross-reference map, and annex map.
2. **Inspect:** Review every bounded unit exhaustively against the shared map and every applicable dimension in this rubric.
3. **Reconcile:** Aggregate all unit ledgers and recheck cross-unit progression, proportions, duplication, gaps, terminology, claims, numbers, references, and annex relationships.

Treat these as rounds of work, not a fixed number of workers. Scale each round to the document. Complete all units before presenting the whole-document diagnosis.

## 3. Maintain the issue ledger

Create one authoritative ledger. Give every issue a globally unique, immutable identifier:

`HUM-{scope}-{category}-{sequence}`

Use `G` for global, `X` for cross-unit, or the stable unit identifier for local scope. Use these category codes:

- `SIT`: communicative situation;
- `DOC`: document architecture;
- `SEC`: section function;
- `PAR`: paragraph progression;
- `SEN`: sentence, reference, or rhythm;
- `LEX`: diction or register;
- `STA`: stance or epistemics;
- `PAT`: recurring rhetorical pattern;
- `CON`: internal consistency;
- `FID`: fidelity risk;
- `FMT`: format or artifact risk.

For example, use `HUM-U014-PAR-003`, not a heading title that may later change.

Record every issue with these fields:

- **ID:** immutable issue identifier.
- **Scope:** global, cross-unit, unit, paragraph, sentence, phrase, table, figure, note, or format object.
- **Category:** one primary rubric category; add cross-references rather than duplicate the issue.
- **Exact anchor:** file or annex, stable unit ID, heading path, paragraph or object ID, sentence or cell, and page or line when available.
- **Excerpt:** the smallest excerpt that makes the issue recognizable; omit only when the issue concerns pure structure or formatting.
- **Diagnosis:** the concrete rhetorical, semantic, logical, linguistic, or artifact problem.
- **Reader effect:** the likely misreading, effort, loss of trust, failed action, or weakened force for the intended reader.
- **Proposed treatment:** the change operation and intended result, without drafting the final wording unless needed to disambiguate the plan.
- **Protected elements:** facts, terms, qualifications, sources, effects, or formatting that the treatment must retain.
- **Consequence:** `blocking`, `major`, `moderate`, or `minor` for this document's purpose.
- **Change risk:** `critical`, `high`, `medium`, or `low`, based on the chance that revision could alter meaning, legal effect, evidence, or artifact integrity.
- **Confidence:** `high`, `medium`, or `low`, based on the available internal evidence and certainty of the diagnosis.
- **Dependencies:** prerequisite issue IDs, unresolved content decisions, source conflicts, or format constraints.
- **Approval state:** `pending`, `requires-answer`, `approved`, `excluded`, `superseded`, `resolved`, or `unresolved`.

Keep consequence and disposition independent. Human approval to preserve wording does not reduce a `blocking` consequence when the missing information still prevents the intended reader outcome.

Anchor every material finding exactly. Use both semantic and positional anchors because pagination and line numbers can change:

- For Markdown or text, record heading path, stable unit, paragraph, line, and excerpt.
- For Word, record heading path, stable unit, paragraph or structured-object index, sentence or run excerpt, and rendered page when useful.
- For a table, record table identifier, row label or index, column label or index, and cell excerpt.
- For a figure, record figure identifier, caption, relevant callout, and referring passage.
- For notes, record footnote or endnote number and its anchor passage.
- For an annex, record annex identifier plus its internal heading, object, and location.
- For pasted text, number paragraphs and sentences before diagnosis.
- For global or cross-unit issues, enumerate every affected unit or section and anchor the relationship among them.

Handle recurring patterns without sacrificing exhaustiveness:

- Create one parent `PAT` issue for the shared rationale, reader effect, and proposed treatment, then create a child record for every affected location using suffixes such as `-O001`.
- Give each occurrence its exact anchor and excerpt, plus any local exception or distinct risk.
- Enumerate every location; never substitute `throughout`, `often`, `etc.`, or a sample count for the occurrence ledger.
- Split the parent issue when occurrences have materially different causes, effects, or treatments.
- Keep isolated issues independent rather than forcing them into a pattern.

Do not invent issues to populate a category. Mark a dimension `clear` when a complete review finds no material problem.

## 4. Diagnose at every scale

### 4.1 Communicative situation

- Determine what the document is trying to accomplish, for whom, under which constraints, and with what consequences.
- Test whether its genre, register, level of explicitness, and relation to the reader fit that situation.
- Test whether the writer or institution has the authority, evidence, or situated knowledge implied by the prose.
- Identify missing context that prevents the reader from interpreting or acting on the document.
- Identify costly assumptions about reader knowledge, terminology, procedure, culture, or jurisdiction.
- Identify conflicts between the apparent purpose and the requested action, tone, structure, or level of detail.
- Preserve technical, institutional, legal, academic, literary, and other genre obligations while improving reader fit.

### 4.2 Document architecture

- Build a reverse outline that states each unit's function and its relation to the whole.
- Trace the governing progression: claim, support, qualification, comparison, cause, condition, consequence, recommendation, decision, chronology, procedure, scene, or other genre-specific movement.
- Test whether the opening establishes the right problem, frame, promise, or situation for this genre.
- Test whether the sequence follows the subject and reader task rather than a prefabricated outline.
- Identify missing premises, evidence, counterweights, steps, transitions, syntheses, or conclusions.
- Identify duplication, circular progression, delayed definitions, premature conclusions, and conclusions not earned by the body.
- Test whether space and emphasis reflect actual importance; flag mechanically symmetric treatment of unequal material.
- Test whether headings express the real hierarchy and whether summaries change the reader's understanding or merely repeat.
- Test whether the conclusion, recommendations, and executive material remain faithful to the supporting sections.
- Test whether annexes are integrated, cited, and assigned a clear evidentiary or operational role.

### 4.3 Section function

- State the job of every section in one sentence.
- Test whether every paragraph contributes to that job or belongs elsewhere.
- Test whether the section begins from context available to its intended reader and reaches a discernible result.
- Check the order, proportion, internal arc, and handoff to adjacent sections.
- Identify repeated introductions, generic scene-setting, recap inflation, and conclusions that only paraphrase headings.
- Preserve legitimate shifts in density and register among executive, methodological, analytical, legal, narrative, and annex sections.
- Flag unexplained shifts that make the document sound as if different speakers or templates were assembled without reconciliation.

### 4.4 Paragraph progression

- Identify each paragraph's rhetorical job and relation to the paragraph before and after it.
- Allow a paragraph to perform multiple linked jobs when the genre and reasoning require it.
- Test whether its topic is recoverable and whether new information has an intelligible attachment point.
- Test whether claims receive the needed support, example, explanation, qualification, consequence, or limit.
- Identify hidden topic shifts, orphaned evidence, buried pivots, list-like accumulation, and endings that do not advance the document.
- Distinguish useful repetition from restatement that adds no rhetorical, pedagogical, legal, or aesthetic value.
- Identify uniform paragraph shapes when the functions differ and over-varied shapes when the reader needs procedural regularity.
- Test whether transitions encode real relations rather than merely announcing addition, contrast, or summary.

### 4.5 Sentence, reference, and rhythm

- Reconstruct the proposition before judging style: actor, action, object, scope, modality, negation, conditions, exceptions, quantities, time, and uncertainty.
- Resolve ambiguous, distant, shifting, or falsely continuous references.
- Test whether pronouns, demonstratives, labels, and repeated terms match the reader's current focus.
- Test whether information order makes the sentence attach to prior context and places emphasis where it belongs.
- Identify excessive embedding, distant dependencies, misplaced modifiers, scope ambiguity, and coordination that conceals hierarchy.
- Split or combine sentences only when the conceptual relation, processing load, emphasis, or pace warrants it.
- Evaluate cadence as a functional pattern of syntax, punctuation, sound, emphasis, and pause; never target variation for its own sake.
- Preserve a long sentence when its controlled structure clarifies one relation; preserve a short sentence when it marks a decision, pivot, consequence, or deliberate beat.
- Preserve purposeful fragments, parallelism, asymmetry, or repetition in genres that use them; flag marked forms that perform no discernible job.
- Read difficult or tonally important passages aloud when sound and pacing matter.

### 4.6 Diction and register

- Prefer the most familiar wording that preserves the exact meaning and genre obligation.
- Retain, define, or exemplify technical terms that carry necessary distinctions.
- Preserve one term for one stable concept; flag synonym churn that creates false distinctions or weakens reference.
- Identify generic abstractions that conceal the relevant actor, mechanism, evidence, constraint, or consequence.
- Request source-grounded specificity when the reader needs it; never invent detail to create texture.
- Test idiom, collocation, formality, treatment, metaphor, and evaluative language against language, locale, audience, and genre.
- Evaluate nominalization, passive voice, impersonal form, and dense noun phrases by function, agency, cohesion, and meaning rather than by blanket preference.
- Identify clichés, inflated phrasing, decorative precision, and fashionable terminology only when they impede this document.
- Preserve official names, defined expressions, quotations, jurisdiction-specific terms, and deliberate literary diction.

### 4.7 Stance and epistemics

- Identify who is responsible for every material claim and recommendation.
- Separate observation, measurement, source report, interpretation, inference, allegation, prediction, and institutional position.
- Match certainty to the document's internal evidence and supplied attribution.
- Preserve hedges, ranges, limitations, disagreement, and scope when they carry evidentiary meaning.
- Flag uniform certainty, ritual hedging, empty confidence, false neutrality, and an unsupported view from nowhere.
- Detect changes from association to causation, possibility to probability, recommendation to obligation, or local result to general rule.
- Make agency visible where responsibility matters; preserve impersonal or passive constructions where actor suppression is intentional and legitimate.
- Test whether the document engages its reader appropriately through explanation, direction, invitation, warning, or restraint.
- Preserve a coherent institutional or authorial position across sections while allowing function-driven modulation.

### 4.8 Generated-feeling patterns as rhetorical problems

Translate any reaction that the prose feels generated, generic, or templated into a reader-facing diagnosis. Inspect for:

- abstract claims with no actor, mechanism, evidence, constraint, or consequence;
- over-regular headings, paragraphs, lists, or rhetorical sequences unrelated to importance;
- empty transitions that label no real relation;
- repeated summaries that do not synthesize, decide, qualify, or advance;
- generic openings and closings that could belong to any document on the topic;
- equal emphasis on unequal points and reluctance to make a warranted selection;
- exhaustive-sounding lists that omit the actual decision or trade-off;
- uniform sentence cadence, confidence, distance, or paragraph shape despite changing functions;
- smooth but unsupported leaps between claims;
- generic praise, concern, balance, or significance without accountable judgment;
- pseudo-specific details that are decorative, unsupported, or irrelevant;
- formulaic reader engagement, rhetorical questions, asides, or informality not licensed by the genre;
- connective, synonym, adjective, or metaphor variation that substitutes for conceptual progression.

For every such finding, name the underlying failure: weak purpose, missing relation, insufficient support, poor prioritization, unstable stance, absent situated detail, reader mismatch, or mechanical structure. Preserve conventional phrasing and regularity when the genre, law, procedure, accessibility need, or institutional template requires them. Treat surface features as evidence for inspection, never as proof of origin.

### 4.9 Fidelity and format risks

- Compare every proposed treatment with the protected-content register.
- Flag any treatment that could broaden, narrow, strengthen, weaken, generalize, personalize, or reattribute a claim.
- Flag any treatment that could change a defined term, legal effect, obligation, exception, causal relation, uncertainty, calculation, citation relationship, or institutional position.
- Classify missing substantive input as `requires-answer`; do not fill it with plausible content.
- Preserve styles, heading levels, lists, numbering, tables, figures, captions, equations, notes, citations, cross-references, hyperlinks, fields, comments, and tracked-change state.
- Preserve section and page breaks, headers, footers, orientation, columns, accessibility structure, and navigation when they carry document function.
- Identify manual formatting, broken fields, orphaned captions, detached notes, stale tables of contents, and ambiguous visual hierarchy before revision.
- Record format risks separately from prose findings when they require different tools or verification.

## 5. Check internal consistency

Check only the document and every supplied annex. Build normalized registers for:

- claims, conclusions, recommendations, and evidentiary status;
- definitions, abbreviations, labels, and technical terms;
- names, entities, roles, responsibilities, and relationships;
- numbers, ranges, percentages, currencies, dates, durations, units, and calculations;
- obligations, permissions, prohibitions, conditions, exceptions, deadlines, and responsible actors;
- uncertainty, confidence, attribution, causal strength, population, jurisdiction, and time scope;
- citations, quotations, footnotes, endnotes, references, and source labels;
- tables, figures, captions, notes, totals, and narrative references to them;
- headings, numbered provisions, internal links, cross-references, appendices, and annexes.

Then:

- Compare every repeated item across body text, executive material, tables, figures, notes, and annexes.
- Verify arithmetic and internal derivations when the supplied values make the check possible.
- Verify that a claim summarized elsewhere retains its scope, attribution, qualification, and certainty.
- Verify that obligations and recommendations name the same actor, action, condition, and deadline wherever repeated.
- Verify that every cross-reference resolves to the intended target and that every cited annex or object exists.
- Compare the cross-reference's descriptive label with the target's actual contents. Record an issue when the label promises a topic, evidence type, period, population, calculation, or artifact that the target does not contain, even when the source already used that wording.
- Distinguish a contradiction from a legitimate change of period, population, unit, definition, scenario, or evidentiary status.
- Record unexplained discrepancies as `CON` issues with exact anchors for every conflicting instance.
- State the conflict without choosing which value or statement is factually correct unless the supplied material establishes the answer.
- Link each consistency issue to dependent prose, table, figure, or recommendation issues.

## 6. Assemble the diagnostic report

Write the persistent report in the document's language and the concise chat summary in the request's language unless instructed otherwise. Organize the report in this order:

1. **Diagnostic contract:** language, genre, readers, purpose, expected use, register, constraints, and material in scope.
2. **Coverage statement:** document and annex inventory, semantic unit map, blocked material, and completed coverage matrix.
3. **Document map:** reverse outline, section functions, protected-content register, terminology register, and major claim relationships.
4. **Executive synthesis:** the few global findings that most affect the reader or document purpose, plus successful mechanisms to preserve.
5. **Global and cross-unit findings:** architecture, progression, proportion, stance, consistency, and format risks.
6. **Unit findings:** concise summaries for every bounded unit, with links to issue IDs.
7. **Complete issue ledger:** all issue fields and every recurring-pattern occurrence.
8. **Internal-consistency results:** reconciled registers, contradictions, discrepancies, and unresolved annex relationships.
9. **Revision plan:** one coherent, dependency-ordered treatment plan mapped to issue IDs and protected elements.
10. **Meaning-sensitive decisions:** questions whose answers could change argument, legal effect, evidence, attribution, or institutional position.

Make the synthesis readable without reducing ledger completeness. Group findings by consequence and dependency, not by a vague naturalness score. Keep local examples minimal in the synthesis and exhaustive in the ledger.

## 7. Stop at the human gate

- Finish the diagnosis for the entire material in scope before editing any source text.
- Present the diagnostic report and one coherent revision plan.
- Ask the user to approve the plan as a whole, exclude named issue IDs, or answer meaning-sensitive questions.
- Keep every non-meaning-sensitive issue `pending` until the user acts.
- Mark meaning-sensitive issues `requires-answer` and gate them individually.
- Translate approval into immutable issue states and a frozen revision scope.
- Preserve excluded findings in the ledger; omit them from the revision plan.
- Reconcile any changed instruction with dependent issues before revision begins.
- Leave the original artifact untouched at this gate.

## 8. Apply the completion test

Complete diagnosis only when all of the following are true:

- Every supplied file and annex appears in the manifest.
- Every bounded unit has been inspected against every applicable dimension.
- Every coverage-matrix cell is resolved as `clear`, `issues recorded`, `not applicable`, or `blocked by missing context` with explanation where required.
- Every material local, cross-unit, and global issue has a stable ID and complete ledger fields.
- Every occurrence of every recurring pattern has an exact anchor.
- Every internal-consistency register has been reconciled across the document and annexes.
- Every unexplained contradiction or discrepancy is recorded without unsupported external resolution.
- Every fidelity and format risk is linked to the treatment that creates or mitigates it.
- The reverse outline and global synthesis reflect the assembled document, not a sample of sections.
- The revision plan covers every pending issue and respects dependencies and protected content.
- The report makes no provenance inference and uses no detector metric as evidence or objective.
- The human gate is explicit and no revision has started.
