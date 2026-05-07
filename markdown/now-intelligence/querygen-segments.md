---
title: Segments in the Query Generation semantic layer
description: Segments are predefined filter conditions that map business terminology to specific query filters, helping the semantic layer translate natural language questions into accurate database queries.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Segments in the Query Generation semantic layer

Segments are predefined filter conditions that map business terminology to specific query filters, helping the semantic layer translate natural language questions into accurate database queries.

Segments provide non-obvious context to assist the semantic layer in selecting the correct entity, dimension, and values. For example, in the utterance "How many open emergency change requests are there?", a segment identifies that "open" means "active=true" and "emergency" is a Type, not a Priority.

When a user asks a question, the Query Generation engine searches for matching segments and includes their filters in the LLM prompt so the model can reuse them to construct accurate queries.

There are two types of segments:

-   **Automated Segments**

    System-generated from reports, dashboards, filters, modules, and indicator sources. Names are often technical—for example, "Incidents.Open".

-   **Manual Segments**

    Created by admins via the Manual Segment Config table. Names are user-friendly— for example, "Critical Open Incidents". Manual segments use a two-table data model with automatic synchronization and can be shipped with applications via plugins.


| |Manual Segments|Automated Segments|
|---|---------------|------------------|
|Created by|Admin, shipped via update set|System-generated from reports, dashboards, filters, modules|
|Name quality|User-friendly, tuned for search|Often technical—for example, "Incidents.Open"|
|Search priority|5% boost over automated \(adjustable in**sn\_query\_gen.segments.manual\_segment\_scale\_factor**\)|Standard scoring|
|LLM treatment|Retain all filters unless irrelevant|Critique each filter individually|
|Prompt label|`user_defined_segment`|`automated_segment`|
|Lifecycle|Fully controlled by admin|Tied to source record activity/usage|
|Shipped with app|Yes \(update set\)|No \(generated at runtime\)|

## How segments work

The system uses AI search to find segments that are semantically similar to the user's query. AI search indexes the Name, Description, Entity, and Filter fields in the Segments table, comparing them to the user's query to produce a subset of relevant segments.

In the LLM call, the system passes the Name, Description, Entity, and Filters. The LLM uses the segments as building blocks for generating a new query. For example, if a user asks "Unassigned Incidents located in San Diego" and the segment "Unassigned Incidents" is passed to the LLM, the LLM uses the segment's filter as the starting point and attaches the location filter "San Diego" on top of the segment.

|Step|Purpose|Output|
|----|-------|------|
|1: Input|Capture user's natural language query|Raw query text|
|2: Search|Find semantically similar prebuilt segments|Subset of relevant segments|
|3: Scoring|Rank the set of relevant segments based on their semantic similarity scores|The subset of relevant segments, now ranked and sorted|
|4: Context|Provide segment metadata to LLM|Structured segment data|
|5: Generate|Combine segment logic with new conditions|Complete executable query|

## How manual segments work

Manual segments serve two roles at query time:

-   **Entity discovery**

    On first-time queries with no previous context, segment matches can add or boost entities in the entity list. A match against a manual segment name helps identify the intended entity by adding or boosting it in the candidate list. If a user asks "Show me critical open incidents" and a manual segment named "Critical Open Incidents" exists on the Incident \[incident\] table, the `incident` entity gets boosted in the results.

-   **Filter provision**

    Matching segments are formatted into the LLM prompt context. The LLM sees:

    ```
    **Related Segments**:
    - **Critical Open Incidents** (user_defined_segment)
      - description : High priority incidents that are open and unresolved
      - entity : incident
      - filter : { conditions : [{"field":"incident.priority","operator":"=","value":"1"}, ...] }
    ```

    The LLM then decides whether to reuse the segment's filters fully or partially when constructing the query. Manual segments are labeled `user_defined_segment` in the prompt, which tells the LLM to retain all filters unless completely irrelevant.


## Manual segment scoring boost

Manual segments receive a priority boost. When the engine searches for relevant segments, it scores each result by semantic similarity—how closely the segment's name and description match the user's question. By default, manual segments receive a 5% boost applied on top of their raw similarity score.

The boost factor is configurable via the system property **sn\_query\_gen.segments.manual\_segment\_scale\_factor**. Increasing it, for example to `1.10`, elevates manual segments more strongly. Setting it to `1.0` removes the boost entirely.

