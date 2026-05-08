---
title: Accept or reject a major incident candidate
description: When an incident is proposed as a major incident candidate, a major incident manager can accept or reject the candidate. The manager accepts a candidate as a major incident if the incident requires accelerated resolution.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working on major incident management, Managing major incidents, Incident Management, IT Service Management]
---

# Accept or reject a major incident candidate

When an incident is proposed as a major incident candidate, a major incident manager can accept or reject the candidate. The manager accepts a candidate as a major incident if the incident requires accelerated resolution.

## Before you begin

Role required: major\_incident\_manager

## Procedure

1.  Perform any of the following actions.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

<table id="choicetable_r21_xbw_3db"><thead><tr><th align="left" id="d168686e78">

Option

</th><th align="left" id="d168686e81">

Description

</th></tr></thead><tbody><tr><td id="d168686e87">

**Accept a major incident candidate**

</td><td>

1.  Navigate to **Incident** &gt; **Major Incidents** &gt; **Candidates** and open the candidate to be approved.
2.  Click the additional actions icon ![Additional actions icon](../image/context-menu.png) and select **Promote to Major Incident**.
 **Note:**

-   While promoting the candidate, the major incident manager is prompted to enter work notes and business impact.
-   The incident is promoted to a major incident, and the **Major incident state** field under the Major incident section is changed from **Proposed** to **Accepted**.
-   The incident is assigned to the user who approves the major incident.


</td></tr><tr><td id="d168686e148">

**Reject a major incident candidate**

</td><td>

1.  Navigate to **Incident** &gt; **Major Incidents** &gt; **Candidates** and open the candidate to be rejected.
2.  Click the additional actions menu icon ![Additional actions menu icon](../image/context-menu.png) and select **Reject Major Incident Candidate**.
 **Note:**

-   While rejecting the candidate, the major incident manager is prompted to enter the reason for rejecting the candidate. A notification is sent to the user in the **Assigned to** field.
-   The state of the incident remains the same while the **Major incident state** field is changed to **Rejected**.


</td></tr></tbody>
</table>
**Parent Topic:**[Working on major incident management](../concept/work-on-mim.md)

