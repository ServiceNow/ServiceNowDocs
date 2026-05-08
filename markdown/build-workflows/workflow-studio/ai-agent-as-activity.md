---
title: Use AI agent as an activity
description: Use an existing AI agent as an activity in your playbook to automate tasks. The AI agent gathers the required context, performs the work, and produces outputs that subsequent activities can consume.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Stages and activities, Understanding the playbook components, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Use AI agent as an activity

Use an existing AI agent as an activity in your playbook to automate tasks. The AI agent gathers the required context, performs the work, and produces outputs that subsequent activities can consume.

## Before you begin

Role required: playbook.admin or pd\_author.

Make sure that Now Assist AI agents plugin is installed and you have AI agents available in your instance. For information about installing the Now Assist AI agents plugin, see Install Now Assist AI agents. For information about creating an AI agent, see Create an AI agent.

## About this task

When you add an AI agent to the activity, you select the agent, provide an objective for the agent to complete, and define the expected outputs. You can also define whether you want to run the agent on behalf of the user who triggered the playbook, or the current user. You can interact with the agent from within the playbook, without opening the Now Assist panel.

## Procedure

1.  Navigate to **All** &gt; **Process automation** &gt; **Workflow Studio**.

2.  Select the playbook where you want to add the **Use an AI agent** activity.

3.  In a new or an existing stage, select **Add an activity**.

    ![Image showing the option to add an activity.](../images/use-ai-agent.png)

4.  From the list of activities, under **Common Activities**, select **Use an AI agent**.

5.  In the **Automation** tab, configure the AI agent.

<table id="table_slj_c1t_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI agent

</td><td>

The AI agent that you want to add to the activity.

</td></tr><tr><td>

Objective

</td><td>

Text directions for the AI agent. You can use a combination of plain text and data pill picker. Provide a descriptive instruction for the AI agent about what do you want to achieve. For example, `Summarize the incident (Parent record->Incident-> Number) and suggest the next steps to resolve the incident.`.

</td></tr><tr><td>

Run as

</td><td>

The user on behalf of whom you want the agent to run.-   **Active user**: The AI agent runs when the user selects **Start Now Assist**.
-   **The user triggering the playbook**: The AI agent when the playbook is triggered.


</td></tr><tr><td>

Expected outputs

</td><td>

Outputs that you want the AI agent to generate.

</td></tr></tbody>
</table>6.  Select **Show additional options** to configure the optional properties.

<table id="table_rsc_pht_33c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Assigned to

</td><td>

An optional field where you can specify a user who can complete, skip, or restart the activity when the agent is working.This field is visible only when you select **Show additional options**.

</td></tr><tr><td>

Assignment group

</td><td>

An optional field where you can specify a user group who can complete, skip, or restart the activity when the agent is working. This field is visible only when you select **Show additional options**.

</td></tr><tr><td>

Conversation label

</td><td>

A name to identify the conversation.

</td></tr></tbody>
</table>7.  Select **Save and close**.


## Using AI agent in a CSM playbook

In the following example, Alex, a CSM/FSM Workspace user, is working on a customer complaint about a product issue. The playbook uses the Complaint Case Research Plan Agent in the research stage to analyze the complaint and create relevant tasks for the next steps. The AI agent is configured to run as the active user in this playbook.

Alex performs all interactions with the AI agent within the playbook, without opening the Now Assist panel.

1.  When the playbook reaches the research stage, Alex selects **Start Now Assist** to run the AI agent.

    ![User clicks Start Now Assist button to run the AI agent.](../images/use-ai-agent-start.png)

2.  Alex can view the tasks that the AI agent is performing.

    ![The AI agent is running and Alex can view the tasks being performed by the agent.](../images/use-ai-agent-status.png)

3.  After analyzing the case and similar cases, the AI agent recommends adding four tasks and prompts Alex for confirmation. Alex can remove any of the recommended tasks or select **Confirm** for the AI agent to create the tasks.

    ![The AI agent prompts for permission before creating tasks for the next steps.](../images/use-ai-agent-worknote.png)

4.  After receiving the confirmation, the AI agent creates the tasks and marks the activity as complete.

    ![AI agent completes the activity.](../images/use-ai-agent-complete.png)


**Parent Topic:**[Stages and activities](../concept/process-automation-designer-lanes-activities.md)

**Related topics**  


[Add and configure a stage in a playbook](add-configure-stage.md)

[Activity definitions](../concept/activity-definitions.md)

[Add and configure an activity in a playbook](add-configure-activity.md)

[Automation Assets](../concept/automation-assets.md)

[Start with delay input properties](../reference/start-with-delay-properties.md)

[Optional activities](../concept/optional-activities.md#)

[Decision activities](create-a-decision-activity.md)

[Decision stages](create-decision-stage.md)

[Questionnaire activity](../reference/questionnaire-activity.md)

[Parallel branches](create-parallel-activity.md)

[Add dynamic inputs to an activity](add-dynamic-inputs-to-activity.md)

[Playbook activity state mapping](../../workspace/concept/playbook-activity-state-mapping.md)

