---
title: Override channel capacity for an agent
description: Change the default number of work items that an agent can handle for a service channel.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Routing work items, Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Override channel capacity for an agent

Change the default number of work items that an agent can handle for a service channel.

## Before you begin

Role required: sn\_wfo\_cfg\_ws.manager

## About this task

By default, the override capacity is valid for 12 hours. Administrator can change the duration using the **sn\_channel\_mgmt.awa\_agent\_temporary\_override\_time.minutes** system property. For information on adding a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US). The capacity resets to the previous value after the specified time. The scheduled job **Reset Temporary Capacity Override** is executed every two minutes to check the invalid or expired overridden capacity and resets to the previous value.

**Note:** You can override the channel capacity for a single agent at a time. Ensure that an agent to whom you want to override the channel capacity needs to be associated with Advanced Work Assignment and the required channels.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Manager Workspace**.

2.  Navigate to an agent's profile.

<table id="choicetable_yv3_zcw_knb"><thead><tr><th align="left" id="d221462e87">

To set the override capacity

</th><th align="left" id="d221462e90">

Do this

</th></tr></thead><tbody><tr><td id="d221462e96">

**From Channels**

</td><td>

1.  Click the Channels icon.
2.  Click the **All Agents** tab.
3.  Click an agent's record.


</td></tr><tr><td id="d221462e120">

**From Teams**

</td><td>

1.  Click the Teams icon.
2.  Click the KPI group.
3.  Select **Group Members** tab.
4.  Click an agent's record.


</td></tr></tbody>
</table>3.  Click the **Overview** tab.

4.  In the **Channels** section, select the service channel for which you want to override the capacity.

5.  Click **Capacity Override**.

    The **Agent Capacity Override** page appears.

6.  In the **Override Capacity** field, enter the new capacity.

7.  Click **Apply**.


## Result

A message appears indicating the capacity update is valid for the defined duration. The capacity resets to the previous value after the specified time.

**Parent Topic:**[Routing work items using Channels in Workforce Optimization for ITSM](../concept/configurable-channels-workforce-optimization-itsm.md)

