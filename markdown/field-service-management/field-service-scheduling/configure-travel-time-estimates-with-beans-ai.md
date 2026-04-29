---
title: Configure travel time estimates with a Third-party provider
description: Use a third-party travel estimate provider, such as Beans.ai, to improve the accuracy of travel time estimates in Schedule Optimization.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Travel estimate provider, Create a scheduling attribute, Schedule Optimization, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure travel time estimates with a Third-party provider

Use a third-party travel estimate provider, such as Beans.ai, to improve the accuracy of travel time estimates in Schedule Optimization.

## Before you begin

When configuring Beans.ai, a connection and credential must have been established before starting this procedure. For more information, see [Set up a connection and credential for Beans.ai travel estimate provider](create-a-connection-and-credential-for-beans-ai.md).

Role required: wm\_admin

## About this task

Schedule Optimization supports integration with third-party travel estimate providers to extend mapping capabilities. Beans.ai is one supported provider. To configure any third-party provider, follow the steps in this topic and enter the credentials and API authentication details for your provider.

## Procedure

1.  Navigate to **All** &gt; **Map Integrations for Field Service** &gt; **Travel Time Estimate Configuration**

2.  Select **Create New**.

    **Note:** Beans.ai operates on a bring your own licensing model. If no third-party provider is configured, travel estimates default to straight-line.

3.  On the form, provide a name for the configuration and an optional description.

4.  In the **Select a travel estimate provider** field, select Beans.ai, Straight-line, or New provider to configure a different third-party provider.

5.  Ensure that the travel time estimate is calculated and updated continuously by selecting the **Enable real-time** check box.

6.  Select **Submit**.

7.  Adjust travel for specific times of day by adding travel band modifiers.

    **Note:** Travel bands can vary in duration, ranging from 30 minutes to 4 hours, and can't overlap.

    1.  Select an existing provider record.

    2.  Scroll down to the **Travel Band Modifiers** tab.

    3.  Select **New**.

    4.  On the form, fill in the fields.

<table id="table_eqz_1xv_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to activate the travel band configuration.

</td></tr><tr><td>

Days of week

</td><td>

The days of the week when the travel band modifier is active.

</td></tr><tr><td>

Start time

</td><td>

The beginning time of the travel band or time window during which the modifier applies.

</td></tr><tr><td>

End time

</td><td>

The ending time of the travel band or time window during which the modifier applies.

</td></tr><tr><td>

Multiplier

</td><td>

A numerical factor applied to the base travel time to increase travel time to adjust for predicted higher traffic or other conditions during the specified time range.If the multiplier is greater than 1, it increases travel time. For example, a multiplier of 1.2 increases travel time by 120%.

Use a multiplier less than 1 to decrease travel time for off-peak hours when travel is faster than normal. For example, a multiplier of 0.8 reduces travel time by 80%.

</td></tr><tr><td>

Use map provider time of day

</td><td>

When selected, sends the travel band's day and time window to the map provider to return a travel time estimate based on historical traffic data for that period.

</td></tr></tbody>
</table>    5.  Select **Submit**.

    6.  Select **Update**.


**Related topics**  


[https://support.servicenow.com/kb?sys\_kb\_id=77fb7ba7871736142d5cbbb5cebb35e9&amp;id=kb\_article\_view](https://support.servicenow.com/kb?sys_kb_id=77fb7ba7871736142d5cbbb5cebb35e9&id=kb_article_view)

