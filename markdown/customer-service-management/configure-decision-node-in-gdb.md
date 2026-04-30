---
title: Add a follow-up set of questions or instructions in a decision tree
description: Configure a question node in Decision Tree Builder to add follow-up questions or instructions. Answer to these questions either lead to a guidance or a further set of questions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring decision trees in Decision Tree Builder, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Add a follow-up set of questions or instructions in a decision tree

Configure a question node in Decision Tree Builder to add follow-up questions or instructions. Answer to these questions either lead to a guidance or a further set of questions.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select **Open in Builder**.

4.  In Decision Tree Builder, add a new node by selecting the Add path icon \(![Add path icon](../image/icon-add-path.png)\) on a node.

5.  Select **Add node**.

6.  In the pop-up window, select **Ask users at least one question** to configure a question node.

7.  Enter a name for the node.

8.  In the Question 1 section, enter a question or instruction for customers.

9.  Make this question a required question by enabling the **Required question** field.

10. Enter more details related to your question or instruction in the **Additional details** field.

11. Select the type of answer.

    For a description of the answer types, see [Answer types for questions](../reference/type-of-answer.md).

    The answer the customer provides is passed to other nodes and paths via input mapping.

12. Link inputs to reuse answers from prior nodes.

    For more information, see [Reuse answers at decision points](map-inputs-in-decision-guidance-node.md).

13. Add more questions or instructions.

14. Select **Save and close**.


## What to do next

Continue building your decision tree.

-   Add a next set of questions. For more information, see [Add a follow-up set of questions or instructions in a decision tree](configure-decision-node-in-gdb.md)
-   Provide guidance to agents. For more information, see [Provide actions to agents in a decision tree](configure-guidance-in-gdb.md)

