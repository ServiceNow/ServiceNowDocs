---
title: Advanced form configuration
description: Administrators can configure advanced form features, such as form focus, form splits, and derived fields.The Insert and Insert and Stay options are disabled by default for task records such as incidents and change requests. You can set a system property to show these options for task records.Switch the focus on a form to the first element on the page instead of the first writable field to make the form more accessible to users who use screen readers.Administrators can hide the template bar for a table by creating a system property.By default, when you press the Enter key in a simple one-line text field, a choice list, or a Boolean field, the form is submitted.Form splits enable you to organize fields on a form into columns. Administrators must add a property to enable form splits.You can specify which form fields are required in forms. This action prevents users with the personalize\_form role from removing the field by configuring the form layout.You can configure the type of label that appears for derived fields.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Administer, Form administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Advanced form configuration

Administrators can configure advanced form features, such as form focus, form splits, and derived fields.

## Allow insert options on task records

The **Insert** and **Insert and Stay** options are disabled by default for task records such as incidents and change requests. You can set a system property to show these options for task records.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Locate the property **Allow the use of the "Insert" and "Insert and Stay" options on task derived tables** \(**glide.ui.task.insert**\).

3.  Select the check box to enable or clear the check box to disable \(default\) the options for tasks.

4.  Click **Save**.


## Turn off focusing on the first writable field of a form

Switch the focus on a form to the first element on the page instead of the first writable field to make the form more accessible to users who use screen readers.

### Before you begin

Role required: admin

### About this task

By default, forms set focus on the first writable field on the form. With first-field focus turned off, the form focuses on the first element on the page instead. Focusing on the first element, instead of the first writable element, helps orient users who use screen readers so they can find all the elements on a form.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Set the property **glide.ui.focus\_first\_element** to **false**.


## Hide the template bar for a table

Administrators can hide the template bar for a table by creating a system property.

### Before you begin

Role required: admin

### About this task

Creating a table-specific property and setting it to false prevents users from displaying the template bar on a record for the specified table.

### Procedure

1.  Navigate to `sys_properties.list`.

2.  [Add a system property](../../reference-pages/reference/r_AvailableSystemProperties.md#) with the following settings.

    |Property|Value|
    |--------|-----|
    |Name|glide.ui.show\_template\_bar.&lt;TABLENAME&gt;|
    |Type|true \| false|
    |Value|false|

3.  Click **Submit**.


## Deactivate form submission with the Enter key

By default, when you press the `Enter` key in a simple one-line text field, a choice list, or a Boolean field, the form is submitted.

### Before you begin

Role required: admin

### About this task

You can use a system preference to deactivate this feature if you do not want the `Enter` key to submit the form.

### Procedure

1.  From the left navigation pane, select **User Administration** &gt; **User Preferences**.

2.  Select the **enter\_submits\_form** preference.

3.  Set the value to **false**.

4.  Click **Update**.

    The change does not take effect until user preferences are reloaded either at login or when a session is created.


## Enable multiple form splits

Form splits enable you to organize fields on a form into columns. Administrators must add a property to enable form splits.

### Before you begin

Role required: admin

### About this task

![Configuration of two form splits](../image/FormSplitConfiguration.png "Configuration of two form splits")

![Two form splits](../image/FormSplitExample.png "Example of the form with two form splits")

When you organize fields in this manner and the user is viewing the form on a small mobile device, the fields within the first split are listed before the fields in the second split. In this example, the **Asset tag**, **State**, **Serial number**, and **Substate** field are listed before any of the fields below them. You can also create elements that span the form at the top of the form.

### Procedure

1.  Enter `sys_properties.list` in the Navigation filter.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  If the property does not exist, click **New**.

3.  Enter the following information.

<table id="choicetable_qyc_wqq_pt"><tbody><tr><td id="d281132e556">

**Name**

</td><td>

glide.ui.form\_multiple\_splits

</td></tr><tr><td id="d281132e565">

**Description**

</td><td>

Enable multiple form splits

</td></tr><tr><td id="d281132e574">

**Type**

</td><td>

true \| false

</td></tr><tr><td id="d281132e583">

**Value**

</td><td>

true

</td></tr></tbody>
</table>4.  Click the form context menu icon and select **Save**.

    The **Categories** related list appears.

5.  Click **Edit** and move **UI** to the **Categories List**.

6.  Click **Save**.

    The System Property form reopens and the new property appears in the UI Properties page.


## Define required fields

You can specify which form fields are required in forms. This action prevents users with the personalize\_form role from removing the field by configuring the form layout.

### Before you begin

Role required: admin

The Required Form Fields plugin must be active.

### About this task

If present on a form, only an administrator can remove required fields. When you configure a form, required fields appear in a gray color and have a tooltip indicating they are required. Required fields are defined in the Required Form Fields \[sys\_ui\_element\_required\] table.

The expected \(although not the only\) use case for this feature is as part of a delegated administration scheme. For example, you can grant branch offices the rights to modify forms by granting the personalize\_form role, but not allow them to remove certain fields which are critical to overall business processing.

### Procedure

1.  Navigate to `sys_properties.list`.

2.  Locate the property named **glide.ui.form.enforce\_required\_fields** and make sure it is set to true.

3.  Navigate to **System UI** &gt; **Required Form Fields**.

4.  Click **New**.

5.  Select the table and field, and then select the **Required** check box.

    The following example sets the **Short description** field on the Incident form to be required.

    ![Required form field](../image/RequiredFormField.png)

    If you decide later that you do not want to make the field required, clear the **Required** checkbox. This action is preferable to deleting the record.

6.  Click **Submit**.


### Result

If the table specified has extension tables, then the Required Form Field record applies to forms of all extended tables. For example, if an administrator specifies that the **Short description** field is required for the Task table, then this configuration applies to the Incident form, Change Request form, Problem form, and so on.

An extended table can override the Required Form Field rule of its base table. For example, if the **Short description** field is required for the Task table, but not required for the Incident table, it is required for all Task tables except Incident.

## Control the label type for derived fields

You can configure the type of label that appears for derived fields.

### Before you begin

Role required: admin

### About this task

An example would be displaying the email address for the caller when looking at an incident record. The email address is not stored in the Incident table, but is obtained by following the caller reference from the incident to the User table. You control the label type by setting a system property. For example, the field label for an incident email address can be either of the following strings.

-   **Caller Email**, which represents the complete label to uniquely identify this field as the email from the caller user record. If you display the email address for the person the ticket is assigned to, its label would be **Assigned to Email**.
-   **Email** which is the label for the target field. This label is not unique on the form if, for example, you are also displaying the email address of the person assigned to the incident. However, usually the placement of the field on the form makes it clear what the field represents.

<table id="table_DisplayingInformationFromOtherRecords"><tbody><tr><td>

![Available fields](../image/AvailableTableFields.png "Available table fields")

 Choose the **Caller** field and click the expander icon.

</td><td>

![Caller fields](../image/CallerFields.png "Caller fields")

 Select the available fields associated with the **Caller** field.

</td></tr></tbody>
</table>### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System**.

2.  Locate the **Use short labels for all fields. For example, if a form contains the caller's email address, use the "Email" label rather than the full label of "Caller Email"** \(**glide.short.labels**\) property.

    The default value is **true**, meaning that the short label is displayed in all forms.

3.  If you want to display the complete label in forms, clear the check box.

4.  Click **Save**.


