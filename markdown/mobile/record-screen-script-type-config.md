---
title: Configure the script field for records screens
description: Configure script screen fields to display calculated or personalized content in your mobile forms, without modifying the underlying database values.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Add screen fields to a record screen, Screen fields, Configure a details screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure the script field for records screens

Configure script screen fields to display calculated or personalized content in your mobile forms, without modifying the underlying database values.

## Before you begin

Role required: admin

**Note:** For use cases and examples of how the script screen field is used, see [Dynamic variable support in record screens](../reference/record-screen-script-type.md).

## Procedure

1.  In the web-based UI, enter `sys_sg_screen_field.list` in the filter navigator.

2.  Select either an existing form field or select **New** to open the Screen fields page.

3.  On the Screen fields page, fill in the required fields.

<table id="table_ktr_wbt_k3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Type of screen field. For a list of types and a description of how they're used, see [Screen fields](../concept/sg-screen-field-enhancements.md).For this configuration, select **Script**.

</td></tr><tr><td>

Form field

</td><td>

Table field that the screen field uses as a data source. Select a field that contains the dynamic variable you want to use for the script.

</td></tr><tr><td>

Hidden

</td><td>

Option to avoid this field from showing on the record screen.

</td></tr><tr><td>

Order

</td><td>

Order in which this field appears. Fields appear on the record screen from the lowest to the highest value.

</td></tr><tr><td>

Value only

</td><td>

Value of the field without the field label.

</td></tr><tr><td>

Screen

</td><td>

Record screen field that displays data from the table field specified in **Form Field** field.

</td></tr><tr><td>

Execution script

</td><td>

Script that runs when the record screen is displayed. The script must return a JSON object containing the Type and Value to display.

</td></tr></tbody>
</table>4.  Select **Script** from the **Type** field.

5.  From the **Screen** field, select the record screen where the execution script is to be activated.

6.  Enter your script in the **Execution Script** area, including any dynamic variables.

    **Note:** For configuration information, see [Dynamic variable support in record screens](../reference/record-screen-script-type.md).

7.  Select **Submit**.


**Parent Topic:**[Add screen fields to a record screen](sg-mobile-add-screen-field.md)

