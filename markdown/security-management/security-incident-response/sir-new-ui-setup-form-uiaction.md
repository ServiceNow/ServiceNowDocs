---
title: Form UI actions
description: You can configure the UI actions that are displayed in the Security Analyst Workspace.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Additional Security Analyst Workspace configuration, Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Form UI actions

You can configure the UI actions that are displayed in the Security Analyst Workspace.

**Prerequisites:**

Before you configure any UI actions, you must perform certain steps to enable them so that they are available for configuration in the Security Analyst Workspace. See [Enable UI Actions](sir-new-ui-setup-enable-uiaction.md) for details.

To configure a Form UI action for the Security Analyst Workspace, follow these steps:

1.  Navigate to **Security Incidents** &gt; **Analyst Workspace Setup \(New UI\)** &gt; **Form UI Actions**.
2.  Enter the following details:

<table id="table_jph_zrr_blb"><thead><tr><th>

Field Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Select an UI action from the choice list.

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

For the selected UI Page, you can specify additional query parameters here. The template provided with the base system constructs and returns `sysparm_sys_id` parameter only. You can override this by specifying different parameters here.

</td></tr><tr><td colspan="2">

**Server-side Action** If you select Server side action in the Type field, enter the following details:

</td></tr><tr><td>

Scripted Rest Resource

</td><td>

Select the Scripted Rest Resource that defines the action.**Note:** The **SIR UI ANALYST** ACL must be added to the Rest resource.

</td></tr></tbody>
</table>3.  Click **Submit**.
4.  Navigate to **Security Incidents** &gt; **Incidents \(New UI\)** page.
5.  Click on a security incident number to view the security incident record. You can see the new UI action at the top of the page.

To modify an existing Form UI action, click the Action Name to navigate to the Form UI Actions page. You can modify the Action Name, Type, and the rest of the fields based on the selected type.

