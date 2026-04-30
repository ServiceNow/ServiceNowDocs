---
title: Enable connected content autosync system property
description: Content updates are automatically synced when you enable the autosync system property.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage connected content from topic pages, Taxonomy and connected content, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Enable connected content autosync system property

Content updates are automatically synced when you enable the autosync system property.

## Before you begin

Role required: admin

## About this task

By enabling this property, you can gain visibility into new and outdated content and manage content life cycle through automation for performance improvement.

**Note:** The connected content autosync system property is available from Zurich and above.

-   Auto-sync content additions and removals on topic pages in bulk.
-   Eliminate the need to manually update the content additions and deletions. For more information, see [Run the scheduled job for content association](schduld-job-link-cntnt.md).

## Procedure

1.  In the Navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Search for the `Taxonomy.category.content_auto_sync` property and open.

3.  Set the property value to **true**.

    **Note:** Default value is **false**.


## Result

The system property syncs updates automatically.

However, to check the updated content in categories manually, see [Check for updated content in categories](may-associate-updated-content-categories-topics.md).

**Parent Topic:**[Manage connected content from topic pages](mnge-content-topics.md)

