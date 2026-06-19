---
title: Reorder promoted LLM conversational subflows, actions, and topics
description: Rearrange LLM assets like conversational subflows, conversational actions, and topics to the desired order after promoting them for recommendation by the Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/sort-promoted-va-topics.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Reorder promoted LLM conversational subflows, actions, and topics

Rearrange LLM assets like conversational subflows, conversational actions, and topics to the desired order after promoting them for recommendation by the Virtual Agent.

## Before you begin

Role required: virtual\_agent\_admin or admin

Promote the LLM assets that you want to reorder in Virtual Agent Designer. For more information on promoting assets, see [Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/promote-demote-va-topics.md)

## About this task

By default, promoted LLM assets are presented in alphabetical order in the assistant. You can rearrange promoted assets in any desired order by editing their records from the Promoted Skills \[sys\_cs\_context\_profile\_promoted\_skill\] table. When conditions are applied to a promoted asset, and when the asset meets the condition, then it is displayed first by the assistant, irrespective of its set order.

## Procedure

1.  Navigate to the Promoted Skills \[sys\_cs\_context\_profile\_promoted\_skill\] table by selecting **All** and entering `sys_cs_context_profile_promoted_skill.list` in the filter.

2.  For the LLM topic, conversational subflow, or conversational action that you want to reorder, select the **Order** value.

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

**Parent Topic:**[Getting started with Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

