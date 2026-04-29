---
title: Activate an AI Agent in Public Sector Digital Services AI Agent Collection
description: Configure and activate standalone AI agents to perform various tasks.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Activate an AI Agent in Public Sector Digital Services AI Agent Collection

Configure and activate standalone AI agents to perform various tasks.

## Roles required to activate and access agentic AI

The roles required to activate and access the AI Agents respectively are as follows:

<table id="table_cnc_nyr_dfc"><thead><tr><th>

Roles

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td>

PSDS AI admin \[sn\_gsm\_ai\_agents.admin\]

</td><td>

-   Configure the agentic workflow.
-   Change AI settings.
-   Create and manage new workflows and AI agents.
-   Access and update Autonomous AI Assistant tables.

</td></tr><tr><td>

PSDS AI agent \[sn\_aia\_agent\]

</td><td>

Read, create, update, and delete records in the AI agent table.

</td></tr></tbody>
</table>## Before you begin

Install the Now Assist for Public Sector Digital Services \(PSDS\) plugin \(sn\_psds\_gen\_ai\), and ensure that it is up to date.

Role required: admin, sn\_gsm\_ai\_agents.admin

To access AI agents for use with Public Sector:

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

2.  Select **Create and manage** &gt; **AI agents**.

3.  Under AI agents, select and activate all the AI agents one by one to make them available in the Now Assist panel.

4.  Select **Define the specialty**, review the fields, and confirm that the AI agent meets your requirements.

    If it doesn't meet your requirements, you can edit the AI agent. To modify the AI agent, [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements. You can activate the AI agent template by making triggers active and setting the display settings to include the Now Assist panel.

    **Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

5.  Select **Add tools and information** to review the skills, scripts, and tools available for the AI agent to perform its role.

6.  Select **Define Security Controls** to review:

    -   User access: Users who can access and interact with the AI agent \(an ACL is generated automatically\).
    -   Data access: The user identity that the agent runs as, which determines roles and data access permissions.
7.  Select **Add triggers** and configure conditions that start the AI agent.

    Triggers can include record conditions, schedules, or inbound email.

    For more information, see [Add a trigger to an AI agent](https://www.servicenow.com/docs/access?context=add-trigger-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

8.  Select **Channels and status** to choose the channels where this AI agent will be available for users to initiate interactions, and set its availability status.

    For more information, see [Select channels and status for an AI agent](https://www.servicenow.com/docs/access?context=channels-access-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

9.  Select **Save and test**.

    On this page, you can test how the AI agent completes a task.


## What to do next

**Important:** When you modify an agentic workflow, AI agent, or tool, make sure that you update all instructions accordingly.

Use the Testing playground to [Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) using example utterances.

If activation fails, check roles and skill configuration.

