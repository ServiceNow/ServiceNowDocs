---
title: Add questions or instructions to a decision tree
description: Add questions you want to ask your customers or instructions you want to provide to them and configure answer types in a start node in Decision Tree Builder.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring decision trees in Decision Tree Builder, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Add questions or instructions to a decision tree

Add questions you want to ask your customers or instructions you want to provide to them and configure answer types in a start node in Decision Tree Builder.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

The start node is the first node in a decision tree. It contains a task input and a minimum of one question or instruction. You can configure one or more questions to ask customers or instructions to provide to them.

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select **Open in Builder**.

4.  In Decision Tree Builder, select **New node**.

5.  In the **Node name** field, enter a name for the start node.

6.  In the **Reference table** field, select a table for the record type.

    The table that you select for the task input does not necessarily have to be a task table. For example, you can select a case, incident, or interaction table for the record context to recommend this decision tree in a workspace.

    **Note:** You must select the same table as the reference table for the context record in Recommended Actions.

7.  In the Question 1 section, enter a question or instruction for customers.

    You can add text formatting, images, or links using the controls at the top of the Question 1 section.

8.  Make this question a required question by selecting the **Required question** field.

9.  Select the type of answer for your question.

    For a description of the answer types, see [Answer types for questions](../reference/type-of-answer.md).

    The answer the customer provides to a question can be passed to other nodes and paths via input mapping.

10. Link inputs to reuse answers from prior nodes.

    For more information, see [Reuse answers at decision points](map-inputs-in-decision-guidance-node.md).

11. Add more questions or instructions.

12. Select **Save and close**.


## What to do next

[Determine the next node displayed in a decision tree](configure-path-in-gdb.md)

