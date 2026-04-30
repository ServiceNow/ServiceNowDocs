---
title: Add a decision to an app's playbook in Creator Studio
description: Add decisions, which are if/then conditions, to define branches, or different paths of an automation's playbook in Creator Studio.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Working with automation in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Add a decision to an app's playbook in Creator Studio

Add decisions, which are if/then conditions, to define branches, or different paths of an automation's playbook in Creator Studio.

## Before you begin

To add decisions to a playbook, you must be given permission to work on the app.

## About this task

Each decision should have at least two branches, with each branch representing a possible outcome for the decision. The second branch can be the ELSE branch, which is required. The ELSE branch will be followed when all other conditions on other branches are false. Think of the else branch as the catch-all case for the decision.

![A playbook in Creator Studio in Diagram view](../image/crs-playbook-diagram.png "Example decision with branches")

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the app that contains the playbook you want to add a decision to.

3.  Select the form that contains the playbook that you want to add a decision to.

4.  Select the automation that contains the playbook that you want to add a decision to.

    ![Select the automation in the navigation panel](../image/crs-auto-copy-nav.png "Select automation that has the playbook")

5.  Select the add icon \(![](../image/cs-add-icon.png)\) on the connector here you want to add a decision and choose the diamond-shaped **Add a decision** icon \(![](../image/cs-add-decision-icon.png)\) in the menu that pops up.

    **Note:** You must be in the Diagram view to add a decision.

6.  Specify the decision's basic attributes on the **Details** tab of the Decision properties panel that appears.

    |Field|Description|
    |-----|-----------|
    |Playbook name|Unique, user-facing name for the decisions, which appears to agents and fulfillers while the playbook is running.|
    |Description|Optional details about what the decision accomplishes.|

    ![Basic details for a decision](../image/cs-decision-properties.png "Playbook decision properties")

7.  Define the decision's schedule.

<table id="table_i3x_lkn_n1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start rule

</td><td>

Choose when you want your activity to start running. The options are:-   **When stage starts**: The decision starts running as soon as the stage starts running, which is when your playbook is triggered.
-   **After specific activities**: The decision starts running after the specified activities have finished running.


</td></tr><tr><td>

Starts after

</td><td>

Select the activity that must finish running for the decision to happen. This field is editable only if you selected to start the rule **After specific activities**. You can choose only activities that happen before this decision in the playbook.

</td></tr></tbody>
</table>8.  Specify more scheduling conditions for the decision, such as whether there's a delay, by selecting **Show additional options**.

<table id="table_qcx_nmn_n1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display order

</td><td>

Order in which this activity occurs during a playbook run.

</td></tr><tr><td>

Start with delay

</td><td>

Toggle to specify that the ServiceNow AI Platform waits for a duration of time before running the decision after the start rule is met. For more information on how to specify the delay duration, see [Start with delay input properties](https://www.servicenow.com/docs/access?context=start-with-delay-properties&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Restart rules

</td><td>

What the decision does when a playbook is restarted. The options are:-   **Skip on restart**: Skip this decision when the playbook run is due to a restart.
-   **Run always**: Always run this decision, including first runs.
-   **Skip on first run**: Skip this decision during the first run.
For more information, see [Restart a playbook](https://www.servicenow.com/docs/access?context=restart-a-playbook&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

</td></tr></tbody>
</table>9.  Create the conditions for each branch, or possible outcome for the decision on the **Branches** tab of the Decision properties panel.

    1.  Enter a name for the branch in the **Branch label** field.

    2.  Select the **Add condition** button and specify what conditions should be met for the branch to take effect.

        You can use the answer from the associated form to define the conditions for the decision branch. To do so, complete the following steps:

        1.  Choose **Questions** in the **Field** field.
        2.  Select the form's question to use as the condition from the **Question** field.
        3.  Specify the condition **Operator** and the answer's **Value**.
        4.  Select **Apply** when you're done defining the condition.
        For details on working with conditions, see [Create a condition statement using the condition builder](https://www.servicenow.com/docs/access?context=create-cond-state-using-cond-build&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

    3.  Select the **Add new branch** button and add as many branches as needed.

    4.  If you add two or more branches, select how you want your decision activity to run the different branches.

<table id="table_xnb_dsj_41c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process any &amp; all branches that are true

</td><td>

The app processes all branches with conditions that are met.

</td></tr><tr><td>

Process only the first one that is true

</td><td>

The app processes only the first listed branch with conditions met.If you select this option, drag the branch that you want processed first to the top.

</td></tr></tbody>
</table>    5.  Adjust the order of branches as needed by dragging them into a new position.

10. Select **Save and close**.


**Parent Topic:**[Working with automation in Creator Studio](../concept/creator-studio-working-with-automations.md)

