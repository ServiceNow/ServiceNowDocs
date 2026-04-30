---
title: Add a next node after a guidance node
description: Add a next node that is a decision node after a guidance node. If a next node is configured, the execution of the decision tree continues after the agent performs the guidance and the guidance history is marked as complete.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Editing decision trees in Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Add a next node after a guidance node

Add a next node that is a decision node after a guidance node. If a next node is configured, the execution of the decision tree continues after the agent performs the guidance and the guidance history is marked as complete.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

You can only add a decision node after a guidance node.

-   You can add an intermediate decision node to add another guidance node.
-   You can configure a linking node after this decision node to link another decision tree.

You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create new decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select the guidance node.

4.  Select **Set Next Node**.

5.  In the **Label** field, enter a name for the next decision node.

6.  Select **Update**.


## What to do next

Continue building the decision tree.

-   [Add questions or instructions to a decision input](create-decision-input.md)
-   [Determine the next node in a decision tree](create-decision-paths.md)

