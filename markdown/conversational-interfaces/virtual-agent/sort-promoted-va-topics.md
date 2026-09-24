---
title: Reorder promoted conversational subflows, actions, and topics
description: Rearrange AI assets like conversational subflows, conversational actions, and Virtual Agent topics to the desired order after promoting them for recommendation by Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/sort-promoted-va-topics.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Promote or demote AI assets, Build conversations, Virtual Agent, Conversational Interfaces]
---

# Reorder promoted conversational subflows, actions, and topics

Rearrange AI assets like conversational subflows, conversational actions, and Virtual Agent topics to the desired order after promoting them for recommendation by Virtual Agent.

## Before you begin

Role required: virtual\_agent\_admin or admin

Promote the AI assets that you want to reorder in Assistant Designer. For more information about promoting assets, see [Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/promote-demote-va-topics.md)

## About this task

By default, promoted AI assets are presented in alphabetical order in the assistant. You can rearrange promoted assets in any desired order by editing their records from the Promoted Skills \[sys\_cs\_context\_profile\_promoted\_skill\] table. When conditions are applied to a promoted asset, and when the asset meets the condition, then it is displayed first by the assistant, irrespective of its set order.

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_context_profile_promoted_skill.list` in the filter.

2.  For the Virtual Agent topic, conversational subflow, or conversational action that you want to reorder, select the **Order** value.

    \[Omitted image "reorder.png"\] Alt text: Promoted skills table with Temporary Badge Request record name and Order highlighted.

3.  In the **Order** field, enter the new order and select **Update**.

    \[Omitted image "reorder-new.png"\] Alt text: Order field highlighted in Temporary Badge Request record.

    In the assistant, the promoted skills will appear in the set order.

    \[Omitted image "reorder-new-chat.png"\] Alt text: Reordered skills in chat.

4.  To add a condition, in the **Condition** builder, enter the required parameters and select **Update**.

    \[Omitted image "reorder-add-condition.png"\] Alt text: Temporary badge request record with Condition builder highlighted.

    In the assistant, the conditionally promoted skill will appear before the other assets.

    \[Omitted image "reorder-condition.png"\] Alt text: Conditionally reordered Temporary badge request in chat window.


## Result

The list of promoted assets is presented in a Virtual Agent conversation based on the Order value of each asset and the conditions applied.

## What to do next

Repeat the previous steps to adjust any other promoted assets to sort them in a preferred order.

**Parent Topic:**[Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/promote-demote-va-topics.md)

