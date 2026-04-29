---
title: Service Exchange onboarding agentic workflows
description: Use the Service Exchange onboarding agentic workflow to register your consumers in Service Exchange.
locale: en-US
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Service Exchange onboarding agentic workflows

Use the Service Exchange onboarding agentic workflow to register your consumers in Service Exchange.

## Service Exchange onboarding agentic workflow overview

The Service Exchange onboarding agentic workflow helps providers register a consumer user in Service Exchange. It also helps identify any issues during consumer registration and helps you resolve those problems.

To modify the Service Exchange onboarding agentic workflow, you must duplicate the workflow and adjust the settings according to your requirements. For more information, see [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

You can initiate the onboarding workflow from the Now Assist panel by entering the prompt `start onboarding`. For more information on the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Access the Service Exchange onboarding agentic workflow

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Service Exchange Onboarding**.

To create an agentic workflow, see [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Test the Service Exchange onboarding agentic workflow

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Test AI reasoning**.
3.  Select the agentic workflow and version, and select **Start test**.

To test the use case, see [Manually test the execution of an agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## AI agents and their role in the Service Exchange onboarding agentic workflow

The following AI agents are used to execute the instructions for the Service Exchange onboarding agentic workflow.

To create an AI agent, see [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

<table id="table_c23_w11_jgc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Registration Initiator

</td><td>

This AI agent assists in initiating the registration process and managing the early stages of the process.

</td></tr><tr><td>

Registration Error Monitor

</td><td>

This AI agent assists users with a summary of the Service Exchange errors, enabling them to make informed decisions and take the appropriate actions.

</td></tr><tr><td>

Registration Monitor

</td><td>

This AI agent monitors registration life cycle events, validates registration status, and evaluates settings record creation. It posts concise success or failure updates to the registration task work notes to ensure clear visibility and accountability.**Note:** To use this agent, you must enable the **When registration moves to WIP** trigger. For more information about triggers, see [Add a trigger to an AI agent](https://www.servicenow.com/docs/access?context=add-trigger-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>