In practice, automated segments often have names that partially match user utterances. For example, a report called "Open Incidents" may score similarly to a manual segment called "Critical Open Incidents". The boost ensures that your handmade, domain-tuned segments surface ahead of system-generated ones when both are close matches.

## How segment scoring works

1.  AI Search returns a raw semantic similarity score \(0.0–1.0\) for each candidate segment.
2.  Segments below the match threshold \(default `0.70`\) are discarded.
3.  Manual segment scores are multiplied by the scale factor \(default `1.05`\).
4.  Results are sorted by boosted score and capped at the result limit.

## Automatic segment sources

The system auto-generates segments from existing data sources on a schedule. The Query Generation Sync Segments job creates segments automatically, running at installation and then weekly by default.

|Source|What it pulls|
|------|-------------|
|Saved Reports \(sys\_report\)|Report filters from recently viewed reports|
|Report Sources \(sys\_report\_source\)|Analytics data source filters|
|PA Indicators \(pa\_cubes\)|Performance Analytics indicator conditions|
|Saved Filters \(sys\_filter\)|Global saved filters only \(excludes user-specific and group-specific filters\)|
|App Modules \(sys\_app\_module\)|Module-level list view filters|

## Automated segment rules

To reduce noise from outdated and irrelevant segments, the job follows specific rules. Segments based on reports, report sources, or indicator sources are active only if the records meet certain criteria:

-   Reports must be shared, created by a user with an analytics manager role \(admin, dashboard\_admin, report\_admin, pa\_admin, or viz\_admin\), and have run recently \(within 180 days by default\).
-   Report sources must be included in a data visualization or used in a report that has run recently.
-   Indicator sources must be linked to indicators with scores that have recently changed.

**Important:** Segments cannot be created from indicator sources or modules on domain-separated instances.

For reports, "run recently" is defined by the **sn\_query\_gen.segments.reports.last\_viewed\_threshold\_days** system property. The default value is 180 days.

For indicator sources, the time span for "recently changed" depends on the indicator frequency:

-   Daily: last 7 days
-   Weekly: last 30 days
-   Bi-weekly: last 30 days
-   Monthly: last 90 days
-   Four weeks: last 90 days
-   Bi-monthly: last 90 days
-   Quarterly: last 180 days
-   Fiscal quarterly: last 180 days
-   Six months: last 12 months
-   Yearly: last 24 months
-   Fiscal yearly: last 24 months

You can change the time spans for indicator sources by applying a multiplier using the **sn\_query\_gen.segments.indicator.inactivity\_threshold\_multiplier** system property. The value must be an integer, meaning you can only lengthen the periods, not shorten them.

## Disabling segment sources

You can disable segment creation altogether, or for individual source types. You might disable segment generation to troubleshoot, or if segments from a source are "noisy." Each source type has a corresponding **sn\_query\_gen.segments.disable.\*** system property. Disable segments for that source by setting the corresponding system property to **true**. All existing segments created from sources of that type are excluded from AI Data Explorer search results. No new segments of that type are created. During the next Sync Segments job, all segments of that type are deactivated. For more information, see [Query Generation properties](querygen-properties.md).

-   **[Guidelines for segments](general-guidelines-segments.md)**  
Follow these suggestions to help you use segments in the semantic layer effectively.
-   **[Create a manual segment](../task/querygen-create-segment-manually.md)**  
Manual segments are admin-created saved searches with friendly names that bridge natural language questions and database filters for the Query Generation semantic layer.
-   **[Manual segment data model and sync behavior](manual-segment-data-model-sync.md)**  
Manual segments use a two-table data model with automatic synchronization between the configuration table and the runtime table used for search operations.
-   **[Shipping manual segments via plugins](shipping-manual-segments-plugins.md)**  
Business unit application developers can ship manual segments with their applications to provide domain-specific saved searches that work from the moment the app is installed.

**Parent Topic:**[Tuning the semantic layer](../../ai-data-explorer/concept/semantic-layer-tuning-overview.md)

**Related topics**  


[Create a manual segment](../task/querygen-create-segment-manually.md)

[Manual segment data model and sync behavior](manual-segment-data-model-sync.md)

[Shipping manual segments via plugins](shipping-manual-segments-plugins.md)

[Guidelines for segments](general-guidelines-segments.md)

[Roles, tables, and scheduled jobs included with Query Generation](tables-sched-jobs-query-gen.md)

[Query Generation properties](querygen-properties.md)

