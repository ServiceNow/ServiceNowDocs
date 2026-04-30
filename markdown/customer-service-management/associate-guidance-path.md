---
title: Provide actions to agents in a decision tree
description: Associate a guidance to a guidance node so that service agents can act to resolve or escalate a customer issue.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Editing decision trees in Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Provide actions to agents in a decision tree

Associate a guidance to a guidance node so that service agents can act to resolve or escalate a customer issue.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

Create a guidance path first. A guidance node is automatically created with the same name as the guidance path.

## About this task

A guidance is an outcome of a decision tree.

You can either create a guidance or select a guidance from a list. For a complete list of guidances that are available by default, see [Components installed with Guided Decisions Experience](../reference/components-installed-with-guided-decisions.md). You can then enter guidance inputs, as required.

You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select the guidance node created.

4.  In the **Guidance** field, select a guidance to associate with the guidance node.

5.  Depending on the guidance you selected, enter guidance inputs, as required.

    **Note:** If you selected the Attach Knowledge Article guidance, enter the knowledge article to link to.

    If you selected the Provide Resolution guidance, enter the case, resolution notes, and a resolution code.

    If you selected the Create Work Order guidance, enter the task to link to.

6.  Select **Update**.


## What to do next

[Link task input in the start node to the guidance](associate-task-input-to-guidance.md)

