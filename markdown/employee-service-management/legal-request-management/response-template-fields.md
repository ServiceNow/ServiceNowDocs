---
title: Response Template form
description: Legal configurator can use the Response Template form to create or modify a response template for reusable messages.
locale: en-US
release: yokohama
product: Legal Request Management
classification: legal-request-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Response Template form

Legal configurator can use the Response Template form to create or modify a response template for reusable messages.

Create or modify a response template by navigating to **All** &gt; **Legal Administration** &gt; **Response Template Configuration**.

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

Short description that identifies the response template when using chat in Legal Counsel Center.Use the short name with a quick command \(/\) to show the text from the template body of the response template while in chat. This feature provides a fast and consistent way to populate text while in chat.

 For example, the short name `gm` identifies the chat response template for a Good Morning greeting. Enter **/gm** in a chat window to show the text from this response template.

</td></tr><tr><td>

Table

</td><td>

Name of the table that the response template is associated with.**Note:** If you’re creating a response template for Legal Counsel Center chat, you must select the Interaction \[interaction\] table. For other response templates, you must select a table from the Legal Service Delivery apps.

</td></tr><tr><td>

Condition

</td><td>

Conditions to determine when the response template is available for use.When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

 **Note:** The conditions available depend on the table that you select. For chat response templates, specify the condition: **\[Type\] \[is\] \[Chat\]**

</td></tr><tr><td>

Application

</td><td>

The application that created the response template.

</td></tr><tr><td>

Group visibility

</td><td>

User groups who have access to the response template.**Note:** Leaving this field empty makes the response template available to all Legal groups.

</td></tr><tr><td>

Template body

</td><td>

Text of the response template that provides instructions to the legal fulfillers on how to respond to an assigned legal request or legal matter.You can reference field values by selecting variables from the **Variables** list based on the table you select.

 Place the cursor where you want the custom variable reference to appear, then click **Insert Current User** to insert the current user variable \(`${current_user}`\) or **Insert Current Date** to insert the current date variable \(`${Date}`\).

</td></tr><tr><td>

Select variables

</td><td>

Fields from the selected table that you can include in the template body as variables.For example, say you selected the Legal Request \[sn\_lg\_ops\_request\] table in the **Table** field and then inserted the **Requested for** field variable in the template body. When the response template is used, this field variable will be replaced with the actual name of the user for whom the legal request was submitted.

</td></tr></tbody>
</table>**Parent Topic:**[Legal Request Management reference](legal-request-management-reference.md)

