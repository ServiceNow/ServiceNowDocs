---
title: Form designer for building attended automation forms
description: Form designer is an Integrated Development Environment \(IDE\) for building attended automation forms in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Create an attended automation form in RPA Desktop Design Studio, Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Form designer for building attended automation forms

Form designer is an Integrated Development Environment \(IDE\) for building attended automation forms in RPA Desktop Design Studio.

## Form designer overview

A form is a custom interface to interact with multiple applications by using the Forms functionality within the RPA Desktop Design Studio. Forms can be used to insert various elements and arrange them as per the desired layout.

## Access the Form Designer

To access the Form Designer, right-click the desired form in the Project Explorer pane and select **Design**.

## Sections of the Form Designer

Form Designer has four parts as shown in the following example:

-   Toolbox pane: The elements used for designing the form are displayed in the example.
-   Outline pane: Lists the elements and resources in the form. You can view and focus on a specific element of the form, as you are designing the form.
-   Design surface: Create designs by selecting elements from the Toolbox pane and drawing on the form within the Design surface.
-   Properties pane: View and edit the properties of an element or a window in the form that help to fine-tune its functionality. The important properties are highlighted in bold.

![Form Designer dialog box.](../image/form-designer.png "Form Designer dialog box")

## Details of the Toolbox pane elements

The following elements from the Toolbox pane can be used to design the form.

<table id="table_hpq_h11_wrb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Button](../reference/form-control-button.md)

</td><td>

Helps you to add one or more buttons on the form. Enables the user to click it to perform an action.

</td></tr><tr><td>

[TextBlock](../reference/form-control-textblock.md)

</td><td>

Helps you to add a label on the form. Enables the user to view a text block as read-only information.

</td></tr><tr><td>

[TextBox](../reference/form-control-textbox.md)

</td><td>

Helps you to add a text box to the form. Enables the user to provide information to the form within a text box.

</td></tr><tr><td>

[Date](../reference/form-control-date.md)

</td><td>

Helps you to provide a date picker on the form. Enables the user to select a specific date on the form.

</td></tr><tr><td>

[Time](../reference/form-control-time.md)

</td><td>

Helps you to provide a time picker on the form. Enables the user to select a specific time on the form.

</td></tr><tr><td>

[DateTime](../reference/form-control-datetime.md)

</td><td>

Helps you to provide a date and time picker on the form. Enables the user to select a specific date and time on the form.

</td></tr><tr><td>

[CheckBox](../reference/form-control-checkbox.md)

</td><td>

Helps you to present yes, no, true, or false selections.You can also use the check box element in groups to display multiple choices in a form.

</td></tr><tr><td>

[RadioButton](../reference/form-control-radiobutton.md)

</td><td>

Enables you to select a choice from the group of choices.

</td></tr><tr><td>

[ComboBox](../reference/form-control-combobox.md)

</td><td>

Displays the data in a drop-down combination box. By default, the ComboBox element appears in two parts.

 The top part is a text box that enables you to type a list item.

 The second part is a list box that displays a list of items that you can select from.

</td></tr><tr><td>

[ListBox](../reference/form-control-listbox.md)

</td><td>

Displays a list of items that you can select one or more Items from.

</td></tr><tr><td>

[DataGrid](../reference/form-control-datagrid.md)

</td><td>

Enables you to display and manipulate the tabular data.

</td></tr><tr><td>

[PasswordBox](../reference/form-control-passwordbox.md)

</td><td>

Displays placeholder characters while you type a string.

</td></tr><tr><td>

[ImageControl](../reference/form-control-imagecontrol.md)

</td><td>

Displays images in the form.

</td></tr><tr><td>

[ImageViewer](../reference/form-control-imageviewer.md)

</td><td>

Enables you to open and view image files including JPEG, GIF, WMF, and other image formats. It also provides options to stretch the images, shrink the images, and rotate the images at different angles through all axis.

</td></tr><tr><td>

GroupBox

</td><td>

Provides an identifiable grouping for other elements. Typically, you use group boxes to subdivide a form by function.

</td></tr><tr><td>

[TabControl](../reference/form-control-tabcontrol.md)

</td><td>

Helps you add one or more tabs in your form.

</td></tr><tr><td>

ScrollViewer

</td><td>

Enables you to add a scrolling functionality to the form.

</td></tr><tr><td>

Grid

</td><td>

Defines a flexible grid area that consists of columns and rows.

</td></tr><tr><td>

GridSpiltter

</td><td>

Helps you to split a grid element into multiple parts.

</td></tr><tr><td>

[Web Browser](../reference/form-control-webbrowser.md)

</td><td>

Hosts web pages and provides web browsing capabilities to your application.

</td></tr><tr><td>

[Form Renderer](../reference/form-control-formreneder.md)

</td><td>

Helps you build forms quickly with the following controls:-   TextBox
-   ComboBox
-   CheckBox
-   RadioButton
-   ToggleButton
-   Date
-   Time
-   PasswordBox

</td></tr><tr><td>

Border

</td><td>

Enables you to draw a border, background, or both with the form.

</td></tr></tbody>
</table>**Parent Topic:**[Create an attended automation form in RPA Desktop Design Studio](../task/create-rda-form.md)

**Related topics**  


[Methods and events of an attended automation form](../reference/form-methods-events.md)

[Methods and events of elements](../reference/form-control-methods-events.md)

