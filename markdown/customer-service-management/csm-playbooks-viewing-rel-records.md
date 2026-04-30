---
title: Viewing dynamic related records in the contextual side panel
description: Customer service agents can view dynamic related records in the contextual side panel in CSM Configurable Workspace. This feature displays related records that dynamically change based on the context of the current record or playbook activity.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Playbooks for Customer Service Management, Automate and optimize, Using Customer Service Management, Customer Service Management]
---

# Viewing dynamic related records in the contextual side panel

Customer service agents can view dynamic related records in the contextual side panel in CSM Configurable Workspace. This feature displays related records that dynamically change based on the context of the current record or playbook activity.

Agents can view, search, and sort the records in the Related Records tab in the contextual side panel. These records appear in the Related Records tab as read-only cards.

The Related Records tab displays related records that dynamically change based on the context of the current record or playbook activity. The records that are displayed in the Related Records tab depend on the following settings:

-   The related record contexts and definitions that have been configured for a record or playbook activity.
-   The agent's access permissions to data.

Depending on the related record configuration for the source record or playbook activity, agents can see the following types of related records:

-   SLAs
-   Emails
-   Escalations for the case or customer \(account and contact or consumer\).
-   Blocked By
-   Sold Products
-   Install Base Items
-   Active Contracts
-   Active Entitlements
-   Special Handling Notes
-   Tasks

<table id="table_dyn_rel_records_in_side_panel"><thead><tr><th>

Task

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

View related records in the contextual side panel

</td><td>

Click the Related Records tab \(![Related Records icon.](../image/contextual-side-panel-related-records.jpg)\) to view the Related Records list.

 Related records appear in the list in a card format. The initial set of records displayed in the list is determined by the record type selected in the filter at the top of the list.

</td></tr><tr><td>

Select the type of related record to view

</td><td>

Use the filter at the top of the Related Records list to select the type of related records to view. Agents can also use the filter to see the current selection.

1.  Click the Filter icon \(![Filter icon.](../image/dynamic-related-records-filter-icon.png)\).
2.  Select a record type from the dropdown menu.

 The dropdown menu includes the related lists that have been configured for the parent record.

</td></tr><tr><td>

Search the related records list

</td><td>

Use the search field at the top of the Related Records list to perform a text search. Records that match the search text are highlighted.

1.  Enter the search text in the search field at the top of the Related Records list.
2.  Click the search icon.

 The search field is grayed out if search is not available for the selected type of related records.

</td></tr><tr><td>

Open a related record in a sub-tab

</td><td>

Click a card in the Related Records list to open the record in a sub-tab under the parent record. In the sub-tab, the agent can view the record details and perform available actions.

</td></tr><tr><td>

Open the related record list in a list view in a sub-tab

</td><td>

Click the list view icon \(![List view icon.](../image/dynamic-related-records-list-view-icon.png)\) to display the related records in a list view in a sub-tab under the parent record.

</td></tr><tr><td>

Create a new record for the selected related list

</td><td>

Create a new record for the record type currently selected in the Related Records list. This action opens a new record form in a sub-tab under the parent record.

1.  Click the Create record icon \(![Create record icon.](../image/dynamic-related-records-create-record-icon.png)\) at the top of the Related Records list.
2.  Fill in the fields on the record form and click **Save**.

</td></tr></tbody>
</table>**Related topics**  


[Filter playbook activities](../task/csm-playbook-filter-activities.md)

[Using the activity stream in the contextual side panel](csm-playbooks-using-activity-stream.md)

[Viewing ribbon information in the contextual side panel](csm-playbooks-viewing-ribbon-info.md)

[Add an optional activity](using-customized-playbook-experience-for-customer-service-management.md)

[Summarize a case](case-summarization-in-process-page.md)

[Create a record using a playbook](../task/csm-playbook-create-record.md)

