---
title: Segments in the Query Generation semantic layer
description: Segments are predefined filter conditions that map business terminology to specific query filters, helping the semantic layer translate natural language questions into accurate database queries.Manual segments are admin-created saved searches with friendly names that bridge natural language questions and database filters for the Query Generation semantic layer.Follow these suggestions to help you use segments in the semantic layer effectively.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [manual segments, query generation, semantic layer, saved searches]
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

    Created by admins via the Manual Segment Config table. Names are user-friendly— for example, "Critical Open Incidents".


## How segments work

The system uses AI search to find segments that are semantically similar to the user's query. AI search indexes the Name, Description, Entity, and Filter fields in the Segments table, comparing them to the user's query to produce a subset of relevant segments.

In the LLM call, the system passes the Name, Description, Entity, and Filters. The LLM uses the segments as building blocks for generating a new query. For example, if a user asks "Unassigned Incidents located in San Diego" and the segment "Unassigned Incidents" is passed to the LLM, the LLM uses the segment's filter as the starting point and attaches the location filter "San Diego" on top of the segment.

|Step|Purpose|Output|
|----|-------|------|
|1: Input|Capture user's natural language query|Raw query text|
|2: Search|Find semantically similar prebuilt segments|Subset of relevant segments|
|3: Context|Provide segment metadata to LLM|Structured segment data|
|4: Generate|Combine segment logic with new conditions|Complete executable query|

## Automatic segment sources

The system auto-generates segments from existing ServiceNow data sources on a schedule. The Query Generation Sync Segments job creates segments automatically, running at installation and then weekly by default.

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

**Related topics**  


[Roles, tables, and scheduled jobs included with Query Generation](tables-sched-jobs-query-gen.md)

[Query Generation properties](querygen-properties.md)

## Create a manual segment

Manual segments are admin-created saved searches with friendly names that bridge natural language questions and database filters for the Query Generation semantic layer.

### Before you begin

Role required: sn\_query\_gen.admin or higher

### About this task

Create manual segments in the following circumstances:

-   Your organization has standard terminology that maps to specific filters \(for example, "Sev1", "VIP", "overdue"\)
-   Users repeatedly ask the same filtered question and the system does not automatically pick up the right filter
-   You want to encode business logic that cannot be inferred from field values alone \(for example, "at-risk accounts" = combination of multiple conditions\)
-   The special terminology of your organization is not translated accurately to filter conditions

**Tip:** The name and description are what AI search matches against. Use natural phrasing your users would say. Keep one segment per concept. Test by asking the question and checking if the segment appears in the logs.

### Procedure

1.  Navigate to **Query Generation** &gt; **Administration** &gt; **Manual Segment Config**.

2.  Press **New**.

3.  In the Manual Segment Config form, fill in the following information.

    |Field|Description|
    |-----|-----------|
    |Table Name|The table \(entity\) the segment applies to. Must have an active entity in the semantic layer. The system looks for the entity table first, then the segment within that table.|
    |Name|User-friendly name describing the segment in plain language a user would use when asking a question. No abbreviations or internal codes. Maximum 255 characters. For example, "Critical Open Incidents" instead of "P1\_OPEN\_INC".|
    |Description|An optional short phrase that expands on the name using similar, commonly used terms. Helps the LLM determine when to apply the segment. Use this to disambiguate similar segments or provide additional context. Maximum 4,000 characters.|
    |Filter|Encoded query defining the segment's filter conditions. Uses the condition builder \(v2\). Maximum 4,000 characters, although filters longer than 2,000 characters may be truncated in the LLM prompt.|
    |Active|Whether the system uses the segment. Defaults to selected. When cleared, the segment is deactivated and excluded from search.|

4.  Press **Submit**.

    A business rule fires asynchronously and syncs the record into the `sn_query_gen_segment` table, which is queried at search time.


### Result

The manual segment is active and available for Query Generation searches.

### Manual segments for the incident table

The following examples show well-crafted manual segments for the `incident` table:

|Name|Description|Table|Filter|
|----|-----------|-----|------|
|Critical Open Incidents|High priority incidents that are currently open and unresolved. Includes all assignment groups.|`incident`|`priority=1^state!=7^state!=8`|
|My Team's Overdue Incidents|Incidents assigned to the current user's group that have passed their SLA due date.|`incident`|`assignment_group=javascript:getMyGroups()^sla_due<javascript:gs.nowDateTime()^state!=7`|
|Recent P1 and P2 Escalations|Priority 1 and 2 incidents escalated in the last 7 days.|`incident`|`priority<=2^escalation=1^sys_updated_on>=javascript:gs.daysAgoStart(7)`|

## General guidelines

Follow these suggestions to help you use segments in the semantic layer effectively.

-   Test segments by asking natural language questions that should match them. The segment should appear in **Query Generation** &gt; **Logs**.
-   Monitor query logs to verify segments are being matched correctly and to identify the most valuable segments.
-   Disable noisy auto-generated segments rather than trying to overfit with multiple manual ones.
-   Use natural phrasing that matches how your users actually speak.
-   Keep one segment per concept to avoid confusion.
-   Refine segment names and descriptions based on user feedback and usage patterns
-   Consider creating manual segments for recurring questions that are not handled well by the existing segments.

