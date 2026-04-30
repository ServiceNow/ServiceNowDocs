---
title: Related List UI Actions
description: You can add new UI actions to the related lists that appear in the Security Analyst Workspace.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Related List configuration, Additional Security Analyst Workspace configuration, Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Related List UI Actions

You can add new UI actions to the related lists that appear in the Security Analyst Workspace.

**Prerequisites:**

Before you configure any UI actions, you must perform certain steps to enable them so that they are available for configuration in the Security Analyst Workspace. See [Enable UI Actions](sir-new-ui-setup-enable-uiaction.md) for details.

To add a new Related List UI action, follow these steps:

1.  Navigate to **Security Incidents** &gt; **Analyst Workspace Setup \(New UI\)** &gt; **Related List Configurations**.
2.  Click on the Group Name. The Related List Group configuration page is displayed.
3.  Click on the Related List for which you want to add a UI action.
4.  Click **Add** in the Related List UI Actions section.
5.  Enter the following details:

<table id="table_jph_zrr_blb"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Select a UI action from the choice list.

</td></tr><tr><td>

Type

</td><td>

Select the type of action. This can be:-   Dialog based action: This type of action is used when user interaction or inputs are required to execute specific business logic.
-   Server side action: This action executes the required business logic without any additional user input.
 **Note:** Before you configure any UI actions, you must perform certain steps to enable them so that they are available for configuration in the Security Analyst Workspace. See [Enable UI Actions](sir-new-ui-setup-enable-uiaction.md) for details.

</td></tr><tr><td>

Application

</td><td>

The name of the application scope \(Security Incident Response UI\) in which the UI action is being added is displayed here.

</td></tr><tr><td colspan="2">

**Dialog Based Action** If you select Dialog based action in the Type field, enter the following details:

</td></tr><tr><td>

UI Page

</td><td>

Select the UI page associated with the action.

</td></tr><tr><td>

Dialog Title

</td><td>

Enter a title for the dialog action.

</td></tr><tr><td>

Dialog Width and Height

</td><td>

Enter the height and width of the dialog in pixels.

</td></tr><tr><td>

Script

</td><td>

For the selected UI Page, you can specify additional query parameters here. The template provided with the base system constructs and returns `sysparm_incident_id`, `sysparm_record_table`, and`sysparm_related_sys_ids ` parameters only. You can override them by specifying different parameters here.

</td></tr><tr><td colspan="2">

**Server side Action** If you select Server side action in the Type field, specify the following:

</td></tr><tr><td>

Scripted Rest Resource

</td><td>

Select the Scripted Rest Resource that defines the action.**Note:** The **SIR UI ANALYST** ACL must be added to the Rest resource.

</td></tr></tbody>
</table>6.  Click **Submit**.
7.  Navigate to **Security Incidents** &gt; **Incidents \(New UI\)** page.
8.  Click on a security incident number to view the security incident record. Launch the respective Related List to view the new UI action.

