---
title: Reopen an SRM incident
description: Reopen a closed incident if you think the issue is not yet resolved.
locale: en-US
release: australia
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with incidents in SRM, Working with SRM reliability tasks, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Reopen an SRM incident

Reopen a closed incident if you think the issue is not yet resolved.

## Before you begin

Role required: srm\_manager, srm\_responder, or srm\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select **Reliability tasks** \(![Reliability tasks icon](../image/icon-sr-reliability-tasks.png)\).

3.  Find and open the incident you want to reopen.

    Check your filters if you don't see them.

4.  You have two options.

<table id="choicetable_llb_1fq_vyb"><thead><tr><th align="left" id="d317225e104">

Option

</th><th align="left" id="d317225e107">

Steps

</th></tr></thead><tbody><tr><td id="d317225e113">

**In the incident list view**

</td><td>

1.  Double-click the **State** field \(or use the keyboard shortcut\) for the incident and select from the list menu.
2.  Select **OK**.
 **Tip:** If you have the srm\_admin role, you can update multiple incidents at once. First, select the relevant incidents and select **Edit**. Then use the **State** drop-down to choose the appropriate value and select **Update**.

</td></tr><tr><td id="d317225e149">

**In the incident form**

</td><td>

1.  Select a new **State** field value from the list menu.
2.  Select **Save**.


</td></tr></tbody>
</table>    For value choices, see [SRM incidents](../reference/sr-incidents-workspace.md).

    The new state is displayed in the incident list view, incident form, and form header.


**Parent Topic:**[Working with incidents in SRM](../concept/sr-work-incidents.md)

