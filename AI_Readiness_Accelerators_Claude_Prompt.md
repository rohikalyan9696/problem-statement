# Curated Prompt for Claude — "AI-Readiness Platform: Stage-1 & Stage-2 Accelerator Strategy"

> **How to use this file.** Copy everything inside the fenced block titled **"PROMPT TO PASTE INTO CLAUDE"** and paste it into Claude (Claude.ai, Claude in Cursor, or the API). Claude will return (1) a fully-referenced **Word document** and (2) a **professional, vivid, detailed slide deck (PPT) outline**. The reference library, framework, and agent inventory Claude needs are all embedded in the prompt so it does not have to guess or hallucinate.
>
> Everything below is anchored to the two-stage framework in the source slide ("**Curated Data vs AI-Ready Data — Two Distinct Stages**", Hexaware) and to the agent inventory in the referenced repo `https://github.com/rohikalyan9696/123.git`.

---

## Background & rationale (read this first — do NOT paste this section)

**Who/what this is for.** We (Hexaware) are building an **AI-Readiness Platform**. To position it, we are benchmarking how the market delivers "accelerators" against a **two-stage data-readiness model**:

- **Stage 1 — Curated Data ("make this ready"):** Data Quality Validated → Lineage Tracked End-to-End → Governance Enforced → Business Context Enriched → Continuously Observed. *Trustworthy for business decisions; eligible for AI prep, but not yet AI-consumable.*
- **Stage 2 — AI-Ready Data ("AI layer"):** Vectorized & Embedded → Indexed for Retrieval → Feature-Engineered for ML → Semantically Enriched → Responsible-AI Metadata Attached. *Only this state supports production-scale AI.*

**The three platforms to benchmark:** **Snowflake**, **Microsoft Fabric**, **Databricks**.

**Our current agent inventory** (from the `123` repo — feed this to Claude so it can map "what we already have" to gaps):

- **Built / ready:** Data Profiler Agent, DQ Check Agent, Data Quality Agent (conversational), Data Catalog Agent, Data Modeler Agent (3NF + Star), Data Transformation Agent, KB (Knowledge Base) Agent, Synthetic Data Generator.
- **Planned / WIP:** Data Vault 2.0 Agent, Code Review Agent (PySpark standards), STTM Agent — DataStage→PySpark, STTM Agent — Informatica→PySpark, STTM Agent — SAS→Snowpark.

