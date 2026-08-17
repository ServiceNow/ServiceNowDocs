---
title: Create an attended automation form in RPA Desktop Design Studio
description: Design attended automations by creating an attended user interface \(UI\) form in RPA Desktop Design Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/create-rda-form.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Build, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Create an attended automation form in RPA Desktop Design Studio

Design attended automations by creating an attended user interface \(UI\) form in RPA Desktop Design Studio.

## Before you begin

Ensure that the project type is **Attended Automation**. For more information, see [Create an automation project manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-automation-project.md).

Role required: none

## About this task

An attended automation form is a container for all the elements that make up the UI. A form is a custom interface that you can use to interact with multiple applications within the RPA Desktop Design Studio. You can use forms to insert various elements and arrange them in layouts.

## Procedure

1.  In the RPA Desktop Design Studio, from the Project Explorer pane, navigate to **Forms** and expand it.

2.  Choose an option and complete the action.

<table id="choicetable_ehw_rzz_vrb"><thead><tr><th align="left" id="d281309e94">

Option

</th><th align="left" id="d281309e97">

Action

</th></tr></thead><tbody><tr><td id="d281309e103">

**To create a new form**

</td><td>

Right-click **Forms** in the Project Explorer pane and select **New Form**.

</td></tr><tr><td id="d281309e118">

**To access the Form Designer**

</td><td>

Right-click a form in the Project Explorer pane and select **Design**.For more information on the Form Designer, see [Form designer for building attended automation forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-designer-overview.md).

</td></tr></tbody>
</table>3.  In the Form Designer, from the Toolbox pane, select an element that you want to add to your form and draw it on the Design surface.

    For example, to draw a text block on the form, select the TextBlock element from the Toolbox pane and draw it on the Design surface. Similarly, select the TextBox and Button element and draw them on the Design surface, as shown in the following example.

    \[Omitted image "form-designer-textblock.png"\] Alt text: TextBlock, TextBox, and Button element on the Design Surface.

4.  In the Form Designer, from the Properties pane, update the name of an element in the **Name** field, as shown in the following example.

    \[Omitted image "form-designer-textblock-name.png"\] Alt text: Update the Name field in the Properties pane.

5.  Choose an option and complete the action.

<table id="choicetable_zm4_lwz_vrb"><thead><tr><th align="left" id="d281309e199">

Option

</th><th align="left" id="d281309e202">

Action

</th></tr></thead><tbody><tr><td id="d281309e208">

**To edit the properties of an element**

</td><td>

Select the desired element in the Outline pane or on the Design surface and edit the required properties in the Properties pane.For example, to edit the display label of the TextBlock element, enter a label in the **Text** field in the Properties pane, as shown in the following example.

 \[Omitted image "form-designer-text-name-change.png"\] Alt text: Enter a name in the Text field in the Properties pane.

</td></tr><tr><td id="d281309e236">

**To edit the properties of a window**

</td><td>

Select the window in the Outline pane and edit the required properties in the Properties pane.For example, to resize the window, select an option from the **ResizeMode** field in the Properties pane, as shown in the following example.

 \[Omitted image "form-designer-window-properties.png"\] Alt text: Resize the window in the ResizeMode field in the Properties pane.

</td></tr><tr><td id="d281309e264">

**To arrange the elements**

</td><td>

Move them as required in the Outline pane.

</td></tr><tr><td id="d281309e273">

**To view the added elements under the desired form**

</td><td>

Perform the following actions:1.  In the Project Explorer pane, close the form in which you added the elements.
2.  Expand the form and view the elements that are added under the form as shown in the following example.

\[Omitted image "elements-form-appear.png"\] Alt text: Elements appear under the form.

</td></tr><tr><td id="d281309e304">

**To delete an element on the Design surface**

</td><td>

In the Outline pane, right-click the element to be deleted and select **Delete**.

</td></tr><tr><td id="d281309e316">

**To view the methods and events for a form**

</td><td>

Double-click the created form in the Project Explorer pane.The methods and events are displayed in the Object Explorer pane. For more information, see [Methods and events of an attended automation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-methods-events.md).

</td></tr><tr><td id="d281309e338">

**To view the methods and events for an element**

</td><td>

Double-click the element in the Toolbox pane of the Form Designer.The methods and events are displayed in the Object Explorer pane. For more information, see [Methods and events of elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-methods-events.md).

</td></tr><tr><td id="d281309e357">

**To delete a form**

</td><td>

Do the following actions:1.  Delete all the references of the elements that are used in other activities, if any.

Use the **Find All References** option to do this step.

2.  In the Project Explorer pane, right-click the form and select **Delete**.
3.  In the Confirmation dialog box, select **Yes**.


</td></tr><tr><td id="d281309e389">

**To find all the references of an element that are used in other activities**

</td><td>

Right-click the desired form in the Project Explorer pane and select **Find All References**.Results are displayed in the Find All References dialog box.

</td></tr><tr><td id="d281309e404">

**To rename a form**

</td><td>

Do any of the following actions:-   In the Project Explorer pane, right-click the form and select **Rename** to enter a new name.
-   Double-click the form and in the Properties pane, change the name in the **Name** field.


</td></tr></tbody>
</table>
-   **[Form designer for building attended automation forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-designer-overview.md)**  
Form designer is an Integrated Development Environment \(IDE\) for building attended automation forms in RPA Desktop Design Studio.
-   **[Configure the form fields for the Form Renderer element](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-form-fields.md)**  
Configure the form fields in the Form Renderer element while you are building an attended automation form in RPA Desktop Design Studio.

**Parent Topic:**[Building automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/rpa-studio-build.md)

**Related topics**  


[Methods and events of an attended automation form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-methods-events.md)

[Methods and events of elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/form-control-methods-events.md)

