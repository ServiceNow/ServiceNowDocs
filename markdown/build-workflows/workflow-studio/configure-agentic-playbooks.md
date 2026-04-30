---
title: Configuring Agentic Playbooks
description: As a playbook author in Workflow Studio, configure AI agents to perform a playbook activity.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-09-05"
reading_time_minutes: 2
breadcrumb: [Agentic Playbooks, Playbooks, Explore, Workflow Studio, Build workflows]
---

# Configuring Agentic Playbooks

As a playbook author in Workflow Studio, configure AI agents to perform a playbook activity.

## Before you begin

-   Role required: admin, playbook.admin, pd\_author, or playbook.write
-   Make sure you have the latest Workflow Studio and Now Assist for Platform apps.

## About this task

Agentic Playbooks come preconfigured with AI agents that are integral to the Playbook Activity Assist agentic workflow. The workflow works seamlessly with the preconfigured AI agents, without adding any additional agents. To make a playbook agentic, simply enable the AI agents for your playbook activity and provide clear instructions for the AI agents to complete the tasks.

You can set up AI agents to automatically complete activities or provide recommendations for you to review, edit, and approve.

You can enable AI agents for all default activities. For custom activities, make sure to enable AI agents in the activity definitions and then in playbook. You can configure the following activities to be completed independently by AI agents:

-   New Record Form
-   Questionnaire
-   Email Form
-   Record Form

To learn more about activity definitions, see [Activity definitions](../concept/activity-definitions.md).

## Procedure

1.  In Workflow Studio, open the playbook that you want to use AI agents for.

2.  Select and open the side panel for the activity that you want AI agents to perform.

3.  On the **AI Agents** tab, select **Activate AI agents**.

    ![Image of the side panel of an activity showing the AI agents tab and its settings.](../images/agentinc-playbook-configure-user.png)

4.  In the **Complete activity independently** field, select if you want to enable AI agents to complete the activity.

    |Choice|Description|
    |------|-----------|
    |**On**|The AI agents update the record, complete the activity, and automatically move the playbook to the next activity.|
    |**Off**|The activity waits until a human reviews and approves the AI generated outputs.|

    Follow the instructions on your screen to allow AI agents to complete the activity independently.

    **Note:** Test the playbook extensively to make sure that the AI agents can complete the activities independently. Select **View progress** while testing the playbook to see the agent activities on the Now Assist panel.

    For activities that cannot be completed independently by the AI agents, the system saves the data. The activity is completed if the data matches any Wait for condition in your playbook.

5.  The **Impersonate User** field is pre-selected to run the activity as the user who triggers the playbook.

6.  In the **Instructions** field, enter instructions for the task that you want the AI agent to perform.

    For guidelines about how to write instructions for AI agents, see [Guidelines for writing AI agent instructions](../reference/guidelines-agent-instruction.md).

7.  Select **Save and close**.

8.  Repeat as needed for any other activities that you want an AI agent to help perform.

9.  [Test the playbook](test-process.md).


## Result

Your activities will be performed by an AI agent during runtime.

**Parent Topic:**[Agentic Playbooks](../concept/agentic-playbooks-landing.md)

