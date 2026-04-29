---
title: Create and use a variable in RPA Desktop Design Studio
description: Create a variable in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Build, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Create and use a variable in RPA Desktop Design Studio

Create a variable in RPA Desktop Design Studio.

## Before you begin

Role required: none

## About this task

There are two types of variables:

-   Local: This variable is declared within an activity and can be used only within the declared activity.
-   Global: This variable is declared at a project level and can be used in any activity within the automation workflow.

    Variables have four attributes and they’re assigned during an automation execution at different times:

    -   Identifier
    -   Data Location
    -   Type
    -   Value

## Procedure

1.  To create a local variable, perform either of the following actions:

    -   In the Toolbox pane, navigate to **General** and drag the Variable component to the Design surface.
    -   In the Toolbox pane, navigate to **General** and drag the Variable component onto the activity under the Project Explorer pane.
    -   In the Project Explorer pane, right-click the desired activity and select **Create a Variable**.
2.  To create a global variable, perform either of the following actions:

    -   In the Project Explorer pane, right-click **Global Objects** and select **Create a Variable**.
    -   In the Toolbox pane, navigate to **General** and drag the Variable component to **Global Objects** onto the Project Explorer pane.
3.  If you want to convert a local variable to global, right-click the local variable from Project Explorer and select **Convert to global**.

    You can use this option if you have created a variable as local.

4.  After the variable is created, drag the variable to the Design surface as shown in the following example.

    ![Variable is dragged to the Design surface.](../image/create-variable-drag.png "Variable is dragged to the Design surface")

5.  Connect the data and control ports of the variable to the corresponding ports of the other components.

6.  To assign a variable to either the Data In or the Data Out port, perform the following actions:

    1.  On the Design surface, right-click the Data In or Data Out port of the variable and select **Override**.

    2.  In the PORT PROPERTIES dialog box, click **Select** next to the **Mapped Variable** field to choose a required variable.

        **Note:** If you select this option, the Data In port on the component disappears and the variable name appears on the port.

    3.  In the CHOOSE VARIABLE dialog box, choose a mapped global or a local variable to read or store data depending on whether you want to override the Data In or the Data Out port.

    4.  Click **OK**.

7.  To use variables in either a Data In or a Data Out port, drag the variable onto the Data In or Data Out port on the Design surface as shown in the following example.

    ![Drag the variable to the Data In port on the Design surface.](../image/variable-data-in-port-drag.png "Drag the variable to the Data In port on the Design surface")

    The following example shows the output when the variable is dragged to the Data In port.



    ![Output when the variable is dragged to the Data In port.](../image/varriable-data-port-output.png)

    **Important:** You might come across the following behaviours when you drag and drop an automation component from the Toolbox, Object explorer, Project explorer, and Skills explorer to the Design surface:

    -   If you drag and drop a component to the same component in the Design surface, then the new component replaces the existing component. For example, if you already have the **ActionSet** component on the Design surface and you drag and drop another **ActionSet** component to the existing **ActionSet**, then the new version replaces the existing component.

        All the connections \(control and data connections\), variables, or static data associated to the existing component gets associated to the newly dropped component if the port name and the port data type are the same.

    -   If you drag and drop a new component to a different component or method in the Design surface then the new component replaces the existing component.

        All the connections, variables, or static data associated to the existing component gets associated to the newly dropped component if the port names and the port data types are the same.

    -   If you drag and drop a component between two components that are already connected in the Design surface, then the component is placed between the existing components. You may come across the following behaviours when you drag and drop a component between two components:
        -   If port names and the port data types of the newly dropped component match with the connected components, then the data connections are created.
        -   If the port names are the same and the port data types are different, then the data connections are created only if the port data type is can be converted \(the source port data must be converted to target data type. This is known as typecasting or type conversion. For more information on type casting, see [Java Type Casting](https://www.w3schools.com/java/java_type_casting.asp)\). For example, integer to object but not object to integer.
        -   If the port names are the same and the port data type can be converted, but there is already an existing data connection between the two components, then no new data connection is created.

**Parent Topic:**[Building automations](../concept/rpa-studio-build.md)

