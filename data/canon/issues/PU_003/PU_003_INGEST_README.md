# BLACKPAPER PU #003 COMPLETE INGEST

Canonical ingest unit for **Power Unlimited issue #003, October 1993**.

This package is the final packaging/normalization product of the completed
human + machine reconstruction. It does not restart discovery.

## Authority order

1. **Human visual / reconciled canon**
   - authoritative for visually verified review identity, reviewer association,
     scores and report fields.
2. **Direct issue text**
   - authoritative for body text, letters, news, features, columns, tips,
     advertisements and other issue wording.
3. **Machine structuring / inference**
   - used for page types, summaries, entity indexing and semantic boundaries.
   - never silently overrides tiers 1 or 2.
4. **External enrichment**
   - not included in this PU #003 ingest package.

## Final issue accounting

- 84 physical PDF pages.
- 84 page transcript records.
- 42 scored game rows in the games contents.
- 1 extra scored Space Hulk board-game evaluation on page 52.
- 43 canonical scored evaluations.
- 43/43 final scores resolved.
- 178 semantic RAG chunks.
- 93 issue-grounded entities.
- 20 aliases / normalization records.
- 60 editor-evidence records.
- 35 issue-knowledge records.

## Files

### `PU_003_BEST_MACHINE_TRANSCRIPT_FULL.txt`
Complete 84-page best-available machine transcript with explicit page boundaries.
Embedded PDF text is preferred. OCR fallback is explicit and separately traceable.

### `PU_003_PAGE_TRANSCRIPTS.jsonl`
Exactly one machine-readable record per physical PDF page.

### `PU_003_RAG_CHUNKS.jsonl`
178 semantic retrieval chunks covering:
review articles, score/verdict blocks, issue knowledge, page fallbacks,
multi-page section clusters and list blocks.

### `PU_003_HUMAN_CANON_REVIEWS.jsonl`
Authoritative 43-record scored-evaluation census.
Original 10-point notation is preserved; normalized 0–100 values are derived convenience fields only.

### `PU_003_ENTITY_INDEX.jsonl`
Issue-grounded works, people, pseudonyms, platforms, sections, hardware,
companies and named issue topics.

### `PU_003_ALIAS_MAP.jsonl`
Issue-native title variants, OCR/speech reconciliation aliases and reviewer-code mappings.
No external/web aliases are silently mixed in.

### `PU_003_EDITOR_EVIDENCE.jsonl`
Issue-local factual evidence for editors/reviewers, including masthead roles,
direct review authorship, Testteam choices and signed features/columns.

### `PU_003_ISSUE_KNOWLEDGE.jsonl`
Non-review issue knowledge, including hardware, reader debate, historical terminology,
Jurassic Park film/technology material, Nintendo Service-Lijn, censorship/policy,
Eeuwig Leven, Power Sales and editorial/column material.

### `PU_003_ISSUE_METADATA.json`
Final issue census, source hashes, authority model and completed layer flags.

### `PU_003_PROVENANCE.jsonl`
Merged provenance for transcript, all 84 pages, canon/knowledge artifacts and all RAG chunks.

### `PU_003_MYSQL_PAGE_UPSERT.sql`
Safe MySQL page upsert template targeting only PU #003.

### `PU_003_RAG_CHUNKS_IMPORT.sql`
Safe MySQL semantic-chunk table + idempotent import with FULLTEXT indexing.
No vector database is required.

### `PU_003_CONFLICTS.txt`
Human-machine reconciliation history and preserved special cases.

### `PU_003_QA_REPORT.txt`
Final completeness, duplicate/orphan checks and hard ingest gates.

## Recommended Blackpaper ingest order

1. `PU_003_ISSUE_METADATA.json`
2. `PU_003_PAGE_TRANSCRIPTS.jsonl`
3. `PU_003_MYSQL_PAGE_UPSERT.sql`
4. `PU_003_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_003_ENTITY_INDEX.jsonl`
6. `PU_003_ALIAS_MAP.jsonl`
7. `PU_003_EDITOR_EVIDENCE.jsonl`
8. `PU_003_ISSUE_KNOWLEDGE.jsonl`
9. `PU_003_RAG_CHUNKS.jsonl`
10. `PU_003_RAG_CHUNKS_IMPORT.sql`
11. `PU_003_PROVENANCE.jsonl`
12. `PU_003_QA_REPORT.txt`

## Important PU #003 exceptions

- `ROLE GIRL` is a directly printed reviewer pseudonym for Realms of Arkania.
  No real-person identity is inferred.
- Space Hulk board-game sound is `n.v.t.` and is never converted into 0.
- Street Fighter II Turbo / Mortal Kombat scorecards are associated by direct visual layout.
- Bubble Bobble Part 2 graphics = 5,5.
- Backgammon sound = 8,5.
- Asterix Game Boy reviewer = Adam Eeuwens.
- Gordo 106 and V for Victory retain their direct printed titles.
- Tuff E Nuff is the direct title; Fighting Spirit remains issue-local strap/subtitle context.

## Future issue contract

Future issue packages should retain these filenames with the issue number changed,
the same evidence tiers, one transcript record per physical PDF page,
exact original score notation and explicit unresolved/pseudonym handling.

The original issue scan remains the final source authority for what was printed.
