---
title: Add screen fields to a record screen
description: Add screen fields to improve the usability of your record screens. Screen fields enable you to change how information is shown in your form or you can provide access to additional elements, such as attachments, videos, or links.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Screen fields, Configure a details screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Add screen fields to a record screen

Add screen fields to improve the usability of your record screens. Screen fields enable you to change how information is shown in your form or you can provide access to additional elements, such as attachments, videos, or links.

## Before you begin

Role required: admin

To add screen fields to your record screen, confirm that you have configured a record screen that contains a details screen. For more information, see [Configure a details screen for a record screen](configure-form-details-screen.md).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **Screens** from the menu.

4.  Select an existing Record screen record.

5.  In the configuration tree, select the Details screen record where you want to add a screen field.

6.  Select a table in the **Data** area of the Details screen field.

7.  Locate the **Screen fields** area and select **New.**

8.  On the Screen field form, fill in the fields.

<table id="table_tsy_nsn_p3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Parent screen

</td><td>

This field is auto-populated, listing the screen where this field is used.

</td></tr><tr><td>

Type

</td><td>

Type of screen field. For a list of types and a description of how they're used, see [Screen fields](../concept/sg-screen-field-enhancements.md).**Note:**

-   Select the **Auto** option to link the field type with the selected **Form Field** option. The **Auto** option includes the following field types: **Text**, **Percentage**, **Image**, **Video**, **File**, **HTML**, **Date**, and **Script**.

**Note:** For more information about using the script screen option, see [Dynamic variable support in record screens](../reference/record-screen-script-type.md).

-   The **Auto** field type doesn't include field types **Attachments List** and **Checklist**. You must manually select these options from the **Type** field.


</td></tr><tr><td>

Form field

</td><td>

Table field that the screen field uses as a data source. Some field types require a specific type of value. These requirements are described in [Screen fields](../concept/sg-screen-field-enhancements.md).**Note:** This option isn't available for the field types **Attachments List** and **Checklist**.

</td></tr><tr><td>

Field name

</td><td>

Enter the name `Attachment` or `Checklist` for this field, this text displays as the field label.**Note:** This option is only available for  the field types **Attachments List ** and **Checklist**.

</td></tr><tr><td>

Record ID field

</td><td>

For the **Attachment list** field type, enter `sys_id`.**Note:** This option is only available for  the field types **Attachments List ** and **Checklist**.

</td></tr><tr><td>

Order

</td><td>

Order in which this field appears. Fields appear on the record screen from the lowest to the highest value.

</td></tr><tr><td>

Hidden

</td><td>

Option to avoid this field from showing on the record screen.

</td></tr><tr><td>

Value Only

</td><td>

Value of the field without the field label.**Note:** This option is only available for  the field types **Auto**, **Text**, **Percentage**, **Date**, and **Script**.

</td></tr></tbody>
</table>9.  Select **Save**.


-   **[Dynamic variable support in record screens](../reference/record-screen-script-type.md)**  
Use the script screen field in record screens to display dynamic field values. The script runs to determine the field value before it displays in your form. The value returned by the script doesn't replace the database value. For example, you can display translated content for dynamic variables within an email.
-   **[Configure the script field for records screens](record-screen-script-type-config.md)**  
Configure script screen fields to display calculated or personalized content in your mobile forms, without modifying the underlying database values.

**Parent Topic:**[Screen fields](../concept/sg-screen-field-enhancements.md)

