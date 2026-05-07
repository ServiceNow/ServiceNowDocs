---
title: Create a major incident
description: Create a major incident directly or review the candidates and promote the candidates to major incidents.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working on major incident management, Managing major incidents, Incident Management, IT Service Management]
---

# Create a major incident

Create a major incident directly or review the candidates and promote the candidates to major incidents.

## Before you begin

Role required: major\_incident\_manager

## Procedure

1.  Perform any of the following actions.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

<table id="choicetable_mzp_swn_gdb"><thead><tr><th align="left" id="d208182e78">

Option

</th><th align="left" id="d208182e81">

Description

</th></tr></thead><tbody><tr><td id="d208182e87">

**Promote an incident to a major incident manually**

</td><td>

On the context menu, click **Promote to Major Incident**. The incident directly becomes a major incident.**Note:**

-   Only a major incident manager can promote an incident to a major incident. If an incident is in the resolved, closed, or canceled state, the **Promote to Major Incident** option does not appear on the context menu.
-   When an incident is promoted to a major incident, the incident itself is considered as a major incident and no new incident is created.

To get this behavior, you need to set the major incident management property **Create major incident from candidate – A new incident is created from a candidate as a major incident. The candidate is associated with the new incident as a child.** \(**sn\_major\_inc\_mgmt.com.snc.incident.mim.major\_incident\_creation**\) to **Promote candidate to a major incident**.

</td></tr><tr><td id="d208182e125">

**Create a major incident from application navigation**

</td><td>

1.  Click **Incident** &gt; **Major Incidents** &gt; **Create Major Incident**.
2.  Fill in the fields and click **Submit**.


</td></tr></tbody>
</table>
**Parent Topic:**[Working on major incident management](../concept/work-on-mim.md)

