---
name: humanify
description: Diagnose, draft, and revise prose through an evidence-based, human-gated workflow that preserves meaning, technical precision, genre, formatting, and internal consistency. Use only when the user explicitly invokes /humanify for pasted text or a single-language en-US or es-CO .txt, .md, .docx, or diagnostic PDF, including long documents and supplied PDF or spreadsheet annexes. Do not invoke implicitly for ordinary writing, superficial paraphrasing, or detector evasion.
disable-model-invocation: true
---

# Humanify

Improve prose by making an accountable writer's purpose, evidence, judgment, and relationship to the reader legible. Treat naturalness as successful writing within a real genre and situation, not as informality, imperfection, statistical unpredictability, or resemblance to a detector's human class.

## Hold the contract

Apply this priority order unless an explicit higher-order constraint requires otherwise:

1. Preserve factual and semantic fidelity.
2. Preserve the validity, scope, and traceability of reasoning and evidence.
3. Honor genre, language, institutional, legal, technical, and format constraints.
4. Help the intended reader find, understand, feel, decide, or act as the genre requires.
5. Preserve coherent source tendencies while using a strong genre-appropriate default; do not imitate a personal voice.
6. Improve coherence, emphasis, cadence, idiom, and polish.

Never trade an earlier priority for a later one silently. Preserve names, numbers, dates, units, definitions, quotations, citations, attributed speakers, modality, negation, conditions, exceptions, causal force, uncertainty, obligations, and jurisdiction-specific terms unless the approved plan explicitly changes them.

Keep reader, author, institutional speaker, subject-matter owner, approver, decision-maker, and action owner distinct. An intended audience does not acquire authority, responsibility, or an obligation merely because the document asks that audience to read or consider something. Do not infer a decision actor or change `may`, `should`, `is due`, or an undecided state to `must` without supplied and approved support.

Do not:

- optimize for GPTZero or any other detector;
- promise that prose is human-written or undetectable;
- add typos, fragments, slang, contractions, anecdotes, sensory detail, emotions, beliefs, sources, or personal experience merely to appear human;
- maximize perplexity, burstiness, lexical variety, sentence-length variance, readability scores, or any other proxy;
- apply universal bans to passive voice, nominalization, transitions, hedges, repeated terms, punctuation marks, or sentence lengths;
- invent facts, evidence, examples, citations, provenance, prior drafts, or authorial commitments;
- turn technical, institutional, academic, or juridical prose into generic conversation;
- use external evidence to correct the document unless the user separately requests factual research.

Read [editorial-principles.md](references/editorial-principles.md) before diagnosing or composing prose. Use its evidence boundaries when a familiar style maxim conflicts with the document's purpose.

## Route the request

Do not present diagnose, revise, and draft as a menu. Infer the entry path from the supplied material.

### Existing text or document

Run the full sequence:

`inspect -> map -> diagnose -> reconcile -> report -> human gate -> revise -> integrate -> verify -> deliver`

Complete the diagnosis and revision plan before changing the source or creating a purported final revision. Stop at the human gate and wait for approval.

### New document

Run the full sequence:

`establish contract -> map claims and warrants -> propose structure -> human gate -> draft -> self-diagnose -> revise -> verify -> deliver`

Before the gate, state the inferred genre, audience, purpose, intended reader outcome, language, section functions, constraints, factual boundary, and proposed structure. Also map every planned material conclusion, recommendation, instruction, or decision to its supplied evidence and necessary warrant.

Approval authorizes a position or drafting choice; it does not supply a missing factual premise. When the supplied material does not support a planned conclusion:

1. name the missing premise or decision criterion;
2. do not describe the conclusion as evidence-based or as an editorial judgment that follows from the facts;
3. ask for the missing support, propose a neutral decision frame, or ask whether the user wants the position presented transparently as an institutional or authorial choice despite the evidentiary gap; and
4. preserve the gap in the approved contract and final prose unless supporting material is supplied.

After approval, draft and complete the diagnostic and revision passes without another routine gate. Stop again only when a newly discovered decision could materially alter meaning, evidence, legal effect, institutional position, or authorial commitment. A post-draft audit may not silently repair an unsupported recommendation by deleting its explicit rationale while leaving the unsupported conclusion in place.

## Select references before analysis

Load only the modules required for the request:

