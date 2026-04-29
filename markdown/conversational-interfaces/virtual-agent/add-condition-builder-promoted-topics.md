---
title: Add a condition builder to promoted assets
description: You can define a condition for a given promoted Virtual Agent asset to bring it higher up on the list of promoted assets in a panel conversation.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [virtual agent, promoted, asset, condition, builder]
breadcrumb: [Getting started with Virtual Agent Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Add a condition builder to promoted assets

You can define a condition for a given promoted Virtual Agent asset to bring it higher up on the list of promoted assets in a panel conversation.

## Before you begin

Role required: virtual\_agent\_admin or admin.

To define a condition for an asset, you must promote it first. For more information, see [Promote or demote LLM conversational subflows, actions, and topics in Assistant Designer](promote-demote-va-topics.md).

## About this task

Add a condition to a chosen Virtual Agent topic to have it displayed higher on the list of promoted assets in a panel conversation. This condition overrides the **Number** value on the Promoted Skills \[sys\_cs\_context\_profile\_promoted\_skill\_list\] table.

## Procedure

1.  Navigate to **All**, then enter `sys_cs_context_profile_promoted_skill.list` in the filter.

2.  Select your chosen promoted asset from the list.

3.  In the **Condition** field, set the chosen condition for your promoted asset.

    For example, `URL > contains > conversation`.

4.  In the **Condition mode** field, select your condition.

    **Note:** In the current release, **Simple** is the only available condition mode.

5.  Select **Update**.


## Result

The promoted asset’s **Condition** on the Promoted Skills table shows the defined condition.

![Promoted skills table showing asset with defined condition.](../images/va-defined-promoted-topic-01.png)

The promoted asset now shows **Condition defined** next to the **Promoted** checkmark.

The promoted asset also displays at the top of the list of promoted assets in a Virtual Agent Now Assist panel chat window.

![Virtual Agent Now Assist panel chat window showing condition defined asset over other promoted assets.](../images/va-defined-promoted-topic-02.png)

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

