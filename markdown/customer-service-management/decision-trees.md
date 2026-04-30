---
title: Editing decision trees in Core UI
description: You can edit decision trees created in Core UI to improve or extend a troubleshooting process.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Editing decision trees in Core UI

You can edit decision trees created in Core UI to improve or extend a troubleshooting process.

**Note:** You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create new decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](decision-trees-in-gdb.md).

![Decision tree configuration flow.](../image/editing-decision-tree.png "Decision tree configuration flow in Core UI")

The following table provides high-level information for editing a decision tree in the Core UI.

<table id="table_hxd_yc1_3xb"><thead><tr><th>

Decision tree step

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure a start node and a task input

</td><td>

Each decision tree includes a start node of type decision and a task input. The task input stores a reference of the record that the agent is working on. For more information, see [Edit a decision tree](../task/configure-decision-trees.md).Select the start node from the Decision Tree Nodes related list. Create inputs to add initial questions you want to ask customers. Select the input type for the expected answer and configure the answers in the related list. For more information, see [Add questions or instructions to a decision input](../task/create-decision-input.md).

</td></tr><tr><td>

Create a decision path

</td><td>

Create a decision path and configure conditions for the next decision node. For example, you can set up a condition to select an answer for the question in the start node. When a user selects this answer, this path that leads to a decision node is taken. For more information, see [Determine the next node in a decision tree](../task/create-decision-paths.md).A decision node is automatically created.

</td></tr><tr><td>

Create inputs to add follow-up questions in the decision node

</td><td>

Select the input type for the expected answer and configure the answers in the related list. For more information, see [Add questions or instructions to a decision input](../task/create-decision-input.md).

</td></tr><tr><td>

Create a guidance path

</td><td>

Create a guidance path and configure conditions for the next guidance node. For example, you can set up a condition to select an answer for the question in the start node or decision node. When a user selects that answer, this path leads to a guidance node. For more information, see [Determine the next node in a decision tree](../task/create-decision-paths.md).A guidance node is automatically created.

</td></tr><tr><td>

Configure the created guidance node

</td><td>

Configure the guidance node to provide resolution to a customer. Associate a guidance to the guidance node and configure the guidance inputs. For more information, see [Provide actions to agents in a decision tree](../task/associate-guidance-path.md).

</td></tr><tr><td>

Create a linking path

</td><td>

Create a linking path and configure conditions for the next decision tree. For example, you can set up a condition to select an answer for the question in the decision node. When a user selects that answer, this path leads to the next decision tree. For more information, see [Determine the next node in a decision tree](../task/create-decision-paths.md).A linking node is automatically created.

</td></tr><tr><td>

Configure the created linking node

</td><td>

Configure the linking node to link another decision tree to this decision tree. For more information, see [Link another decision tree to this decision tree](../task/configure-linking-node.md).

</td></tr><tr><td>

Configure a next node

</td><td>

Configure a next node that is a decision node.

 **Note:** You can't add another guidance node after a guidance node.

 -   You can add an intermediate decision node to add another guidance node.
-   You can configure a linking node after this decision node to link another decision tree.

 For more information, see [Add a next node after a guidance node](../task/add-next-node-after-guidance.md).

</td></tr><tr><td>

Map inputs from one node to another

</td><td>

Map inputs from one node to another to reuse answers by selecting a source node and a source input and a destination input.In the guidance node, you can pass inputs from the prior nodes to the guidance inputs by using the Pill-picker icon \(![Pill-picker icon](../image/icon-pill-picker.png)\) to reuse answers.

For more information, see [Reuse answers at decision points](../task/create-input-mappings.md).

</td></tr></tbody>
</table>**Note:** To go back to your decision tree from any node, select the Preview this record icon \(![Preview this record icon](../image/preview-record.png)\) next to the **Decision Tree** field and then select **Open Record**. You can see all the nodes that you created in the related list.

