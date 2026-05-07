---
title: Create a customer engagement sequence
description: Drive personalized outreach by creating customer engagement sequences that automate timely, relevant interactions that are ideal for nurturing leads, onboarding clients, or re-engaging inactive customers.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Customer Engagement Sequences, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Create a customer engagement sequence

Drive personalized outreach by creating customer engagement sequences that automate timely, relevant interactions that are ideal for nurturing leads, onboarding clients, or re-engaging inactive customers.

## Before you begin

Check whether features you need to access are supported by reviewing the table in [Compatibility information for Customer Engagement Sequences](../reference/compatibility-matrix-upgrade-info.md).

Your instance must be integrated with platforms such as Amazon Connect.

Delegated developer roles should be assigned to designated users. For more information, see [Grant delegated developer permissions for managing sequences](grant-delegated-developer-permissions.md).

You should be familiar with using Workflow Studio and Playbook Experience.

Role required: sn\_crm\_sequence.admin, sn\_crm\_sequence.writer

**Note:** If you're using Customer Engagement Sequences 1.0.0, you need the playbook.admin or pd\_author role to create sequences.

## About this task

**Important:**

-   Create sequences from the Sequences module in the CSM/FSM Configurable Workspace, not from Workflow Studio. If you create a playbook of the type Sequence directly in Workflow Studio, the required Setup, Configure sequence activities, and Tear Down stages are not added automatically.
-   Setup and Tear Down are predefined stages in the Customer Engagement Sequences playbook. Do not remove these stages or add more activities in these stages. Avoid making any other changes to the Start Sequence and End Sequence activities.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Select **Create New Sequence**.

5.  On the Create new Sequence window, specify a name and optionally a description for your sequence.

6.  Select **Create**.

    You’re redirected to Workflow Studio and a playbook of the type sequence is created with the following predefined stages:

    -   Setup
    -   Configure sequence activities
    -   Tear Down
7.  Select a source table whose records will trigger the sequence.

    1.  Select the Edit icon ![](../image/icon-pencil.png) above the Start pill.

    2.  Select a table from the **Parent table** drop-down list.

        For example, you might want the sequence to trigger when a record is created or updated in the Lead \[sn\_lead\_mgmt\_core\_lead\] table.

    3.  Select **Save and close**.

        The Triggers icon ![](../image/triggers-icon.png) is activated on the left sidebar.

8.  Define trigger conditions that initiate a sequence.

    For more information, see [Define trigger conditions](define-trigger-conditions.md).

9.  Change the priority with which a sequence task is created by navigating to the **Automation** tab of the Start sequence activity properties under the Setup stage.

    When the trigger condition is met, this activity creates a sequence task with a state of Work in progress and a priority of Moderate by default.

    **Note:** Do not remove this stage or add more activities to this stage. Avoid making any other changes to the Start Sequence activity.

10. In the sequence diagram, configure sequence steps in the Configure sequence activities stage.

    Use this stage to configure activities you want to make available to the sales representative as guided sequence steps during runtime. For more information, see [Add and configure an activity in a playbook](https://www.servicenow.com/docs/access?context=add-configure-activity&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    You can add any number of activities to this stage in your sequence. For example, for telesales workflows, you might want to add a schedule call activity. For more information, see [Add a schedule call activity to a telesales workflow sequence](add-schedule-call-activity.md).

11. Add decision nodes to activate the next stage in the playbook based on the outcome of the previous stage.

    For more information, see [Add decision nodes to a sequence](add-decision-nodes-sequences.md).

12. Add a stage for the new branch you created and repeat the steps to add more activities as needed, including the schedule call activity as needed.

    For information about adding new stages, see [Add and configure a stage in a playbook](https://www.servicenow.com/docs/access?context=add-configure-stage&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

13. Update the sequence task record by selecting the **Customer Engagement Sequences** &gt; **Update sequence task** activity from the activity picker.

    You can also use the Update sequence task activity to exit early from the sequence. For more information, see [Add the Update sequence task activity to a sequence](add-update-sequence-task-activity.md).

14. Review the configuration in the Tear Down stage.

    This predefined stage uses the Update sequence task activity to update the sequence task record when the sales representative completes all the sequence steps in their sequence task. By default, the system updates the state of the sequence task record as complete \(indicated by State = 3\) in the Customer Engagement Sequence Task \[sn\_crm\_sequence\_task\] table.

    **Note:** Do not remove this stage or add more activities to this stage. Avoid making any other changes to the End Sequence activity.

15. Verify the sequence by selecting **Test**.

16. Publish the sequence by selecting **Activate**.

17. View the sequence in the CSM/FSM Workspace by selecting the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg) and navigating to **Sequences** &gt; **All Sequences**.


## What to do next

[Assign runtime permissions while creating sequences](configure-runtime-permission-sequence-playbooks.md).

-   **[Define trigger conditions](define-trigger-conditions.md)**  
Define trigger conditions that start a sequence by configuring simple triggers, or combining multiple triggers for initiating workflows from multiple record-based events.
-   **[Add a schedule call activity to a telesales workflow sequence](add-schedule-call-activity.md)**  
Add a schedule call activity in your sequences to support telesales workflows.
-   **[Add decision nodes to a sequence](add-decision-nodes-sequences.md)**  
Activate the next stage in the playbook based on the outcome of the previous stage by adding decision nodes while creating or updating a sequence.
-   **[Add the Update sequence task activity to a sequence](add-update-sequence-task-activity.md)**  
Dynamically update the sequence task records based on predefined configuration using the Update sequence task activity while designing customer engagement sequences.
-   **[Assign runtime permissions while creating sequences](configure-runtime-permission-sequence-playbooks.md)**  
Use permission sets to control access to sequence records such as sequence tasks and steps.

**Parent Topic:**[Using Customer Engagement Sequences](../concept/using-customer-engagement-sequences.md)

**Related topics**  


[Stages and activities](https://www.servicenow.com/docs/access?context=process-automation-designer-lanes-activities&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Triggers](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

[Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

[Enabling playbook restart](https://www.servicenow.com/docs/access?context=restart&version=australia&pubname=australia-build-workflows&ft:locale=en-US)

