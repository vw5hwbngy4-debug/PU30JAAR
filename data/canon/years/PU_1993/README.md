# Power Unlimited 1993 — YEAR_SYNTHESIS v1

Status: **YEAR_SYNTHESIS_COMPLETE**

This package is a derived knowledge layer over the five closed issue ingests PU #001–#005. It does **not** merge or replace those issue units.

## Core census
- Issues: 5/5
- Pages represented upstream: 420/420
- Canon scored evaluations: 209
- Scores resolved: 209/209
- Reviewer real-person identity unresolved or intentionally unlinked: 6 records
- Upstream RAG chunks indexed across the five issue packages: 876 (schemas differ between PU #001 and later issue-factory packages)
- Year mean score: 7.7928/10

## Authority
1. PU #001 consolidated human/scan review canon or PU #002–#005 HUMAN_CANON_REVIEWS for scored evaluation identity, reviewer and score fields.
2. Page transcripts for direct magazine text.
3. ISSUE_KNOWLEDGE where it points back to direct issue text.
4. YEAR_SYNTHESIS relations/statistics are derived and never override source layers.
5. RAG chunks are retrieval aids only.

## Important modeling decisions
- Every platform evaluation remains a separate review record.
- Review/preview terminology is preserved in its 1993 PU meaning. The year layer does not silently reinterpret PREVIEW as unfinished software.
- Michael **Schaefer/Schaeffer** is only unified in the explicitly inferred year-identity statistical view. Source spellings remain untouched.
- Joint bylines are not apportioned to individual reviewer averages.
- Pseudonymous printed bylines without real-person resolution remain unlinked.
- Genre statistics were **not** invented because the five source packages do not expose one stable authoritative genre taxonomy across all 209 evaluations.
- No external knowledge was used to decide whether any 1993 prediction later came true.

## Files
- `PU_1993_YEAR_REVIEW_INDEX.jsonl`: 209 one-to-one canon evaluation pointers.
- `PU_1993_REVIEWER_PROFILES.jsonl`: source-strict + explicitly inferred year identity profiles.
- `PU_1993_PLATFORM_SCORE_STATS.jsonl`: platform aggregates with transparent spelling normalization.
- `PU_1993_MULTI_PLATFORM_COMPARISONS.jsonl`: separate platform versions compared without merging.
- `PU_1993_CROSS_ISSUE_GAME_CONTINUITY.jsonl`: exact-title recurrence across issues.
- `PU_1993_HARDWARE_ARCS.jsonl`: 3DO, Jaguar, VR, CD32 chronology.
- `PU_1993_READER_FEEDBACK_LOOPS.jsonl`: reader ↔ editorial/review/tips continuity.
- `PU_1993_PREDICTIONS_REVISIONS_CONTRADICTIONS.jsonl`: preserved epistemic differences.
- `PU_1993_RECURRING_CRITICISM_SIGNALS.jsonl`: transparent motif retrieval signals.
- `PU_1993_COMPONENT_SCORE_GAPS.jsonl`: technically high component scores vs lower overall scores.
- `PU_1993_EDITOR_CONTINUITY.jsonl`: masthead change and continuity.
- `PU_1993_SYNTHESIS_RAG_CHUNKS.jsonl`: retrieval-friendly low-authority year summaries.
- `PU_1993_SOURCE_REGISTER.json`: hashes and authoritative source pointers.
- `PU_1993_PROVENANCE.jsonl`: derivation/provenance policy.
- `PU_1993_YEAR_CENSUS.json`: census.
- `PU_1993_QA_REPORT.txt`: validation gates.

This package is intended to be comparable later with `PU_1994_YEAR_SYNTHESIS`, without destroying issue-level provenance.
