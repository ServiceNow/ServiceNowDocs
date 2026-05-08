---
title: Set the number of list collector items visible in the available column
description: You can modify the glide.xmlhttp.excessive property to change the number of items that appear in the Available column of the list collector.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure items on forms or in lists using a list collector, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Set the number of list collector items visible in the available column

You can modify the **glide.xmlhttp.excessive** property to change the number of items that appear in the **Available** column of the list collector.

## Before you begin

Role required: admin

## Procedure

1.  Add the property to the System Properties \[sys\_properties\] table.

2.  Change the **Type** to **Integer**.

3.  Enter a number in the **Value** field.

    **Warning:** The default value is 100. Selecting a number significantly higher than 100 can lead to performance issues on your instance as the data is loaded into the list collector.

4.  Save the property.


**Parent Topic:**[Configure items on forms or in lists using a list collector](t_UseSlushbuckets.md)

**Related topics**  


[bundle-platadm.t_AddAPropertyUsingSysPropsList]