**What "good" looks like in the market** (public reference accelerators, e.g., Tiger Analytics' *Intelligent Data Express (IDX)*, *iDEA*, *IDQ*; Databricks *Brickbuilder*/*Solution Accelerators*; Snowflake *Cortex Code* skills; Microsoft Fabric *templates* & *solution accelerators*). Real, verified links are embedded in the prompt's Reference Library so Claude cites correctly.

---

## PROMPT TO PASTE INTO CLAUDE

```text
ROLE
You are a Principal Data & AI Platform Strategist and technical writer. You produce
board-ready, fully-referenced strategy artifacts. You are meticulous about accuracy:
you cite only the sources provided (or ones you can state with high confidence), and
you clearly label anything that is your own analysis or recommendation vs. a sourced fact.

MISSION
We are building an enterprise "AI-Readiness Platform." I need a competitive/strategic
analysis of data-readiness ACCELERATORS across three platforms — Snowflake, Microsoft
Fabric, and Databricks — organized around a two-stage readiness model, plus a concrete
set of accelerators we should build for OUR platform.

Produce TWO deliverables in one response:
  1) A professional WORD DOCUMENT (well-structured long-form report WITH inline
     citations and a reference list).
  2) A PROFESSIONAL, VIVID, DETAILED SLIDE DECK (PPT) — a slide-by-slide outline with
     titles, on-slide content, speaker notes, and visual/design direction.

============================================================
THE FRAMEWORK (this is the backbone — everything maps to it)
============================================================
Two distinct stages of data readiness:

STAGE 1 — CURATED DATA ("make this ready"): trustworthy for business decisions,
eligible for AI prep, but NOT yet AI-consumable. Five pillars:
  1. Data Quality Validated — de-duplicated, normalized, consistent formats, DQ scores
     per attribute, completeness verified, validated against business rules.
  2. Lineage Tracked End-to-End — full provenance (origin, transformations, consumption),
     auditable, data-stewardship roles, populated metadata catalog.
  3. Governance Enforced — RBAC/access controls, PII detection & masking, regulatory
     compliance (GDPR/HIPAA/CCPA), data contracts, policies enforced at scale.
  4. Business Context Enriched — business glossary linked, semantic meaning documented,
     domain ownership, data products with agreed SLAs & freshness targets.
  5. Continuously Observed — pipeline health, anomaly/drift/freshness detection in real
     time, incident alerting, trust score maintained and visible to consumers.

STAGE 2 — AI-READY DATA ("AI layer"): curated data further enriched, structured, and
optimized so AI systems (LLMs, ML models, agents) can consume, learn from, and act on it
at scale. Five pillars:
  1. Vectorized & Embedded — text/docs/images → numerical embeddings; enables semantic
     search and RAG pipelines for LLM consumption.
  2. Indexed for Retrieval — chunked and stored in vector DBs; agents retrieve context at
     query time (no full-table scans).
  3. Feature-Engineered for ML — domain features derived and stored in feature stores;
     required for training, batch scoring, real-time inference.
  4. Semantically Enriched — ontologies, knowledge graphs, domain tags; LLMs reason about
     meaning, not just format. Critical for enterprise GenAI accuracy.
  5. Responsible-AI Metadata Attached — bias flags, explainability attributes, model
     cards, data provenance linked to every AI asset; auditability and trust.

============================================================
PLATFORMS TO BENCHMARK
============================================================
Snowflake, Microsoft Fabric, Databricks.
For EACH platform, identify BOTH:
  - a "Stage-1 accelerator" story (how curated/governed data is accelerated), and
  - a "Stage-2 accelerator" story (how AI-ready data — vectors, retrieval, features,
    semantics, responsible-AI — is accelerated),
distinguishing FIRST-PARTY (vendor-native) accelerators from PARTNER/PUBLIC accelerators
(e.g., Tiger Analytics and other SIs).

============================================================
OUR CURRENT AGENT INVENTORY (map "what we already have")
============================================================
Built/ready: Data Profiler Agent; DQ Check Agent (nulls, completeness, duplicates,
uniqueness, domain rules); Data Quality Agent (conversational Q&A on data health);
Data Catalog Agent (business-readable catalog from schema + business docs); Data Modeler
Agent (3NF + Star Schema from metadata); Data Transformation Agent (tool-calling,
human-in-the-loop); KB Agent (sourced answers from docs/runbooks/Jira/code); Synthetic
Data Generator (schema-aware, relationship-aware).
Planned/WIP: Data Vault 2.0 Agent; Code Review Agent (PySpark standards -> PASS/FAIL/
WARNING/CRITICAL); STTM Agent DataStage->PySpark; STTM Agent Informatica->PySpark;
STTM Agent SAS->Snowpark.

============================================================
WHAT TO ANALYZE AND DELIVER (content requirements)
============================================================
A) STAGE-MAPPED MARKET SCAN. A comparison matrix: rows = the 5 Stage-1 pillars and the
   5 Stage-2 pillars; columns = Snowflake, Microsoft Fabric, Databricks; each cell names
   the concrete first-party accelerator/feature AND a representative public/partner
   accelerator (cite the source). Call out where the market is strong vs. thin.

B) PUBLIC/PARTNER ACCELERATOR DEEP-DIVE. Profile at least Tiger Analytics
   (IDX / iDEA / IDQ, Snowflake Cortex accelerators) as the exemplar, plus 2-3 other
   public accelerator families (e.g., Databricks Brickbuilder/Solution Accelerators,
   Snowflake Cortex Code skills & Native Apps, Microsoft Fabric templates & solution
   accelerators). For each: what it does, which stage/pillars it hits, and the proof/link.

C) OUR GAP MAP. Plot our built + planned agents onto the 10 pillars. Show clearly which
   pillars we already cover (mostly Stage 1) and which are white space (mostly Stage 2:
   vectorization, retrieval/RAG, feature stores, knowledge graphs, responsible-AI
   metadata). Be honest about gaps.

D) TEN UNIQUE ACCELERATORS FOR OUR PLATFORM. Propose exactly 10 DISTINCT accelerators we
   should build (differentiated from what already exists in-market — do not just rename
   Tiger/Databricks features). Spread them across BOTH stages (roughly balanced). For EACH
   of the 10, provide a structured entry:
     - Name (crisp, product-style) and one-line pitch
     - Stage & pillar(s) it targets (from the framework above)
     - What it does (3-5 sentences)
     - How it differs from existing market accelerators (the "unique" claim)
     - Justification / business case (pain solved, measurable outcome, e.g., cycle-time
       or cost reduction) and the PROOF: analogous market evidence + a REFERENCE LINK for
       each (use the Reference Library below; add well-known official docs only if you are
       confident they are correct).
     - Which of our existing agents it reuses/extends (traceability).
     - Platform fit (Snowflake / Fabric / Databricks / all).
   Present the 10 as a numbered deep-dive AND summarize them in one comparison table.

E) RECOMMENDATION & ROADMAP. Priority order (impact vs. effort) for the 10; a phased
   build sequence (foundation -> differentiation -> moat); and 3-5 KPIs to prove AI-
   readiness (e.g., % data with responsible-AI metadata, RAG answer accuracy, time-to-
   AI-ready-dataset). Do NOT express the roadmap in calendar days/weeks — use phases,
   dependencies, and effort tiers (S/M/L) instead.

============================================================
REFERENCE LIBRARY (cite these; every claim about a named accelerator needs a link)
============================================================
Tiger Analytics — Snowflake accelerators (Cortex-AI STTM->code, Data Modeling, SQL
  optimization): https://www.tigeranalytics.com/partnerships/snowflake/
Tiger Analytics — Intelligent Data Express (IDX) on Databricks:
  https://www.tigeranalytics.com/perspectives/blog/powering-data-analytics-modernization-with-tiger-analytics-intelligent-data-express-idx-on-databricks/
Tiger Analytics — iDEA (Intelligent Data Engineering Agent) on Databricks Lakehouse:
  https://www.tigeranalytics.com/perspectives/blog/elevating-the-craft-idea-the-agentic-ai-platform-for-modern-data-engineering-on-the-databricks-lakehouse/
Tiger Analytics — Snowflake partner page (Native Data Quality framework, Snowpark):
  https://www.snowflake.com/en/why-snowflake/partners/all-partners/tiger-analytics/
Databricks — GenAI Partner Accelerators for Data Engineering & Migration (lists Hexaware,
  Tiger, and 20+ partners): https://www.databricks.com/blog/introducing-databricks-genai-partner-accelerators-data-engineering-migration
Databricks — Partner Solutions & Accelerators (Brickbuilder catalog):
  https://www.databricks.com/partners/consulting-and-si/partner-solutions
Databricks — Brickbuilder Accelerators (Lakehouse) launch:
  https://www.databricks.com/blog/databricks-expands-brickbuilder-program-include-lakehouse-accelerators
Databricks — Brickbuilder Unity Catalog Accelerators (governance):
  https://www.databricks.com/blog/databricks-expands-brickbuilder-program-include-unity-catalog-accelerators
Databricks — Solution Accelerators (free first-party notebooks):
  https://www.databricks.com/solutions/accelerators
Snowflake — Cortex AI (LLMs, agents, AISQL, governance & observability):
  https://www.snowflake.com/en/product/features/cortex/
Snowflake — Cortex Code Data Governance Skills (natural-language governance):
  https://www.snowflake.com/en/blog/engineering/cortex-code-governance-skills/
Snowflake — Cortex Code bundled skills (data-quality DMFs, profiling, native apps):
  https://docs.snowflake.com/en/user-guide/cortex-code/bundled-skills
Snowflake — Data governance skills for Cortex Code (docs):
  https://docs.snowflake.com/en/user-guide/governance-skills
Microsoft Fabric — Data Factory pipeline templates:
  https://learn.microsoft.com/en-us/fabric/data-factory/templates
Microsoft Fabric — "AI-Ready Apps" RAG pipeline (chunk/redact/embed) blog:
  https://blog.fabric.microsoft.com/en-US/blog/ai-ready-apps-build-rag-data-pipeline-from-azure-blob-storage-to-sql-database-in-microsoft-fabric-within-minutes/
Microsoft Fabric — RAG pipeline sample repo:
  https://github.com/Azure-Samples/fabric-sqldb-ai-ragpipeline
Microsoft — Unified Data Foundation with Fabric solution accelerator (medallion +
  Purview + Databricks + Fabric Data Agent):
  https://github.com/microsoft/unified-data-foundation-with-fabric-solution-accelerator
(If you cite any additional source, prefer official vendor docs and clearly mark it.)

============================================================
DELIVERABLE 1 — WORD DOCUMENT (format & style)
============================================================
- Length: comprehensive (~2,500-4,000 words). Executive, board-ready, confident tone.
- Structure (use real headings/subheadings):
    1. Cover block (title, subtitle, "Confidential", version/date placeholder)
    2. Executive Summary (10-12 lines: the two-stage thesis, market posture, our gap,
       the 10-accelerator bet)
    3. The Two-Stage Readiness Model (Stage 1 & Stage 2, the 10 pillars)
    4. Stage-Mapped Market Scan (matrix + narrative) — section A
    5. Public/Partner Accelerator Deep-Dive — section B
    6. Our Gap Map — section C
    7. Ten Unique Accelerators for Our Platform — section D (numbered deep-dive + table)
    8. Recommendation & Roadmap — section E
    9. References (numbered; every link from the library actually used)
- Citations: use inline numeric markers like [1], [2] tied to the numbered References list.
- Include at least two tables (the market-scan matrix and the 10-accelerator summary).
- Output the document as clean, copy-pasteable Markdown that maps 1:1 to Word headings
  (H1/H2/H3, bullet lists, and Markdown tables), so I can paste it straight into Word or
  run it through a Markdown->docx converter. Do NOT wrap the whole thing in a code block.

============================================================
DELIVERABLE 2 — SLIDE DECK / PPT (format & style)
============================================================
- 14-18 slides. Professional, vivid, executive-grade. Design system callouts included.
- For EACH slide provide: Slide number + Title | On-slide content (headline + 3-6 tight
  bullets or a described visual/diagram) | Speaker notes (2-4 sentences) | Visual direction
  (chart/diagram/icon/layout suggestion).
- Suggested flow:
    1  Title slide (platform name placeholder + tagline)
    2  The problem: why "curated" != "AI-ready"
    3  The Two-Stage Model (hero diagram: Stage 1 -> Stage 2 with the 10 pillars)
    4  Stage 1 deep (5 pillars)
    5  Stage 2 deep (5 pillars)
    6  Market scan matrix (Snowflake / Fabric / Databricks x 10 pillars)
    7  Snowflake accelerators (Stage 1 & 2)
    8  Microsoft Fabric accelerators (Stage 1 & 2)
    9  Databricks accelerators (Stage 1 & 2)
    10 Public/partner exemplar: Tiger Analytics (IDX / iDEA / IDQ)
    11 Our current agents mapped to the model (gap map)
    12-14 The 10 unique accelerators (grouped; ~3-4 per slide, with the "why unique")
    15 Prioritization (impact vs. effort 2x2)
    16 Phased roadmap (phases/effort tiers, not calendar dates)
    17 KPIs to prove AI-readiness
    18 Call to action / next steps
- Add a "Design system" note: color palette (deep indigo/blue like the source slide,
  white space, one accent), font pairing, iconography style, and a rule that each slide
  has one clear message. Provide alt-text for the hero diagram.

============================================================
QUALITY BAR & RULES
============================================================
- Accuracy first. Only attach a reference link to a named accelerator when the link
  supports it. If you are inferring or recommending, say "our analysis" / "proposed".
- The 10 accelerators must be genuinely distinct from each other AND from existing market
  offerings; each must state its unique angle explicitly.
- Keep it vendor-neutral in judgment; be specific and concrete, not generic.
- No calendar-time estimates; use effort tiers (S/M/L) and dependencies.
- End with a one-paragraph note on assumptions and what would sharpen the analysis.

Now produce Deliverable 1 (Word document) first, then Deliverable 2 (slide deck).
```

---

## Optional add-ons you can append to the prompt

- **Tighten to your brand:** replace *"our platform"* with your platform's real name and add your brand colors so the deck's design system matches.
- **Ask for the .docx/.pptx files directly:** if you are using Claude with a tool/skill that can emit files, append: *"Also generate the actual `.docx` and `.pptx` files, not just the outline."*
- **Localize the 10 accelerators:** append your top 2-3 industries (e.g., banking, retail) so the accelerators and proof points are industry-specific.
- **Depth control:** append *"Expand each of the 10 accelerators to ~250 words with a mini business case and one quantified before/after metric."*

## Verified reference library (same links embedded in the prompt)

| # | Source | Link |
|---|--------|------|
| 1 | Tiger Analytics — Snowflake accelerators | https://www.tigeranalytics.com/partnerships/snowflake/ |
| 2 | Tiger Analytics — Intelligent Data Express (IDX), Databricks | https://www.tigeranalytics.com/perspectives/blog/powering-data-analytics-modernization-with-tiger-analytics-intelligent-data-express-idx-on-databricks/ |
| 3 | Tiger Analytics — iDEA agentic platform, Databricks | https://www.tigeranalytics.com/perspectives/blog/elevating-the-craft-idea-the-agentic-ai-platform-for-modern-data-engineering-on-the-databricks-lakehouse/ |
| 4 | Tiger Analytics — Snowflake partner page (Native DQ framework) | https://www.snowflake.com/en/why-snowflake/partners/all-partners/tiger-analytics/ |
| 5 | Databricks — GenAI Partner Accelerators (lists Hexaware & Tiger) | https://www.databricks.com/blog/introducing-databricks-genai-partner-accelerators-data-engineering-migration |
| 6 | Databricks — Partner Solutions & Accelerators (Brickbuilder catalog) | https://www.databricks.com/partners/consulting-and-si/partner-solutions |
| 7 | Databricks — Brickbuilder Lakehouse Accelerators | https://www.databricks.com/blog/databricks-expands-brickbuilder-program-include-lakehouse-accelerators |
| 8 | Databricks — Brickbuilder Unity Catalog Accelerators | https://www.databricks.com/blog/databricks-expands-brickbuilder-program-include-unity-catalog-accelerators |
| 9 | Databricks — Solution Accelerators (free notebooks) | https://www.databricks.com/solutions/accelerators |
| 10 | Snowflake — Cortex AI | https://www.snowflake.com/en/product/features/cortex/ |
| 11 | Snowflake — Cortex Code Data Governance Skills | https://www.snowflake.com/en/blog/engineering/cortex-code-governance-skills/ |
| 12 | Snowflake — Cortex Code bundled skills (DMF data-quality, profiling) | https://docs.snowflake.com/en/user-guide/cortex-code/bundled-skills |
| 13 | Snowflake — Data governance skills for Cortex Code (docs) | https://docs.snowflake.com/en/user-guide/governance-skills |
| 14 | Microsoft Fabric — Data Factory pipeline templates | https://learn.microsoft.com/en-us/fabric/data-factory/templates |
| 15 | Microsoft Fabric — "AI-Ready Apps" RAG pipeline blog | https://blog.fabric.microsoft.com/en-US/blog/ai-ready-apps-build-rag-data-pipeline-from-azure-blob-storage-to-sql-database-in-microsoft-fabric-within-minutes/ |
| 16 | Microsoft Fabric — RAG pipeline sample repo | https://github.com/Azure-Samples/fabric-sqldb-ai-ragpipeline |
| 17 | Microsoft — Unified Data Foundation w/ Fabric solution accelerator | https://github.com/microsoft/unified-data-foundation-with-fabric-solution-accelerator |

> **Note on accuracy:** these links were verified via web search at the time of writing. Ask Claude (or a reviewer) to re-check any link before publishing externally, and to only attach a link to a claim the source actually supports.
