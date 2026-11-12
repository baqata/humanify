# Final verification

## Contents

[Purpose](#purpose) · [Evidence](#required-evaluation-evidence) · [Process gate](#process-gate) · [Acceptance gates](#acceptance-gates) · [Failure records](#record-verification-failures)

## Purpose

- Evaluate accountable writing quality, not inferred authorship.
- Treat naturalness as fitness for the document's purpose, reader, genre, language, and evidentiary boundary.
- Evaluate the diagnosis, issue ledger, approved revision, and final artifact as separate products.
- Compare the revision with the source and every supplied annex; do not judge the revision in isolation.
- Exclude detector scores, perplexity, burstiness, stylometric similarity, and lists of alleged “AI words” from every verification and acceptance decision.
- Prefer observable reader and document outcomes over generic style ratings.

## Required evaluation evidence

- Collect the original artifact, supplied annexes, audience and genre contract, protected-content register, diagnostic report, issue ledger, approval record, revised artifact, and verification record.
- Preserve stable unit and issue identifiers throughout the evaluation.
- Record explicit user constraints and any conservative assumptions made during intake.
- Distinguish supplied facts, source claims, author claims, editor inferences, and unresolved conflicts.
- Render `.docx` outputs before accepting them; inspect both their content and visual layout.
- Use the `pdf` skill for PDF sources and the `xlsx` skill for actual workbook, CSV, or TSV evidence; preserve their format-specific evidence and visual-review records.
- Inspect Markdown as source and as rendered content when its target renderer matters.
- Mark each gate `PASS`, `FAIL`, or `N/A`; justify every `FAIL` with anchored evidence.
- Accept the result only when every applicable gate passes; never average a hard failure into an overall passing score.

## Process gate

- Require a complete diagnosis and revision plan before any revision of supplied text.
- Require explicit approval after diagnosis and before revision.
- Require a purpose, audience, genre, constraint, factual-boundary, and structure proposal before drafting new text.
- Require a pre-draft map from every planned material conclusion, recommendation, instruction, and decision to its supplied evidence and necessary warrant.
- Fail the process if the plan presents an unsupported conclusion as an editorial inference from the facts or treats human approval as a substitute for missing evidence.
- Require approval of that proposal before drafting.
- Apply only approved issue identifiers and separately approved meaning-sensitive decisions.
- Fail the workflow if editing begins before the applicable gate, if approval is assumed, or if unapproved material changes appear.
- Treat approval to preserve an unresolved passage as authorization not to invent, not as evidence that the document is complete.

## Acceptance gates

### 1. Fidelity

- Lock names, entities, dates, quantities, units, ranges, percentages, definitions, quotations, citations, attributions, commands, interface labels, legal modalities, conditions, exceptions, causal language, and uncertainty markers.
- Compare each source proposition with its revised counterpart, including negation, scope, temporality, jurisdiction, population, actor, and degree of certainty.
- Preserve the distinction between observation, interpretation, recommendation, allegation, and established fact.
- Preserve technical and legally defined terms unless an approved change explicitly replaces them.
- Keep intended reader, author, institutional speaker, approver, decision-maker, and action owner distinct; fail any authority, responsibility, or modality inferred from audience alone.
- Trace every new example or clarification to supplied material; label a permitted invented example as hypothetical.
- Fail on any unauthorized addition, deletion, strengthening, weakening, causal upgrade, changed attribution, altered obligation, numeric drift, citation drift, or invented experience.

### 2. Reasoning

- Reconstruct the document's claim, support, qualification, concession, condition, and consequence relations.
- Check whether each conclusion follows from material available inside the supplied document set.
- Check whether revisions expose missing premises rather than silently inventing them.
- Preserve evidentiary limits, alternative interpretations, and unresolved ambiguities.
- Verify that approval authorized expression of a position but was not treated as new factual support for it.
- Separate an author's position from a cited source's position and from editorial inference.
- Flag internally unsupported reasoning; do not use external evidence to prove or repair it unless separately authorized.
- Fail when the revision hides a logical gap, introduces a new inference as fact, collapses correlation into causation, or makes the argument more certain than its support.

### 3. Genre

- Identify one macro-genre and the function of each section before judging style.
- Test technical documentation for accurate conditions, exact terminology, warnings, commands, and task completion.
- Test institutional prose for appropriate authority, neutrality, accountability, accessibility, and traceability.
- Test legal prose for stable defined terms, explicit scope, obligations, permissions, exceptions, and legal effect.
- Test academic prose for reproducible distinctions among method, result, interpretation, limitation, and conclusion.
- Test literary and poetic prose for point of view, sound, image, implication, pace, purposeful ambiguity, and foregrounding.
- Test informal prose for relationship, intention, channel, tact, and credible conversational register.
- Preserve section-specific registers without fragmenting the document's institutional or authorial identity.
- Fail when a generic template, conversational tone, plain-language rule, or expository clarity rule overrides the genre's actual work.

### 4. Audience

- State who must read, who must act, what they already know, what they need to learn, and what misreading would cost.
- Test whether the intended reader can find, understand, and use the necessary information.
- Calibrate definitions, inferential bridges, examples, and redundancy to the reader's knowledge and stakes.
- Preserve productive inference, suspense, or ambiguity when the genre and audience require it.
- Avoid unexplained specialist terms for non-specialists and unnecessary explanations for expert readers.
- Fail when the revision addresses a generic reader, changes the relationship with the reader, or obscures the requested action or understanding.
- Fail a purported final artifact when an unresolved gap still prevents the intended reader from acting safely or understanding a material rule, route, recommendation, or conclusion.

### 5. Global and section structure

- Compare the reverse outline before and after revision.
- Verify that document order follows the argument, procedure, chronology, decision path, or aesthetic design.
- Verify that each section has a distinct function and an appropriate proportion.
- Detect duplicated work, buried premises, unsupported pivots, missing bridges, gaps, and conclusions placed before their warrant unless the genre calls for that order.
- Verify that headings express the real hierarchy instead of mechanically dividing equal-sized blocks.
- Reconcile local improvements with the whole-document progression.
- Fail when an individually fluent section weakens global logic, repeats another section's function, or contradicts the document's macro-purpose.

### 6. Local prose

- Assign each paragraph a recoverable function and relation to its neighbors.
- Resolve unstable references, ambiguous actors, false transitions, needless abstraction, and unnecessary processing load.
- Preserve meaningful repetition and stable terminology; reject synonym cycling performed only for variety.
- Shape cadence, sentence length, subordination, emphasis, and paragraph movement according to communicative function.
- Keep real logical relations visible without adding a transition to every paragraph.
- Retain marked fragments, asymmetry, repetition, or abruptness only when they perform a genre-appropriate rhetorical job.
- Reject universal targets for sentence length, paragraph length, lexical diversity, active voice, or variation.
- Fail when prose remains formulaic, becomes choppy, obscures agency, flattens emphasis, or gains polish without improving a specified reader or document need.

### 7. Language realization

- Evaluate English and Spanish directly in their own language; never translate a language-specific judgment or micro-rule from one into the other.
- Make English judgments natively in `en-US`.
- Make Spanish judgments natively in `es-CO`.
- Apply shared functional principles separately in each language.
- For English, verify idiom, reference, information flow, modality, punctuation, agreement, and `en-US` spelling without enforcing a rigid old-to-new template.
- For Spanish, verify topic and focus, marked order, tacit and overt subjects, clitics, agreement, subordination, and referent continuity.
- For Spanish, distinguish active voice, the `ser` passive, passive-reflexive `se`, and impersonal `se`; preserve the intended actor and responsibility.
- For Spanish, verify connector meaning and scope, opening question and exclamation marks, commas, greeting punctuation, quotation conventions, capitalization, accents, and treatment of foreign terms.
- For Spanish, keep `es-CO` treatment, verb forms, regional vocabulary, domain register, and gender or inclusion policy coherent without manufacturing Colombian slang.
- Preserve foreign quotations, official names, citations, jurisdiction-specific expressions, and branded spellings in either language.
- Fail English leakage into Spanish, Spanish leakage into English, locale drift, literal translation, inconsistent treatment, ungrammatical `se`, or language-specific punctuation errors.

### 8. Internal consistency

- Build and compare registers for definitions, terms, entities, claims, dates, numbers, units, responsibilities, recommendations, uncertainty, citations, tables, figures, cross-references, and annex references.
- Check every supplied annex against the main document and against other annexes.
- For every descriptive cross-reference, confirm that its target exists and that the description promises no topic, evidence type, period, population, calculation, or artifact absent from the target. Fail inherited overclaims as well as newly introduced ones.
- Enumerate each contradiction or unexplained discrepancy with exact locations.
- Preserve a conflict as unresolved when the supplied material does not establish which claim is correct.
- Check that summaries, executive sections, conclusions, tables, and captions agree with the detailed body.
- Fail when a contradiction is missed, silently harmonized, or resolved without internal support.

### 9. Format and artifact integrity

- Leave the original artifact untouched and verify that revision occurs in a new copy.
- Verify that `.docx`, PDF, and spreadsheet mechanics were delegated to the `docx`, `pdf`, and `xlsx` skills, respectively.
- For Markdown, preserve valid heading hierarchy, links, citations, tables, lists, code blocks, footnotes, anchors, and intentional raw markup.
- For `.docx`, preserve styles, sections, tables, figures, captions, notes, comments, citations, cross-references, headers, footers, numbering, and page behavior as far as technically possible.
- Require native tracked changes when the active document tooling can emit them reliably. Otherwise require an honest, usable visual or comparison redline that is never labeled as native tracking. Require a clean copy when the approved workflow calls for one.
- Render every revised Word file and inspect clipping, overflow, blank pages, broken tables, orphaned headings, misplaced notes, and pagination damage.
- For spreadsheet evidence, preserve formulas, numeric and date types, formats, ranges, comments, charts, and workbook structure; inspect the relevant values and formulas and visually render every relevant sheet or range.
- Fail on source overwrite, lost content, corrupt files, hidden formatting damage, unusable change tracking, or a format change the user did not authorize.

### 10. Coverage

- Define semantic units by headings and genuine topic boundaries, never by arbitrary page or token cuts alone.
- Verify exhaustive local review of every unit and global review across all units.
- Require an exact anchor for every proposed local change.
- Allow repeated occurrences to share one explanation, but require the issue ledger to enumerate every affected location.
- Reconcile terminology, repetition, numbers, claims, structure, and annex relations across unit boundaries.
- Verify that every approved issue identifier has a disposition and that every excluded identifier remains unapplied.
- Require unresolved blocking issues to remain visibly blocking in status records and to produce a provisional, not final, artifact.
- For long documents, verify resumable state, stable identifiers, completed assignments, and final reconciliation.
- Ignore agent count; verify completion of the logical map, inspect, and reconcile rounds with as many workers as the artifact required.
- Fail on silent sampling, missing units, unanchored findings, unreviewed annexes, or any claim of complete coverage without evidence.
- Fail a completion claim when preserved source wording leaves a reader-blocking issue unresolved, even if the limitation appears in a separate change record.

### 11. Absence of fake human quirks

- Search the revision for invented anecdotes, sensory details, feelings, opinions, quotations, citations, observations, measurements, authority, biography, or lived experience.
- Search for inserted typos, comma splices, false starts, random fragments, arbitrary slang, forced idioms, gratuitous contractions, or manufactured regionalisms.
- Search for mechanical sentence-length oscillation, synonym churn, decorative specificity, forced rhetorical questions, and indiscriminate removal or insertion of transitions, hedges, passive voice, or punctuation.
- Preserve authentic irregularity when the source and genre justify it; do not mistake polish for artificiality.
- Fail on any fabricated human signal, fake provenance trace, invented prior draft, or detector-oriented manipulation.

## Record verification failures

- Record a critical failure for invented facts or experience, changed legal or technical meaning, lost citations or numbers, source overwrite, silent conflict resolution, missing human gate, format corruption, or false complete-coverage claims.
- Record a major failure for genre or audience mismatch, global structural damage, a missed material issue, systemic language interference, inconsistent terminology, or repeated local-prose defects.
- Record a minor failure for an isolated, non-consequential grammar, punctuation, cadence, or formatting defect.
- Anchor every failure to a stable unit, issue identifier, page or heading, paragraph, table cell, note, or exact excerpt.
- Preserve the smallest source and output excerpts that demonstrate the failure.
- Distinguish missed findings, incorrect findings, harmful edits, unauthorized edits, gate violations, coverage gaps, and artifact damage.
- Treat an ungrounded evaluator preference as insufficient evidence; require a reader, genre, fidelity, or format consequence.
