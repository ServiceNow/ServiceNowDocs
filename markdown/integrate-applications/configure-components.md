---
title: Use a component in RPA Desktop Design Studio
description: Design automation projects by using components in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Use, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Use a component in RPA Desktop Design Studio

Design automation projects by using components in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

Components are reusable blocks that are used for designing automations and to abstract functionality.

RPA Desktop Design Studio hosts a wide range of components that you can use while you’re creating automation projects.

Each component has ports that are used while creating an automation workflow. For more information, see [RPA Desktop Design Studio ports](../concept/overview-ports-rpa-studio.md).

Enhance the automation logic with text instructions, either in an empty activity or by selecting a component in an existing one by using the Now Assist for RPA Hub application. For more information, see [Build an automation with Now Assist](build-automation-now-assist.md).

## Procedure

1.  In the RPA Desktop Design Studio, from the Toolbox pane, navigate to a parent component category to select a component.

2.  To use a component, drag a component to the Design surface as shown in the following example.

    ![Use an OCR Text component.](../image/component-ex-ocr-tex.png "Drag the OCR Text component to the Design surface")

    **Important:** You might come across the following behaviours when you drag and drop an automation component from the Toolbox, Object explorer, Project explorer, and Skills explorer to the Design surface:

    -   If you drag and drop a component to the same component in the Design surface, then the new component replaces the existing component. For example, if you already have the **ActionSet** component on the Design surface and you drag and drop another **ActionSet** component to the existing **ActionSet**, then the new version replaces the existing component.

        All the connections \(control and data connections\), variables, or static data associated to the existing component gets associated to the newly dropped component if the port name and the port data type are the same.

    -   If you drag and drop a new component to a different component or method in the Design surface then the new component replaces the existing component.

        All the connections, variables, or static data associated to the existing component gets associated to the newly dropped component if the port names and the port data types are the same.

    -   If you drag and drop a component between two components that are already connected in the Design surface, then the component is placed between the existing components. You may come across the following behaviours when you drag and drop a component between two components:
        -   If the port names and the port data types of the newly dropped component match with the connected components, then the data connections are created.
        -   If the port names are the same and the port data types are different, then the data connections are created only if the port data type is can be converted \(the source port data must be converted to target data type. This is known as typecasting or type conversion. For more information on type casting, see [Java Type Casting](https://www.w3schools.com/java/java_type_casting.asp)\). For example, integer to object but not object to integer.
        -   If the port names are the same and the port data type can be converted, but there is already an existing data connection between the two components, then no new data connection is created.
3.  Connect the following ports:

    1.  Connect the Control In port of the OCR Text component with the Control Out port of another component.

    2.  Connect the Control Out port of the OCR Text component with the Control In port of the next component.

    3.  Connect the Data In \(Bitmap\) port of the OCR Text component with the Data Out port of another component.

    4.  Connect the Data Out \(String\) with the Data In port of another component.

4.  Do any of the following options for a desired action.

<table id="choicetable_vmv_2f1_5rb"><thead><tr><th align="left" id="d258818e213">

Option

</th><th align="left" id="d258818e216">

Action

</th></tr></thead><tbody><tr><td id="d258818e222">

**Search for a component that is available within the Toolbox**

</td><td>

Enter the text in the **Filter by Name** field.

</td></tr><tr><td id="d258818e234">

**Edit the configuration or settings of a component**

</td><td>

Either double-click the component title bar or click the settings icon \(![Settings icon.](../image/component-settings-icon.png)\). For example, to edit the settings of the OCR Text component, click the settings icon \(![Settings icon.](../image/component-settings-icon.png)\) over the OCR Text component. The OCR SETTINGS dialog box appears. You can define the properties in the dialog box that is shown in the following example.

 ![OCR Settings dialog box.](../image/ocr-settings.png "OCR Settings dialog box")

 The settings icon \(![Settings icon.](../image/component-settings-icon.png)\) doesn't appear for all components.

</td></tr><tr><td id="d258818e279">

**Edit the properties of a component**

</td><td>

Change the required property in the Properties pane.

</td></tr><tr><td id="d258818e288">

**Set a breakpoint**

</td><td>

Right-click the component title bar and select **Breakpoint** For more information on Breakpoints, see [Set a breakpoint to pause a component in RPA Desktop Design Studio](set-breakpoint-rpa-studio.md).

</td></tr><tr><td id="d258818e311">

**Start the workflow execution from a selected component**

</td><td>

Right-click the component title bar and select **Run From Here**.

</td></tr><tr><td id="d258818e323">

**Handle the errors at a component level**

</td><td>

Right-click the component title bar and select **Error Handler** To learn more about handling errors, see [Handle errors in RPA Desktop Design Studio](error-handling-rpa-studio.md).

</td></tr><tr><td id="d258818e348">

**Delete a component**

</td><td>

Right-click the component title bar and select **Delete**.

</td></tr><tr><td id="d258818e360">

**Skip a component in an automation**

</td><td>

To enable the automation to skip a component, right-click the component title bar and select **Skip This**.**Note:**

-   If you set a breakpoint and the **Skip This** option on the same component, the automation still skips the component and moves to the next executable component.
-   If you use the **Skip This** option on the **For Each** and **For Loop** components under the **Loop** section in the Toolbox, the automation doesn't execute the Loop part of those components.
-   If you use the **Skip This** option on the **Try Catch** component, the automation skips the component and exceptions, if any, appear in the respective component in the automation.
-   If you use the **Skip This** option on a component where you have set a delay using the **Delay After Execution** or **Delay Before Execution** options, the automation still skips the component.
-   The **Skip This** option ignores the Decision component and dependencies on the component, if any.
-   You can't use the **Skip This** option on the **Start**, **End**, or any event-related component.


</td></tr><tr><td id="d258818e438">

**Execute a single component**

</td><td>

To test and debug any issue in an automation by isolating a single component, right-click the component title bar and select **Run This**.**Note:**

-   If you apply a breakpoint on a component before or after applying the **Run This** option, the breakpoint pauses the execution of the component.
-   In the For Loop component, the **Run This** option completes the loop that you specify but the execution doesn't proceed to the Control Out port.
-   If you set a delay in the execution of a component using the **Delay After Execution** or **Delay Before Execution** options and then use the **Run This** option, the component will execute after the delay that you have set.
-   You can't use the **Run This** option on any event-related component.


</td></tr></tbody>
</table>5.  To search for a component that is available within the Toolbox, enter the text in the **Filter by Name** field.


**Parent Topic:**[Using automations](../concept/rpa-studio-use.md)

**Related topics**  


[Set a breakpoint to pause a component in RPA Desktop Design Studio](set-breakpoint-rpa-studio.md)

[Start a workflow execution from a selected component in RPA Desktop Design Studio](run-from-here-rpa-studio.md)

[Handle errors in RPA Desktop Design Studio](error-handling-rpa-studio.md)

[Build an automation with Now Assist](build-automation-now-assist.md)

