---
title: Semantic usage instructions
description: Semantic usage instructions teach the system how to query data by defining matching strategies, expansion logic, and data conventions. Use these instructions when the right table or field is selected but the query is constructed incorrectly.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 3
keywords: [semantic usage instructions, query logic, matching strategy, LLM prompt]
breadcrumb: [Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Semantic usage instructions

Semantic usage instructions teach the system how to query data by defining matching strategies, expansion logic, and data conventions. Use these instructions when the right table or field is selected but the query is constructed incorrectly.

The Semantic Usage Instructions field is injected directly into the LLM prompt when a table or field is selected. This field functions as a custom prompt at the field level, teaching the system how to query the data.

## When to edit semantic usage instructions

Edit semantic usage instructions when:

-   The right table or field is selected, but the query is constructed incorrectly.
-   A field has non-standard data that needs special handling, such as free-text, abbreviations, or hierarchical values.

## Where to edit semantic usage instructions

Semantic usage instructions for tables are in the Entity \[sn\_query\_gen\_entity\] table. Semantic usage instructions for columns/fields are in the Dimension \[sn\_query\_gen\_dimension\] table. To edit these tables, you must have the sn\_query\_gen.admin role or higher.

## Writing effective usage instructions

Follow these guidelines when writing semantic usage instructions:

-   Be specific and structured. Include rules, examples, and edge cases
-   Use numbered steps or labeled sections if the logic is complex
-   Include example user questions and what the query should look like
-   For free-text fields, specify matching strategy \(CONTAINS, exact match\) and expansion rules
-   Keep instructions focused on one entity or field's needs

## Usage instructions vs. Segments

Usage instructions teach the LLM how to query a field dynamically, allowing the LLM to handle many scenarios based on your rules. Segments hard-code specific filter values. For fields like free-text location, usage instructions are the correct approach because you cannot predefine every possible location query. Segments are better for fixed business terminology such as "Sev1" = priority 1.

## Examples

The following examples show different types of usage instructions:

## Data conventions

For a State field that stores abbreviations:

```
"Values in this field may be full state names or two-letter abbreviations (e.g. 'California' or 'CA'). Always query for both forms. For country names, also include common aliases (e.g. 'United Kingdom' OR 'UK')."
```

## Complex query logic

For a free-text Approximate Location field with hierarchical expansion and synonym handling:

-   **Field: Approximate Location - Usage Instruction**

    The Approximate Location field is a non-normalized, free-text string. All queries must use case-insensitive CONTAINS matching and handle hierarchical expansion.

-   **Core Query Logic**
    1.  Identify the geographic entity \(Neighborhood, City, State, Country, Region, or Continent\).
    2.  Expand broader entities into explicit lists of sub-entities before querying.
    3.  Use OR logic for all expanded terms and synonyms.
-   **Expansion Rules**
    -   Continents: Expand to a list of all major countries within that continent.
    -   Regions: Expand to relevant states or countries \(e.g. "Atlantic Coast" -&gt; NC, VA, FL, etc.\).
    -   States/Provinces: Include both full names and standard abbreviations \(e.g. "North Carolina" OR "NC"\).
    -   Countries: Include common aliases \(e.g. "UK" OR "United Kingdom"\).
-   **Implementation Pattern**

    1.  Extract geographic intent.
    2.  Classify entity level.
    3.  Expand downward \(Continent &gt; Country\) or include synonyms \(State &gt; Abbreviation\).
    4.  Construct a single query string using OR-based CONTAINS filters.
    Notice the pattern: the instruction defines rules and examples, and the LLM can handle many related queries dynamically based on the rules you provide. You teach the logic once, and the model applies it to any input.

-   **Examples of user questions converted to queries**
    -   User: "Show me things in Japan" → Query: location CONTAINS "Japan"
    -   User: "Show me things in Asian countries" → Decomposition: Asia -&gt; \[Japan, China, Indonesia...\] → Query: location CONTAINS "Japan" OR location CONTAINS "China" OR location CONTAINS "Indonesia"...

    -   User: "Show me things in North Carolina" → Query: location CONTAINS "North Carolina" OR location CONTAINS "NC"
    -   User: "Show me everything in Europe" → Decomposition: Europe &gt; \[UK, Spain, France, Germany...\] → Query: location CONTAINS "UK" OR location CONTAINS "United Kingdom" OR location CONTAINS "Spain" OR location CONTAINS "France"...

**Parent Topic:**[Tuning the semantic layer](semantic-layer-tuning-overview.md)

**Related topics**  


[Roles, tables, and scheduled jobs included with Query Generation](../../par-for-workspace/concept/tables-sched-jobs-query-gen.md)