- Read [diagnostic-rubric.md](references/diagnostic-rubric.md) for every diagnosis, revision, post-draft audit, or pre-draft reasoning audit for a new document.
- Read [english-us.md](references/english-us.md) for an English document and normalize general prose to `en-US`.
- Read [spanish-colombia.md](references/spanish-colombia.md) for a Spanish document and normalize general prose to `es-CO`.
- Read [file-handling.md](references/file-handling.md) when the input or output is a file.
- Read [long-document-workflow.md](references/long-document-workflow.md) when the material has multiple substantive units, annexes, cross-references, distributed claims, or cannot be deeply audited as one coherent unit.
- Read [evaluation.md](references/evaluation.md) before final verification.

Assume one primary document language. Preserve foreign quotations, titles, citations, official names, branded forms, and jurisdiction-specific terms as protected spans. If the document contains substantial English and Spanish prose, stop and process them as separate source documents.

Treat a document as one macro-genre with section-level functions. Allow an executive summary, methodology, analysis, recommendations, legal qualifications, and annexes to use different local registers while preserving one coherent identity, terminology system, and line of thought.

## Inspect without rewriting

For existing material:

1. Resolve the exact source and all explicitly supplied annexes. Do not sweep unrelated neighboring files into scope.
2. Preserve the source untouched and establish the output and working locations.
3. Identify the primary language and route to `en-US` or `es-CO`.
4. Infer the macro-genre, section functions, intended audience, reader knowledge, purpose, desired reader action or experience, stakes, and governing house constraints.
5. Inventory headings, paragraphs, tables, figures, notes, citations, cross-references, annexes, and other structural elements.
6. Establish a protected-content register before proposing changes.
7. State material inferences in the diagnosis. Ask only when an ambiguity would change the analysis or authorization.

For file work, follow [file-handling.md](references/file-handling.md) and delegate format mechanics to the maintained format skill:

- invoke the `docx` skill for every `.docx` inspection, creation, or modification;
- invoke the `pdf` skill for every PDF inspection or diagnostic source;
- invoke the `xlsx` skill when an actual `.xlsx`, `.xls`, `.csv`, or `.tsv` file is supplied as evidence, an annex, or an explicitly approved output.

A table inside Word remains part of the Word document and does not trigger the spreadsheet skill. Do not select or document low-level libraries in `humanify`; the active format skill owns its file operations and render-and-verify contract.

## Diagnose at local and global scales

Follow [diagnostic-rubric.md](references/diagnostic-rubric.md). Examine, as applicable:

- communicative purpose, audience, genre, and register;
- whole-document argument, narrative, procedure, hierarchy, pace, and proportion;
- section function and relationships among sections;
- paragraph focus, development, information progression, and transitions;
- sentence reference, syntax, dependency load, emphasis, rhythm, and punctuation;
- diction, idiom, abstraction, specificity, repetition, and terminology;
- stance, agency, attribution, evidence, uncertainty, obligation, and relationship to the reader;
- templated structures, empty symmetry, generic abstraction, empty transitions, and uniform calibration that make prose feel unaccountable or generated;
- semantic, technical, legal, citation, internal-consistency, and format risks.

Translate reactions such as "this feels AI-written" into concrete reader or document problems. Never diagnose provenance from prose and never report an AI probability.

Analyze every bounded unit exhaustively. Allow recurring occurrences to share one rationale and treatment, but enumerate every affected location with a stable anchor. Keep local issues connected to the global document map so that an apparently redundant passage is not removed when it performs a necessary function elsewhere.

Check only internal consistency by default. Compare the document and supplied annexes across definitions, claims, dates, numbers, units, entities, actors, responsibilities, recommendations, uncertainty, citations, tables, figures, and cross-references. For every descriptive cross-reference, verify both that the target exists and that the description names only content the target actually contains; inherited source wording is not exempt. Flag contradictions, overclaims, or unexplained differences without deciding which conflicting claim is externally true.

## Scale orchestration to the document

For a short, coherent text, perform the workflow locally. Do not spawn agents merely to satisfy a diagram.

For a document requiring decomposition, follow [long-document-workflow.md](references/long-document-workflow.md). Treat `Map`, `Inspect`, and `Reconcile` as logical rounds, not fixed worker counts. Let each round use as many bounded workers and integrators as needed. After approval, scale `Revise`, `Integrate`, and `Verify` independently.

