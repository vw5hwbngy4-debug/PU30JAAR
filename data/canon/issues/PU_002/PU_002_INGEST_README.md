# BLACKPAPER PU #002 COMPLETE INGEST

Canonical ingest unit for **Power Unlimited issue #002, September 1993**.

This package is the final packaging/normalization product of a completed
human + machine issue reconstruction. It does not restart discovery.

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
   - not included in this PU #002 ingest package.

## Files

### `PU_002_BEST_MACHINE_TRANSCRIPT_FULL.txt`
Complete 84-page best-available machine transcript with explicit page boundaries.
Embedded PDF text is preferred. PDF pages 6 and 42 required an explicit OCR fallback.

### `PU_002_PAGE_TRANSCRIPTS.jsonl`
Exactly one machine-readable record per physical PDF page.
Includes page provenance, transcript origin, confidence and machine page-type hints.

### `PU_002_RAG_CHUNKS.jsonl`
172 semantic retrieval chunks.
Contains separate review-article, score/verdict, issue-knowledge,
page-section and section-cluster retrieval units.

### `PU_002_HUMAN_CANON_REVIEWS.jsonl`
Authoritative 47-record scored-evaluation census.
Preserves original 10-point scores and a derived 0–100 convenience value.

### `PU_002_ENTITY_INDEX.jsonl`
85 issue-grounded entities: reviewed works, people, platforms,
recurring sections and directly referenced issue topics.

### `PU_002_ALIAS_MAP.jsonl`
14 issue-native or reconciliation aliases.
No web-derived aliases are hidden in this file.

### `PU_002_EDITOR_EVIDENCE.jsonl`
63 issue-local editor/reviewer evidence records.
Designed for factual grounding of reconstructed editor answers,
not for manufacturing permanent personality claims.

### `PU_002_ISSUE_KNOWLEDGE.jsonl`
26 non-review knowledge records covering news, technology,
historical terminology, reader/editorial commentary and other useful issue knowledge.

### `PU_002_ISSUE_METADATA.json`
Final issue-level census, source hashes and completed layer flags.

### `PU_002_PROVENANCE.jsonl`
Merged provenance for the full transcript, all 84 pages,
canon/knowledge artifacts and all RAG chunks.

### `PU_002_MYSQL_PAGE_UPSERT.sql`
Safe PHP/MySQL-friendly page import/upsert.
Targets `PU_002` only and includes a generic adaptable page table.

### `PU_002_RAG_CHUNKS_IMPORT.sql`
Safe MySQL semantic-chunk schema + idempotent import.
No vector database is required; a FULLTEXT index is included.

### `PU_002_CONFLICTS.txt`
Human-machine reconciliation history and final special-case preservation.

### `PU_002_QA_REPORT.txt`
Final census, integrity checks and hard ingest gates.

## Recommended Blackpaper ingest order

1. `PU_002_ISSUE_METADATA.json`
2. `PU_002_PAGE_TRANSCRIPTS.jsonl`
3. `PU_002_MYSQL_PAGE_UPSERT.sql`
4. `PU_002_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_002_ENTITY_INDEX.jsonl`
6. `PU_002_ALIAS_MAP.jsonl`
7. `PU_002_EDITOR_EVIDENCE.jsonl`
8. `PU_002_ISSUE_KNOWLEDGE.jsonl`
9. `PU_002_RAG_CHUNKS.jsonl`
10. `PU_002_RAG_CHUNKS_IMPORT.sql`
11. `PU_002_PROVENANCE.jsonl`
12. `PU_002_QA_REPORT.txt`

## Important PU #002 exceptions

- **Shadowrun RPG**: reviewer intentionally unresolved.
- **Shadowrun Superior**: reviewer intentionally unresolved.
- **Wolfenstein -3D2 / Spear of Destiny**: printed byline is `Game girl`;
  the underlying identity is not inferred.
- **Inca**: Graphics 9,0, Geluid 9,0, final 9.
- **Night Trap**: Bjorn + Adam shared/direct-layout authorship.
- **Civilization**: one shared PC / Macintosh review.
- **Zen: Intergalactic Ninja**: the visually printed red/down report indicators
  are preserved even where the wording sounds positive.
- **Dark Castle**: the visually printed green/up indicator for
  `Teleurstellend beeld en geluid` is preserved rather than semantically repaired.
- **Mario interview pp44–45**: treated as a satirical/fictionalized feature,
  not as real-world Mario biography.

## Future issue contract

Future PU issue packages should use these same filenames with only the issue
number changed, preserve the same authority boundaries, maintain exactly one
page transcript per physical PDF page, keep original score notation, and never
promote unresolved or inferred authorship to direct fact.

The ingest package should always remain traceable back to the original issue scan.


## Factory v1.1 normalization

This package was audited against `BLACKPAPER_PU_ISSUE_FACTORY_PORTABLE v1.1`.
The original PU #002 content passed its substantive accounting, but the final archive ZIP omitted four v1.1 handoff artifacts and used a legacy score-status field. This normalized edition adds:

- `PU_002_HUMAN_PASS_OBSERVATIONS.jsonl`
- `PU_002_HUMAN_PASS_LOG.txt`
- `PU_002_ISSUE_CENSUS.json`
- `PU_002_RUNTIME_HANDOFF.json`
- `PU_002_FACTORY_V1_1_QA_REPORT.txt`

It also adds `issue_number: 2` to canon review records and separates `score_status: RESOLVED` from the human visual verification authority. No review, score, component score, verdict, page transcript, RAG chunk or provenance record was removed.
