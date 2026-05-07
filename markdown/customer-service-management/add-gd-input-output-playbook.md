---
title: Add Guided Decision with inputs/outputs to Playbook
description: Add decision trees created using the Guided Decision with Inputs and Outputs activity in the Guided Decisions Experience application to a playbook, so customer service agents can work through it to resolve cases more efficiently.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Add Guided Decision with inputs/outputs to Playbook

Add decision trees created using the Guided Decision with Inputs and Outputs activity in the Guided Decisions Experience application to a playbook, so customer service agents can work through it to resolve cases more efficiently.

## Before you begin

Role required: admin, pd\_content\_author

## About this task

The Guided Decision with Inputs and Outputs activity is a playbook activity that enables decision trees to be used in playbooks with the ability to pass input parameters and retrieve output values. This activity allows you to select a specific decision tree version and configure input parameters that map to the questions defined in the first node of the decision tree. The activity supports versioning, where each activation of the decision tree builder creates a new version, and playbook activities continue using their configured version until manually updated. When a decision tree is activated to create a new version, you receive a notification message listing all playbooks and activities that reference the decision tree, with direct links to facilitate version updates.

For more details on playbooks for Customer Service Management, see [Playbooks for Customer Service Management](../concept/customer-service-case-playbooks.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Process Automation Designer**.

    Playbooks opens in a new tab.

2.  Select the process you want to add the decision tree to.

3.  Select **Add activity**.

4.  Select **Guided Decisions Experience** &gt; **Guided Decisions with inputs/outputs**.

5.  In the Details tab, fill in the details of the activity and select **Save and close**.

<table id="table_j5f_wx3_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique name for your activity. This name appears in user-facing views of the playbook.

</td></tr><tr><td>

Description

</td><td>

Brief description of the activity.

</td></tr><tr><td>

Activity definition

</td><td>

 

</td></tr><tr><td colspan="2">

Schedule

</td></tr><tr><td>

Start rule

</td><td>

Defines when to start the process the activity. Select one of the following:-   When stage starts: Your stage starts running as soon as the playbook starts.
-   After specific activities: Your stage starts running after specified stage\(s\) have finished running.

Starts after

</td></tr><tr><td>

Display order

</td><td>

When there are multiple stages running at the same time, define the order in which stages appear during a playbook run.**Note:** In Workflow Studio, this can also be helpful when viewing parallel activities in Diagram view.

</td></tr><tr><td>

Start with delay

</td><td>

Waits for a certain duration before running the activity when the start rule is met. For more information, see [Start with delay input properties](https://www.servicenow.com/docs/r/0MvJg~UYByX0VxWLomI71w/0bU5ECLrTgx0LIrj6BCf~w).

</td></tr><tr><td>

Restart rules

</td><td>

Defines how the activity runs when the playbook is restarted. -   Skip on restart
-   Run always
-   Skip on first run


</td></tr></tbody>
</table>6.  In the Automation tab, fill in the following fields and select **Save and close** button.

<table id="table_rqy_cbj_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automation

</td><td>

See or open the action, subflow, or flow that drives the activity.

</td></tr><tr><td>

Inputs

</td><td>

Configure inputs for the action, subflow, or flow that is driving the activity. Not all activities require user input. Define the values of the activity's inputs.

</td></tr><tr><td colspan="2">

Inputs

</td></tr><tr><td>

Decision tree

</td><td>

Decision tree as one of the steps within a playbook.

</td></tr><tr><td>

Decision tree version

</td><td>

Active version of the decision tree.**Note:** The activity supports versioning, where each activation of the decision tree builder creates a new version, and playbook activities continue using their configured version until manually updated.

</td></tr><tr><td>

Outputs

</td><td>

Outputs of the action, subflow, or flow that is driving the activity.

</td></tr></tbody>
</table>    **Note:** The activity provides a refresh capability that allows you to update to the latest decision tree version while preserving existing input mappings and adding any new input fields that were introduced in the newer version.

7.  In the UI Layout tab for knowledge articles, fill in the following fields and select **Save and control**.

    |Field|Description|
    |-----|-----------|
    |Article height|Default height of the article.|
    |Collapse knowledge article|When selected, the article appears collapsed in the playbook.|

8.  In the main header, select **Activate**.

    Activating your process publishes it so that it runs when triggered.


## Result

The decision tree is added to the playbook. Depending on the context of the case, customer service agents can access the decision trees from cases on Agent Workspace. An agent can restart this activity by selecting the **Restart Activity** option in a playbook. For more information on how to restart an activity, see [Restart a playbook](https://www.servicenow.com/docs/access?context=restart-a-playbook&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Related topics**  


[Configuring Guided Decisions](../concept/setting-up-guided-decisions.md)

[Configuring guidances and decision trees](../concept/configuring-guided-decisions.md)

