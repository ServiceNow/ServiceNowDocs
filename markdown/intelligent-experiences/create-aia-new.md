---
title: Create an AI agent
description: Create an AI agent in AI Agent Studio to solve problems for your users and coordinate with other AI agents in agentic workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-aia-new.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 5
breadcrumb: [AI Agent Studio, AI agents and agentic workflows, Enable AI Experiences]
---

# Create an AI agent

Create an AI agent in AI Agent Studio to solve problems for your users and coordinate with other AI agents in agentic workflows.

## Before you begin

Role required: sn\_aia.admin

## About this task

In the ServiceNow agentic ecosystem, an AI agent is a set of large language model \(LLM\) instructions and tools that can perform specific tasks.

An AI agent can collaborate with other agents to achieve better results by using fewer LLM calls. AI agents can also request help or information from the user.

There are three ways to create an AI agent. The following procedure describes the steps for the full guided setup. You complete every section yourself, from the definition through tools, security, triggers, channels, and memory. Use it when you already know what the agent must do and have intended prompts in mind.

You can also create an AI agent conversationally. You describe the agent, and Virtual Agent drafts the definition and displays suggested tools, which you then review and finish in the guided setup. Use it to get to a first draft quickly. You can create only AI agents with this method, not agentic workflows. For those instructions, see Create an AI agent conversationally.

The third way to build an AI agent is through an automation opportunity. When you build from the automation opportunities list, the identified automation context is applied to the AI agent. For those instructions, see [Create an AI agent for an automation opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-aia-aut-opp.md).

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Home**.

2.  Select **Create new agentic solution**, then select **New AI agent for a task**.

3.  In the new AI Agent pop-up window, describe your AI agent and select **Next**.

    Alternatively, you can select **Skip** to open a new AI agent form.

4.  Select **Create an agent from scratch** and select **Next**.

    To create an external AI agent instead, see [Create an external AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-a2a-agent-new.md).

5.  Describe the purpose of the AI agent, then select **Check**.

    The LLM uses your description to generate suggested content for the general prompt of the AI agent. Confirm that your description names the goal, what starts the work, the records and tables involved, and the outcome that counts as done. For example, "Categorize incoming ITSM incidents by reading the short description and description, select the best-fit category and subcategory, and update the incident with a short rationale in the work notes."

    The LLM also uses the description to generate tool suggestions that help the AI agent achieve its goal.

    If other agentic solutions accomplish a goal similar to the one you describe, the check identifies them so you can edit a matching solution instead.

    You can skip this step by selecting **Skip**.

6.  [Review or draft the content in the **Expected behavior** section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-aia-new.md).

    You can edit any content that the LLM generates.

    The Orchestrator uses the description, role, and instructions when the AI agent is invoked, either alone or as part of an agentic workflow. This content gives the Orchestrator the context it requires to use the AI agent for its intended purpose.

    After making any changes to the AI agent in this guided setup, you can select **Save** to save your progress.

7.  [Add tools and information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-tool-aia-new.md) your AI agent can use to accomplish its goals.

    The tools give the AI agent the capabilities necessary to accomplish tasks. An AI agent requires tools to perform tasks.

    You can also add information sources, such as knowledge graphs, that the AI agent uses when making decisions.

    Information can reach an agent at run time in multiple ways. Knowledge graphs supply relationships between entities. Search retrieval tools retrieve content from defined sources. File upload tools give the agent specific documents.

8.  [Define the AI agent access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/define-sec-aia-new.md).

    The security controls configure user access and data access to the AI agent. You can also set the discoverability of the AI agent by AI specialists or third parties.

9.  [Add test scenarios for evaluations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/create-scenarios-aia.md).

    Automated evaluations of your AI agent require configured test scenarios to run against. You can add existing table records as scenarios or manually enter different test objectives to cover the full range of conditions your AI agent can encounter.

10. [Add a trigger to automatically invoke your AI agent if a specified event occurs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia-new.md).

    A trigger isn't required if your AI agent is used only in chats.

11. [Determine how and where users can invoke your AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/channels-access-aia-new.md).

    To let users invoke the AI agent directly, add it to Virtual Agent chat assistants.

12. [Set up long-term memory and active learning controls for your AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/map-ltm-aia-new.md).

    AI agents can learn from previous interactions, if configured to do so. You can choose the categories of information from previous interactions that the AI agent uses when handling new requests.

13. Select **Save** to save your changes.


## Result

Your AI agent has the context that the AI Agent Orchestrator requires and the tools to accomplish its intended tasks.

## What to do next

You can [test your AI agent on a record manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/test-ai-asset-new.md) to see an example execution. You can also [create an automated agentic evaluation to test the AI agent over repeated interactions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/launch-aia-eval.md). Automated evaluations can display optimization suggestions when LLM judges detect patterns behind low success rates.

To make your AI agent ready for use, select **Activate**.

