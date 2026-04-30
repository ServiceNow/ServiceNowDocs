---
title: Configure activity patterns for Self-Service Analytics
description: Configure an activity pattern to combine the pattern element, pattern element group, or both for a user entity and link them to an outcome.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Self-Service Analytics, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure activity patterns for Self-Service Analytics

Configure an activity pattern to combine the pattern element, pattern element group, or both for a user entity and link them to an outcome.

## Before you begin

[Configure pattern element groups for Self-Service Analytics](configure-pattern-element-group.md).

Role required: sn\_ssa\_core.self\_service\_manager

## About this task

By default, the system includes activity patterns for the activities Consumer created a case and Customer created a case. These pattern elements are available with the Self-Service Analytics for Customer Service plugin \[com.snc.pa.self\_service\_analytics\_csm\].

## Procedure

1.  Navigate to **All** &gt; **Self-Service Analytics** &gt; **Configuration** &gt; **Activity Pattern**.

2.  Either configure an existing activity pattern for your user entity or create a new one.

    -   Select an existing activity pattern in the Activity Patterns list.
    -   Create a new activity pattern by clicking **New**.
3.  On the Activity Pattern form, verify the default field values for an existing activity pattern or fill in the values for a custom configuration.

<table id="table_omb_d3m_nlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the activity pattern.

</td></tr><tr><td>

Description

</td><td>

Summary of the activity pattern.

</td></tr><tr><td>

Primary Activity

</td><td>

Activity to be tracked in the activity sequence after a pattern matches with an outcome using the pattern recognition. An activity sequence is a stream of activities a user performs.

</td></tr><tr><td>

Outcome

</td><td>

Result of an activity pattern.

</td></tr><tr><td>

Application

</td><td>

Scope of the application that contains the user entity. This field is automatically set based on the application scope selected in the application picker.

</td></tr><tr><td>

Match If

</td><td>

Pattern recognition using the Match If function to associate the pattern with an outcome.For example, you can indicate that if the activity Consumer created a case is not found, you want to match it with the Confirmed Deflection outcome.

</td></tr><tr><td>

Domain

</td><td>

Domain in which the activities records exist.

</td></tr></tbody>
</table>4.  Click **Submit** and then select the newly created activity pattern link from the Activity Patterns list.

5.  In the Elements related list, select elements to map with the primary activity and use the **Order** column to decide the order of each element mapping.

    -   To use an existing element, select an element, modify the fields and click **Update**.
    -   To create another pattern element or pattern element group, click **New** and select the type of element, fill in the fields on the form, and then click **Submit**.
    An element can be a pattern element or pattern element group. For more information, see [Configure pattern elements for Self-Service Analytics](configure-pattern-element.md) and [Configure pattern element groups for Self-Service Analytics](configure-pattern-element-group.md).

    In the **Order** column, the following conditions apply:

    -   If there is only one matching table map, the system uses that map.
    -   If there are multiple matching table maps with the same order, the system uses the map with the older created date.
    -   If there are multiple matching table maps with different orders, the system uses the map with the highest order.
6.  On the Activity Pattern form, click **Update**.


## What to do next

[Set up the deflection configuration for Self-Service Analytics](configure-deflection-ssa.md).

**Parent Topic:**[Configure Self-Service Analytics](config-ssa.md)

