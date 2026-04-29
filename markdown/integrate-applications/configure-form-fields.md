---
title: Configure the form fields for the Form Renderer element
description: Configure the form fields in the Form Renderer element while you are building an attended automation form in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create an attended automation form in RPA Desktop Design Studio, Build, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Configure the form fields for the Form Renderer element

Configure the form fields in the Form Renderer element while you are building an attended automation form in RPA Desktop Design Studio.

## Before you begin

Create an attended automation form in RPA Desktop Design Studio. For more information, see [Create an attended automation form in RPA Desktop Design Studio](create-rda-form.md).

Ensure that your attended automation form contains a Form Renderer element. For more information, see [Form designer for building attended automation forms](../concept/form-designer-overview.md).

Role required: none

## About this task

The Form Renderer element helps you to build forms quickly with the available controls.

## Procedure

1.  In the RPA Desktop Design Studio, from the Project Explorer pane, navigate to **Forms** and expand it.

2.  Right-click the Form Renderer element and select **Configure** to configure the form fields.

3.  In the CONFIGURE FORM FIELDS dialog box, click the add icon \(![Add icon.](../image/add-icon-configure-form-fields.png)\) to add a new **Field** tab.

4.  In the Fields section, expand a Field option and fill in the following details:

<table id="table_omh_kfc_srb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the field that appears as a label name on the form.

</td></tr><tr><td>

Type

</td><td>

Type of the field:-   TextBox
-   ComboBox
-   CheckBox
-   RadioButton
-   ToggleButton
-   Date
-   Time
-   PasswordBox


</td></tr><tr><td>

Required

</td><td>

Option for enabling this field as a required field on the form.

</td></tr><tr><td>

Read Only

</td><td>

Option for enabling this field as a read-only field on the form.

</td></tr><tr><td>

Field Help

</td><td>

Help information for the field:-   None
-   Text
-   Link


</td></tr><tr><td>

Help Text

</td><td>

Help text information for the field.This field appears only when **Text** is selected from the **Field Help** field.

</td></tr><tr><td>

Help Link

</td><td>

Help link URL for the field.This field appears only when **Link** is selected from the **Field Help** field.

</td></tr></tbody>
</table>5.  Click **OK**.

6.  Repeat steps 3 to 5 to add a new field.

7.  To delete a field, do the following actions:

    1.  Expand the field option that you want to delete and click the delete icon \(![Delete icon.](../image/delete-icon-configure-form-fields.png)\).

    2.  In the Confirmation dialog box, click **Yes**.

8.  In the Form Settings section, fill in the fields.

<table id="table_snl_ngc_srb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Title of the form.

</td></tr><tr><td>

Field Help

</td><td>

Help information for the form:-   None
-   Text
-   Link


</td></tr><tr><td>

Help Text

</td><td>

Help text information for the form.This field appears only when **Text** is selected from the **Field Help** field.

</td></tr><tr><td>

Help Link

</td><td>

Help link URL for the form.This field appears only when **Link** is selected from the **Field Help** field.

</td></tr><tr><td>

Show Popups Inside

</td><td>

Option for enabling pop-up windows inside the form.

</td></tr></tbody>
</table>9.  Click **OK**.


**Parent Topic:**[Create an attended automation form in RPA Desktop Design Studio](create-rda-form.md)

**Related topics**  


[Form designer for building attended automation forms](../concept/form-designer-overview.md)

[Methods and events of the Form Renderer element](../reference/form-control-formreneder.md)

