---
title: Manual segment data model and sync behavior
description: Manual segments use a two-table data model with automatic synchronization between the configuration table and the runtime table used for search operations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-16"
reading_time_minutes: 3
keywords: [manual segments, data model, sync behavior, query generation, semantic layer]
breadcrumb: [Segments, Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Manual segment data model and sync behavior

Manual segments use a two-table data model with automatic synchronization between the configuration table and the runtime table used for search operations.

## Data model overview

Manual segments use a two-table architecture that separates configuration from runtime data. This design ensures that the configuration table remains the single source of truth while the runtime table is optimized for search performance.

-   **configuration table: `sn_query_gen_segment_table_config`**

    This is where you define manual segments. Each record represents one segment configuration that administrators create and maintain.

-   **Synced table: `sn_query_gen_segment`**

    You do not write to this table directly. When a manual segment config is created or updated, a business rule automatically syncs it into this table, which is queried at search time.


## Configuration table fields

The `sn_query_gen_segment_table_`configuration table contains the following fields for defining manual segments:

|Field|Column Name|Max Length|Required|Purpose|
|-----|-----------|----------|--------|-------|
|Table Name|**table\_name**|—|Yes|The table \(entity\) the segment applies to. Must have an active entity in the semantic layer.|
|Name|**name**|255 chars|Yes|User-friendly name that the LLM matches against during semantic search.|
|Description|**description**|4,000 chars|No|Optional clarification using commonly-used terms. Helps the LLM understand when to apply the segment.|
|Filter|**filter**|4,000 chars|Yes|Encoded query defining the segment's filter conditions. Uses the condition builder \(v2\).|
|Active|**active**|—|No|Defaults to **true**. When **false**, the segment is deactivated and excluded from search.|

## Synced table fields

The `sn_query_gen_segment` table contains the runtime data used for search operations:

|Field|Source|
|-----|------|
|**name**|Copied from manual segment config|
|**description**|Copied from manual segment config|
|**filter**|Copied from manual segment config|
|**table**|From **table\_name**|
|**entity**|Resolved reference to `sn_query_gen_entity`|
|**source\_table**|Always `sn_query_gen_segment_table_config`|
|**source\_id**|Sys\_id of the manual segment config record|
|**active**|`manual_segment.active AND entity.active`|

## Sync behavior

Manual segments are synced automatically between the configuration and runtime tables. You do not need to trigger synchronization manually.

|Trigger|When|What Happens|
|-------|----|------------|
|Business rule on config|Insert or update on `sn_query_gen_segment_table_config`|Syncs the individual record into `sn_query_gen_segment` \(async\)|
|Entity insert/update|When an entity is created or updated with **active=true**|Re-syncs all segments \(including manual\) for that entity|
|Weekly scheduled job|Saturdays at midnight|Full sync of all 6 segment sources; cleanup of orphaned records|

During sync, a manual segment is eligible if:

1.  **active = true** on the config record
2.  The referenced table has an active entity in `sn_query_gen_entity`

If either condition is not met, the synced segment is deactivated \(not deleted\).

## Activation and deactivation

A synced segment's active status is: `manual_segment.active AND entity.active`.

|Event|Result|
|-----|------|
|Manual segment config **active** → **false**|Synced segment deactivated|
|Manual segment config **active** → **true**|Synced segment reactivated \(if entity is also active\)|
|Entity **active** → **false**|All segments for that entity deactivated|
|Manual segment config deleted|Synced segment deleted|
|Entity deleted|Orphaned segments cleaned up by scheduled job|

Deactivated segments are excluded from search results.

## ACL protections

The synced segment table has strict ACLs so that the configuration table remains the single source of truth:

-   **Create:** Blocked \(**admin\_overrides = false**\) — segments can only be created via sync
-   **Write to __name__:** Blocked — must be changed on the config record
-   **Write to __description__:** Blocked — must be changed on the config record

## Filter length considerations

While the **filter** field supports up to 4,000 characters, the system property **sn\_query\_gen.segments.max\_filter\_length** defaults to 2,000. Filters longer than this threshold are truncated when included in the LLM prompt.

**Tip:** Keep filters concise for best results. Consider splitting complex segments into multiple focused segments instead of creating one segment with many conditions.

## Domain separation

Manual segments support domain separation. When creating a segment config record with a specific **sys\_domain**, the synced segment inherits that domain. At search time, segments are filtered by the user's domain context.

If domain separation is not enabled on your instance, this field is inactive and can be ignored.

**Parent Topic:**[Segments in the Query Generation semantic layer](querygen-segments.md)

**Related topics**  


[Create a manual segment](../task/querygen-create-segment-manually.md)

[Guidelines for segments](general-guidelines-segments.md)

[Query Generation properties](querygen-properties.md)

