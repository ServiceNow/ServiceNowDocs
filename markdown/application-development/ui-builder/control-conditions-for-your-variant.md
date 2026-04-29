---
title: Control the conditions for a page variant
description: Set the conditions and manage the criteria that determine when a page variant is displayed. UI Builder page variants enable you to create different versions of a page to tailor content for a specific audience.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create a page variant, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Control the conditions for a page variant

Set the conditions and manage the criteria that determine when a page variant is displayed. UI Builder page variants enable you to create different versions of a page to tailor content for a specific audience.

## Before you begin

Role required: ui\_builder\_admin

## About this task

If you have multiple page variants that all have the same conditions, the variants go by the order setting.

## Procedure

1.  Create a page variant.

    For more information, see [Create a page variant](create-variant.md).

2.  Set the conditions for a new variant.

    In this example, you configure a page variant to display when you open a record from the Task table.

    1.  On the **First, select a template** screen, locate the **Standard record** template and select **Use template**.

        **Note:** Conditions can only evaluate parameters that have been added. In this example, the **Standard record** template includes the **table** and **sys\_id** parameters.

    2.  Enter a name for your page and select **Continue**.

    3.  Review the URL parameters and select **Looks good**.

        Notice that **table** and **sysId** are added as required parameters, which appear in the URL preview.

        ![Required parameters 'table' and 'sysId' along with the URL preview for the page.](../image/control-conditions-parameters.png)

    4.  On the **Tell us about your variant** screen, enter a name for your variant.

    5.  In the form section, fill out the fields.

<table id="table_wtq_2vw_tbc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Parameter

</td><td>

The aspect or attribute that you want to check.

</td><td>

**table**, **sys\_id****Note:** Conditions can only evaluate the added parameters. However, conditions written for subpages inherit additional outputs from the parent page controllers, providing a wider range of parameters options.

</td></tr><tr><td>

Operator

</td><td>

The rule that compares the parameter to the value. It tells you how the comparison is made.

</td><td>

**is**, **is not**, **starts with**

</td></tr><tr><td>

Value

</td><td>

The number, text, or option input that you want to compare with the parameter.

</td><td>

"`Incident`", "`12345`", "`Active`", "`Change Request`"

</td></tr></tbody>
</table>        **Note:** The **table** and **sysId** parameters are available options for the **Parameter** field because they're required parameters as a part of the **Standard record** template.

        ![Tell us about your variant screen with 'Name' set to 'Task', 'Parameter' to 'table', 'Operator' to 'is', and 'Value' to 'task'.](../image/control-conditions-fields.png)

    6.  Select **Create**.

3.  Review the conditions created for your variant.

    1.  In the Experience view, find the variant for which you want to view the conditions.

    2.  Select the **View** button to display the conditions set for that variant.

4.  Edit the existing conditions for your variant.

    1.  From the Experience view, find the variant for which you want to edit the conditions.

    2.  Select **Settings**.

    3.  Under Conditions, select **Edit conditions**.

        The condition you previously set appears. You can update these fields.

    4.  On the **Edit variant conditions** screen, next to the condition, select the **and**\(![Button labeled 'and'.](../image/control-conditions-and-button.png)\) or **or**\(![Button labeled 'or'.](../image/control-conditions-or-button.png)\) button to add another condition and specify the criteria.

        For example, by adding the following **AND** condition \(**\[sysId\]** **\[is\]** `[abcd1234]`\), you configure the page variant to display when you access a record from the Task table with a sys\_id of abcd1234.

        **Note:** You can add **AND** or **OR** conditions. To mix both types, you must write an encoded query.

        ![Page variant conditions with 'table = task' AND 'sysId = abcd1234'.](../image/control-conditions-and.png)

    5.  Select **Enter as text** to write an encoded query that specifies the criteria.

        The **Edit variant conditions** screen displays the encoded query field, where the conditions you previously set are shown in encoded query form: `table=task^sysId=abcd1234`.

        For example, by adding the following 'OR' condition \(`^ORsysId=efgh5678`\), you set the page variant to display when you access a record from the Task table with a sys\_id of either abcd1234 or efgh5678. For more information on writing encoded queries, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

        ![Edit variant conditions screen displaying encoded query 'table=task^sysId=abcd1234^ORsysId=efgh5678' in the field.](../image/control-conditions-or.png)


**Parent Topic:**[Create a page variant](create-variant.md)

