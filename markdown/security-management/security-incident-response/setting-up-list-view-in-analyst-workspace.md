---
title: List view in SIR Workspace
description: The list view consists of the security incidents, response tasks, phishing emails, and assessments.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Explore, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# List view in SIR Workspace

The list view consists of the security incidents, response tasks, phishing emails, and assessments.

The list view has pre applied filters such as Assigned to Me, Assigned to Team, Unassigned, All Open, All, and so on.

Using these list categories and filtered lists, analysts can quickly find the required Security Incidents and Response Tasks records that they need to work on.

To get to the list view, you need to click the list icon \(![list view icon](../image/listview-icon.png)\). When you click a record in a list view, the record opens in a new tab.

## List types

The following gives you an example view of the lists.

![Landing page list view](../image/landing-page-list-view.png)

The list pane contains the following sections:

<table id="table_gkm_1lr_55b"><thead><tr><th>

List item

</th><th>

Description

</th><th>

Capability

</th></tr></thead><tbody><tr><td>

Security Incidents

</td><td>

View the list of security incidents and navigate to the desired incident to start working on them. The following lists are available:-   **Visible to Me**: Security incidents that are visible to the logged in user.
-   **Assigned to Me**: Security incidents that are assigned to the analyst.
-   **Assigned to the Team**: Security incidents that are assigned to all the teams that the analysts belongs to.
-   **Unassigned**: List of unassigned security incidents.
-   **All Open**: List of all open security incidents.
-   **All**: List of all security incidents.

</td><td>

-   On the List view, the Analyst can configure the list of columns by clicking on the gear icon which is available above the incident columns.
-   The analyst can select one or more security incident\(s\) and assign those incidents to the other users.
-   The analyst can delete the security incidents.
-   The analyst can create a new security incident.
-   The analyst can apply the quick filters. Apply the filters by clicking on the **Quick Filters** option instead of using the advance **Filter** option. Using the quick filters, you can quickly filter the list of security incidents that needs immediate attention. For more information, see [Working with quick filters](configure-quick-filters.md).
-   The analysts can refresh the list of incidents.
-   The analyst can export the list view to Excel, CSV, JSON, and PDF formats.

</td></tr><tr><td>

Shift Handover Records

</td><td>

View the list of Shift Handover records. The following lists are available:-   **Assigned to the Team**: Shift Handover records that are assigned to all the teams/user groups that the analysts belongs to.
-   **All**: List of all security incidents.

</td><td>

Shift Handover supports the following three roles:-   Admin: Shift owner role
-   Security Analyst: Shift analyst role
-   Security Manager: Shift owner role, but doesn't have access to user group to which the Shift Handover record is assigned to.

-   The users with the Shift Owner/Analyst role who are part of the user group in the active shift can add or modify content in the shift handover records in the draft state.
-   The users who don't have the Shift owner/analyst role or are not part of the user group in the active shift can only view the content in the Shift Handover records.

</td></tr><tr><td>

Response Tasks

</td><td>

View the list of response tasks and navigate to the desired response task to start working on them. The list view contains:-   **Assigned to Me**: Response tasks that are assigned to the analyst.
-   **Assigned to the Team**: Response tasks that are assigned to the teams to the analysts belongs to.
-   **Unassigned**: List of unassigned response tasks.
-   **All Open**: List of all open response tasks.
-   **All**: List of all response tasks.

</td><td>

-   On the List view, the Analyst can configure the list of columns by clicking on the gear icon which is available above the incident columns.
-   The analyst can select one or more response task\(s\) and assign those tasks to other users.
-   The analyst can create a new response task.
-   The analyst can apply the quick filters. Apply the filters by clicking on the **Quick Filters** option instead of using the advance **Filter** option. Using the quick filters, you can quickly filter the list of response tasks that needs immediate attention.
-   The analysts can refresh the list of response tasks.
-   The analyst can export the list view to Excel, CSV, JSON, and PDF formats. For more information, see [Export Security Incidents or Response Tasks](export-security-incidents-or-response-tasks.md).

</td></tr><tr><td>

Phishing Emails

</td><td>

View the list of all Phishing emails. The list view will be sorted based on the last update.

</td><td>

-   Report Phishing Email. For more information, see [Report Phish Email](../task/report-phish-email.md) on how to report a phishing email.
-   Delete phishing emails.
-   Export the phishing emails list view to Excel, CSV, JSON, and PDF formats.

</td></tr><tr><td>

Assessments

</td><td>

View the list of assessments needed to perform post incident review.-   **My pending Assessments**: List of pending assessments.
-   **My All Assessments**: List of all assessments.

</td><td>

Take assessments.

</td></tr></tbody>
</table>-   **[Personalize a list](personalize-a-list.md)**  
Security analysts or managers can personalize the security incidents or response tasks or phishing emails custom list view based on their individual preferences.
-   **[Apply quick filters on Security Incidents and Response Tasks lists](use-quick-filters-for-security-incidents.md)**  
Apply the predefined quick filters on Security Incidents and Response Tasks lists to get the desired work items.
-   **[Assign Security Incidents](assign-security-incident.md)**  
Assign security incidents.
-   **[Close multiple security incidents](../task/close-multiple-incidents-sir.md)**  
Close multiple security incidents at the same time to avoid having to close related incidents individually, such as incidents created with a common root cause or false positive incidents.
-   **[Assign Response Tasks](../task/assign_response_tasks.md)**  
Assign Response tasks for a security issue.
-   **[Report Phish Email](../task/report-phish-email.md)**  
Report phishing emails from the lists view.
-   **[Working with quick filters](configure-quick-filters.md)**  
Quick filters are easily accessible filters that are available on, security incidents and response tasks lists.
-   **[Export Security Incidents or Response Tasks](export-security-incidents-or-response-tasks.md)**  
Export the security incidents or response tasks from the list view.
-   **[Manage Shift Handover records](manage-shift-handover-records.md)**  
Use the Shift Handover records list view to create, edit, copy, or delete Shift Handover records. Each Shift Handover record is associated with a Shift Handover Report Template.

**Parent Topic:**[Exploring SIR Workspace](../reference/exploring-security-incident-response-workspace.md)

**Related topics**  


[SIR Workspace plugins](../reference/components-installed-with-analyst-workspace.md)

[SIR Workspace features](../reference/key-features.md)

[SIR Workspace interface overview](../reference/overview.md)

[Upcoming section](../task/upcoming-section.md)

[Quick links section](quick-links.md)

[Shift Handover Records section](shift-handover-records-section.md)

