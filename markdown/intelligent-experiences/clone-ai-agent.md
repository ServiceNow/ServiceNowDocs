---
title: Duplicate an AI agent
description: Duplicate an existing AI agent in AI Agent Studio so that you can save time by not having to manually configure or create AI agents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Duplicate an AI agent

Duplicate an existing AI agent in AI Agent Studio so that you can save time by not having to manually configure or create AI agents.

## Before you begin

Role required: sn\_aia.admin

## About this task

Duplicate the AI agents to do the following tasks:

-   Duplicate the record.
-   Disallow any AI agents with existing names.

Custom columns, such as the Tools and Knowledge sources, Status, and a column with the Duplicate icon \(![Duplicate icon.](../image/ai-agents-clone-icon.png)\) are available for the AI agents list.

**Note:** The duplicated AI Agents use the same tools as the original agent and modifying the agent tools in the duplicated AI agent affects the agent tools in the original AI agent. To use the tools in a duplicated AI agent, you can either use the duplicated agent tools without making changes to them or add a new tool.”

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents** and open the AI agents list in AI Agent Studio.

2.  Duplicate the AI agent from either the Manage agentic workflows and AI agents page or the AI agent form.

    |Current location|Navigation option|
    |----------------|-----------------|
    |**Manage agentic workflows and AI agents page**|On the AI agents list, select the duplicate icon \(![Duplicate icon.)](../image/ai-agents-clone-icon.png)\) for the AI agent that you would like to duplicate.|
    |**AI agent form**|Open the AI agent that you want to duplicate, select the menu icon \(![Menu icon.](../image/three-dots-icon.png)\) next to **Exit** on the Describe and instruct form, and select **Duplicate**.|

    You see a confirmation message in a pop-up window.

    ![Confirmation pop-up window that asks you to either duplicate the AI agent or cancel the action.](../image/clone-ai-agent-confirm.png)

3.  Create a copy of the AI agent with the same information from the original AI agent's record by selecting **Duplicate**.

    **Note:** The name of the duplicated AI agent is appended with the suffix `(Copy)` so that you can clearly identify the duplicated AI agent from the original AI agent. For example, `Knowledge Article Agent (Copy)`. You can rename the duplicated AI agent and also edit the other information that is duplicated from the original AI agent.

4.  After editing the details in the Describe and instruct section, select **Save and continue**.

5.  In the Add tools and information section, edit the details that are from the original AI agent or add new tools for your requirements and select **Save and continue**.

6.  In the Toggle display section, turn on the Status for the duplicated AI agent and select **Save and continue**.


## Result

You’re redirected to the AI Agent Studio home page. In the Manage and configure AI Agents to solve agentic workflow section on the **AI Agents** tab, you see the duplicated AI agent.

