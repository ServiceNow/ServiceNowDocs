---
title: General guidelines for optimizing your clone duration
description: A reference topic that includes general guidelines to optimize your clone duration when requesting a clone.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-09-29"
reading_time_minutes: 1
breadcrumb: [Reference, Instance Clone, Configure core features, Administer]
---

# General guidelines for optimizing your clone duration

A reference topic that includes general guidelines to optimize your clone duration when requesting a clone.

Configuring additional settings for your clone request can significantly increase your clone completion time.

When creating a clone request, consider the following guidelines.

-   Set the amount of data copied from the task table to `Full`. This option clones all data from the task table and its child tables to the target instance.

    **Note:** The `Last 90 days` option can increase duration, as it takes longer to remove records from the task table that are older than 90 days after restoration.

-   Selecting Exclude Attachment Data on the clone request form can add to your clone duration.
-   Don't preserve large amounts of data in your request. If you must preserve table data, such as users, groups, and roles, consider exporting the records to a file and importing them after cloning.
-   Add conditions to the preservers configured for the clone request to only preserve the data that you need.
-   Use clone chaining to split up your request, see [Clone terminology](clone-terminology.md).

**Parent Topic:**[Instance Clone reference](instance-clone-reference.md)

