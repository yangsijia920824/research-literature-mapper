---
name: research-literature-mapper
description: Build goal-driven maps of research literature through high-throughput title-first triage, search-assisted coarse and fine grouping, nonexclusive tagging, residual review, and research-direction synthesis. Use when a user needs to understand a large literature library, classify references without reading every paper, compare candidate directions, refine a topic or experimental plan, identify useful papers, process an unclassified queue, or turn a literature collection into an actionable field map.
---

# Research Literature Mapper

## Overview

Convert a literature collection into an actionable map rather than treating classification or exhaustive reading as the goal. Preserve a fixed baseline collection, create reversible tags, learn from search feedback, and stop refining when the map supports the user's next research action.

## Operating Principles

- Begin with the research decision, problem, or next action the map must support.
- Treat groups as working tags and prompts, not as an authoritative taxonomy.
- Prefer nonexclusive tags unless the user has a clear reason for mutually exclusive buckets.
- Search from a fixed baseline collection; use a shrinking unclassified queue for discovery and progress tracking.
- Start with titles. Expand to abstracts only when title evidence is insufficient or the focused result set is small.
- Use counts as attention signals, not as evidence of scientific importance.
- Keep uncertain, irrelevant, deferred, and priority records explicit rather than forcing every record into a theme.
- Preserve provenance: record collection scope, search expressions, dates, counts, and material changes.
- Do not delete source records while mapping. Make operations reversible.
- Separate comprehensive collection from selective reading: broad intake can be redundant, but close reading must be purpose-driven.

## Workflow

### 1. Define the Mapping Goal

Classify the request into one or more working scenarios:

1. The field or direction is unclear.
2. A problem is known, but the state of research is unclear.
3. Several candidate directions must be compared.
4. A topic is known, but the experiment, theory, or study design needs refinement.
5. A failed or anomalous result needs explanations and troubleshooting paths.
6. A paper, review, proposal, or thesis structure must be built.

State the intended output before grouping. Load [scenario-and-granularity.md](references/scenario-and-granularity.md) when choosing scope or depth is difficult.

### 2. Establish Stable Working Sets

Create or identify:

- `baseline`: the fixed collection used for complete searches and count checks.
- `unclassified`: a working copy or queue whose count decreases as records are handled.
- `transit`: temporary search results used to inspect ambiguity before assigning tags.
- `priority`, `reference`, `uncertain`, `deferred`, and `irrelevant` as needed.

Record the initial counts. If the tool supports saved searches rather than physical groups, use them while preserving the same logical roles.

### 3. Build a Coarse Field Map

Choose a deliberate sort order such as title, date, or journal. Scan title batches for decision-relevant expressions:

- concepts, materials, populations, objects, or systems;
- methods, mechanisms, measurements, outcomes, and applications;
- abbreviations, roots, partial words, spelling variants, punctuation, symbols, and equivalent expressions.

For a large collection in an unknown field, a broad high-yield expression can be the first pass when it quickly removes hundreds or thousands of records and still defines a meaningful branch that can be refined later. Otherwise, prefer medium-frequency expressions that create useful distinctions without swallowing most of the collection.

Test each candidate expression against the baseline. Inspect false positives and false negatives, adjust the expression, then assign a nonexclusive tag. Remove handled records from `unclassified`, not from `baseline`.

Do not use a very common term merely because it is common. Use it only when its branch meaning, speed advantage, and later refinement plan are clear. Avoid almost-empty terms early unless they answer the user's immediate question. Load [grouping-and-search.md](references/grouping-and-search.md) for detailed search tests.

### 4. Refine Only Relevant Branches

Choose branches that are large, ambiguous, strategically important, or directly connected to the research goal. Within each selected branch:

1. Collect synonyms and broader/narrower expressions.
2. Search from the appropriate fixed parent set.
3. Create second- or third-level tags only when they clarify a decision.
4. Inspect remaining titles manually after search-based grouping stops producing useful distinctions.
5. Add multiple tags to a record when it informs several dimensions.

Possible dimensions include research object, material or population, intervention, method, morphology or structure, scale, performance, mechanism, context, application, and failure mode.

### 5. Process Residual Records

Treat the unclassified remainder as evidence, not failure. It can contain:

- rare terminology and hidden synonyms;
- malformed or incomplete metadata;
- weakly related or irrelevant records;
- records that require abstract review;
- genuinely new directions missed by initial searches.

Prioritize the residual queue most likely to change the research decision. Use rapid title triage, then selective abstract checks. Load [unclassified-and-quality-control.md](references/unclassified-and-quality-control.md) for audit rules.

### 6. Derive Research Outputs

Turn the tags into a structured map:

- dominant and emerging themes;
- competing approaches and trade-offs;
- underexplored combinations that have a real problem-based rationale;
- methods or frameworks transferable across fields;
- candidate research questions;
- experimental or analytical options;
- priority reading sets;
- unresolved terminology and evidence gaps;
- next searches or validation steps.

Do not equate a rare combination with a valuable topic. Test candidate directions against real-world relevance, feasibility, novelty, and the user's constraints. Load [research-direction-map.md](references/research-direction-map.md) for synthesis templates.

### 7. Apply the Stop Rule

Pause grouping when the current granularity lets the user choose or start the next action. Continue only when the map is still too coarse to formulate a study, compare options, troubleshoot, or write.

The process is iterative. Return to searching, importing, regrouping, or abstract review when later work exposes a missing distinction.

## Expected Deliverables

Unless the user requests another format, provide:

1. Mapping goal and collection baseline.
2. Tag hierarchy or flat tag matrix.
3. Search-expression log with scope and counts.
4. Residual and uncertainty report.
5. Research-direction map with supporting evidence.
6. Priority reading list and next actions.

Clearly distinguish observed counts and metadata from interpretation. Never invent corpus statistics.

## Tool Adaptation

Implement the logical workflow in the user's available reference manager, spreadsheet, database, or code environment. Menu names and export limits change over time; verify current software behavior when exact operational instructions matter.
