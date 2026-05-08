---
title: Edit search resource display field record
description: Use the search result display fields to provide titles, descriptions, and additional details for contextual search results.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Edit search resource display field record

Use the search result display fields to provide titles, descriptions, and additional details for contextual search results.

## Before you begin

Role required: admin

## About this task

ServiceNow provides pre-defined additional resource or search sources to the user. You can't create or delete search result display configurations. Each table referred by an additional resource has a search result display configuration record. You can edit the values in the **Card title field**, **Card description field**, and the **Card additional fields**.

![Search result with card title, card description field, and card additional fields highlighted.](../image/additional-resource-fields.png)

**Note:** Ensure that you select the contextual search property **Shows meta data on form contextual search results** to view **Card additional fields** in the search result.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Search Result Display Configurations**.

2.  Open the search result display configuration record that you want to modify.

    **Note:** Search result display configuration records with the Platform UI type do not affect search for Knowledge articles, Catalog Items, or pinned articles. You can configure settings for platform Knowledge article searches using Knowledge search properties.

3.  In the form, edit the fields.

    |Field|Description|
    |-----|-----------|
    |UI type|\[Read-only\] Interface where the values of the search result display fields should appear. It can appear in platform or workspace.|
    |Table|\[Read-only\] Name of the table in which the values of the search result display fields should appear. For example, if you mention Incident \[incident\] as the table, then the additional resource field values appear in the search result for the Incident \[incident\] table.|
    |Application|\[Read-only\] Application scope of the record. The record is available for all applications or for scoped applications.|
    |Card View|
    |Card icon|\[Workspace\] Icon name displayed on the search result card view.|
    |Card label|\[Workspace\] Label displayed on the search result card view.|
    |Card title field|\[Platform or Workspace\] Field whose value is shown as title in the search result title.|
    |Card additional fields|\[Platform or Workspace\] List of field names displayed on the search result to provide more context to the search result. The card additional fields appear at the bottom of a search result record.|
    |Card description field|\[Platform or Workspace\] Name of the field whose value is shown as the search result description.|
    |Card display updated date|\[Workspace\] Check box to display the latest date on the search result card view.|
    |Details View \(only when the UI type is Workspace\)|
    |Detail title field|Field whose value is shown as title in the search result detail view.|
    |Detail link field|Field used as clickable link on the search result detail view.|
    |Detail additional fields|List of field names displayed on the search result detail view.|
    |Detail show last work note|Check box to display the latest work note on the search result detail view.|

4.  Select **Update**.


**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

