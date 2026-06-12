# Grouping and Search

## Candidate Expression Discovery

Scan titles in batches after sorting by title, date, journal, or another informative field. Look for expressions that form useful branches and change a research decision.

When the field is unknown and the collection is large, a broad-first pass can be efficient: select the most frequent meaningful feature observed in a title sample, tag its large result set, then refine that branch in a second or third pass. This rapidly exposes the field outline and shrinks the working unclassified queue. Do not confuse a ubiquitous background term with a meaningful feature.

When a broad branch would not be useful, prefer medium-frequency expressions. Rare expressions are usually better deferred until the map has enough structure to interpret them.

Test:

- full terms and abbreviations;
- singular, plural, and spelling variants;
- stems and partial words;
- capitalization and spacing;
- hyphens, slashes, formulas, symbols, and punctuation;
- broader, narrower, and operationally equivalent expressions;
- named platforms, instruments, models, datasets, or study frameworks.

Unknown terminology can be discovered by deleting restrictive parts of a known expression and inspecting the broader result set. Search feedback is a learning mechanism.

## Search Validation Loop

1. Run the candidate expression against the fixed baseline.
2. Inspect a sample from the beginning, middle, and end of the result set.
3. Identify false positives, false negatives, and hidden variants.
4. Modify the expression or split the concept.
5. Save the tag and its provenance.
6. Remove tagged records from the working unclassified queue.
7. Recheck counts from the baseline when inconsistencies appear.

Use a transit group when a result set requires manual filtering before it can be assigned.

## Nonexclusive and Exclusive Modes

Default to nonexclusive tagging because a paper normally contains several useful dimensions. Search each tag from the full fixed parent collection so records in earlier tags remain discoverable.

Use exclusive buckets when:

- the collection is small;
- overlap is low;
- the user explicitly needs a partition;
- a sequential screening workflow requires one final disposition per record.

In exclusive mode, search and review the shrinking unclassified queue. State that the resulting counts depend on classification order.

## Search Scope

- Titles are the default for rapid mapping.
- Add abstracts and keywords when title-only recall is inadequate, the result set is small, or a concrete study is being designed.
- Avoid abstract-wide expansion across every coarse tag in a large collection before the user knows which branches matter.
- Read full text only for selected questions that cannot be resolved from metadata, title, or abstract.

## Automation Limits

Word frequency, clustering, topic modeling, embeddings, and AI suggestions can propose candidates. They cannot independently determine which features matter to the user's research goal. Always validate automated groups against records and intended decisions.
