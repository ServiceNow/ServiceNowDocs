---
title: Form designer for building attended automation forms
description: Form designer is an Integrated Development Environment \(IDE\) for building attended automation forms in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/form-designer-overview.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
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

\[Omitted image "form-designer.png"\] Alt text: Form Designer dialog box.

## Details of the Toolbox pane elements

The following elements from the Toolbox pane can be used to design the form.

<table id="table_hpq_h11_wrb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Button](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-button.md)

</td><td>

Helps you to add one or more buttons on the form. Enables the user to click it to perform an action.

</td></tr><tr><td>

[TextBlock](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-textblock.md)

</td><td>

Helps you to add a label on the form. Enables the user to view a text block as read-only information.

</td></tr><tr><td>

[TextBox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-textbox.md)

</td><td>

Helps you to add a text box to the form. Enables the user to provide information to the form within a text box.

</td></tr><tr><td>

[Date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-date.md)

</td><td>

Helps you to provide a date picker on the form. Enables the user to select a specific date on the form.

</td></tr><tr><td>

[Time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-time.md)

</td><td>

Helps you to provide a time picker on the form. Enables the user to select a specific time on the form.

</td></tr><tr><td>

[DateTime](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-datetime.md)

</td><td>

Helps you to provide a date and time picker on the form. Enables the user to select a specific date and time on the form.

</td></tr><tr><td>

[CheckBox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-checkbox.md)

</td><td>

Helps you to present yes, no, true, or false selections.You can also use the check box element in groups to display multiple choices in a form.

</td></tr><tr><td>

[RadioButton](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-radiobutton.md)

</td><td>

Enables you to select a choice from the group of choices.

</td></tr><tr><td>

[ComboBox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-combobox.md)

</td><td>

Displays the data in a drop-down combination box. By default, the ComboBox element appears in two parts.

 The top part is a text box that enables you to type a list item.

 The second part is a list box that displays a list of items that you can select from.

</td></tr><tr><td>

[ListBox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-listbox.md)

</td><td>

Displays a list of items that you can select one or more Items from.

</td></tr><tr><td>

[DataGrid](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-datagrid.md)

</td><td>

Enables you to display and manipulate the tabular data.

</td></tr><tr><td>

[PasswordBox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-passwordbox.md)

</td><td>

Displays placeholder characters while you type a string.

</td></tr><tr><td>

[ImageControl](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-imagecontrol.md)

</td><td>

Displays images in the form.

</td></tr><tr><td>

[ImageViewer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-imageviewer.md)

</td><td>

Enables you to open and view image files including JPEG, GIF, WMF, and other image formats. It also provides options to stretch the images, shrink the images, and rotate the images at different angles through all axis.

</td></tr><tr><td>

GroupBox

</td><td>

Provides an identifiable grouping for other elements. Typically, you use group boxes to subdivide a form by function.

</td></tr><tr><td>

[TabControl](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-tabcontrol.md)

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

[Web Browser](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-webbrowser.md)

</td><td>

Hosts web pages and provides web browsing capabilities to your application.

</td></tr><tr><td>

[Form Renderer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-formreneder.md)

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
</table>**Parent Topic:**[Create an attended automation form in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-rda-form.md)

**Related topics**  


[Methods and events of an attended automation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-methods-events.md)

[Methods and events of elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-methods-events.md)

