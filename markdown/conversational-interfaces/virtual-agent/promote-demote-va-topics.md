---
title: Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer
description: You can promote assets, including conversational subflows, conversational actions, and topics, after associating them with an assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/promote-demote-va-topics.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Promote, Demote, LLM, Large language model, assist, topics, Virtual Agent Designer]
breadcrumb: [Build conversations, Virtual Agent, Conversational Interfaces]
---

# Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer

You can promote assets, including conversational subflows, conversational actions, and topics, after associating them with an assistant.

## Before you begin

Associate a Virtual Agent topic, conversational subflow, or conversational action with an assistant. For more information, see the following:

-   [Creating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md)
-   [Managing conversational subflows in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/managing-conversational-subflows.md)
-   [Managing conversational actions in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/managing-conversational-actions.md)

Role required: virtual\_agent\_admin or admin

## About this task

After you associate a conversational subflow, conversational action, or topic with an assistant, you can promote the asset so that the LLM assistant suggests it to users. Promoted assets can also be demoted to remove them from the list of suggested assets.

System topics, setup topics, topic blocks, custom controls, and small talk topics can't be promoted.

For promotion controls for AI assets, you can check the asset's **Promoted** status under the Show actions for this row icon \[Omitted image "kebab-menu.png"\] Alt text:. The **Promoted** status shows a check mark when the topic is promoted.

For more information about assistants, see [LLM assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/llm-assistants.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  From the **Select assistant** drop-down menu, select the LLM assistant that will promote the asset.

    The list of assets reduces to AI assets associated with the LLM assistant.

4.  Find the asset that you want to promote or demote.

5.  Select the Show actions for this row icon \[Omitted image "kebab-menu.png"\] Alt text:, and then select **Promote** to toggle the asset's **Promoted** status.

    If the asset is already promoted, the asset has a check mark next to the **Promoted** status. Demoting the asset removes the check mark.


## Result

\[Omitted image "promoted-llm-topic-list.png"\] Alt text: Virtual Agent chat window showing a list of promoted assets.

The asset is added to the list of assets promoted by the assistant, while a demoted asset is removed from the list.

A toast message also appears for four seconds, confirming that the asset has been promoted or demoted. You can close the message by selecting the Close icon \[Omitted image "gray-x-icon.png"\] Alt text:.

## What to do next

Reorder promoted conversational subflows, actions, and topics in Virtual Agent. For more information, see [Reorder promoted conversational subflows, actions, and topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/sort-promoted-va-topics.md).

-   **[Reorder promoted conversational subflows, actions, and topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/sort-promoted-va-topics.md)**  
Rearrange AI assets like conversational subflows, conversational actions, and Virtual Agent topics to the desired order after promoting them for recommendation by Virtual Agent.
-   **[Add a condition builder to promoted assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/add-condition-builder-promoted-topics.md)**  
You can define a condition for a given promoted Virtual Agent asset to bring it higher up on the list of promoted assets in a panel conversation.

**Parent Topic:**[Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

