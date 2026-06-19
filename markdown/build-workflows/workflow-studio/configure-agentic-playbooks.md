---
title: Configuring Agentic Playbooks
description: As a playbook author in Workflow Studio, configure AI Agents to perform a playbook activity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/configure-agentic-playbooks.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Agentic Playbooks, Playbook, Explore, Workflow Studio, Build workflows]
---

# Configuring Agentic Playbooks

As a playbook author in Workflow Studio, configure AI Agents to perform a playbook activity.

## Before you begin

-   Make sure you have the latest Workflow Studio and Now Assist for Platform apps.
-   Role required: admin, playbook.admin, pd\_author, or playbook.write

## About this task

Agentic Playbooks come preconfigured with AI Agents that are integral to the Playbook Activity Assist agentic workflow. The workflow works seamlessly with the preconfigured AI Agents, without adding any additional agents. However, you can also add your custom agent to the activity according to your requirements. To make a playbook agentic, simply enable the AI Agents for your playbook activity and provide clear instructions for the AI Agents to perform the tasks.

You can set up AI Agents to automatically complete activities or provide recommendations for you to review, edit, and approve.

You can enable AI Agents for all default activities. For custom activities, make sure to enable AI Agents in the activity definitions and then in playbook. You can configure the following activities to be completed independently by AI Agents:

-   New Record Form
-   Questionnaire
-   Email Form
-   Record Form

To learn more about activity definitions, see [Activity definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/activity-definitions.md).

## Procedure

1.  In Workflow Studio, open the playbook that you want to use AI Agents for.

2.  Select and open the side panel for the activity that you want AI Agents to perform.

3.  On the **AI Agents** tab, select how you want to use the AI Agents.

    \[Omitted image "enable-ai-agent-june2026.png"\] Alt text: Option to enable and select the scope of AI Agents.

    |Option|Description|
    |------|-----------|
    |**Collaborative**|The AI Agents generate and fill the values, then wait until a human reviews and approves the AI-generated value.|
    |**Autonomous**|The AI Agents update the record, complete the activity, and automatically move the playbook to the next activity.|
    |**No AI Agents**|AI Agents are turned off for the activity.|

    **Note:** Test the playbook extensively to make sure that the AI Agents can complete the activities independently. Select **View progress** while testing the playbook to see the agent activities on the Now Assist panel.

    For activities that can't be completed independently by the AI Agents, the system saves the data. The activity is completed if the data matches any Wait for condition in your playbook.

4.  In the **AI Agents** field, select a custom agent that you want to add to the activity.

5.  In the **AI Agent Instructions** field, enter instructions for the task that you want the AI Agent to perform.

    For guidelines about how to write instructions for AI Agents, see [Guidelines for writing AI agent instructions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/guidelines-agent-instruction.md).

6.  Select **Save and close**.


## What to do next

Repeat as needed for any other activities that you want an AI Agent to help perform.

After the playbook is complete, test the playbook. For information, see [Test a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/test-process.md).

**Parent Topic:**[Agentic Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/agentic-playbooks-landing.md)

