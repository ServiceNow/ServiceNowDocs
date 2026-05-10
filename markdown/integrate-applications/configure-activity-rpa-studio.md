---
title: Create and use an activity in RPA Desktop Design Studio
description: Create and use an activity to provide modularity to an automation project in RPA Desktop Design Studio.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Build, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Create and use an activity in RPA Desktop Design Studio

Create and use an activity to provide modularity to an automation project in RPA Desktop Design Studio.

## Before you begin

Set up the RPA Desktop Design Studio application and add the ServiceNow instance details. For more information, see [Set up RPA Desktop Design Studio](set-up-rpa-studio.md).

Role required: none

## About this task

Activities are a reusable set of instructions that are designed for an automation on the Design surface of RPA Desktop Design Studio.

You can design automation workflows in an activity on the Design surface by using various components.

Each activity contains two components by default: Start and End. These components can't be deleted because they are the starting and ending points of the activity.

You can reuse each activity multiple times within the same automation project by dragging the activity to the Design surface. You can also import activities in different automation projects.

To create an activity using Now Assist, see [Create an activity with Now Assist](create-activity-now-assist.md).

## Procedure

1.  In the Project Explorer pane, navigate to **Activities**.

    The Activities section lists all the activities that are created under each project. By default, a Main activity is created when a new project is initiated. The automation execution starts from the startup activity, in this case, Main activity as shown in the following example.

    ![Main activity is created when a new project is initiated.](../image/main-activity-proj-exp.png)

2.  Do any of the following options for a desired action.

<table id="choicetable_zm4_lwz_vrb"><thead><tr><th align="left" id="d492843e140">

Option

</th><th align="left" id="d492843e143">

Action

</th></tr></thead><tbody><tr><td id="d492843e149">

**To create a new activity**

</td><td>

Right-click **Activities** in the Project Explorer pane and select **New Activity**.

</td></tr><tr><td id="d492843e164">

**To create a new activity with Now Assist**

</td><td>

Right-click **Activities** in the Project Explorer pane and select **New activity using Now Assist**. For more information, see [Create an activity with Now Assist](create-activity-now-assist.md).To access the Now Assist for RPA Hub feature in RPA Desktop Design Studio, perform the following steps:

-   Install the Now Assist for RPA Hub application to add the generative AI capability. For more information, see [Configure Now Assist for RPA Hub](configure-now-assist-rpa-hub.md).
-   Turn on the RPA bot generation skill to use the generative AI capability. For more information, see [Turn on the RPA bot generation skill](turn-rpa-bot-generation-skill.md).
-   After activating the RPA bot generation skill, relaunch the RPA Desktop Design Studio application to apply the modified settings.
If you skip these steps, the Now Assist for RPA Hub feature doesn’t appear in RPA Desktop Design Studio.

</td></tr><tr><td id="d492843e246">

**To rename an activity**

</td><td>

Do one of the following actions:-   In the Project Explorer pane, right-click the activity and select **Rename** to enter a new name.
-   Double-click the activity and in the Properties pane, change the name in the **Name** field.
 For example, Test 1 and Test 2.

</td></tr><tr><td id="d492843e273">

**To add the input parameters to an activity**

</td><td>

Click the plus icon \(![Plus icon.](../image/add-image-icon.png)\) on the Start component.When you drag this activity into another activity, the input parameters appear as Data Input ports.

</td></tr><tr><td id="d492843e292">

**To add the output parameters to an activity**

</td><td>

Click the plus icon \(![Plus icon.](../image/add-image-icon.png)\) on the End component.When you drag this activity in another activity, the output parameters appear as Data Output ports.

</td></tr><tr><td id="d492843e310">

**To open an activity on the Design surface**

</td><td>

Double-click the activity.

</td></tr><tr><td id="d492843e319">

**To set a particular activity as the starting point for the automation project**

</td><td>

Right-click the activity and select **Mark As Startup**.By default, the Main Activity is marked as start up.

 When you click **Run** under the **Design** tab to run this project, the automation begins from the activity that is marked as startup.

</td></tr><tr><td id="d492843e343">

**To reuse an activity within the same automation project**

</td><td>

