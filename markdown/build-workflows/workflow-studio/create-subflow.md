---
title: Create a subflow in Workflow Studio
description: Reuse an entire flow's content as a subflow. Define the input data the subflow uses and the output data it generates. Call subflows from other flows or script.​
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Building subflows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a subflow in Workflow Studio

Reuse an entire flow's content as a subflow. Define the input data the subflow uses and the output data it generates. Call subflows from other flows or script.​

## Before you begin

[Set up an application in Guided Application Creator](https://www.servicenow.com/docs/access?context=set-up-app&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) to store Workflow Studio content.

Role required: flow\_designer or admin

## About this task

Users with the flow\_designer or admin role should know the application table structure and be aware of any existing business logic associated with the target tables of a flow or subflow. Be sure to disable any conflicting business rules or workflows before creating a flow or subflow.

Creating a custom application to contain your Workflow Studio content allows you to [deploy](https://www.servicenow.com/docs/access?context=c_SharingApplications&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) it using the application repository or the ServiceNow Store.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click **New** &gt; **Subflow**.

    The Subflow properties screen displays.

3.  Fill in the following fields:

<table id="table_kt4_t1l_mcb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subflow name

</td><td>

Name of the subflow.

</td></tr><tr><td>

Description

</td><td>

Description of the subflow.

</td></tr><tr><td>

Application

</td><td>

Application scope to create the subflow in.

</td></tr><tr><td>

Domain

</td><td>

Domain scope of the subflow. For more information about domain separation, see [Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

</td></tr><tr><td colspan="2">

**Additional properties**

</td></tr><tr><td>

Accessible From

</td><td>

Accessible from all application scoped or only within the specified application scope.

</td></tr><tr><td>

Category

</td><td>

Defined category within the application scope for a subflow. Beginning with the Xanadu release, you can create a custom category to organize your subflows.

</td></tr><tr><td>

Protection

</td><td>

Select whether the subflow is read-only. You can only select a value when you create the subflow in an application scope you own. The default value is None.

</td></tr><tr><td>

Subflow annotation

</td><td>

Help text that appears under the subflow title in Workflow Studio to help flow authors understand what the subflow does when used in a flow.

</td></tr><tr><td>

Run as

</td><td>

Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows. Running as the initiating user also ensures the actions taken during flow execution are limited by the user's ACL restrictions. Flows run by the initiating user will also respect user-specific settings like date/time format.**Note:** When choosing the option to run as the user who initiates the session, ensure that your security restrictions do not prevent your users from making any changes the flow executes.

</td></tr><tr><td>

Run with roles

</td><td>

Roles that the flow runs with. This option is only available when **Run as** is set to **user who initiates the session**.

</td></tr><tr><td>

Flow priority default

</td><td>

Priority level at which you want the system to run this subflow by default. Options include:

-   Low
-   Medium \(Default\)
-   High
 To learn about flow priority levels, see [Flow priority](../concept/flow-priority.md).

</td></tr></tbody>
</table>4.  Create subflow inputs to specify the data available to the subflow when it starts running.

    Each input you define for a subflow becomes a configuration option in the Workflow Studio interface. To use the subflow in a flow, you must define a value for each mandatory input. The more inputs a subflow has, the more data you must define and the more familiar you must be with the underlying data model to use the subflow effectively.

    1.  Click **+** to open the Inputs &amp; Outputs pane.

    2.  Click **+** to add a new input.

    3.  Define the name and type for the input.

        **Note:** Subflow input names can't include any of the following reserved system names:

        -   sys\_id
        -   sys\_created\_by
        -   sys\_created\_on
        -   sys\_updated\_on
        -   sys\_updated\_by
        -   sys\_mod\_count
    4.  To make the input a mandatory configuration option, select the **Mandatory** flag.

    5.  Click ![Open icon](../images/icon-advanced-input.png) to view the advanced options and define values.

        Inputs provide advanced options based on their data type. All inputs have advanced options to add a hint or provide a default value. Use advanced options to guide flow designers through adding and configuring a subflow to a flow. For example, create a choice input to provide flow designers with a pre-defined list of configuration options to choose from. For more information about the configuration options available to particular data types, see [field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

5.  Create subflow outputs by defining the names and data types.

    Subflow outputs specify the data available to the parent flow after the subflow completes.

    1.  Click **+** to add a new output.

    2.  Define the name and the data type.

        Output values are assigned in later steps.

        **Note:** Subflow output names can't include any of the following reserved system names:

        -   sys\_id
        -   sys\_created\_by
        -   sys\_created\_on
        -   sys\_updated\_on
        -   sys\_updated\_by
        -   sys\_mod\_count
    ![Inputs and outputs in a subflow.](../images/subflow-inputs-outputs.png)

6.  To add actions, flows, subflows, or flow logic, select **Add an Action, Flow Logic, or Subflow**.

    1.  Select an option.

<table id="table_smq_3ys_tcb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Select the desired action. Workflow Studio includes [Workflow Studio actions](../concept/flow-actions.md) that are available to flows and subflows. Alternatively, a user with the action\_designer role can create additional actions to add to flows. The [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) and [Spokes](../concept/spokes.md) plugins install additional actions.

 To add draft actions from the More Actions menu, set **Show draft actions** to **true**.

 To view spokes that are available in the ServiceNow Store, set **Show store spokes** to **true** from the More Actions menu.

**Note:** Under **Not Installed Spokes**, the system displays spokes that are available in the ServiceNow Store based on compatibility with the ServiceNow version and application dependency on Workflow Studio.

</td></tr><tr><td>

Flow Logic

</td><td>

Select an option to specify conditional or repeated operations.

</td></tr><tr><td>

Subflow

</td><td>

Select a published subflow and define the input values. In addition to adding a subflow as a flow action, you can enable the **Show triggered flows** option from the More Actions menu to select an activated flow and define the required inputs. Running a triggered flow ignores its trigger conditions and runs all actions.

</td></tr></tbody>
</table>        To change the order of an action in a flow, drag the handle on the left side of the action to the desired location.

        The system displays a set of fields depending on the option that you selected.

    2.  To configure the action, flow logic, or subflow, fill in the fields.

    3.  Select **Done**.

    4.  Repeat adding actions until complete.

7.  Assign subflow outputs to a value.

    You can assign a subflow output to multiple values, enabling you to create conditional outputs based on flow logic.

    1.  Under **Actions**, click **+** and select **Flow Logic**.

    2.  Click **Assign Subflow Outputs**.

    3.  In the **Name** field, select an output you created in the Inputs &amp; Outputs section.

        You can assign values onlyl to outputs that have already been given a name and data type.

    4.  In the **Data** field, enter a value or select a data pill from the data panel.

    5.  Click **Done**.


## What to do next

Test the subflow, and publish it when it is ready to be added to a flow or called from a script.

**Note:** You can only test or publish subflows that contain at least one action.

**Parent Topic:**[Building subflows](../concept/subflows.md)

