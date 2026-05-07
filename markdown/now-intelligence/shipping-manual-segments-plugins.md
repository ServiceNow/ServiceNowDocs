---
title: Shipping manual segments via plugins
description: Business unit application developers can ship manual segments with their applications to provide domain-specific saved searches that work from the moment the app is installed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-16"
reading_time_minutes: 4
keywords: [manual segments, plugins, shipping, application development, query generation]
breadcrumb: [Segments, Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Shipping manual segments via plugins

Business unit application developers can ship manual segments with their applications to provide domain-specific saved searches that work from the moment the app is installed.

## Shipping overview

Manual segments are the recommended way to ship domain-specific saved searches with your application. They receive a priority boost over automated segments during search, and the LLM is instructed to retain all their filters unless completely irrelevant—whereas automated segment filters are critiqued individually.

Shipping manual segments with your plugin ensures that users can immediately ask natural language questions about your application's data using business terminology, without waiting for automated segments to be generated from usage patterns.

## How to ship manual segments

1.  Create your manual segment config records in a development instance.
2.  Verify they sync correctly and produce expected search results.
3.  Include the `sn_query_gen_segment_table_config` records in your app's update set.

## Plugin installation behavior

Understanding how manual segments behave during plugin installation is important for setting proper expectations:

-   Business rules are **bypassed** during plugin installation—the async sync will not fire automatically at install time.
-   The records will be synced into `sn_query_gen_segment` the next time the **Generate Semantic Layer** scheduled job runs \(post-install\) or when the weekly **Sync Segments** job runs.
-   Ensure your plugin does not ship duplicate records. There is no unique constraint at the database level—admins must ensure no duplicate names per entity.

**Important:** Manual segments shipped via plugin will not be immediately available for search after installation. They become active after the next scheduled sync job runs.

## Example: Full configuration for a table

The following example shows manual segments for the `incident` table that could be shipped with an ITSM application:

**Prerequisite:** The `incident` table must have a record in `sn_query_gen_table_config` with **enable\_semantic\_generation = true** and an active entity.

|Name|Description|Table|Filter|
|----|-----------|-----|------|
|Critical Open Incidents|High priority incidents that are currently open and unresolved. Includes all assignment groups.|`incident`|`priority=1^state!=7^state!=8`|
|My Team's Overdue Incidents|Incidents assigned to the current user's group that have passed their SLA due date.|`incident`|`assignment_group=javascript:getMyGroups()^sla_due<javascript:gs.nowDateTime()^state!=7`|
|Recent P1/P2 Escalations|Priority 1 and 2 incidents escalated in the last 7 days.|`incident`|`priority<=2^escalation=1^sys_updated_on>=javascript:gs.daysAgoStart(7)`|

## Best practices for shipping segments

-   **Focus on high-value, high-traffic tables**

    Concentrate manual segments on the tables your users ask about most. A handful of well-crafted segments on your app's primary tables will have more impact than broad coverage across rarely-queried tables.

-   **Use business language, not technical codes**

    Segment names should match how users naturally speak about your domain. "Critical Open Incidents" is better than "P1\_OPEN\_INC".

-   **Provide descriptions for disambiguation**

    If you ship multiple segments for the same table, descriptions help the LLM pick the right one. Without descriptions, the LLM may arbitrarily choose between similar matches.

-   **Test before shipping**

    Verify in a test environment that segments sync correctly and appear in search results for relevant utterances. Check the query logs to confirm matching behavior.

-   **Avoid duplicating automated segments**

    Before creating a manual segment, check whether an automated segment already covers the same filter. If one exists but has a poor name, consider improving the source rather than creating a duplicate.


## Checklist before shipping

Verify the following before including manual segments in your plugin:

-   Each target table has an active entity in the semantic layer \(`sn_query_gen_table_config` with **enable\_semantic\_generation = true**\)
-   Segment names are written in plain user language, not technical shorthand
-   Descriptions are provided for segments where the name alone may be ambiguous
-   Filters are valid encoded queries and under 2,000 characters for optimal LLM prompt inclusion
-   No duplicate records \(same name + table combination\) exist in your update set
-   All `sn_query_gen_segment_table_config` records are included in your app's update set
-   You have verified in a test environment that segments sync correctly and appear in search results for relevant utterances

## Monitoring after deployment

After shipping manual segments with your application:

-   Monitor which segments are being matched in the query logs
-   Verify that generated queries are correct for the intended use cases
-   Collect user feedback on query accuracy and coverage
-   Iterate on segment names and descriptions based on usage patterns

If a segment is matching but producing wrong results, the issue is usually the name being too generic or the filter being too broad. Refine the name and description before adjusting system properties.

**Parent Topic:**[Segments in the Query Generation semantic layer](querygen-segments.md)

**Related topics**  


[Create a manual segment](../task/querygen-create-segment-manually.md)

[Manual segment data model and sync behavior](manual-segment-data-model-sync.md)

[Guidelines for segments](general-guidelines-segments.md)

