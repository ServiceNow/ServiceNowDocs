---
title: Add Guided Decisions to playbooks
description: Add decision trees created using the Guided Decisions Experience application to a playbook, so customer service agents can work through it to resolve cases more efficiently.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Add Guided Decisions to playbooks

Add decision trees created using the Guided Decisions Experience application to a playbook, so customer service agents can work through it to resolve cases more efficiently.

## Before you begin

Role required: admin, pd\_content\_author

## About this task

A playbook is set of steps that defines a process. A decision tree can be added as one of the steps within a playbook.

Playbooks are displayed in cases on Agent Workspace based on trigger definitions defined for each playbook in the Process Automation Designer. For more details, see Process Automation Designer. Based on the context of the case the customer service agent is working on, the playbook and any associated decision trees are displayed.

For more details on playbooks for Customer Service Management, see [Playbooks for Customer Service Management](../concept/customer-service-case-playbooks.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Process Automation Designer**.

    Playbooks opens in a new tab.

2.  Select the process you want to add the decision tree to.

3.  Select **Add activity**.

4.  Select **Guided Decisions Experience** &gt; **Guided Decisions**.

5.  In the Details tab, fill in the basic details of your activity.

<table id="choicetable_n4l_ydt_vlb"><tbody><tr><td id="d165125e136">

**Label**

</td><td>

Unique name for your activity. This name appears in user-facing views of your playbook.

</td></tr><tr><td id="d165125e145">

**Description**

</td><td>

Description of your activity.

</td></tr><tr><td id="d165125e154">

**Run condition**

</td><td>

After the activity starts, the activity runs only if specific conditions are met.

</td></tr><tr><td id="d165125e163">

**When to start**

</td><td>

Options when your activity must start:-   **After Previous**: This activity starts when the preceding activity has a state of Skipped or Complete.
-   **Immediately**: This activity starts when its stage starts running. Your activity doesn't depend on the state of any preceding activities.
-   **With Previous**: This activity starts when the immediately preceding activity starts running.


</td></tr></tbody>
</table>6.  Select **View all properties**.

7.  In the Automation tab, in the **Decision tree** field, select the decision tree you want to add to the guided decision.

8.  Select **Done**.

9.  In the main header, select **Activate**.

    Activating your process publishes it so that it runs when triggered.


## Result

The decision tree is added to the playbook. Depending on the context of the case, customer service agents can access the decision trees from cases on Agent Workspace.

**Related topics**  


[Configuring Guided Decisions](../concept/setting-up-guided-decisions.md)

[Configuring guidances and decision trees](../concept/configuring-guided-decisions.md)

