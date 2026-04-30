---
title: Reorder promoted LLM topics in Virtual Agent
description: Arrange large language model \(LLM\) topics to a desired non-alphabetical order after promoting them for recommendation by the Virtual Agent.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-09-13"
reading_time_minutes: 1
breadcrumb: [Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Reorder promoted LLM topics in Virtual Agent

Arrange large language model \(LLM\) topics to a desired non-alphabetical order after promoting them for recommendation by the Virtual Agent.

## Before you begin

Promote any Virtual Agent LLM topics you want to reorder. For more information, see [Promote or demote LLM topics in Virtual Agent Designer](promote-demote-va-topics.md)

Role required: virtual\_agent\_admin or admin

## About this task

Promoted LLM topics are presented in alphabetical order by default. You can rearrange promoted topics in any desired order by editing their records in the Promoted Skills \[sys\_cs\_context\_profile\_promoted\_skill\] table.

## Procedure

1.  Navigate to **All** &gt; **sys\_cs\_context\_profile\_promoted\_skill.list**.

2.  Under the topic you want to reorder, select the **Order** value.

3.  Enter a number.


## Result

The list of promoted skills is presented in a Virtual Agent conversation based on the Order value of each topic from lowest to highest number relative to other promoted topics.

## What to do next

Repeat the previous steps to adjust any other promoted topics to sort them in a desired order.

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

