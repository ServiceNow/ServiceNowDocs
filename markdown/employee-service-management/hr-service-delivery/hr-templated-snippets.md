---
title: Response templates for HR Service Delivery
description: You can use response templates with HR Service Delivery to resolve cases faster and more efficiently.Several types of components are installed with activation of the Templated Responses \(com.sn\_templated\_snip\) plugin, including tables and user roles.Create or modify a response template \(formerly known as a templated snippet\) to define a reusable message. You can copy these messages when responding to employees to provide quick and consistent messages.Follow these steps to create a response template channel. Response template channels ensure the correct response templates appear for use with chat, email, or HR case or task.Copy response template \(formerly known as templated snippet\) content to any field on an HR case form that meets the specified conditions.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Response templates for HR Service Delivery

You can use response templates with HR Service Delivery to resolve cases faster and more efficiently.

Response templates \(formerly known as templated snippets\) are reusable messages. You can copy these messages created from these templates to an HR case, task, email, or chat to provide quick and consistent messages to employees. For example, a response template for a payroll discrepancy case enables HR agents to use a standardized message when responding to that case type.

**Note:** For more information on response templates, see [Response templates](https://www.servicenow.com/docs/access?context=response-templates-templated-snippets&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Response template channels

Response templates can correspond to multiple channels. A channel represents the media you want the response template to be available for. For example:

-   Chat channel: Provides response templates for chat conversations.
-   Email channel: Provides response templates for emails.
-   Form: Provides response templates for HR case or tasks.

If you create a new response template and do not assign it to a channel, it is not available to use.

To create a universal response template that is available for all channels, assign it to all channels.

**Note:** Any response templates created prior to the Quebec release are associated with all channels preserving their prior behavior and can be used universally.

## Activation information

The response templates feature automatically activates when Case and Knowledge Management activates. See [Activate response templates](https://www.servicenow.com/docs/access?context=activate-templated-snippets&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

To use response templates in a chat in Agent Workspace for HR Service Delivery, activate: Advanced Work Assignment for HRSD \(com.sn\_hr\_awa\) plugin.

For more information, see  and Setting up Workspace Agent Chat.

For more information on setting up chat in Virtual Agent, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## How to use response templates with form \(HR case or task\)

HR administrators and managers can create response templates. Each template is associated with an HR table that is an extension of the Task \[task\] table. Configure the template to include variables pulled from that table. Also, use a condition builder to specify what a case must meet for the template to be available, such as for a specific HR service.

For more information on creating or modifying a response template, see [Create or modify an HR Service Delivery response template](hr-templated-snippets.md#).

Response templates appear for an HR case form for templates associated with the Form channel and satisfy the conditions on the response template. For the HR case form, the **Responses** button appears at the top. If there are multiple templates available, you can select the appropriate one. See [Work an HR case](../task/t_CreateAnHRCase.md).

**Note:** For more information on using a response template with an HR case, see [Copy a response template to an HR case](hr-templated-snippets.md#).

For Agent Workspace for HR Service Delivery, the Response Templates icon \(![Response template icon](../reference/images/response-template-icon.png)\) appears in the Contextual sidebar. For more information, see .

## Components installed with response templates

Several types of components are installed with activation of the Templated Responses \(com.sn\_templated\_snip\) plugin, including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

### Roles installed

By default, the following HR roles contain the following response template roles.

**Note:** The Templated Responses \[com.sn\_templated\_snip\] plugin activates the sn\_templated\_snip.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only Response Template admin user by requiring a minimum number \(default is two\) of active users with this role.

<table id="table_ks1_2k3_ldb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Response templates administrator\[sn\_templated\_snip.template\_snippet\_admin\]

</td><td>

Grants access to scoped administration of the response templates feature.

</td><td>

sn\_templated\_snip.template\_snippet\_writer

</td></tr><tr><td>

Response templates writer\[sn\_templated\_snip.template\_snippet\_writer\]

</td><td>

Grants access to create, read, update, and delete \(CRUD\) response template content.

</td><td>

sn\_templated\_snip.template\_snippet\_reader

</td></tr><tr><td>

Response templates reader\[sn\_templated\_snip.template\_snippet\_reader\]

</td><td>

Grants access to read response template content.

</td><td>

None

</td></tr></tbody>
</table>You can assign these roles to the appropriate roles, groups, or users in your application.

-   To assign a role to another role, see [Add a role to an existing role](https://www.servicenow.com/docs/access?context=t_AddARoleToAnExistingRole&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

For further information on user administration and how to manage users, see [User administration](https://www.servicenow.com/docs/access?context=c_UserAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

### Tables installed

<table id="table_ytw_vj3_ldb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Response Template\[sn\_templated\_snip\_note\_template\]

</td><td>

Stores response template information. Response templates are reusable messages that can be copied to case or task forms. Response templates provide quick and consistent messages to users, or display standard chat response messages to requesters in Agent Chat.

</td></tr><tr><td>

M2M Response Template to Channel\[m2m\_response\_template\_to\_channel\]

</td><td>

Maps channels to response templates.

</td></tr><tr><td>

Response Template Channel\[sn\_templated\_snip\_channel\]

</td><td>

Stores information about response template channels.

</td></tr><tr><td>

Note Template for Table\[sn\_m2m\_note\_template\_for\_table\]

</td><td>

Maps notes to response templates.

</td></tr></tbody>
</table>For further information on table administration and how to manage data, see [Table administration](https://www.servicenow.com/docs/access?context=c_TableAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Create or modify an HR Service Delivery response template

Create or modify a response template \(formerly known as a templated snippet\) to define a reusable message. You can copy these messages when responding to employees to provide quick and consistent messages.

### Before you begin

Role required: sn\_hr\_core.manager, sn\_templated\_snip.template\_snippet\_admin

Each template is associated with an HR table that is an extension of the Task \[task\] table. The template can be configured to include variables pulled from that table. For example, if you choose the HR Case \(sn\_hr\_core\_case\) table, you can select the Subject person variable to appear in the Template body and it will replace the variable with the actual name of the subject person when the response template is used.

Also, use condition builder to define when a case meets the criteria for a template, such as for a specific HR service.

### Procedure

1.  Navigate to **HR Administration** &gt; **Response template configuration**.

2.  Select **New** to create a response template.

    Or, select an existing response template to modify from the list.

3.  Fill in the fields on the form.

<table id="table_wtn_xd3_ldb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the response template.

</td></tr><tr><td>

Short Name

</td><td>

Short description that identifies the response template when using chat in Agent Workspace.Use the short name with a quick command \(/\) to show the text from the template body of the response template while in chat. This feature provides a fast and consistent way to populate text while in chat.

 For example, the short name `gm` identifies the chat response template for a Good Morning greeting. Enter **/gm** in a chat window to show the text from this response template.

</td></tr><tr><td>

Table

</td><td>

Name of the table that the response template is associated with.If you are creating a response template for Agent Workspace chat, the associated table is the Interaction \[interaction\] table. For other response templates, the table must be an extension of the Task \[task\] table.

 **Note:** Creating custom COE tables do not allow you to add the Copy to Clipboard UI action. Users can still use the copy and paste function.

</td></tr><tr><td>

Condition

</td><td>

Conditions that determine when the response template is available for use.When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

 **Note:** The conditions available depend on the table you select. For chat response templates, specify the condition: **\[Type\] \[is\] \[Chat\]**

</td></tr><tr><td>

Application

</td><td>

The application that created the response template.

</td></tr><tr><td>

Group visibility

</td><td>

Indicates what groups have access to the response template.Adding groups filters who can view the response template.

 **Note:** Leaving this field empty makes the response template available to all groups.

</td></tr><tr><td>

Template body

</td><td>

Text of the response template providing instructions to the agent on how to respond to a specific case or task.You can reference field values by selecting variables from the variables list based on the table you select.

 You can manually enter custom variable references:

-   Current user: `${current_user}`
-   Current date: `${Date}`
 Or, place your mouse where you want the custom variable reference to appear and select the **Insert Current User** or **Insert Current Date** buttons.

 **Note:** Response templates do not support rich text.

</td></tr><tr><td>

Select variables

</td><td>

Variables you can add to the template body. For example, if you choose the HR Case \(sn\_hr\_core\_case\) table, you can select the Subject person variable to appear in the Template body and it will replace the variable with the actual name of the subject person when the response template is used.**Note:** The variables available depend on the table you select.

</td></tr></tbody>
</table>    The following GIF shows an example of an HR manager in the HR Service Delivery application creating a response template to escalate payroll discrepancy cases. The template is associated with the HR Payroll Case \[sn\_hr\_core\_case\_payroll\] table, and a condition is set to filter on cases that match the Payroll Discrepancy HR service. The template text is pasted into the body, and then a variable for the subject person is added to the salutation.

    ![Response Template](../image/response-template.png)

    ![How you can create a response template with conditions and variables.](../image/response-template-example.gif)

4.  Click **Submit** or **Update**.

    Channels limit the response template to only the channels you add. If you leave this blank, the response template is available to no channels. This feature allows you to have different messages for chats, emails, or form. For more information, see [Create a response template channel](hr-templated-snippets.md#).

    The Channels related list appears.


### What to do next

You can copy response template content to any field on a form that meets the specified conditions.

The following GIF shows an example of an HR case writer in the HR Service Delivery application opening a payroll discrepancy case and copying a payroll discrepancy escalation template to the comments field in the HR case form for the employee to read.

![How you can copy response template content to a field on a case form.](../image/response-template-example-2.gif)

## Create a response template channel

Follow these steps to create a response template channel. Response template channels ensure the correct response templates appear for use with chat, email, or HR case or task.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Response Template Configuration**.

2.  Select an existing response template or click **New**.

3.  Select **Channels**.

4.  Select the ![Lookup using list icon](../image/magnifying-glass.png) **Lookup using list** icon.

5.  Select **New**.

    Fill in the fields on the form.

<table id="table_wfs_mjz_xkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the channel. Channels represent a category you want the response template to appear for.The base system provides:

-   Chat
-   Email
-   Form
**Note:** The Advanced Work Assignment for HRSD \(com.sn\_hr\_awa\) plugin must be activated to use response templates in chat.

</td></tr><tr><td>

Value

</td><td>

The name of the channel you want to remain consistent in relation to different languages. For example, if I am working in French, the **Name** field could be LeChat, but Chat in the **Value** field. This ensures that the correct template is selected regardless of language.

</td></tr><tr><td>

Application

</td><td>

The application the response template is available to use in.

</td></tr><tr><td>

Active

</td><td>

Activates the Response Template Channel.**Note:** Unchecking the box inactivates the record without deleting it.

</td></tr></tbody>
</table>6.  Select **Save**.

    Channels limit the response template to only the channels you add. If you leave this blank, the response template is available to no channels. This feature allows you to have different messages for chats, emails, or form. For more information, see [Create a response template channel](hr-templated-snippets.md#).

    The Channels related list appears.

7.  Click **New** to create a new channel or **Edit** to access an existing channel.

8.  After you select the channel\(s\), click **Save**.

    The **Response Template** form returns.

9.  Click **Update**.

    For more information on response templates, see [Create or modify an HR Service Delivery response template](hr-templated-snippets.md#).


## Copy a response template to an HR case

Copy response template \(formerly known as templated snippet\) content to any field on an HR case form that meets the specified conditions.

### Before you begin

Role required: sn\_hr\_core.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **All HR Cases**, and open one of the modules, such as **Assigned to me** or **Open**.

2.  Open the HR case.

3.  Click **Responses** to open the **Response Templates** side panel.

    **Note:** If the **Responses** button is not visible, make sure that a response template that meets the conditions for the open case is available to use. See [Create or modify an HR Service Delivery response template](hr-templated-snippets.md#) for more information.

    ![Click Responses to open the Response Templates side panel.](../image/response-template-1.png)

4.  In the **Response Templates** side panel, you can select a template and copy it to the clipboard.

    ![In the Response Templates side panel, you can select a template and copy it to the clipboard.](../image/response-template-2.png)

5.  Once copied, you can paste the content to a field on the form, such as to **Comments**, or into an email that you send to the employee.

    **Note:** For information on using response templates in HR Agent Workspace, see .


