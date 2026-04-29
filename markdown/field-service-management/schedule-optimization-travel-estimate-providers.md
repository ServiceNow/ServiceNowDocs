---
title: Schedule Optimization travel estimate providers
description: Travel estimate providers used by Schedule Optimization.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Field Service Management]
---

# Schedule Optimization travel estimate providers

Travel estimate providers used by Schedule Optimization.

Efficient allocation of work order tasks to agents depends on accurate estimation of travel time, taking into account both the agent's location and the task's location. Schedule Optimization supports two options to calculate distances between agents and task, Straight-line and Beans.AI. An administrator is required to select a travel estimate provider for all qualifier-level groups. See, [Create a scheduling attribute for Schedule Optimization](../task/configure-scheduling-attributes.md) for more information on where the options are located.

## Straight-line

To enter straight-line travel estimate configuration properties, an administrator can navigate to **All** &gt; **Schedule Optimization** &gt; **Configuration** &gt; **Scheduling Attributes** and open the travel estimate configuration record.

In the **General** tab, you can add the speed limit for the region in the speed multiplier field.

In the **Multipliers** tab, the multipliers defined in the straight-line calculation are the values that the estimated straight-line travel time is multiplied by, depending on the time bracket the estimate falls in. If the travel time is less than 15 minutes, multiply by a value greater than 1, to increase the estimated travel time. If the travel time is greater than 15 minutes, multiply by a positive value smaller than 1 to decrease the estimated travel time.

**Note:** Straight-line distance calculation is a fallback logic in case a customer doesn’t want to choose a map provider for travel time estimates.

## Beans.AI

Beans.AI is the map provider that Schedule Optimization supports for travel time estimates.

To create a connection and credential record for Beans.AI, an administrator can navigate to **All** &gt; **IntegrationHub** &gt; **Connection and Credentials** &gt; **Connection and Credentials Aliases**.

Travel estimates are obtained every time Schedule Optimization runs. An administrator can limit the number of locations that are queried from Beans.AI. For example, if optimization runs for two agents and two tasks, a 4x4 matrix is sent to Beans.AI to find the shortest distance to the new location. A 4x4 matrix sends 16 location elements to Beans.AI. If the number of locations queried exceeds the set value, the query defaults to straight-line. To change the maximum number of location points allowed in a provider call, an administrator can navigate to **All** &gt; **Schedule Optimization** &gt; **Configuration** &gt; **** &gt; **Properties** &gt; **** and change the value in the Travel Time Estimates field. The default value is set to 300.

To change the configurations for Beans.AI, an administrator can navigate to **All** &gt; **Map Integrations for Field Service** &gt; **Map Provider Configuration**.

By default, the **Inputs** field is set to Beans.AI. By default **Decision table** is set up as indicated in the table.

|Field|Value|
|-----|-----|
|Request Threshold Limit|5000 \[considering 50 runs a day with 100 groups in each run\]|
|Max Location Element Count|250,000 \[considering 500 x500 matrix support per Map Provider call\]|

**Note:** Straight-line distance calculation is a fallback logic in case a customer doesn’t want to choose a map provider for travel time estimates.

**Parent Topic:**[Field Service Management reference](../../planning-and-policy/reference/fsm-reference.md)