Use semantic units in this hierarchy:

`document -> part or chapter -> section -> subsection -> paragraph cluster`

Do not split paragraphs, tables, quotations, footnote sequences, or tightly connected arguments. Give each worker the shared document map, protected-content register, terminology and claim context, and adjacent-unit summaries. Let workers write isolated findings or proposed unit revisions. Keep one coordinator responsible for the issue ledger and the authoritative revised copy. Never permit concurrent edits to that copy.

Persist a resumable review record for large jobs. Track every unit from inventory through diagnosis, approval, revision, and verification. Continue across turns rather than sampling silently, dropping annexes, or claiming full review without coverage evidence.

## Produce the diagnosis and stop

Write the persistent diagnostic report and issue ledger in the document's language. Write the concise chat summary in the user's request language unless instructed otherwise.

Include:

1. the inferred document contract and normalization route;
2. the scope and coverage inventory;
3. protected content and preservation risks;
4. global findings;
5. section- and unit-level findings;
6. an exhaustive issue ledger with stable IDs and exact anchors;
7. internal contradictions or unresolved cross-document differences;
8. one coherent revision plan, ordered by dependency and consequence;
9. meaning-sensitive decisions requiring explicit resolution;
10. the intended output artifacts and format-preservation limits.

Do not edit the source or create a final revised artifact in this phase. Ask the user to approve the whole plan, reject it, amend it, or exclude named issue IDs. If approval leaves a meaning-sensitive issue unresolved, preserve the original passage.

Classify whether each unresolved issue is compatible with the intended reader outcome. Preserving source wording does not resolve a gap. If an unresolved issue prevents the reader from acting safely, determining legal or technical effect, following the procedure, or understanding a material conclusion, retain its `blocking` status even when the user authorizes no change.

## Revise the approved plan

Apply only approved changes and their direct consequences. Work from global structure toward local wording:

1. resolve approved document-level order, hierarchy, omissions, and duplication;
2. align section purpose, proportion, and progression;
3. repair paragraph focus, evidence placement, inference paths, and transitions;
4. repair reference, syntax, information flow, agency, stance, idiom, and cadence;
5. normalize `en-US` or `es-CO` mechanics after the substantive language is stable;
6. reassemble through one coordinator and one authoritative copy;
7. update the issue ledger and change record as each approved item is applied.

Prefer no edit over taste-driven churn. Preserve productive ambiguity, suspense, inference, repetition, abstraction, formality, or complexity when the genre and reader benefit from it. Mark a new example as hypothetical unless it is grounded in supplied material.

An approved instruction to preserve an unresolved passage authorizes non-invention; it does not authorize a completion claim. If a blocking gap remains after revision, create a clearly named provisional artifact and an unresolved-issues record. Do not label it final, publication-ready, verified without limitation, or complete. Do not insert editorial caveats into the document itself unless the genre and approval authorize them.

## Verify before delivery

Follow [evaluation.md](references/evaluation.md). Verify at least:

- every approved issue is applied or explicitly reported as unresolved;
- every source unit and supplied annex is accounted for;
- protected facts and semantic relationships remain intact;
- claims, definitions, terms, numbers, citations, cross-references, and uncertainty remain internally consistent;
- the whole document still supports its intended reader outcome and genre;
- the selected language module passes its native checks;
- no fake human texture or detector-oriented manipulation has been introduced;
- reader, author, approver, decision-maker, and action-owner roles retain their supplied actors and modalities;
- the source remains untouched and the required revised, redline, clean, diagnostic, and change-record artifacts exist;
- file structure and rendering remain sound.

Do not claim completion when a unit, annex, requested artifact, applicable verification, or reader-blocking issue remains unresolved. A limitation that materially affects use must appear in the delivery status and unresolved-issues record; a provisional artifact may still be useful, but it does not pass the final completion gate.

## Deliver

Lead with the completed outcome only when every completion gate passes. Link the revised artifact and the diagnostic report. Include the clean and redline versions when required by the file route. Summarize material structural or meaning-sensitive changes, unresolved items, and verification performed. If a blocking issue remains, lead with the provisional status, link the provisional artifact and unresolved-issues record, and state what must be supplied or decided before finalization. Do not include detector scores, generic writing advice, internal orchestration chatter, or a claim that the result is human-authored.
