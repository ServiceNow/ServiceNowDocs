---
title: Close multiple security incidents
description: Close multiple security incidents at the same time to avoid having to close related incidents individually, such as incidents created with a common root cause or false positive incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-06-23"
reading_time_minutes: 2
breadcrumb: [List view in SIR Workspace, Explore, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Close multiple security incidents

Close multiple security incidents at the same time to avoid having to close related incidents individually, such as incidents created with a common root cause or false positive incidents.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select the Security Incidents icon ![](../image/listview-icon.png).

3.  In the **Lists** tab, select **Security Incidents** &gt; **All Open**.

4.  Select one or more security incidents to close and select **Close**.

    The Bulk Close the security incidents window displays links to access lists of the security incidents selected to be closed.

    -   If at least one selected security incident has pending activities such as active tasks, playbooks, child SIs, assessments, or active flows, the **Security incidents with active tasks, playbooks, child SIs, assessments and active flows** link is displayed.
    -   If at least one security incident selected for closing has no pending closing activities, the **Security incidents ready to be closed** link is displayed.
    ![Close multiple security incidents](../image/bulk-closure-sir.png)

    Any active pending active tasks, playbooks, child SIs, assessments, and active flows will automatically be closed when you proceed with the bulk closure.

5.  If you're not sure whether active items for incidents should be closed, review the security incidents with active items.

    1.  Select the **Security incidents with active tasks, playbooks, child SIs, assessments and active flows** link.

    2.  Open the security incident you want to review.

    3.  If any changes are necessary, make them and select **Save**.

    4.  Close the incident tab.

    5.  Select **Take me back**.

6.  Select **next**.

7.  In the **Close Code** field, select the applicable close code.

    The available close codes are:

    -   Investigation completed
    -   Threat mitigated
    -   Patched vulnerability
    -   Invalid vulnerability
    -   Not resolved
    -   False positive
8.  In the **Close notes** field, enter any notes.

9.  Select **Bulk Close**.


## Result

The incident closing activity runs in the background.

**Parent Topic:**[List view in SIR Workspace](../concept/setting-up-list-view-in-analyst-workspace.md)

**Related topics**  


[Personalize a list](../concept/personalize-a-list.md)

[Apply quick filters on Security Incidents and Response Tasks lists](../concept/use-quick-filters-for-security-incidents.md)

[Assign Security Incidents](../concept/assign-security-incident.md)

[Assign Response Tasks](assign_response_tasks.md)

[Report Phish Email](report-phish-email.md)

[Working with quick filters](../concept/configure-quick-filters.md)

[Export Security Incidents or Response Tasks](../concept/export-security-incidents-or-response-tasks.md)

[Manage Shift Handover records](../concept/manage-shift-handover-records.md)

