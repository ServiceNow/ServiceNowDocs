---
title: Create a manual segment
description: Manual segments are admin-created saved searches with friendly names that bridge natural language questions and database filters for the Query Generation semantic layer.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-10"
reading_time_minutes: 4
keywords: [manual segments, query generation, semantic layer, saved searches]
breadcrumb: [Segments, Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Create a manual segment

Manual segments are admin-created saved searches with friendly names that bridge natural language questions and database filters for the Query Generation semantic layer.

## Before you begin

Role required: sn\_query\_gen.admin or higher

## About this task

Use manual segments to ship domain-specific saved searches with your application. They receive a priority boost over automated segments during search. This boost is set in **sn\_query\_gen.segments.manual\_segment\_scale\_factor**. The LLM retains all their filters unless irrelevant, whereas automated segment filters are critiqued individually.

Create manual segments in the following circumstances:

-   Your organization has standard terminology that maps to specific filters \(for example, "Sev1", "VIP", "overdue"\)
-   Users repeatedly ask the same filtered question and the system does not automatically pick up the right filter
-   You want to encode business logic that cannot be inferred from field values alone \(for example, "at-risk accounts" = combination of multiple conditions\)
-   The special terminology of your organization is not translated accurately to filter conditions

**Tip:** The name and description are what AI search matches against. Use natural phrasing your users would say. Keep one segment per concept. Test by asking the question and checking if the segment appears in the logs.

When creating segment names, use the same language a user would use when asking a question. The name is the primary field the LLM matches against during semantic search. Avoid abbreviations, internal codes, or technical jargon. Think about how a user would phrase the question that this segment answers.

## Naming guidelines

Follow these guidelines when creating segment names and descriptions:

-   **Use plain language**

    Write names in the same language users would use when asking questions. Avoid technical abbreviations or internal codes that users would not recognize.

-   **Think like your users**

    Consider how users would phrase questions about this data. The segment name should match their natural language patterns.

-   **Be specific but clear**

    Names should be descriptive enough to distinguish from similar segments while remaining understandable to your audience.

-   **Use descriptions for context**

    When segment names might be ambiguous, use the description field to provide additional context using commonly-used terms.


## Procedure

1.  Navigate to **Query Generation** &gt; **Administration** &gt; **Manual Segment Config**.

2.  Press **New**.

3.  In the Manual Segment Config form, fill in the following information.

    |Field|Description|
    |-----|-----------|
    |Table Name|The table \(entity\) the segment applies to. Must have an active entity in the semantic layer. The system looks for the entity table first, then the segment within that table.|
    |Name|User-friendly name describing the segment in plain language a user would use when asking a question. Use the same language a user would use when asking a question. Avoid abbreviations, internal codes, or technical jargon. Maximum 255 characters. Examples: "Critical Open Incidents" \(good\) instead of "P1\_OPEN\_INC" \(poor\), "Active Benefits HR Cases" \(good\) instead of "HR Cases — Active, Cat=Benefits" \(poor\).|
    |Description|Optional but strongly recommended. Gives the LLM additional context to decide whether a segment is relevant. Use commonly-used terms and explain what the segment captures. Helps disambiguate similar segments. Maximum 4,000 characters. Example: "High priority incidents that are currently open and unresolved. Includes all assignment groups. Useful for executive dashboards and escalation reporting." \(good\) instead of "Filters for priority 1." \(poor\).|
    |Filter|Encoded query defining the segment's filter conditions. Uses the condition builder \(v2\). Maximum 4,000 characters, although filters longer than 2,000 characters may be truncated in the LLM prompt.|
    |Active|Whether the system uses the segment. Defaults to selected. When cleared, the segment is deactivated and excluded from search.|

4.  Press **Submit**.

    A business rule fires asynchronously and syncs the record into the `sn_query_gen_segment` table, which is queried at search time.


## Result

The manual segment is active and available for Query Generation searches.

## Manual segments for the incident table

The following examples show well-crafted manual segments for the `incident` table:

|Name|Description|Table|Filter|
|----|-----------|-----|------|
|Critical Open Incidents|High priority incidents that are currently open and unresolved. Includes all assignment groups.|`incident`|`priority=1^state!=7^state!=8`|
|My Team's Overdue Incidents|Incidents assigned to the current user's group that have passed their SLA due date.|`incident`|`assignment_group=javascript:getMyGroups()^sla_due<javascript:gs.nowDateTime()^state!=7`|
|Recent P1 and P2 Escalations|Priority 1 and 2 incidents escalated in the last 7 days.|`incident`|`priority<=2^escalation=1^sys_updated_on>=javascript:gs.daysAgoStart(7)`|

**Parent Topic:**[Segments in the Query Generation semantic layer](../concept/querygen-segments.md)

**Related topics**  


[Manual segment data model and sync behavior](../concept/manual-segment-data-model-sync.md)

[Shipping manual segments via plugins](../concept/shipping-manual-segments-plugins.md)

[Guidelines for segments](../concept/general-guidelines-segments.md)

[Query Generation properties](../concept/querygen-properties.md)

