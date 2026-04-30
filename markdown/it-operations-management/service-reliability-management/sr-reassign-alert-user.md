---
title: Reassign an SRM alert
description: Reassign an alert to a responder when the alert task should be addressed by a particular user.REVISE FOR SRM
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with alerts in SRM, Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Reassign an SRM alert

Reassign an alert to a responder when the alert task should be addressed by a particular user.

## Before you begin

This action is available when the **Assigned to** field in the alert is populated.

Role required: Responder, Manager, or Administrator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  From the left navigation pane, select the reliability tasks icon \(![Reliability tasks icon](../image/icon-sr-reliability-tasks.png)\).

3.  You have two options.

<table id="choicetable_llb_1fq_vyb"><tbody><tr><td id="d470328e100">

**Option**

</td><td>

Description

</td></tr><tr><td id="d470328e109">

**In the alert list view**

</td><td>

Select one or more alerts using the check box to the left of the alert, and select**Edit** in the list view header.Scroll down to the value you want to edit.

If the alert has not been acknowledged, acknowledge it first, and reassign.

Select **Update**.

**Note:** If you bulk select alerts, the change applies to all the alerts selected. For assignments, team members are notified according to their notification preferences.

</td></tr><tr><td id="d470328e132">

**In the alert form**

</td><td>

If the alert has not been acknowledged, acknowledge it first, and then delete the name in the **Assigned to** field and reassign. Select **Save**.

</td></tr></tbody>
</table>    The alert is now assigned to the new responder and an email notification sent. The assignee is displayed in the list view and on the form.


**Parent Topic:**[Working with alerts in SRM](../concept/sr-work-alerts.md)

