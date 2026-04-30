---
title: Create a new help context
description: You can create new help contexts to supplement or replace the default help contexts. For example, if your organization has heavily customized a form, you might create a new help context for that form. The customized help context could link to more relevant information, such as a company knowledge base article.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Context-sensitive help, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a new help context

You can create new help contexts to supplement or replace the default help contexts. For example, if your organization has heavily customized a form, you might create a new help context for that form. The customized help context could link to more relevant information, such as a company knowledge base article.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Help Contexts**.

2.  Click **New**.

3.  Complete the Help Context form from the fields in the table.

<table id="table_hwc_gzr_sr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select **Form**, **List**, or **Record**.

 If you select **Record**, the **Table name** field is replaced by the **Document** field.

</td></tr><tr><td>

Table name

</td><td>

Select the table for which the help context is being defined.

 If the **Type** is **Record**, this field is replaced by the **Document** field.

 **Note:** The list shows only tables and database views that are in the same scope as the help context.

</td></tr><tr><td>

Document

</td><td>

Click the reference lookup icon \(![Reference lookup icon](../image/IconReferencelookup.png)\) to open the document selection dialog box \(pictured\). Select the table and document \(record\) for this help context.

 ![Help context document select](../image/select-the-document.png)

 This field is only visible if you have selected **Record** as the **Type**.

</td></tr><tr><td>

Language

</td><td>

Select the language of the help page to which you are linking. The choices available depend on which I18n Translation plugins you have activated. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

 This field allows you to create multiple help contexts for the same form, list, or record, each directing to a help page in a different language. For example, you might have two help contexts for Form X: one for English and the other for Spanish. If a user whose language is set to Spanish clicks the help icon while viewing Form X, the help page defined in the Spanish help context opens.

</td></tr><tr><td>

Active

</td><td>

Select this check box to have the system use the help context. This check box is selected by default for new help contexts.

</td></tr><tr><td>

ServiceNow Product Documentation

</td><td>

Indicates if this help was created by a customer or was provided by ServiceNow. Clear this check box to create custom help for your organization. Do not attempt to modify existing help topics provided by ServiceNow for your own use. The system is configured to use your custom records rather than the default help contexts, even when they are created on the same table.

</td></tr><tr><td>

URL or page name

</td><td>

Identifies the topic to display when a user clicks the help icon while viewing a form, list, or record. You can enter the complete URL of the help page or just the target file name if you set a [base URL](../concept/c_ContextSensitiveHelp.md) in the **help.base.default** system property.

</td></tr></tbody>
</table>    **Note:** If you reconfigure the fields on the form, you see the available fields **Plugin ID** and **System Property Base URL**. Do not use these fields. They are for internal use only.

4.  Click **Submit**.


**Parent Topic:**[Context-sensitive help](../concept/c_ContextSensitiveHelp.md)

**Related topics**  


[Help context types and prioritization](../reference/r_HelpContextTypes.md)

[Context-sensitive help](../concept/c_ContextSensitiveHelp.md)

