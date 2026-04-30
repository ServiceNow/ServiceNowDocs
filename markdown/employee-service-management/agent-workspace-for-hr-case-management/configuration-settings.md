---
title: Page Configurations reference
description: A description of the page configuration settings in Agent Workspace for HR Case Management.
locale: en-US
release: yokohama
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Agent Workspace for HR Case Management reference, Agent Workspace for HR Case Management \(Configurable\), HR Service Delivery, Employee Service Management]
---

# Page Configurations reference

A description of the page configuration settings in Agent Workspace for HR Case Management.

<table id="table_gkz_3fz_jzb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

**Record**

</td></tr><tr><td>

Minimum input for adhoc approval user search

</td><td>

Minimum number of alphanumeric values required to initiate a search in the **Add an approval** pop-up.

</td></tr><tr><td>

Timeline for ER cases

</td><td>

Option to configure the display of case timeline on record page. ER \(Employee Relations\) agents use case timelines to track ER cases.To preview your configured setting before applying it on the case, select **Preview**.

</td></tr><tr><td>

Case tab title field

</td><td>

Tab title displayed for each HR case.**Note:** If the **Case tab title field** isn’t specified, the sn\_hr\_core\_case property is applied for all associated extensions.

To preview your configured setting before applying it on the case, click **Preview**.

</td></tr><tr><td>

Playbook card configuration

</td><td>

Toggle to determine the playbook card configuration table depending on versions installed.To preview your configured setting before applying it on the case, select **Preview**.

</td></tr><tr><td>

Manager email template ID

</td><td>

Sys\_id of the email template displayed, when the manager's email ID is selected from the manager name's pop over in the **At a Glance** sidebar.

</td></tr><tr><td>

Copy case attributes

</td><td>

Option to edit attributes that are auto- populated when copying a case.

</td></tr><tr><td class="sub-head" colspan="2">

Contextual side panel

</td></tr><tr><td>

Sidebar tabs visibility

</td><td>

List of tables associated with the sidebar tabs in [Contextual Side Panel](../concept/agent-ws-hr-case-mgmt-context-sidebar.md). To hide a sidebar tab from the Contextual Side Panel, remove its corresponding table entry from JSON file.

</td></tr><tr><td class="sub-head" colspan="2">

At a glance

</td></tr><tr><td>

Cases limit

</td><td>

Maximum number of recent cases displayed in the **At a Glance** panel.To preview your configured setting before applying it on the case form, select **Preview**.

</td></tr><tr><td>

Manager fields for pop over

</td><td>

Fields displayed in the pop over when the manager's name is selected from the **At a Glance** sidebar.To preview your configured setting before applying it on the case form, click **Preview**.

</td></tr><tr><td>

User field

</td><td>

Field-value pairs that determine what user is displayed in the **At a Glance** panel.To preview your configured setting before applying it on the case form, select **Preview**.

</td></tr><tr><td>

Update employee info

</td><td>

Option to navigate to configure settings in HR profile form. This option contains information related to the employee in the **At a Glance** panel.To preview your configured setting before applying it on the case form, select **Preview**.

</td></tr><tr><td class="sub-head" colspan="2">

Agent assist

</td></tr><tr><td>

Agent assist configuration

</td><td>

List of table names and sys\_id of the associated agent assist configuration record.**Note:** A sys\_id is a unique 32-character GUID \(Globally Unique ID\), that identifies each record in an instance. For more information, see [Unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

To preview your configured setting before applying it on the case form, select **Preview**.

</td></tr><tr><td>

Table configuration

</td><td>

Option to configure agent assist related search results in the Table Configurations form.

</td></tr><tr><td class="sub-head" colspan="2">

Response templates

</td></tr><tr><td>

Response templates configuration

</td><td>

List of table names and sys\_id of the associated response template configuration record.To preview your configured setting before applying it on the case form, select **Preview**.

</td></tr><tr><td>

Table configuration

</td><td>

Option to configure response templates settings in the Table Configurations form.

</td></tr><tr><td class="sub-head" colspan="2">

Fulfillment instructions

</td></tr><tr><td>

Fulfillment instructions configuration

</td><td>

Option to navigate to the HR Fulfillment Instructions form to configure the Fulfillment instructions section on HR case.

</td></tr><tr><td class="sub-head" colspan="2">

Email Client Templates

</td></tr><tr><td>

Email Client Templates configuration

</td><td>

Option to navigate to the Email Client Templates form to configure the Email Templates section on an HR case.

</td></tr><tr><td class="sub-head" colspan="2">

**List**

</td></tr><tr><td>

List configuration ID

</td><td>

The sys\_id of the list configuration \[sys\_ux\_list\_menu\_config\] record in the UX List Menu Configuration table.

</td></tr><tr><td>

Highlighted value configuration ID

</td><td>

Sys\_id of the highlighted value configuration \[sys\_ux\_highlighted\_value\_config\] record in the UX Highlighter Value Configuration table.

</td></tr><tr><td class="sub-head" colspan="2">

**Case creation**

</td></tr><tr><td>

Case creation employee fields

</td><td>

Employee fields displayed on the case creation page.

</td></tr><tr><td class="sub-head" colspan="2">

**Landing page**

</td></tr><tr><td class="sub-head" colspan="2">

HR case card configurations

</td></tr><tr><td>

High priority HR cases

</td><td>

Filter to determine which high priority cases are displayed in the landing page.You can also set text to be displayed when a user views records or when a list is empty.

</td></tr><tr><td>

Recently updated HR cases

</td><td>

Filter to determine which recently updated HR cases are displayed in the landing page.You can also set text to be displayed when a user views records or when a list is empty.

</td></tr><tr><td>

HR cases SLA at risk

</td><td>

Filter to determine what high priority cases are displayed in the landing page.You can also set text to be displayed when a user views records or when a list is empty.

</td></tr><tr><td>

Announcements

</td><td>

Option to navigate to the Schedule Content page to configure the Announcements section in landing page.

</td></tr><tr><td>

Quick links

</td><td>

Option to navigate to the Schedule Content page to configure the Quick links section in landing page.

</td></tr><tr><td>

My frequently used apps

</td><td>

Option to navigate to the Schedule Content page to configure the My frequently used apps section in landing page.

</td></tr></tbody>
</table>**Parent Topic:**[Agent Workspace for HR Case Management reference](agent-ws-reference.md)

**Related topics**  


[Create a new case form](case-creation-form-aws.md)

[Highlighted value condition form](highlighted-value-form.md)

[Bulk case request form](bulk-case-request-form.md)

