---
title: Response templates
description: Resolve cases or support issues faster and more efficiently with response templates. Response templates \(formerly known as templated snippets\) are reusable messages that can be copied to case or task forms to provide quick and consistent messages to users, or to display standard chat response messages to requesters in Agent Chat.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Response templates

Resolve cases or support issues faster and more efficiently with response templates. Response templates \(formerly known as templated snippets\) are reusable messages that can be copied to case or task forms to provide quick and consistent messages to users, or to display standard chat response messages to requesters in Agent Chat.

**Note:** Response templates are available only for existing records.

## Assign response template roles

The following roles are installed when you activate the response templates plugin.

<table id="table_kb3_2kr_v2b"><thead><tr><th>

Response template role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Response template administrator\[sn\_templated\_snip.template\_snippet\_admin\]

</td><td>

Grants access to scoped administration of the response templates feature.

</td></tr><tr><td>

Response template writer\[sn\_templated\_snip.template\_snippet\_writer\]

</td><td>

Grants access to create, read, update, and delete \(CRUD\) response template content.

</td></tr><tr><td>

Response template reader\[sn\_templated\_snip.template\_snippet\_reader\]

</td><td>

Grants access to read response template content.

</td></tr><tr><td>

System Administrator\[admin\]

</td><td>

Response template administrator \[sn\_templated\_snip.template\_snippet\_admin\]

**Note:** Admin inherits this role by default. When the Templated Responses \[com.sn\_templated\_snip\] plugin is activated without activating related HR applications, you can still use response templates.

-   Admin can reassign this role to other users.
-   Admin can also remove the Contained Role \[sys\_user\_role\_contains\] table so Admin users do not inherit this role by default. Or:
    1.  Enter **sys\_store\_app\_list.do** in the Filter navigator search bar of an instance, or **https://YOUR\_INSTANCE/sys\_store\_app\_list.do** from a web browser.
    2.  Search for and select **Templated Snippets**.
    3.  Scroll down to **Related Links**.
    4.  Click **Remove from the role contained by admin**.

</td></tr></tbody>
</table>Before you begin using response templates, you must assign these roles to the appropriate roles, groups, or users in your application.

-   To assign a role to another role, see [Add a role to an existing role](https://www.servicenow.com/docs/access?context=t_AddARoleToAnExistingRole&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

For example,

-   In the HR Service Delivery application, users with the HR administrator role are assigned the response template administrator role, users with the HR manager role are assigned the response template writer role, and users with the HR case writer role are assigned the response template reader role.
-   In the Customer Service Management application, users with the customer service manager role \(sn\_customerservice\_manager\) inherit the response template writer role. Users with the customer service agent role \(sn\_customerservice\_agent\) inherit the response template reader role and can access response templates assigned to all groups to which they belong.

## How to use response templates

Users with the response template writer \[sn\_templated\_snip.template\_snippet\_writer\] role can create response templates. Each template is associated with a table that is an extension of the Task \[task\] or Interaction \[interaction\] table. Response templates include a short name for specifying a shortcut that can be used to identify the message. For chat response templates used in Agent Workspace, agents use the slash command with a short name to present the standard message during a chat. You can also configure the template to

-   Include variables pulled from a table
-   Specify a condition builder to specify the conditions that must be met for the template to be available for use, such as for a specific HR service

For more information, see [Create or modify a response template](../task/create-modify-templated-snippet.md).

Users with the response template reader \[sn\_templated\_snip.template\_snippet\_reader\] role can then copy response template content and use it in their responses to users when working on case or task forms that meet the specified conditions. For example, a response template for payroll discrepancy cases enables HR agents to use a standardized message when responding to that case type. See [Copy a response template to an HR case](https://www.servicenow.com/docs/access?context=hr-templated-snippets&version=australia&pubname=australia-employee-service-management&section=add-templated-snippet-to-hr-case&ft:locale=en-US) for an HR-specific example.

## Response template to escalate payroll discrepancy cases

You are part of an enterprise HR organization using the HR Service Delivery application. You want your HR agents to respond to and, when necessary, escalate payroll discrepancy cases quickly and consistently. Create a response template so that HR agents have a reusable message to use when responding to employees about that case type.

One of your HR managers with the response template writer role is responsible for creating the template to escalate payroll discrepancy cases. The template is associated with the HR Payroll Case \[sn\_hr\_core\_case\_payroll\] table, and a condition filters on cases that match the appropriate HR service called Payroll Discrepancy. In the template body, the response text appears with variables, such as the subject person name in the salutation.

HR case writers with the response template reader role can copy the response template content and use it in their responses to employees when working on cases. Response templates provide a faster and efficient way to resolve cases.

## Activation information

To use response templates in your application, you must [activate response templates](../task/activate-templated-snippets.md). For information on what components are installed with the feature, see [Components installed with response templates](../reference/components-installed-with-response-templates.md).

