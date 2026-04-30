---
title: Link task input in the start node to the guidance
description: Link the task input in the start node to the task input in the guidance to pass record information.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Provide actions to agents in a decision tree, Editing decision trees in Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Link task input in the start node to the guidance

Link the task input in the start node to the task input in the guidance to pass record information.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

The task input in the start node holds a reference of the record that an agent is working on in a workspace. For example, if you want to attach a KB article to a case, you would need the case number.

You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create new decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select the guidance node created.

4.  Select **Create Input Mapping**.

5.  In the **Source Node** field, select the start node of your decision tree.

6.  In the **Source Input** field, select the task input.

7.  In the **Destination Input** field, select the task input associated with the guidance.

    **Note:** The **Destination Node** is automatically filled with the value of the decision node that you’re creating the input mapping from.

8.  Select **Submit**.


