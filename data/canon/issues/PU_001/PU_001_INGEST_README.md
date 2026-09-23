# BLACKPAPER PU #001 COMPLETE INGEST

**Contract:** `BLACKPAPER_ISSUE_INGEST_V1`  
**Issue:** Power Unlimited #001  
**Publication year:** 1993  
**Physical PDF pages:** 84  
**Human-verified scored evaluation census:** 37

This directory is the canonical issue-level ingest unit for BLACKPAPER.PAGE. It packages the completed human + machine reconstruction into a reusable schema intended to be repeated for PU #002, PU #003, and later issues.

## Authority model

1. **HUMAN_VISUAL_VERIFIED** — human-confirmed issue facts such as review identity, score, reviewer/layout interpretation and known special cases. Highest authority.
2. **DIRECT_ISSUE_TEXT** — text recovered from the scan/transcript, including review bodies, editorials, features, captions, lists and advertisements.
3. **MACHINE_STRUCTURING_INFERENCE** — article classification, normalization, summaries, style signals and inferred boundaries. Must remain marked.
4. **EXTERNAL_ENRICHMENT** — canonical modern game identity, aliases, developers/publishers/genre/franchise metadata. Never evidence for what PU itself said.

## Files

### `PU_001_BEST_MACHINE_TRANSCRIPT_FULL.txt`
Page-delimited best-available full issue transcript. All 84 physical pages are represented. Pages without an embedded text layer remain transparently marked as partial/low-confidence where necessary. No paraphrased summaries are substituted for unreadable source prose.

### `PU_001_PAGE_TRANSCRIPTS.jsonl`
Exactly one record per physical PDF page. Contains page identity, printed page when visible, page type, title hint, best transcript, transcript sources, repair flag, confidence and completeness.

### `PU_001_RAG_CHUNKS.jsonl`
Semantic retrieval units rather than blind fixed-token slices. Contains one source-grounded score/report chunk for every scored evaluation, full review-body chunks when page layout permits safe isolation, and semantic units for editorial/news/features/lists/columns/tips/ads. Advertisements are explicitly typed as advertisements.

### `PU_001_HUMAN_CANON_REVIEWS.jsonl`
Authoritative 37-record scored-evaluation canon. Scores and review identities are HUMAN_VISUAL_VERIFIED. Reviewer status distinguishes `DIRECT_BYLINE`, `DIRECT_LAYOUT_ASSOCIATION`, `CONTEXTUAL_CANDIDATE`, and `UNRESOLVED`. External canonical titles are nested and marked as enrichment.

### `PU_001_ENTITY_INDEX.jsonl`
Issue-grounded entities only: games/software actually present, people, reviewers/editors, platforms, companies, named sections and selected hardware/systems. External metadata is not allowed to manufacture issue presence.

### `PU_001_ALIAS_MAP.jsonl`
Retrieval aliases and normalization mappings. Every mapping states its source: direct issue text, transcript repair, human-pass normalization, or external enrichment. Example: the issue-native `Star Fox -> StarWing` relationship remains distinct from the external canonical `StarWing -> Star Fox` mapping.

### `PU_001_EDITOR_EVIDENCE.jsonl`
Direct authorship, masthead/testteam evidence, review subjects/scores and short issue-grounded language samples. Mechanical style signals are marked as inference and must not be treated as biography/personality fact.

### `PU_001_ISSUE_KNOWLEDGE.jsonl`
Structured non-review issue knowledge: the opening editorial, 3DO, Teleplay, Hellraiser investigation, Virgin charts, The ZONE, scoring semantics, Super FX, Hacker/Steve Jackson history, Eeuwig Leven, Power Quest and other queryable issue facts. Excerpts are direct; summaries are marked machine structuring.

### `PU_001_ISSUE_METADATA.json`
Issue-level metadata, source hashes, layer status, review census and historical semantics.

### `PU_001_PROVENANCE.jsonl`
Record-level provenance for pages, reviews, RAG chunks, entities, aliases, editor evidence and issue knowledge. External sources are recorded only where external normalization is actually used.

### `PU_001_MYSQL_PAGE_UPSERT.sql`
Idempotent issue-scoped page ingest helper. Because the live corpus schema was not supplied, it safely loads/upserts into a dedicated staging/recommended page table and includes a commented adapter template for the existing BLACKPAPER raw corpus table. It never deletes unrelated corpus data.

### `PU_001_RAG_CHUNKS_IMPORT.sql`
Creates a safe MySQL/InnoDB semantic chunk table if needed and upserts PU #001 chunks by unique `chunk_id`. Includes ordinary indexes and MySQL FULLTEXT search. No vector database is required.

### `PU_001_CONFLICTS.txt`
Human-vs-machine reconciliation history, including corrected report wording, title/oral slips, page-layout interpretation, and the intentionally unresolved Beyond Cyberpunk byline.

### `PU_001_QA_REPORT.txt`
Completeness/accounting gates. The package may be ingested only when every hard gate passes.

## Recommended ingest order

1. `PU_001_ISSUE_METADATA.json`
2. `PU_001_PAGE_TRANSCRIPTS.jsonl`
3. `PU_001_MYSQL_PAGE_UPSERT.sql`
4. `PU_001_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_001_ENTITY_INDEX.jsonl`
6. `PU_001_ALIAS_MAP.jsonl`
7. `PU_001_EDITOR_EVIDENCE.jsonl`
8. `PU_001_ISSUE_KNOWLEDGE.jsonl`
9. `PU_001_RAG_CHUNKS.jsonl` / `PU_001_RAG_CHUNKS_IMPORT.sql`
10. `PU_001_PROVENANCE.jsonl` and `PU_001_QA_REPORT.txt`

## Historical article semantics

PU #001's own p17 explanation is authoritative: `REVIEW`/bespreking and `PREVIEW`/voorbespreking primarily encode 1993 availability/import status. Do not automatically map `PREVIEW` to modern prerelease or unfinished-code semantics.

## Known non-blocking transcript limitations

The source PDF contains eight pages without an embedded text layer. They are represented rather than dropped. OCR and visual recovery are marked in page records. This is a **best-available complete issue source**, not a claim that every graphic page has a human-certified word-for-word transcription.

## Future issue contract

Future issue packagers should preserve these filenames and core fields, use one page record per physical PDF page, preserve original score notation, keep human and machine authority separate, and never hide external enrichment inside PU-derived claims. New fields may be added backward-compatibly, but existing meanings should not be changed.
