---
title: Automate recovery tasks
description: Automate the manual recovery task within the business continuity plan. You can classify the manual recovery task as an automated task first and then attach an automated flow to it.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Automate recovery tasks

Automate the manual recovery task within the business continuity plan. You can classify the manual recovery task as an automated task first and then attach an automated flow to it.

## Before you begin

Role required: admin for the Workflow Studio, sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## About this task

Administrators or low-code developers are responsible for building the automation flow. Users with the BCM planner or above role then attach the automation flow to the recovery task. The Workflow Studio is used for this purpose, requiring a local developer persona due to permission restrictions. The Workflow Studio role does not require any extra licensing. However, it requires some special roles. For more information on the Workflow Studio roles and permissions, see User access to Workflow Studio flows.

The flow setup involves these steps:

1.  User defines the permissions to verify the appropriate access and control and creates a subflow to handle the automation process.
2.  User then defines the inputs to provide necessary information for the automation flow.
3.  The automation process includes actions to automate the manual task and update its completion status.

Automated tasks are executed sequentially until a manual task is encountered. If an automated task fails, manual intervention is required to trigger it again. In case of a failure in the automation process,you can retrigger it and verify its completion. If a task fails, the backup assignee is notified via email and must perform the necessary manual actions to address the failure. This confirms that the recovery process continues smoothly even in the event of automation issues.

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** and select a plan record.

2.  On the **Recovery tasks** tab, select a manual recovery task that you want to automate.

    You can automate a manual recovery task in the business continuity plan.

3.  Open Workflow Studio and select **Create new subflow**.

4.  On the form, fill in the fields.

    For more information on creating a customized subflow for automating the tasks in the BCM application, see [Create a subflow form](../reference/create-new-subflow-for-bcm.md).

    For more information on creating a subflow, see Create a subflow in Workflow Studio.

    The properties for the subflow are filled in.

5.  Select **Submit**.

    The subflow is designed to automate the task. Within the Actions section of the subflow, the **Action**, **Flow Logic**, and **Subflow** tabs are displayed.

6.  Create the subflow inputs to specify the data available to the subflow when it starts running.

    To establish a reference to the record linked to the task, you can specify the name and type for the input in the Inputs &amp; Outputs section of the subflow. By defining the inputs, you can create a reference to the task responsible for executing the automation.

    ![Reference to the task.](../image/automated-tasks-input.png)

    1.  Select the label for the input in the **Label** field.

        Within the subflow, there is a special variable known as the Current variable. When the Current variable is chosen in the Inputs section, it is automatically substituted with the task that triggered the automation. This allows for dynamic referencing and processing of the specific task within the subflow.

    2.  Select the name for the input in the **Name** field.

        The Name field is where you must define the variable name to be **current** \(all lower case\). The Type must always be **Document ID.Event task**.

    3.  Select the type for the input in the **Type** field.

        For example, you can select **Document ID.Event task** as the type of the input.

    4.  To mark the input as mandatory, select the **Mandatory** option.

        For information on creating subflow inputs and outputs, see Create a subflow in Workflow Studio.

    5.  Select **+** to add a new input.

    Once you create the flow variables, you can access them on Workflow Studio. For information on creating subflow inputs and outputs, see Create a subflow in Workflow Studio.

7.  In the Actions section, select **Send Email**.

    Expanding the Send Email section displays the fields as shown in the example. The fields on the form are described in the table. ![Revised subflow.](../image/automated-tasks-revised-subflow.png)

<table id="table_fxr_ghx_hbc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Name of the action for the subflow.Default: **Send Email**

</td></tr><tr><td>

Target Record

</td><td>

Associated task record that is used for the subflow.

</td></tr><tr><td>

Table

</td><td>

Name of the table where the task resides. For example, event task \[sn\_recovery\_event\_task\].

</td></tr><tr><td>

Include Watermark

</td><td>

Option to add a watermark in the file that is associated with the task.

</td></tr><tr><td>

To

</td><td>

Email addresses of the recipients that should be addressed directly.

</td></tr><tr><td>

CC

</td><td>

Email addresses of the copied recipients. They can view the list of the recipients that are directly addressed in the email.

</td></tr><tr><td>

BCC

</td><td>

Email addresses of the copied recipients whose names are not displayed in the email.

</td></tr><tr><td>

Subject

</td><td>

Subject of the email that describes the issue and reason for sending the email.

</td></tr><tr><td>

Body

</td><td>

Description and action steps about the issue.

</td></tr></tbody>
</table>8.  Select **Done**.

    Once the automation is triggered, the task is considered complete. In this particular scenario, the email is automatically sent to the user that has been selected.

9.  Select **Update record** in the Actions section of the subflow.

    You can update the original plan task to be completed by updating the record section of the subflow. ![Update the record.](../image/automated-tasks-update-record.png)

    1.  In the **Action** field, select **Update record**.

    2.  In the **Record** field, select **Current**.

    3.  In the **State** field, select **closed complete**.

    4.  Select **Done**.

        The state of the record moves to **Completed**.

10. To publish the workflow, select **Publish**.

    The changes are applied to all instances where the subflow is used. Similarly, you can define new flows in the subflow that can be run as an automation.

11. Navigate to the **Recovery tasks** tab in the plan with the sn\_bcm.program\_manager role and open the manual recovery task that was being edited.

    The recovery task form is displayed.

    ![Tasks in the Automated flow field.](../image/automated-tasks-automated-flow.png)

12. In the **Task classification** field, select **Automated** to change the manual task to an automated task and select **Save**.

    After saving the form, the flow variables are displayed.

    When you select and save the task, the variables associated with the automated flow are displayed in the **Variables** field of the recovery task.![Variables for the automated flow.](../image/automated-tasks-variable.png)

13. In the Assignment details, confirm that the **Backup assignee** field is filled in.

    When converting a manual task to an automated task, the **Backup assignee** field is displayed on the form. In the event of an error causing the automation flow to fail, an email notification is sent to the backup assignee. This email informs them about the failure of the automated flow and the need for manual intervention to resolve the task. The backup assignee can then take the necessary action to complete the task and confirm its resolution.

14. Select **Save**.

    The Recovery task form now includes a Task classification column where the automated tasks are displayed. These automated tasks are executed automatically by the system as part of the plan.


-   **[Create a subflow form](../reference/create-new-subflow-for-bcm.md)**  
Use the Create a subflow form to automate a manual recovery task within the business continuity plan.

**Parent Topic:**[Structured workflows for BCPs](../concept/bcp-tasks-performed-by-bcp-owner.md)

