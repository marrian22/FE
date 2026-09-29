For Single-Shot Execution
Stage 1 (Inventory Ledger):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PIPELINE EXECUTION INSTRUCTION - STAGE 1 (SINGLE-SHOT)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
You are currently operating in: MODE 3 (MASTER / SINGLE-SHOT).
No child contracts are supplied. The attached source represents the complete analytical scope.

Orchestrator Node Context:
ORCHESTRATOR_NODE_ID: <INJECT_UNIQUE_ID_HERE>

Execute PHASE 1 ONLY using the strict TWO-PASS BEHAVIORAL DISCOVERY process.
Apply the ATOMIC INVENTORY IDENTITY TEST. Do not consolidate during Stage 1.
Analyze the attached source and print the complete Source-Behavior Accounting Ledger as a Markdown table.

The table MUST contain these exact columns:
| Inventory ID (INV-<ORCHESTRATOR_NODE_ID>-<id>) | Observable Behavior | Trigger / Context | Source Line Ranges | Primary Behavioral Classification | Planned Primary Artifact Type | Planned Target Artifact ID | Planned Disposition (Mapped / Explicitly Omitted) | Scenario Membership (FS-SCN-<n> / MULTIPLE:<FS-SCN-<n>, ...> / NOT-SCENARIO-DISTINCT) |

Rules:
1. Use these Primary Behavioral Classification values: FLOW, BUSINESS RULE, EXCEPTION, DATA CONTRACT, SQL_MAPPING, INTEGRATION, MISSING IMPLEMENTATION, ANOMALY, UNRESOLVED EVIDENCE, NON_BEHAVIORAL TECHNICAL.
2. Pre-Planning Rule Audit: Before assigning a Planned Target Artifact ID of FS-BRL-*, validate that the behavior adds independent policy content. If it is merely passive data movement or flow sequence, plan it for Section 8 or Section 4 instead.
3. Each Stage 1 Observable Behavior cell must explicitly state, where applicable: input, trigger, condition, transformation/filter/calculation, and outcome. The Trigger/Context column must not be used as a substitute for the behavior's condition or outcome.
4. Do NOT include summary or meta-accounting rows inside the ledger table itself.
5. If the table exceeds token limits, break cleanly at a row boundary and emit: [CONTINUATION REQUIRED - NEXT: <Inventory ID>].

Immediately after the table is complete, print exactly one accounting line:
STAGE 1 ACCOUNTING: Total Inventoried: <n> | Planned Mapped: <n> | Planned Explicitly Omitted: <n> | Unaccounted: 0

Do NOT generate Sections 1-12.
Do NOT generate Appendices A-B.
Stop immediately after printing the footer.

Stage 2 (FSD Generation & Closure):
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PIPELINE EXECUTION INSTRUCTION - STAGE 2 (SINGLE-SHOT)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Now, using EXACTLY the Source-Behavior Accounting Ledger you printed in Stage 1 as your strict baseline, generate the COMPLETE FINAL FUNCTIONAL SPECIFICATION (Sections 1-12 and Appendices A-B).

Requirements for Stage 2:
1. Stage 1 inventory IDs, source ranges, internal provenance, and mapped/omitted dispositions are immutable. Every single item from the Stage 1 table must be accounted for with zero items dropped.
2. Apply the CENTRAL CONSOLIDATION INVARIANT and STAGE 2 CONSOLIDATION PROOF. Ensure any Stage 2 consolidation preserves complete semantics and avoids generic suppression.
3. Track exact deduplicated identifiers from the Stage 1 table via the internal PROVENANCE array, but render ONLY the deduplicated source coordinates into the printed RANGES array (`<!-- TRACE: [...] -->`).
4. Pre-Generation Rule Audit: Before emitting Section 5, validate every proposed FS-BRL. If it is merely a field copy, object assignment, null-substitution, enum conversion, SQL binding, or duplicates an FS-MPF with no additional policy content, reclassify the item to Section 8 or Section 4 and DO NOT create the FS-BRL. 
5. Routing Corrections: If any routing target was altered from Stage 1, you must emit the `ROUTING CORRECTION DISCLOSURE` ledger as Section 11.5 before the Final Validation Checklist.
6. Omission Routing (Invariant 3): Materialize items into Section 11.1, 11.2, or 11.3 exactly according to ACCOUNTING DISPOSITION SEMANTICS.
7. Single-Shot Section 11.4 Rule: Section 11.4 must contain exactly: "N/A - Single-Shot Execution (Governed by Stage 1 Source-Behavior Ledger)."
8. Close the accounting loop in the Completeness Signature by verifying:
   - Total Inventoried Source Behaviors (Stage 1) = Mapped + Explicitly Omitted + Unaccounted (Must be 0).
   - Total Ingested BHV Contracts must be explicitly logged as "N/A".
   - Total BHV Disposition Ledger Rows must be explicitly logged as "N/A - Single-Shot Mode".
   Ensure the stated Total Inventoried count matches the Stage 1 Accounting footer literal count.




