---
title: Enable agentic workflows in Virtual Agent
description: Perform the following if you're trying to trigger an agentic workflow, but don't see the Virtual Agent option in the configuration.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Now Assist in Virtual Agent reference, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Enable agentic workflows in Virtual Agent

Perform the following if you're trying to trigger an agentic workflow, but don't see the Virtual Agent option in the configuration.

-   Change system property:

    Set the **Value** field of the system property **sn\_aia.enable\_va\_conversation** to **True**.

    **Note:** Ensure your application scope is set to Now Assist AI Agents when making this change.

-   Enable in AI Agent Studio:

    1.  Navigate to **AI Agent Studio** &gt; **Overview**.
    2.  Select the agentic workflow you want to use.
    3.  Navigate to **Select channels and status**. The Virtual Agent panel becomes available after setting the system property **sn\_aia.enable\_va\_conversation** to **True**.
    4.  Toggle the **Display** to on for the Virtual Agent panel.
    5.  Select your assistants from the **Assistants where AI agents are discoverable** list.
-   Configure individual AI agents:

    You must also enable the Virtual Agent display for each individual AI Agent that belongs to that workflow. If they are not toggled on, the workflow will not be able to call them during the conversation.

    1.  From AI Agent Studio, select the AI agent that's part of the agentic workflow.
    2.  Navigate to **Select channels and status**.
    3.  in the Engage via Virtual Agent assistants panel, toggle **Allow** to on.
-   Alternative method - Promoting in Assistant Designer:

    If the property is already enabled but the workflow doesn't appear for users, perform the following:

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer** &gt; **Asset library**.
    2.  Select your assistant from the list.
    3.  Find the agentic workflow or AI agent in the Assets section.
    4.  Select the **Show actions from this row** icon and set the Visibility option to **Promoted**.

        This ensures the asset is prioritized and visible in the conversational list.


Agentic workflows are generally intent based. Once enabled for Virtual Agent, the LLM determines when to trigger the workflow based on the user's natural language input. For example, "I need to process an image for a new task".

