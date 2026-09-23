# PU30JAAR / BLACKPAPER PU #004 COMPLETE INGEST

Canonical ingest unit for **Power Unlimited issue #004, November 1993**.

This package is the final packaging/normalization product of a completed
human + machine issue reconstruction. It does not restart discovery.

## Authority order

1. **Human visual / reconciled canon**
   - authoritative for visually verified review identity, reviewer association,
     scores and scorecard report fields.
2. **Direct issue text**
   - authoritative for article body text, letters, news, features, columns,
     tips, advertisements and other issue wording.
3. **Machine structuring / inference**
   - page types, semantic boundaries, summaries and entity indexing.
4. **External enrichment**
   - not included in this PU #004 ingest package.

## Final issue accounting

- 84 physical PDF pages.
- 84 page transcript records.
- 39 canonical scored evaluations.
- 39/39 final scores resolved.
- 185 semantic RAG chunks.
- 101 issue-grounded entities.
- 19 aliases / normalization records.
- 57 editor-evidence records.
- 41 issue-knowledge records.
- B.O.B. reviewer intentionally unresolved.

## Census equation

The games contents contains 38 platform rows.

- Freddy Pharkas appears under Macintosh and PC but has one shared scorecard: `-1`
- MiG-29 vs F-15 is one contents row but contains two scorecards: `+1`
- How to Host a Mystery is a scored board game outside the ordinary games contents: `+1`

Therefore:

`38 - 1 + 1 + 1 = 39`

## Files

1. `PU_004_BEST_MACHINE_TRANSCRIPT_FULL.txt`
2. `PU_004_PAGE_TRANSCRIPTS.jsonl`
3. `PU_004_RAG_CHUNKS.jsonl`
4. `PU_004_HUMAN_CANON_REVIEWS.jsonl`
5. `PU_004_ENTITY_INDEX.jsonl`
6. `PU_004_ALIAS_MAP.jsonl`
7. `PU_004_EDITOR_EVIDENCE.jsonl`
8. `PU_004_ISSUE_KNOWLEDGE.jsonl`
9. `PU_004_ISSUE_METADATA.json`
10. `PU_004_PROVENANCE.jsonl`
11. `PU_004_MYSQL_PAGE_UPSERT.sql`
12. `PU_004_RAG_CHUNKS_IMPORT.sql`
13. `PU_004_CONFLICTS.txt`
14. `PU_004_QA_REPORT.txt`
15. `PU_004_INGEST_README.md`

## Recommended ingest order

1. issue metadata
2. page transcripts
3. raw page upsert
4. human review canon
5. entities
6. aliases
7. editor evidence
8. issue knowledge
9. RAG chunks
10. RAG SQL import
11. provenance
12. QA

## Important PU #004 exceptions

- **B.O.B.** reviewer is `UNRESOLVED`. No reviewer is inherited from the previous article.
- **SPIDERBEN** is a direct playful signature/alias for Ben de Dood.
- The **Spider-Man** p30–31 feature contains four separate platform scorecards:
  Game Gear, Mega Drive, Game Boy and Super Nintendo.
- **X-Men** on Mega Drive is a separate review on p32 by Adam Eeuwens.
- **Zelda: The Wand of Gamelon** has three positive report bullets and no negative bullet.
  The third plus is `Spel is te saven`.
- **How to Host a Mystery** has `n.v.t.` for Graphics and Geluid.
- **Freddy Pharkas** Mac/PC is one shared scorecard.
- **MiG-29 Soviet Fighter / F-15 Strike Eagle** is one contents row mapping to two scorecards.

## Future issue contract

Future deep-canon issue packages should preserve this same 15-file shape,
authority model, one-transcript-record-per-physical-page rule, original score notation,
explicit reviewer uncertainty and non-destructive provenance.

The original magazine scan remains the final evidence for what was printed.
