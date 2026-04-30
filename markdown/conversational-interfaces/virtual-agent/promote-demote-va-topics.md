---
title: Promote or demote LLM conversational subflows, actions, and topics in Virtual Agent Designer
description: Promote assets including conversational subflows, conversational actions, and topics in Virtual Agent Designer, after associating them with a large language model \(LLM\) assistant, to have them suggested to the user by the LLM assistant.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Promote, Demote, LLM, Large language model, assist, topics, Virtual Agent Designer]
breadcrumb: [Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Promote or demote LLM conversational subflows, actions, and topics in Virtual Agent Designer

Promote assets including conversational subflows, conversational actions, and topics in Virtual Agent Designer, after associating them with a large language model \(LLM\) assistant, to have them suggested to the user by the LLM assistant.

## Before you begin

Associate an LLM topic, conversational subflow, or conversational action with an LLM assistant. For more information, see [Create a Virtual Agent topic](create-virtual-agent-topic.md), [Managing conversational subflows in Assistant Designer](../concept/managing-conversational-subflows.md), and [Managing conversational actions in Assistant Designer](../concept/managing-conversational-actions.md).

Role required: virtual\_agent\_admin or admin

## About this task

After you associate a conversational subflow, conversational action, or topic with an LLM assistant, you can promote the asset so that the LLM assistant suggests it to the users. Promoted assets can also be demoted to remove them from the list of suggested assets.

System topics, setup topics, topic blocks, custom controls, and small talk topics cannot be promoted.

**Note:** You can also promote NLU/keyword topics by creating topic recommendations in Conversational Interfaces settings. For more information, see [Using Virtual Agent Topic Recommendations](../concept/va-topic-recommendations.md).

For promotion controls for LLM assets, you can check the asset's **Promoted** status under the Show actions for this row icon ![](../images/kebab-menu.png). The **Promoted** status shows a check mark when the topic is promoted.

For more information about LLM assistants, see [LLM assistants](../../now-assist-in-va/concept/llm-assistants.md).

## Procedure

1.  Navigate to **All** &gt; **Virtual Agent** &gt; **Designer**.

2.  From the **Select assistant** drop-down menu, select the LLM assistant that will promote the asset.

    The list of assets reduces to LLM assets associated with the LLM assistant.

3.  Find the asset that you want to promote or demote.

4.  Select the Show actions for this row icon ![](../images/kebab-menu.png), and then select **Promote** to toggle the asset's **Promoted** status.

    If the asset is already promoted, the asset has a check mark next to the **Promoted** status. Demoting the asset removes the check mark.


## Result

![image.promoted-llm-topic-list-2]

The asset is added to the list of assets promoted by the LLM assistant, while a demoted asset is removed from the list.

A toast message also appears for four seconds, confirming that the asset has been promoted or demoted. You can close the message by selecting the Close icon ![](../images/gray-x-icon.png).

## What to do next

Reorder promoted LLM conversational subflows, actions, and topics in Virtual Agent. For more information, see [Reorder promoted LLM conversational subflows, actions, and topics](sort-promoted-va-topics.md).

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

