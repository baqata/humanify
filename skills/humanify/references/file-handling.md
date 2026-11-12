# File handling

Use these rules for pasted text, `.txt`, `.md`, `.docx`, PDF sources, and spreadsheet files supplied as annexes or evidence.
Keep the source immutable throughout diagnosis, revision, and verification.

`humanify` owns the editorial contract, gates, issue ledger, and fidelity checks. The maintained format skills own file parsing, authoring, round-tripping, rendering, and format-specific verification. Do not duplicate or override their format instructions here.

## Contents

[Boundary](#establish-the-job-boundary) · [Originals](#protect-originals-and-working-state) · [Authoritative copy](#maintain-one-authoritative-copy) · [Pasted text](#handle-pasted-text) · [Plain text](#handle-plain-text) · [Markdown](#handle-markdown) · [Word](#handle-word-documents) · [PDF](#handle-pdfs) · [Spreadsheets](#handle-spreadsheet-evidence-and-annexes) · [Annexes](#scope-annexes) · [Outputs](#name-and-deliver-outputs)

## Establish the job boundary

1. Resolve every supplied source and annex before analysis.
2. Record each file's path, format, size, and role in the review-record manifest.
3. Assign stable identifiers to the main document, annexes, and analysis units.
4. Mark each annex as context-only, consistency evidence, or approved revision scope.
5. Treat an unspecified annex as read-only consistency evidence.
6. Preserve quotations, citations, defined terms, numbers, and other protected spans across format conversion.
7. Detect unsupported, encrypted, corrupted, or partially readable files before promising coverage.
8. State any inaccessible content and exclude it explicitly from completion claims.

## Protect originals and working state

1. Read the original in place or copy it into the private review record.
2. Never save, export, rename, or move content over the original path.
3. Create all intermediate extracts, renders, ledgers, and unit drafts under a job-specific `work/` directory.
4. Keep temporary artifacts out of the user-facing deliverable directory.
5. Place final artifacts in the user's requested destination.
6. Otherwise place final artifacts in a clearly named sibling directory next to the source.
7. Add a numeric suffix when a proposed output path already exists.
8. Retain the source extension for revised editable documents.
9. Record the source-to-output relationship in the change record.
10. Remove internal prompts, review notes, temporary extracts, and verification logs from final deliverables.

## Maintain one authoritative copy

1. Designate one coordinator as the sole owner of the authoritative revised copy.
2. Give workers immutable source units, shared invariants, and stable unit identifiers.
3. Require workers to return findings or isolated proposed revisions rather than editing the authoritative file.
4. Apply approved unit revisions serially through the coordinator.
5. Reject stale proposed revisions when their source text no longer matches the authoritative copy.
6. Reassemble the full document before global verification.
7. Compare the final artifact with the protected-content register and approved issue ledger.

## Handle pasted text

1. Preserve the supplied text verbatim in the review record before annotating it.
2. Record whether the text represents a complete document, an excerpt, or an isolated passage.
3. Limit global claims when surrounding sections or annexes are absent.
4. Assign paragraph or line anchors that remain stable through diagnosis.
5. Present the revised text in chat only when its length remains usable there.
6. Save longer revised text as `.md` or `.txt` when the user requests a file.
7. Label any normalized formatting that could not be inferred from the pasted source.

## Handle plain text

1. Detect the source encoding, byte-order mark, and line-ending convention before revision.
2. Preserve UTF encoding and line endings when they carry workflow significance.
3. Preserve intentional blank lines, indentation, list markers, and fixed-width blocks.
4. Avoid converting plain text into Markdown unless requested.
5. Save the revision as `<stem>-humanified.txt`.
6. Save the diagnostic report and change record separately from the revised text.
7. Compare the output against the source for encoding damage and accidental line loss.

## Handle Markdown

1. Parse the document structurally before revising prose.
2. Preserve YAML or TOML frontmatter keys, delimiters, value types, and ordering where feasible.
3. Treat frontmatter values as protected metadata unless their revision is explicitly approved.
4. Preserve heading levels, anchors, and section hierarchy unless the approved plan changes structure.
5. Preserve code fences, fence languages, inline code, and executable examples verbatim unless explicitly in scope.
6. Preserve link destinations, reference-style link labels, image paths, and title attributes.
7. Preserve footnote identifiers and keep every reference paired with its definition.
8. Preserve table syntax, column count, alignment markers, and embedded line breaks.
9. Preserve HTML blocks, comments, template directives, and component tags unless explicitly in scope.
10. Preserve block quotations and quoted source text verbatim.
11. Preserve repository-specific formatting and line endings when they affect diffs or tooling.
12. Validate frontmatter, fences, links, footnotes, tables, and HTML after reassembly.
13. Save the revision as `<stem>-humanified.md`.
14. Produce a unified diff when the source belongs to a repository or when exact review is useful.
15. Produce `<stem>-humanify-change-record.md` for structural changes and material editorial decisions.
16. Keep diagnostic prose outside the revised Markdown unless comments were explicitly requested.

## Handle Word documents

1. Invoke the `docx` skill for every `.docx` inspection, creation, or modification.
2. Read and follow that skill's complete instructions before touching the document.
3. Use its required render-and-verify workflow for the source and every deliverable.
4. Inspect rendered pages as well as extracted text before defining analysis units.
5. Preserve styles and style inheritance instead of recreating formatting manually.
6. Preserve heading levels, numbered and bulleted lists, and numbering continuity.
7. Preserve tables, merged cells, widths, repeated header rows, captions, and reading order.
8. Preserve footnotes, endnotes, citations, comments, bookmarks, and cross-references.
9. Preserve headers, footers, page numbering, section breaks, columns, and page orientation.
10. Preserve fields, content controls, hyperlinks, and automatic references where the tooling permits safe round-tripping.
11. Preserve embedded media and text boxes unless the approved revision requires a change.
12. Inspect tracked changes and comments already present before deciding how to layer new revisions.
13. Avoid accepting or deleting pre-existing revisions unless explicitly authorized.
14. Produce `<stem>-humanified-redline.docx` with native tracked changes when reliable tooling supports them.
15. Produce a clearly labeled redline representation when native Word tracking cannot be emitted safely.
16. Never describe a visual or comparison redline as native tracked changes.
17. Produce `<stem>-humanified-clean.docx` for every substantial revision.
18. Produce only the requested reviewed copy for a minor revision when a separate clean copy adds no value.
19. Disclose any unsupported Word feature, lost dynamic behavior, flattened field, or substituted redline method.
20. Render every produced `.docx` to page images and inspect the entire rendered output.
21. Check for pagination drift, clipped text, broken tables, orphaned headings, blank pages, and numbering changes.
22. Compare extracted source and output content for omissions, duplication, and protected-span changes.
23. Correct layout or content failures and repeat rendering until the deliverables pass.

## Handle PDFs

1. Invoke the `pdf` skill for every PDF inspection or diagnostic source and follow its complete extraction, rendering, visual-review, and verification instructions.
2. Treat PDF as a diagnostic source rather than a format-preserving revision target.
3. Extract text and inspect rendered pages so layout, tables, captions, and reading order inform the diagnosis; never rely on extraction alone for layout or reading order.
4. Use page numbers plus section or passage anchors for every PDF finding.
5. Distinguish printed page labels from physical PDF page indices when they differ.
6. Record OCR uncertainty, missing fonts, inaccessible layers, or extraction-order problems.
7. Diagnose supplied annexes in PDF form within their approved consistency scope.
8. Request the editable source before beginning format-preserving revision.
9. Offer a clean `.md`, `.txt`, or `.docx` reconstruction only after the user explicitly chooses that conversion.
10. Label any reconstruction as a new document rather than an edited PDF.
11. Avoid promising preservation of the PDF's layout, fields, signatures, annotations, or accessibility structure from extraction alone.

## Handle spreadsheet evidence and annexes

1. Invoke the `xlsx` skill when an actual `.xlsx`, `.xls`, `.csv`, or `.tsv` file is supplied.
2. Do not invoke the spreadsheet skill merely because a Word, Markdown, or PDF document contains a table.
3. Treat a spreadsheet as read-only consistency evidence unless the user explicitly includes workbook revision in scope and approves it at the human gate.
4. Use the spreadsheet skill to inspect relevant values, formulas, labels, units, dates, sheet relationships, comments, and displayed results; do not flatten formulas into extracted values.
5. Render and visually inspect every relevant sheet or range under the spreadsheet skill's contract before claiming that a table, total, label, note, or visual relationship was reviewed.
6. Record workbook, sheet, table or range, and cell anchors for every finding. Preserve enough context to distinguish displayed values from underlying formulas and inputs.
7. Reconcile workbook claims with the main document and other supplied annexes without deciding external truth when the supplied materials conflict.
8. Keep formulas, numeric types, date types, number formats, named ranges, tables, comments, charts, and workbook structure protected unless workbook editing is explicitly approved.
9. If workbook revision is approved, let the spreadsheet skill own authoring, recalculation, export, and visual verification. `humanify` supplies only approved prose replacements, protected-content constraints, and the issue ledger.
10. A prose-heavy workbook may be diagnosed by semantic cell ranges, but it remains a spreadsheet artifact. Do not convert it to Word or Markdown without explicit authorization.

## Scope annexes

1. Include every supplied annex in the manifest and global consistency map.
2. Preserve an annex unchanged when it serves only as evidence or reference.
3. Diagnose contradictions between the main document and annexes without selecting a factually correct side unless the supplied material establishes it.
4. Gate any proposed annex revision separately when it changes the approved file scope.
5. Apply the same format-specific preservation rules to every annex approved for revision.
6. Name an edited annex `<annex-stem>-humanified.<ext>` and keep its original immutable.
7. Verify cross-references between the main document and every annex after revision. Check both target resolution and descriptive scope: the referring text must not promise content the target does not contain.

## Name and deliver outputs

1. Use `<stem>-humanify-diagnosis.md` for the readable diagnostic report.
2. Use `<stem>-humanify-issue-ledger.md` for the exhaustive anchored ledger.
3. Use `<stem>-humanify-change-record.md` for approved changes, exclusions, and material limitations.
4. Use `<stem>-humanified.<ext>` for one revised editable artifact.
5. Add `-redline` and `-clean` before the extension when delivering both Word versions.
6. Use `<stem>-humanify-provisional.<ext>` when an unresolved blocking issue prevents final completion, and produce `<stem>-humanify-unresolved-issues.md`.
7. Do not create or retain a misleading `-humanified` or `-final` filename for a result that remains provisional.
8. Add a numeric suffix rather than overwriting an existing deliverable.
9. Deliver only the artifacts needed to review or use the result.
10. Link user-facing deliverables from their final destination, not from temporary work paths.
11. State which source and annexes received complete review.
12. State which features or regions remained unverified and why.
