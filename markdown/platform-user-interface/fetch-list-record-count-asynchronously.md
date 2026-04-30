---
title: Fetch your list record count asynchronously
description: Users with large lists created from large tables can use the glide.ui.fetch.list.record.count.asynchronously property to continue interacting with their list, while the total record count loads.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Administering lists for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Fetch your list record count asynchronously

Users with large lists created from large tables can use the `glide.ui.fetch.list.record.count.asynchronously` property to continue interacting with their list, while the total record count loads.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_vcf_bw2_35b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of your system property as `glide.ui.fetch.list.record.count.asynchronously`.

</td></tr><tr><td>

Description

</td><td>

Type a brief, descriptive phrase describing the function of the property.

</td></tr><tr><td>

Choices

</td><td>

Comma-separated values for a choice list. If you need a different choice list label and value, use an equal sign \(=\) to separate the label from the value. For example, Blue=0000FF, Red=FF0000, Green=00FF00 displays Blue, Red, and Green in the list, and saves the corresponding hex value in the property value field.

</td></tr><tr><td>

Type

</td><td>

true I false

</td></tr><tr><td>

Value

</td><td>

Set the desired value for property.-   **True** to enable this feature.
-   **False** to disable this feature.


</td></tr><tr><td>

Ignore cache

</td><td>

The system stores system property values in server-side caches to avoid querying the database for configuration settings. When you change a system property value, the system always flushes the cache for the sys\_properties table. Use this field to determine whether to flush this property's value from all other server-side caches.

 The default value of false causes the system to not ignore flushing caches, which results in flushing all server-side caches and retrieving the current property value from the database. Set this field to false when you want to ensure all caches have the current property value. The true value causes the system to ignore flushing some server-side caches, which results in only flushing the cache for the sys\_properties table and preserving the prior property value in all other caches. Set this field to true to avoid the performance cost of flushing all caches and retrieving new property values. Typically, you should only set this field to true when you have a system property that changes more frequently than once a month, and the property value is only stored in sys\_properties table.

</td></tr><tr><td>

Private

</td><td>

Set this property to true to exclude this property from being imported via update sets. Keeping system properties private prevents settings in one instance from overwriting values in another instance. For example, you may not want a system property in a development instance to use the same value as a production instance.

</td></tr><tr><td>

Read roles

</td><td>

Define the roles that have read access to this property.

</td></tr><tr><td>

Write roles

</td><td>

Define the roles that have write access to this property.

</td></tr><tr><td>

Application

</td><td>

The scope of the feature is enabled **Global** by default.

</td></tr></tbody>
</table>4.  Select **Update**.

    The property is now active and the list loads asynchronously.


