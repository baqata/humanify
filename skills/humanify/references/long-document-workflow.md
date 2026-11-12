# Long-document orchestration

Use this workflow when the source is too large or interconnected for one reliable, uninterrupted pass. Scale the workflow to the document. Treat the named rounds as logical stages, not as fixed agents, fixed prompts, or fixed batch sizes.

## Contents

- Foundations: [Operating principles](#operating-principles), [roles](#roles-and-ownership), [review record](#resumable-review-record), and [unitization](#semantic-unitization)
- Diagnosis: [Map](#round-1-map), [Inspect](#round-2-inspect), [Reconcile](#round-3-reconcile), and [human gate](#human-gate)
- Execution: [Revise](#round-4-revise), [Integrate](#round-5-integrate), and [Verify](#round-6-verify)
- Completion: [coverage accounting](#coverage-accounting), [conflicts and concurrency](#conflicts-and-concurrency), and [continuation and stop conditions](#continuation-and-stop-conditions)

## Operating principles

- Preserve the source unchanged and work from an explicit copy or extraction.
- Cover the entire document and every supplied annex within scope.
- Scale each round independently according to length, hierarchy, density, and cross-unit dependence.
- Use no subagents for a short text when one agent can complete every round deeply and reliably.
- Use as many workers and integrators as needed for a long report; never equate one round with one worker.
- Keep the logical sequence: Map, Inspect, Reconcile, human gate, Revise, Integrate, Verify.
- Finish the full diagnosis before asking for revision approval.
- Resume across turns when the full workflow cannot fit in one interaction.
- Record progress in durable artifacts rather than relying on conversational memory.
- Treat every claim of complete review as a coverage claim that the review record must support.
- Prefer semantic boundaries over pages, token windows, or equal-sized chunks.
- Preserve facts, qualifications, citations, terminology, numbers, legal effects, and institutional constraints.
- Check internal consistency against the document and supplied annexes without introducing external evidence.

## Roles and ownership

Assign roles elastically. Let one agent hold several roles for a short document.

### Coordinator

- Own the review record, unit manifest, issue ledger, synthesis, approval record, and coverage account.
- Define assignments and refresh shared context before each round.
- Resolve overlaps and conflicts among worker findings.
- Keep the authoritative source copy read-only.
- Hold exclusive write authority over the authoritative revised file.
- Decide whether a unit requires another inspection or revision pass.
- Report actual coverage and unresolved blockers accurately.

### Workers

- Analyze or revise only the units assigned to them.
- Use the shared document context and adjacent-unit summaries.
- Return findings or proposed revisions as isolated artifacts keyed to stable unit IDs.
- Propose changes to shared registers; let the coordinator accept and merge them.
- Mark uncertainty and cross-unit dependencies explicitly.
- Avoid editing the authoritative revised file or another worker's contribution.

### Cross-cutting reviewers

- Review relationships that cannot be judged within one unit.
- Cover structure, progression, duplication, gaps, terminology, entities, claims, numbers, cross-references, and annex alignment as assigned.
- Anchor every finding to all affected unit IDs.
- Escalate meaning-sensitive conflicts to the coordinator.

### Integrator

- Let the coordinator serve as integrator or designate one integrator under coordinator control.
- Apply approved unit revisions serially to the authoritative revised copy.
- Preserve styles, anchors, numbering, references, tables, notes, and file structure.
- Record every applied, altered, deferred, or rejected revision.

## Resumable review record

Create a durable review record before distributing work. Keep these components current:

- `manifest`: identify source files, annexes, format, language, source revision, hashes or timestamps, and output targets.
- `units`: record stable unit IDs, hierarchy, source spans, titles, dependencies, assignees, and statuses.
- `document-map`: capture purpose, audience, genre, macrostructure, section functions, and reverse outline.
- `protected-content`: record facts, numbers, dates, units, quotations, citations, defined terms, legal language, and intentional constraints.
- `terms-entities`: normalize terminology, abbreviations, named entities, roles, and allowed variants.
- `claims`: map material claims, qualifications, evidence supplied in the document, and locations where each claim recurs.
- `cross-references`: map headings, tables, figures, notes, citations, internal links, and targets.
- `annexes`: map each annex's function, dependencies, referenced values, and links to the main text.
- `issue-ledger`: store local and global findings with stable issue IDs.
- `diagnostic-synthesis`: consolidate the whole-document diagnosis and revision plan.
- `approvals`: record the human decision for every issue or plan component.
- `revision-status`: track proposed, approved, revised, integrated, deferred, and rejected work by unit and issue.
- `verification`: store unit checks, global checks, format checks, discrepancies, and resolution status.
- `coverage`: account for every unit and required operation in every completed round.

Snapshot the review record whenever assignments, approvals, or the authoritative revision change. Reject stale contributions when their source hash or review-record snapshot no longer matches the manifest.

## Semantic unitization

Decompose the source through this hierarchy:

`document > part or chapter > section > subsection > paragraph cluster`

- Start from the document's own hierarchy and preserve its order.
- Treat front matter, executive summaries, appendices, annexes, bibliographies, and back matter as explicit units.
- Select the lowest heading-bounded unit that remains coherent and can be inspected deeply.
- Split an oversized subsection into paragraph clusters at genuine topic, claim, scene, or argumentative boundaries.
- Keep each paragraph intact.
- Keep a table with its title, notes, source line, and indispensable explanatory text.
- Keep a figure with its caption, legend, source, and indispensable explanatory text.
- Keep a quotation with its introduction, attribution, and immediate interpretation.
- Keep a footnote sequence with the passages and references it qualifies.
- Keep lists with their lead-in and any sentence that interprets the list.
- Keep a tightly connected argument, definition chain, example, or qualification in one unit.
- Avoid splitting solely to equalize length or token count.
- Use resource limits only to choose among valid semantic boundaries.
- Assign stable IDs that express hierarchy without depending on mutable page numbers.
- Record exact source anchors separately from stable IDs.
- Preserve parent, child, predecessor, successor, and cross-reference relationships.
- Re-unitize when a proposed boundary hides a dependency needed for sound judgment.

Build a review brief for every unit. Include:
- the unit text and stable ID;
- its parent purpose and section function;
- the document purpose, audience, genre, register, and constraints;
- the current protected-content and terminology registers relevant to the unit;
- relevant claims, entities, cross-references, tables, figures, and annex links;
- concise summaries of the preceding and following units;
- summaries of any nonadjacent units on which the unit depends;
- the current global issues and invariants that constrain local judgment.

## Round 1: Map

Build shared global context before judging prose locally.

1. Inventory every source file and supplied annex.
2. Verify that the source state is stable enough to analyze.
3. Identify the document's primary language, genre, audience, purpose, and governing constraints.
4. Reconstruct the hierarchy and reverse outline.
5. Describe the function of every part, chapter, section, and subsection.
6. Create semantic units and stable IDs.
7. Register protected content.
8. Map terms, entities, claims, qualifications, numbers, dates, units, cross-references, and annex dependencies.
9. Identify preliminary structural tensions and potential contradictions without closing them prematurely.
10. Generate unit briefs and adjacent-unit summaries.
11. Record uncertainties that local inspection must resolve.
Complete Map only when every in-scope source element belongs to a unit, every unit has a review brief, and every known protected or cross-linked element has a register entry.

## Round 2: Inspect

Diagnose every unit against both its local function and the shared global map.

1. Assign all units explicitly; leave no implicit remainder.
2. Match workload to semantic complexity rather than raw length alone.
3. Inspect purpose, development, information flow, stance, cohesion, rhythm, diction, specificity, repetition, and genre fit.
4. Check each unit against protected content and internal claims.
5. Distinguish local defects from symptoms of a global structural issue.
6. Enumerate every affected location for each material issue.
7. Reuse one explanation for a recurring pattern while preserving a separate occurrence entry for every location.
8. Record dependencies that require comparison with other units.
9. Propose treatments without rewriting before the human gate.
10. Return a unit-completion statement and coverage record.
Use this issue schema:

- stable issue ID;
- local, cross-unit, or global scope;
- affected unit IDs and exact anchors;
- short relevant excerpt or structural evidence;
- diagnosis and reader consequence;
- proposed treatment;
- protected elements and meaning risks;
- related claims, terms, cross-references, or annexes;
- confidence and unresolved dependency;
- approval and revision status.
Complete Inspect only when every unit has a reviewed status, every material finding is registered, and every worker's claimed coverage reconciles with the unit manifest.

## Round 3: Reconcile

Aggregate local findings and assess the document again as a whole.

1. Merge worker ledgers into the coordinator-owned issue ledger.
2. Deduplicate explanations while retaining every occurrence and affected unit.
3. Compare the reverse outline with the document's purpose and reader needs.
4. Check progression, proportion, section order, duplication, gaps, pacing, and transitions across boundaries.
5. Check definitions, terminology, entities, responsibilities, recommendations, qualifications, and levels of certainty across units.
6. Reconcile numbers, dates, units, tables, figures, citations, cross-references, and annex references internally.
7. Identify contradictions and unexplained discrepancies without deciding external truth.
8. Reopen local findings when global evidence changes their interpretation.
9. Separate safe editorial treatments from meaning-sensitive decisions.
10. Produce one coherent diagnostic synthesis and ordered revision plan.
11. Update full-round coverage and list any unresolved source-access or interpretation blocker.
Complete Reconcile only when every local ledger has been integrated, every cross-cutting review has a recorded result, and the synthesis accounts for every open issue.

## Human gate

Pause after the complete diagnosis and before any source revision.

- Present the synthesis, revision plan, and accessible issue ledger.
- Let the user approve the plan as a whole, reject it, or exclude named issue IDs.
- Isolate decisions that could change meaning, argument, legal effect, evidence, or institutional position.
- Record approvals and exclusions exactly.
- Ask again only when later evidence exposes a materially different decision.
- Preserve unapproved issues as diagnostic findings without implementing them.
- Resume revision only when the approval record defines the authorized scope.

## Round 4: Revise

Reuse the diagnostic units and approved plan.

1. Refresh each unit brief with approved issue IDs and resolved global decisions.
2. Assign isolated units only when their approved changes can be prepared without editing the authoritative revised file.
3. Revise every approved occurrence, not merely the representative example.
4. Preserve protected content and the unit's role in the whole document.
5. Carry necessary context across unit boundaries without duplicating content.
6. Return a proposed unit revision, issue-by-issue change record, and fidelity check.
7. Flag any newly discovered contradiction or meaning-sensitive choice instead of improvising a resolution.
8. Reinspect the revised unit for new repetition, broken transitions, or changed emphasis.
Complete Revise only when every approved issue is revised, explicitly deferred for a recorded reason, or returned to the human gate because its meaning risk changed.

## Round 5: Integrate

Assemble revisions under exclusive control.

1. Create the authoritative revised copy without overwriting the source.
2. Apply unit revisions serially in document order or another dependency-safe order.
3. Refresh anchors after every structural edit.
4. Resolve overlaps before applying either competing change.
5. Preserve formatting, styles, numbering, links, tables, figures, notes, citations, and tracked-change semantics appropriate to the format.
6. Update the change record and issue status after each applied revision.
7. Reread every modified boundary with its preceding and following unit.
8. Reject or rework a unit revision that conflicts with the approved global plan or a later accepted edit.
Complete Integrate only when one authoritative revised artifact contains every accepted revision and the ledger maps each approved issue to its final disposition.

## Round 6: Verify

Verify both units and the assembled document.

1. Compare protected content against the source.
2. Recheck every revised unit against its approved issues and fidelity constraints.
3. Rerun the global structure and reader-progression review.
4. Rerun internal-consistency checks across text, tables, figures, notes, citations, cross-references, and annexes.
5. Confirm that edits did not create new contradictions, repetition, gaps, register drift, or broken transitions.
6. Validate the output format and render visually when the format requires it.
7. Confirm that the original remains unchanged.
8. Resolve every verification discrepancy or record it as an explicit limitation or blocker.
9. Update coverage to reflect verified, not merely attempted, work.
Complete Verify only when every unit, approved issue, protected-content class, cross-reference class, annex dependency, and format check has a recorded result.

## Coverage accounting

Maintain counts and status lists for:

- total, mapped, inspected, reconciled, approved, revised, integrated, and verified units;
- total issues by status and scope;
- all registered protected-content items checked after revision;
- all claims, terms, entities, numbers, dates, cross-references, and annex links checked;
- all tables, figures, quotations, footnotes, lists, and other preserved structures inspected;
- all contributions accepted, replaced, rejected, or awaiting reconciliation;
- all verification findings resolved, accepted, or blocked.

Require both a count and the corresponding stable-ID list. Treat a missing unit, unassigned span, unexplained count mismatch, or stale review brief as incomplete coverage. Never infer completion from the absence of reported findings.

## Conflicts and concurrency

- Keep source files read-only for all workers.
- Grant write access to the authoritative revised file to one coordinator or integrator at a time.
- Let workers write only separate unit artifacts and ledgers.
- Prevent simultaneous edits to the shared issue ledger; merge proposals through the coordinator.
- Key all output to the source hash, review-record snapshot, unit ID, and issue ID.
- Reject results produced from stale source states or reconcile them explicitly against the current state.
- Resolve competing treatments by applying this order: user approvals, protected meaning, internal consistency, document purpose, section function, genre and reader fit, then local polish.
- Prefer the treatment that preserves more supported meaning when two revisions remain equally plausible.
- Preserve both diagnoses when evidence does not support choosing one; escalate the decision at the human gate.
- Merge duplicate issues under one stable ID while retaining every anchor and occurrence.
- Reinspect all affected units when a global decision changes terminology, structure, or claim framing.
- Serialize overlapping revisions even when nonoverlapping units are prepared concurrently.
- Keep completed contributions unchanged; replace them with corrected copies when necessary.

## Continuation and stop conditions

- Persist the review record before ending a turn or redistributing work.
- Report completed rounds, exact coverage, active assignments, unresolved blockers, and the next resumable action.
- Resume from the recorded manifest and snapshots rather than reconstructing state selectively.
- Revalidate source identity before resuming.
- Continue across turns until every in-scope unit and global relationship receives the required round.
- Avoid sampling as a substitute for full review.
- Label an intentionally sampled audit as partial and obtain explicit user authorization before changing scope.
- Never claim whole-document coverage when any required unit or cross-cutting check lacks a completed record.
- Stop at the human gate after a complete diagnosis.
- Stop for a new human decision when revision exposes a material meaning, legal, evidentiary, or institutional conflict outside the approved plan.
- Stop as blocked when source material, annexes, permissions, or an indispensable decision prevents safe progress; name the exact missing item.
- Finish only when coverage is complete, the authoritative artifact passes verification, all approved issues have final dispositions, and remaining limitations are stated accurately.
