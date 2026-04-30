---
title: Add and customize a field in a table
description: Administrators can add new fields to a table to store and display data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Add and customize a field in a table

Administrators can add new fields to a table to store and display data.

## Before you begin

Role required: admin

## About this task

**Note:** Certain ServiceNow AI Platform subscriptions include custom table entitlements. You can create custom tables for any purpose, up to the entitlement limit in the subscription. To learn more about how your usage administrator maps the custom tables that you create to subscriptions, see [Map custom tables to a product subscription in Subscription Management](../../subscription-management/task/allocate-custom-table-subsc-app-v2.md).

Be aware of these database limitations:

-   The system can only have a maximum of 1000 columns per table. Although 1000 columns is a specified limit, this limit doesn't mean you can physically have 1000 columns within a table. The number of columns within a table is defined by the database used in the ServiceNow datacenter, not by the ServiceNow AI Platform.
-   Every table, regardless of storage engine, has a maximum row size of 65,535 bytes. Storage engines may place additional constraints on this limit, reducing the effective maximum row size.
-   The system can't have more than 10 medium-length or longer **String** fields to a single table. Attempting to save a large number of characters in 11 or more String fields can result in the following error: Syntax Error or Access Rule Violation detected by database \(Row size too large \(&gt; `8126`\).
-   When you create fields, the u\_ prefix is automatically added to the column name. If the column label that you enter contains leading numeric characters, they are replaced by the u\_ prefix.

For more information on database limitations and general questions on tables in your ServiceNow instance, see [KB0749585](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0749585).

## Procedure

1.  Navigate to any form.

2.  Right-click the form header and select **Configure** &gt; **Form Layout**.

3.  In the **Create new field** section, fill in the following fields

<table id="choicetable_qj4_3rw_1r"><tbody><tr><td id="d96251e158">

**Name**

</td><td>

Enter the name of the field as you want it to appear on forms and lists.

</td></tr><tr><td id="d96251e167">

**Type**

</td><td>

Select a field type.

</td></tr><tr><td id="d96251e176">

**Field length**

</td><td>

Select a field length. This field is visible only for certain field types.

</td></tr></tbody>
</table>4.  Click **Add**.

5.  Use the slushbucket to place the field in the desired location on the form.

6.  Click **Save**.

    The field now appears on the form in the designated location.


-   **[Make a field mandatory](t_MakingAFieldMandatory.md)**  
Fields can be marked as mandatory, meaning they must contain a value before the record can be saved. Mandatory fields are marked with a field status indicator before the label.
-   **[Change the field label or hint](../../reference-pages/task/t_ChangeFieldLabelOrHint.md)**  
You can change a field's label or the text that appears as a hint when you point your mouse device to the field.
-   **[Delete a field from a table](../../reference-pages/task/t_DeleteFields.md)**  
You can delete custom fields that you created. Custom fields begin with **u\_**. It is recommended that you remove the field from forms and lists instead of deleting it.
-   **[Add users to a watch list](../../../use/using-forms/task/t_UseAWatchList.md)**  
Watch lists enable you and others to subscribe to notifications of a task.
-   **[Highlight list fields](../../navigation-and-ui/task/highlight-list-fields-platform.md)**  
Color fields in lists to call an agent's attention to them.
-   **[Modify string field length](../../reference-pages/task/t_ModifyingStringFieldLength.md)**  
You can modify the maximum character limit for a string field.
-   **[Specify a default field value](t_SpecifyingADefaultValue.md#)**  
A default value populates a value in a field when a new record is created.
-   **[Make a field dependent](t_MakingAFieldDependent.md)**  
A choice or reference field can be declared dependent on another field on the same table to limit the values available to select based on the value of the dependent field.
-   **[Require unique values for a field](t_RequiringUniqueValuesForAField.md)**  
The system allows you to require that a field's values be unique. When this is done, the system will not let two records have the same value for that field.
-   **[Define field styles](../../navigation-and-ui/task/t_DefineFieldStyles.md)**  
Field styles enable you to declare individual CSS styles for a field in a list or form.
-   **[Record numbering](../concept/c_ManagingRecordNumbering.md)**  
In the base system, several tables are numbered, including Incident, Problem, Change Request, and Knowledge. You can also use these numbers anywhere that script is present, for example to generate watermarks for emails. Records in tables can be numbered automatically.

**Parent Topic:**[Field administration](../../reference-pages/concept/c_IntroductionToFields.md)

