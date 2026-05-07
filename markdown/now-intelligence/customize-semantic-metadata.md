---
title: Customizing semantic metadata
description: Semantic metadata — descriptions, labels, and usage instructions — control how Query Generation interprets natural language questions. Customize these metadata to improve accuracy for your organization's terminology and data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-17"
reading_time_minutes: 5
keywords: [semantic metadata, semantic descriptions, semantic labels, usage instructions, entities, dimensions, query generation, update sets]
breadcrumb: [Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Customizing semantic metadata

Semantic metadata — descriptions, labels, and usage instructions — control how Query Generation interprets natural language questions. Customize these metadata to improve accuracy for your organization's terminology and data.

Both entities \(tables\) and dimensions \(fields\) in the semantic layer have three metadata fields that Query Generation uses when processing a question:

-   **Semantic Label**

    A short name or alias for the entity or dimension. Functions as a search keyword that helps AI search identify the correct table or field when a user's question does not match the default field label.

-   **Semantic Description**

    A natural-language description of what the entity or dimension represents in business terms. Provides context that helps the system distinguish between similar tables or fields.

-   **Semantic Usage Instructions**

    Instructions injected directly into the LLM prompt when the entity or dimension is selected. Teaches the system how to query the data — for example, which operators to use, how to handle abbreviations, or how to expand hierarchical values.


## When to customize

Metadata is auto-generated and works well in its baseline state. Customize it only when you observe consistent, repeatable problems:

-   The system selects the wrong table or cannot find one — edit descriptions and labels
-   The wrong field is selected or a field is missing — edit descriptions and labels
-   Your organization uses different terminology than the auto-generated labels — edit labels
-   The right table or field is selected but the query is constructed incorrectly — edit usage instructions

**Note:** There are thousands of dimensions. Do not try to review them all. Focus on fields that appear in failing queries.

## Two methods for customizing metadata

Two methods are available. Editing the configuration tables is considered the default approach.

|Method|Tables|When to use|
|------|------|-----------|
|Edit records on the Semantic Table Configuration and Semantic Column Configuration tables|Semantic Table Configuration \[sn\_query\_gen\_table\_config\] and Semantic Column Configuration \[sn\_query\_gen\_column\_config\]|Update set compatible. Customizations can be included in update sets and transferred between instances. Overrides values set in the Entity and Dimension tables. Supports entity and dimension descriptions and dimension usage instructions. Doesn't support entity labels or usage instructions.|
|Edit records on the Entity and Dimension tables|Entity \[sn\_query\_gen\_entity\] and Dimension \[sn\_query\_gen\_dimension\]|Simpler. Suitable for testing on a single instance. These customizations cannot be transferred between instances. However, this is the only method for changing entity labels and entity-level usage instructions. Could be overridden by an update to the table from an upgrade.|

**Note:** Both methods require the sn\_query\_gen.admin role or higher.

## Writing effective descriptions

Follow these guidelines when writing semantic descriptions and labels:

-   Keep descriptions to 1–2 sentences focused on how users refer to this data
-   Include common synonyms and abbreviations your users would say
-   Avoid full paragraphs. Concise descriptions match better than verbose ones

## Writing effective usage instructions

Follow these guidelines when writing semantic usage instructions:

-   Be specific and structured. Include rules, examples, and edge cases
-   Use numbered steps or labeled sections if the logic is complex
-   Include example user questions and what the query should look like
-   For free-text fields, specify matching strategy \(CONTAINS, exact match\) and expansion rules
-   Keep instructions focused on one entity or field's needs

## Usage instructions vs. Segments

Usage instructions teach the LLM how to query a field dynamically, allowing the LLM to handle many scenarios based on your rules. Segments hard-code specific filter values. For fields like free-text location, usage instructions are the correct approach because you cannot predefine every possible location query. Segments are better for fixed business terminology such as "Sev1" = priority 1.

## Semantic description

For an Incident entity, instead of using just "Incident table", use a description like "IT incidents, outages, service disruptions, and IT support tickets" to include terminology your users actually say.

## Data conventions in usage instructions

For a State field that stores abbreviations:

```
"Values in this field may be full state names or two-letter abbreviations (for example, 'California' or 'CA'). Always query for both forms. For country names, also include common aliases (for example, 'United Kingdom' OR 'UK')."
```

## Complex query logic in usage instructions

These usage instructions are for a free-text Approximate Location field with hierarchical expansion and synonym handling:

-   **Field: Approximate Location - Usage Instruction**

    The Approximate Location field is a non-normalized, free-text string. All queries must use case-insensitive CONTAINS matching and handle hierarchical expansion.

-   **Core Query Logic**
    1.  Identify the geographic entity \(Neighborhood, City, State, Country, Region, or Continent\).
    2.  Expand broader entities into explicit lists of sub-entities before querying.
    3.  Use OR logic for all expanded terms and synonyms.
-   **Expansion Rules**
    -   Continents: Expand to a list of all major countries within that continent.
    -   Regions: Expand to relevant states or countries \(for example, "Atlantic Coast" -&gt; NC, VA, FL, etc.\).
    -   States/Provinces: Include both full names and standard abbreviations \(for example, "North Carolina" OR "NC"\).
    -   Countries: Include common aliases \(for example, "UK" OR "United Kingdom"\).
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

-   **[Customize entity descriptions for the semantic layer](../task/customize-entity-descriptions.md)**  
Create custom entity descriptions in the Semantic Table Configuration table so that customizations can be transferred between instances via update sets.
-   **[Customize column descriptions and usage instructions](../task/customize-column-descriptions.md)**  
Create custom column descriptions and usage instructions in the Semantic Column Configuration table so that customizations can be transferred between instances via update sets.

**Parent Topic:**[Tuning the semantic layer](semantic-layer-tuning-overview.md)

**Related topics**  


[Roles, tables, and scheduled jobs included with Query Generation](../../par-for-workspace/concept/tables-sched-jobs-query-gen.md)