Drag the activity to the desired Design surface of the activity.

</td></tr><tr><td id="d492843e352">

**To reuse an activity in a different automation project**

</td><td>

Perform the steps in the [Import project in RPA Desktop Design Studio](import-project-activities.md).

</td></tr><tr><td id="d492843e371">

**To handle the errors at an activity level**

</td><td>

Right-click the desired activity and select **Error Handler**.

</td></tr><tr><td id="d492843e384">

**To create a local variable**

</td><td>

Right-click the desired activity and select **Create a Variable**.

</td></tr><tr><td id="d492843e396">

**To create a copy of an activity**

</td><td>

Right-click the desired activity and select **Create a Copy**.For example, if you are creating a copy of the Test 1 activity, a new activity is created as Test1\_Copy under the Activities section.

</td></tr><tr><td id="d492843e411">

**To find all the references of an activity that are used in other activities**

</td><td>

Right-click the desired activity in the Project Explorer pane and select **Find All References**.Results are displayed in the Find All References dialog box.

</td></tr><tr><td id="d492843e426">

**To delete an activity**

</td><td>

Do the following:1.  Delete all the references that are used in other activities, if any. Use the **Find All References** option to do this step.
2.  In the Project Explorer pane, right-click the activity and select **Delete**.
3.  In the Confirmation dialog box, select **Yes**.


</td></tr><tr><td id="d492843e456">

**To resolve conflicts when merging changes from multiple sources of an activity**

</td><td>

Right-click the desired activity in the Project Explorer pane and select **Source Control**. The COMPARE PROCESSES dialog box appears and the changes are highlighted as shown in the following example.

 ![Compare Processes dialog box.](../image/source-control-activity.png "Compare Processes dialog box")

 For more information, see [Resolve conflicts when merging changes from multiple sources of the same activity](source-control-rpa-studio.md).

</td></tr><tr><td id="d492843e500">

**To execute and test the automation of the project that includes all activities**

</td><td>

Do the following:1.  Consolidate all the activities in a single Main activity and arrange them in the execution order to execute the entire automation, as shown in the following example.

![Consolidate Test 1 and Test 2 activities in a single Main activity.](../image/tes1-test2-activities.png "Consolidate Test 1 and Test 2 activities in a single Main activity")

2.  Click **Run** under the **Design** tab to execute the entire automation designed in these two activities.

In this example, the Main activity is marked as startup, which executes the Test 1 activity followed by the Test 2 activity.

</td></tr></tbody>
</table>    **Important:** You might come across the following behaviours when you drag and drop an automation component from the Toolbox, Object explorer, Project explorer, and Skills explorer to the Design surface:

    -   If you drag and drop a component to the same component in the Design surface, then the new component replaces the existing component. For example, if you already have the **ActionSet** component on the Design surface and you drag and drop another **ActionSet** component to the existing **ActionSet**, then the new version replaces the existing component.

        All the connections \(control and data connections\), variables, or static data associated to the existing component gets associated to the newly dropped component if the port name and the port data type are the same.

    -   If you drag and drop a new component to a different component or method in the Design surface then the new component replaces the existing component.

        All the connections, variables, or static data associated to the existing component gets associated to the newly dropped component if the port names and the port data types are the same.

    -   If you drag and drop a component between two components that are already connected in the Design surface, then the component is placed between the existing components. You may come across the following behaviours when you drag and drop a component between two components:
        -   If port names and the port data types of the newly dropped component match with the connected components, then the data connections are created.
        -   If the port names are the same and the port data types are different, then the data connections are created only if the port data type is can be converted \(the source port data must be converted to target data type. This is known as typecasting or type conversion. For more information on type casting, see [Java Type Casting](https://www.w3schools.com/java/java_type_casting.asp)\). For example, integer to object but not object to integer.
        -   If the port names are the same and the port data type can be converted, but there is already an existing data connection between the two components, then no new data connection is created.

**Parent Topic:**[Building automations](../concept/rpa-studio-build.md)

**Related topics**  


[Handle errors in RPA Desktop Design Studio](error-handling-rpa-studio.md)

[Create and use a variable in RPA Desktop Design Studio](configure-variables-rpa-studio.md)

