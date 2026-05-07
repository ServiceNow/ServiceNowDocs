---
title: Create a major incident candidate
description: You can create a major incident candidate in multiple ways. After a major incident candidate is created, the major incident manager evaluates the candidate and decides whether the candidate should be promoted to a major incident.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working on major incident management, Managing major incidents, Incident Management, IT Service Management]
---

# Create a major incident candidate

You can create a major incident candidate in multiple ways. After a major incident candidate is created, the major incident manager evaluates the candidate and decides whether the candidate should be promoted to a major incident.

## Before you begin

Role required: itil, sn\_incident\_write, or admin

## About this task

A major incident manager can accept or reject a major incident candidate.

## Procedure

1.  Perform any of the following actions.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

<table id="choicetable_fk2_2xn_gdb"><thead><tr><th align="left" id="d329101e84">

Option

</th><th align="left" id="d329101e87">

Description

</th></tr></thead><tbody><tr><td id="d329101e93">

**Create major incident trigger rules**

</td><td>

An incident can be marked as a major incident candidate based on the major incident trigger rules. A major incident manager or an incident manager can [Create trigger rules for major incidents](major-incident-trigger-rules.md) to identify major incident candidates automatically.**Note:** The base system major incident trigger rules are disabled by default. A major incident manager or an incident manager needs to activate the trigger rules that define conditions under which an incident is automatically considered as a major incident candidate.

</td></tr><tr><td id="d329101e113">

**Propose an incident as a major incident candidate manually**

</td><td>

Manually propose an existing incident to be a major incident candidate by clicking **Propose Major Incident** from the context menu. You are prompted to enter the reason for proposing the incident as a candidate, and specifying the business impact of the incident. **Note:** If an incident is in the resolved, closed, or canceled state, the **Propose Major Incident** option does not appear on the context menu.

</td></tr><tr><td id="d329101e134">

**Create a candidate from application navigation**

</td><td>

1.  Create a new major incident candidate by clicking **Incident** &gt; **Major Incidents** &gt; **Create Major Incident Candidate**.
2.  Fill in the fields and click **Submit**.


</td></tr></tbody>
</table>    **Note:**

    -   When an incident is proposed as a major incident candidate, the Major incident **State** field in the incident form under the Major incident section is set to **Proposed**.
    -   When you create a new major incident from a candidate, a new incident is created and becomes the major incident. The candidate is added as the child of the major incident. To get this behavior, the incident manager needs to set the major incident management property **Create major incident from candidate** \(**sn\_major\_inc\_mgmt.com.snc.incident.mim.major\_incident\_creation**\). A new incident is created from a candidate as a major incident. The candidate is associated with the new incident as a child.
    -   System automatically assigns the newly created parent major incident to a user when the On-Call Scheduling plugin \(com.snc.on\_call\_rotation\) is activated, a shift is defined for the major incident management group, and a user is available for the on-call shift. If no on-call shift exists, the major incident manager decides the user for the **Assigned to** field.

**Parent Topic:**[Working on major incident management](../concept/work-on-mim.md)

