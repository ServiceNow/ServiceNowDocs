---
title: Determine the next node in a decision tree
description: Create a path to set conditions and priority order for the next node in a decision tree.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Editing decision trees in Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Determine the next node in a decision tree

Create a path to set conditions and priority order for the next node in a decision tree.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

Based on the answer a service agent provides to a question, a decision path guides the agent to the next decision node, a guidance path guides the agent to the next guidance node, and a linking path guides the agent to the next linking node.

You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create new decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select the start node or decision node.

4.  Select one of the following actions.

    |Action|Description|
    |------|-----------|
    |**__Create Decision Path__**|Creates a decision path to link this node to the next decision node. The decision node is automatically created.|
    |**__Create Guidance Path__**|Creates a guidance path to link this node to the next guidance node. The guidance node is automatically created.|
    |**__Create Linking Path__**|Creates a decision path to link this node to the next linking node. The linking node is automatically created.|

5.  In the **Label** field, enter a label for the path.

6.  In the **Order** field, enter a priority order for this path.

    The path with the lowest priority order is executed first.

7.  Configure a condition for this path to display the next node.

    |Path|Description|
    |----|-----------|
    |Decision path|Decision paths include conditions when the next question is displayed to an agent.|
    |Guidance path|Guidance paths include conditions when a guidance that provides resolution for an issue is displayed to an agent.|
    |Linking path|Linking paths include conditions when a next decision tree is executed.|

    You can only access the direct parent node’s inputs while configuring a condition for the path.

8.  Select **Update**.

    **Note:** You can create as many decision, guidance, or linking paths as required.


## What to do next

Continue building the decision tree.

-   [Add questions or instructions to a decision input](create-decision-input.md)
-   [Provide actions to agents in a decision tree](associate-guidance-path.md)
-   [Link another decision tree to this decision tree](configure-linking-node.md)

