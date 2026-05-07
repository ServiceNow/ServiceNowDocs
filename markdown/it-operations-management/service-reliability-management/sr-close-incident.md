---
title: Close an SRM incident
description: Close an incident when it’s not an issue or has already been handled.REVISE FOR SRM
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with incidents in SRM, Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Close an SRM incident

Close an incident when it’s not an issue or has already been handled.

## Before you begin

Role required: srm\_responder, srm\_manager, or srm\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select **Reliability tasks** \(![Reliability tasks icon](../image/icon-sr-reliability-tasks.png)\).

3.  You have two options.

<table id="choicetable_llb_1fq_vyb"><thead><tr><th align="left" id="d601188e97">

Option

</th><th align="left" id="d601188e100">

Steps

</th></tr></thead><tbody><tr><td id="d601188e106">

**In the incident list view**

</td><td>

1.  Double-click the **State** field \(or use the keyboard shortcut\) for the incident and select from the list menu.
2.  Select **OK**.
 **Tip:** If you have the srm\_admin role, you can update multiple incidents at once. First, select the relevant incidents and select **Edit**. Then use the **State** drop-down to choose the appropriate value and select **Update**.

</td></tr><tr><td id="d601188e142">

**In the incident form**

</td><td>

1.  Select a new **State** field value from the list menu.
2.  Select **Save**.


</td></tr></tbody>
</table>    For value choices, see [SRM incidents](../reference/sr-incidents-workspace.md).

    The new state is displayed in the incident list view, incident form, and form header.


## Result

Closed incidents remain in the incidents list view. If they don't appear, try adjusting your filters.

**Note:**

When you close an incident, any related alerts are closed.

**Parent Topic:**[Working with incidents in SRM](../concept/sr-work-incidents.md)

