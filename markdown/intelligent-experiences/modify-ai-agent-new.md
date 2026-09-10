---
title: Modify an AI agent
description: Modify an AI agent in AI Agent Studio to refine its performance, align with business goals, or enable it to perform new tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/modify-ai-agent-new.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 3
breadcrumb: [Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Modify an AI agent

Modify an AI agent in AI Agent Studio to refine its performance, align with business goals, or enable it to perform new tasks.

## Before you begin

Role required: sn\_aia.admin

## About this task

You can make tweaks to your AI agent based on previous performance, refine it to better align with evolving business goals, or make major changes to enable it to perform entirely new tasks. This includes updating the definition and instructions, adjusting security controls, adding or removing triggers, modifying tools to provide more or better capabilities, and changing where and how the AI agent is invoked.

This is also where an agent drafted in a conversation can be revised and completed. Nothing set during a conversation is fixed. The definition, tools, execution modes, security controls, triggers, and channels can all be changed here.

The instructions field supports multiple versions within the same AI agent, allowing you to test different instructions and evaluate performance without losing previous versions. For more information, see [Version control for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/version-control.md).

## Procedure

1.  Navigate to the **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the AI agent that you want to modify.

3.  In the node view, select either the pencil edit icon or the more options icon.

    The first node contains the main configuration settings for the AI agent. The other nodes represent the tools that comprise the underlying architecture.

    The pencil edit icon directs you to the original guided setup for the AI agent. You can add tools in the guided setup, but you can't add child agents.

    If you want to add child agents, select the more options icon and select **Add child agent**. You can add an existing AI agent or create one from scratch. Choosing to add an AI agent from scratch opens a new tab with the guided setup for the AI agent. It will be added as a child agent to the AI agent you're modifying once it's saved.

    Select the more options icon, select **Add tool**, then select the type of tool you want to add to open a new tab with the tool guided setup. See [Add a tool to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-tool-aia-new.md).

4.  [Define the AI agent's specialty](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-aia-new.md).

5.  [Define access rules for the AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-aia-new.md).

6.  [Add a trigger to automatically invoke your AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia-new.md) if a specified event occurs.

7.  [Configure where your AI agent can be invoked and set processing messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/channels-access-aia-new.md).

8.  [Set up long-term memory and active learning controls for your AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/map-ltm-aia-new.md).

    AI agents can learn from previous interactions, if configured to do so. You can choose the categories of information that the AI agent should consider from its previous experiences when approaching new problems.

9.  Select **Save** or **Run test** to save your changes.


## Result

Your AI agent is modified and ready to use.

## What to do next

You can [test an execution of your AI agent manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md) or [evaluate the AI agent using automated tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md).

