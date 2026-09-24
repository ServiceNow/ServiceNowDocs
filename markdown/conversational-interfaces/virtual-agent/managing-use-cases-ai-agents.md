---
title: Managing AI agents in Assistant Designer
description: View AI agents created in AI Agent Studio through Assistant Designer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/managing-use-cases-ai-agents.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Virtual Agent, Designer, AI Agents]
breadcrumb: [Managing asset library items, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Managing AI agents in Assistant Designer

View AI agents created in AI Agent Studio through Assistant Designer.

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

**Role required**: virtual\_agent\_admin

When you select an AI agent, it opens in AI Agent Studio. AI agents currently can't be created or edited in Assistant Designer. You can only view them in Assistant Designer. They can be created, edited, tested, and deleted only in AI Agent Studio. For more details, see [AI Agent Studio overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-agent-studio.md).

## AI agents in Assistant Designer

Select the **AI agents** option to see all the AI agents activated for Assistant Designer.

\[Omitted image "vad-ai-agent.png"\] Alt text: AI agents in the Assistant Designer Asset library.

|Column|Description|
|------|-----------|
|Name|Name of the AI agent. Select the AI agent to open it in AI Agent Studio.|
|Type|AI agent.|
|Status|Status type such as Published.|
|Active|Whether the AI agent is active or inactive.|
|Last modified|Time when the AI agent was last modified.|
|Description|Description of the AI agent.|

Use the row actions icon \( \[Omitted image "kebab-menu.png"\] Alt text:\) to work with visibility settings for **Promoted**, **Discoverable**, **Visible**, and **Active**:

<table id="table_fsb_pt1_cfc"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Promoted

</td><td>

Option to toggle the AI agent's **Promoted** status to show as a suggested conversational asset in the virtual assistant.You must first select an assistant to promote the AI agent.

</td></tr><tr><td>

Discoverable

</td><td>

Option to toggle the AI agent's **Discoverable** status. If discoverable, the AI agent is invoked when matched with a user's utterance.

</td></tr><tr><td>

Visible

</td><td>

Option to toggle the AI agent's visibility to users. If visible, the AI agent appears whenever the **Show me everything** option is selected in the conversation.

</td></tr><tr><td>

Active

</td><td>

Option to toggle the AI agent's active status. If active, the AI agent is available within the conversation.

</td></tr><tr><td>

Delete

</td><td>

Delete option for AI agent is inactive in Assistant Designer. The AI agent can only be deleted from AI Agent Studio.

</td></tr></tbody>
</table>AI agents become available in Assistant Designer based on the display settings in AI Agent Studio. To enable an AI agent to appear in Assistant Designer, perform the following:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select the **AI agents** tab, and open your chosen agent.
3.  Select the **Select channels and status** tab.
4.  In the **Engage via Virtual Agent assistants** card:

    -   Activate the **Allow** toggle switch.
    -   Under **Choose chat assistants**, select the assistants where the AI agent becomes discoverable.
    \[Omitted image "va-card-ai-agent.png"\] Alt text: Virtual Agent card in an AI agent.


For detailed information about creating AI agents, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-next-best-action-agent.md).

-   **[Using AI agents in Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/ai-agent-custom-skill.md)**  
Use an AI agent custom skill to have it perform a task passed to it, such as compiling info on a KB article.

**Parent Topic:**[Managing asset library items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/managing-asset-library-items.md)

**Related topics**  


[Configuring agentic conversations in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/agentic-conversations-vad.md)

