---
title: Decision tree nodes
description: Decision trees include several types of nodes, including start nodes, question nodes, guidance nodes, and linking nodes.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Decision trees in Guided decision, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Decision tree nodes

Decision trees include several types of nodes, including start nodes, question nodes, guidance nodes, and linking nodes.

A decision tree begins with a start node, which presents the first set of questions to an agent. The start node is typically followed by a question node, which asks another set of questions. A question node can be followed by another question node, a guidance node, which provides a recommendation to an agent, or by a linking node, which includes a reference to another decision tree.

You can enable agents to modify their responses in previous nodes:

-   Agents can go back to the previous node by selecting the **Back** button.
-   Agents can jump to any previous node by selecting the Edit icon ![Edit icon](../image/icon-pencil-ac.png)\) in the View my responses tab.

For more information, see [Create a decision tree in Core UI](../task/configure-decision-trees-gdb.md) and [Add questions or instructions to a decision tree](../task/configure-start-node-gdb.md).

## Start nodes

A start node is the first node in a decision tree. When you create a decision tree, you provide internal and external names, a title and short description, and a name for the action label. After saving the record, the system creates the decision tree and the start node. You can use this start node to build the rest of the decision tree.

A start node includes a minimum of one question. A start node always has a task input of reference type so you can reuse the task input in other decision or guidance nodes via linking inputs. The task input includes a reference to the table that stores the record type that the agent is working on.

## Decision or question nodes

A question node asks one or more questions. The answer to the question leads to an outcome, which can be another question, a guidance for the user to follow, or another decision tree.

A question node presents the agent with a question or instructions to follow to evaluate the customer's situation and provide the right solution. You can add HTML formatting, such as images, links, or text formatting to the question node. Examples of typical questions or instructions include:

-   For resetting a password: "What is the customer's account ID?"
-   For troubleshooting a faulty device: "What is the device type or model number?"

The answers to the questions are used to create path conditions.

For more information about the available answer types, see [Answer types for questions](../reference/type-of-answer.md).

**Note:** Using unsupported input types can cause errors in the runtime experience.

## Guidance nodes

A guidance node proposes a solution to a customer’s issue through a reference to a guidance, which provides a recommendation to an agent. Examples of a guidance include recommending a knowledge article, creating a work order, or escalating a case.

A guidance node can be followed only by a question node. The execution of the decision tree continues after the agent performs the guidance, and the guidance history is marked as complete. You can use a question node to connect two guidance nodes.

A guidance can have outputs, which drive further decision making. With a guidance, you can do the following:

-   Define output variables.
-   Define values for the output variables, which are mapped in the Automation Plan flow for the guidance by the Assign Guidance Outputs flow action.
-   Connect the guidance to the guidance node's next node.
-   Map the outputs of the guidance to inputs for the guidance node's next node.

For descriptions of the available guidances, see [Guidances included with Guided Decisions Experience application](../reference/components-installed-with-guided-decisions.md#section_mt1_njl_d5b).

Users with the Decision tree author role can also create guidances to reuse in decision trees or recommended actions. For more information, see [Create a guidance in the Core UI](../task/create-guidances.md).

## Linking nodes

A linking node includes a reference to another decision tree. This type of node connects the execution of the primary decision tree to another decision tree when a defined condition is met.

Linking to another decision tree is useful for complex troubleshooting or for troubleshooting that requires multiple stages.

A linking node includes the following elements:

-   A linked decision tree, where the execution of the primary decision tree continues after this node is reached.
-   Input mapping, which maps the inputs from the nodes preceding the linking node to the start node of the linked decision tree.
-   A path, which connects the previous question node to the start node of the child tree.

For more information, see the following topics:

-   For Decision Tree Builder: [Link an activated decision tree to this decision tree](../task/configure-linking-node-dtb.md).
-   For Core UI: [Link another decision tree to this decision tree](../task/configure-linking-node.md)

