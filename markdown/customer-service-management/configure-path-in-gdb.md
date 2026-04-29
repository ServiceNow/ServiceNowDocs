---
title: Determine the next node displayed in a decision tree
description: Configure a path in Decision Tree Builder to set the conditions for when the next question or a guidance is displayed in a decision tree.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring decision trees in Decision Tree Builder, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Determine the next node displayed in a decision tree

Configure a path in Decision Tree Builder to set the conditions for when the next question or a guidance is displayed in a decision tree.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

You can create two or more paths from any question node.

Because you can add a question node only after a guidance node, the path configuration isn’t required.

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select **Open in Builder**.

4.  In Decision Tree Builder, select the Add path icon \(![Add path icon](../image/icon-add-path.png)\) on a node.

    A new path and a new node are added to the canvas.

5.  Select the new path.

6.  Enter a name for the path.

7.  In the **Path priority** field, enter a priority order for this path.

    The path with the lowest priority order is executed first.

8.  Configure one or more conditions by selecting a question from the previous node, an operator, and an input's value.

    For example, if the answer type is an integer, you can set a condition that when a value that a customer provides is more than the value you specify in the condition, this path must be taken.

    You can access the direct parent node’s inputs only while configuring a condition for the path.

9.  If there are multiple questions in a question node, select **New condition set** to define a complex condition for a combination of answers.

10. Select **Save and close**.


## What to do next

Continue building your decision tree.

-   Add a next set of questions. For more information, see [Add a follow-up set of questions or instructions in a decision tree](configure-decision-node-in-gdb.md).
-   Provide guidance to agents. For more information, see [Provide actions to agents in a decision tree](configure-guidance-in-gdb.md)

