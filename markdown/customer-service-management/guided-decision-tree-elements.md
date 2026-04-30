---
title: Decision tree elements
description: Decision trees are made up of several types of elements including nodes, inputs, and paths.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Decision trees in Guided decision, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Decision tree elements

Decision trees are made up of several types of elements including nodes, inputs, and paths.

Decision trees are built using different elements, which are described in the following table. The terminology for these elements differs slightly between Decision Tree Builder and Core UI but the definitions remain the same. For more information decision tree nodes and paths, see [Decision tree nodes](../concept/guided-decision-tree-node-types.md) and [Decision tree paths](guided-decision-tree-paths.md).

<table id="table_ofw_y5h_vwb"><thead><tr><th>

Core UI term

</th><th>

Decision Tree Builder term

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Decision tree

</td><td>

Decision tree

</td><td>

A multi-step process that includes a series of questions and answers. Based on the answers, each question in a decision tree leads to another question, a guidance for the agent to follow, or another decision tree.

</td></tr><tr><td>

Node

</td><td>

Node

</td><td>

A node is a point in a decision tree. You can create different types of nodes depending on what is happening at that point in the tree. Node types include the following:-   Start node
-   Question node
-   Guidance node
-   Linking node

</td></tr><tr><td>

Start node

</td><td>

Start node

</td><td>

The first node in a decision tree. When you create a decision tree, the system automatically creates the start node. The start node can be a question or a task.

</td></tr><tr><td>

Decision node

</td><td>

Question node\(When adding a node and selecting **Ask users at least one question** in the pop-up window\)

</td><td>

This type of node represents one or more questions. The answers to the questions lead to an outcome, which can be another question, a guidance, or another decision tree.

</td></tr><tr><td>

Guidance node

</td><td>

Guidance node\(When adding a node and selecting **Propose a guidance as an outcome** in the pop-up window\)

</td><td>

This type of node has a reference to a guidance, which provides a recommendation to an agent.

</td></tr><tr><td>

Linking node

</td><td>

Linking node \(When adding a node and selecting **Link decision tree** in the pop-up window\)

</td><td>

A linking node includes a reference to another decision tree. This linking connects the execution of the primary decision tree to another decision tree when a specific condition is met.

</td></tr><tr><td>

Guidance

</td><td>

Guidance

</td><td>

An action that an agent can take or information that an agent can share. You can select guidances included with the Guided Decisions Experience plugin or you can [Create a guidance in the Core UI](../task/create-guidances.md).

</td></tr><tr><td>

Decision input

</td><td>

Question or instruction

</td><td>

A question or instruction with a configured answer type. When working through a decision tree, an agent can provide an answer to the question in the format of answer type that you configure.

</td></tr><tr><td>

Input type

</td><td>

Type of answer

</td><td>

The type of data that the question in a question node can accept as an answer, such as string, integer, or choice.For a list of supported input types, see [Answer types for questions](type-of-answer.md).

</td></tr><tr><td>

Decision input mapping

</td><td>

Link input

</td><td>

Linking inputs from one decision tree node to another to reuse input values in prior decision tree nodes.

</td></tr><tr><td>

Label \(for a node\)

</td><td>

Node name

</td><td>

The name for a question, guidance, or linking node.In Decision Tree Builder, this name appears on the node in the canvas.

</td></tr><tr><td>

Type \(for a node\)

</td><td>

Node purpose

</td><td>

The type of a node in the Decision Tree Node record in Core UI.The purpose of a node in the right panel in Decision Tree Builder.

-   Question node: Ask users at least one question
-   Guidance node: Propose a guidance as an outcome

</td></tr><tr><td>

Not applicable

</td><td>

Path

</td><td>

A path connects two nodes in a decision tree or question node to the start node of the next decision tree. A path is created and associated with a node and represents the potential outcome of that node.

</td></tr><tr><td>

Decision path

</td><td>

Not applicable

</td><td>

A path that provides possible outcomes of a decision node. A decision path links a decision node to the next node of type decision.

</td></tr><tr><td>

Guidance path

</td><td>

Not applicable

</td><td>

A path that links a decision node to the next node of type guidance.

</td></tr><tr><td>

Linking path

</td><td>

Not applicable

</td><td>

A path that links a decision node to the start node of the next decision tree.

</td></tr><tr><td>

Order

</td><td>

Path priority

</td><td>

The priority in which the path is executed.

</td></tr></tbody>
</table>