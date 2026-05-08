---
title: Reassign an SRM incident
description: Reassign an incident to a responder when the incident tasks should be addressed by a particular team member.
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with incidents in SRM, Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Reassign an SRM incident

Reassign an incident to a responder when the incident tasks should be addressed by a particular team member.

## Before you begin

This action is available when the **Assigned to** field in the incident is populated.

Role required: srm\_manager, srm\_responder, or srm\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select **Reliability tasks** \(![Reliability tasks icon](../image/icon-sr-reliability-tasks.png)\).

3.  Select the **Incidents** tab.

4.  You have two options.

<table id="choicetable_llb_1fq_vyb"><tbody><tr><td id="d374512e110">

**Option**

</td><td>

Description

</td></tr><tr><td id="d374512e119">

**In the incident list view**

</td><td>

Double-click the **Assigned to** field for the incident and replace the team member from the list menu.

</td></tr><tr><td id="d374512e131">

**In the __Details__ tab of incident form**

</td><td>

Delete the name in the **Assigned to** field and reassign. Select **Save**.

</td></tr></tbody>
</table>    The incident is now assigned to the new responder and an email notification sent. The assignee is displayed in the list view and on the form.


**Parent Topic:**[Working with incidents in SRM](../concept/sr-work-incidents.md)

