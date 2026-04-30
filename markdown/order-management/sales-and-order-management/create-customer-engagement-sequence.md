---
title: Create a customer engagement sequence
description: Create a customer engagement sequence to guide your sales representatives through engaging with their prospects and customers.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Customer Engagement Sequences, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Create a customer engagement sequence

Create a customer engagement sequence to guide your sales representatives through engaging with their prospects and customers.

## Before you begin

Role required: playbook.admin or pd\_author

## About this task

Setting up a sequence is based on playbooks and requires you to be familiar with using Workflow Studio and Playbook Experience.

**Important:** Setup and Tear Down are predefined stages in the Customer Engagement Sequences playbook. Do not remove these stages or add more activities in it. Avoid making any other changes to the Start Sequence and End Sequence activities.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \(![](../../../reuse/icons/product-icons/list-outline-24.svg)\).

3.  Navigate to **Sequences** &gt; **All Sequences**.

4.  Select **Create New Sequence**.

5.  On the Create new Sequence window, specify a name and optionally a description for your sequence and select **Create**.

    You’re redirected to Workflow Studio and a playbook of the type sequence is created with the following predefined stages:

    -   Setup
    -   Configure sequence activities
    -   Tear Down
6.  Define trigger conditions that initiate a sequence.

    1.  Select the Edit icon ![image.icon-pencil] above the Start pill.

    2.  On the **Schedule** tab of the Playbook properties form, indicate whether you are using an existing trigger, which includes the trigger type and the conditions that set up the sequences, or defining a new one.

        -   To use an existing trigger, select **Choose an existing trigger** and then proceed to step 7.
        -   To define a new trigger, select **Define your own conditions for when your process runs**.
    3.  In the drop-down list for the **Define your own conditions for when your process runs** choice, select the trigger type for the new trigger.

        The available trigger types are:

        -   Record Create
        -   Record Update
        -   Record Create or Update
    4.  In the **Table** field, select the table whose record operations you want to use to trigger your playbook.

        For example, you might want the sequence to trigger when a record is created or updated in the Lead \[sn\_lead\_mgmt\_core\_lead\] table.

    5.  In the **Condition to run** field, add conditions that must be met to trigger your playbook.

        For example, to trigger the sequence when a new record is created in the Lead \[sn\_lead\_mgmt\_core\_lead\] table, you would set the condition **\[Stage\]****\[is\]****\[New\]**.

        For more information, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

    6.  Select the frequency for your trigger from **Run my trigger** drop-down list.

        The available options are:

        -   Once
        -   For each unique change
        -   Only if not currently running
        -   For every update
    7.  Trigger your playbook for tables that extend your selected table by selecting the **Run this trigger on extended table** check box.

    8.  Provide users with the ability to rewind the playbook from the beginning by selecting the **Details** tab and selecting the **Allow this playbook to be restarted during runtime** check box.

    9.  Select **Save and close**.

7.  Change the priority with which a sequence task is created in the Start Sequence activity of the Setup stage.

    When the trigger condition is met, this activity creates a sequence task with a state of Work in progress and a priority of Moderate by default.

    **Note:** Do not remove this stage or add more activities to this stage. Avoid making any other changes to the Start Sequence activity.

8.  In the sequence diagram, configure sequence steps in the Configure sequence activities stage.

    Use this stage to configure activities you want to make available to the sales representative as guided sequence steps during runtime. For more information, see [Add and configure an activity in a playbook](https://www.servicenow.com/docs/access?context=add-configure-activity&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

    You can add any number of activities to this stage in your sequence.

9.  Exit early from the sequence by selecting the **Customer Engagement Sequences** &gt; **Update Sequence Task** activity from the activity picker.

    For more information on adding an activity, see [Add and configure an activity in a playbook](https://www.servicenow.com/docs/access?context=add-configure-activity&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

10. Review the configuration in the Tear Down stage.

    This predefined stage updates the sequence task record when the sales representative completes all the sequence steps in their sequence task. By default, the system updates the state of the sequence task record as complete \(indicated by State = 3\) in the Customer Engagement Sequence Task \[sn\_crm\_sequence\_task\] table.

    **Note:** Do not remove this stage or add more activities to this stage. Avoid making any other changes to the End Sequence activity.

11. Verify the sequence by selecting **Test**.

12. Select **Activate** to publish the sequence.

13. View the sequence in the CSM/FSM Workspace by selecting the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg) and navigating to **Sequences** &gt; **All Sequences**.


## What to do next

View sequence tasks and execute sequence steps. See [Using Customer Engagement Sequences](../concept/using-customer-engagement-sequences.md).

**Related topics**  


[Stages and activities](https://www.servicenow.com/docs/access?context=process-automation-designer-lanes-activities&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

[Triggers](https://www.servicenow.com/docs/access?context=process-automation-designer-triggers&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

[Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

[Restart](https://www.servicenow.com/docs/access?context=restart&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

