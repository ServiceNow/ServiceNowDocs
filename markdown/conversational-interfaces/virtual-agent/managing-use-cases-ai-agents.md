---
title: Managing AI agents in Assistant Designer
description: View AI agents created in AI Agent Studio through Assistant Designer.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-05-19"
reading_time_minutes: 3
keywords: [Virtual Agent, Designer, AI Agents]
breadcrumb: [Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Managing AI agents in Assistant Designer

View AI agents created in AI Agent Studio through Assistant Designer.

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

**Role required**: virtual\_agent\_admin

When you select an AI agent, it opens in AI Agent Studio. AI agents currently can't be created or edited in Virtual Agent Designer. You can only view them in Assistant Designer. They can be created, edited, tested, and deleted only in AI Agent Studio. For more details, see [AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## AI agents in Virtual Agent Designer

Select the **AI agents** option to see all the AI agents activated for Assistant Designer.

![AI agents inAssistant Designer.](../images/vad-ai-agent-2.png)

|Column|Description|
|------|-----------|
|Name|Name of the AI agent. Select the AI agent to open it in AI Agent Studio.|
|Type|AI agent.|
|Status|Status type such as Published.|
|Active|Whether the AI agent is active or inactive.|
|Last modified|Time when the AI agent was last modified.|
|Description|Description of the AI agent.|

Use the row actions icon \( ![](../images/kebab-menu.png)\) to work with visibility settings for **Promoted**, **Discoverable**, **Visible**, and **Active**:

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

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview** and select the AI agent.
2.  Select the **Define availability** tab.
3.  In the **Engage via Virtual Agent assistants** card:

    -   Activate the **Allow** toggle switch.
    -   Under **Choose chat assistants**, select the assistants where the AI agent becomes discoverable.
    ![Virtual Agent card in an AI agent.](../images/va-card-ai-agent-2.png)


For detailed information about creating AI agents, see [Create an AI agent](https://www.servicenow.com/docs/access?context=configure-next-best-action-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

**Related topics**  


[Agentic conversations in Virtual Agent](agentic-conversations-vad.md)

