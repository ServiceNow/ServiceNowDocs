---
title: Configuring decision trees in Decision Tree Builder
description: Configure decision trees using the no-code visual Decision Tree Builder, which provides a canvas for a diagrammatic representation of nodes and their paths in a troubleshooting process.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configuring decision trees in Decision Tree Builder

Configure decision trees using the no-code visual Decision Tree Builder, which provides a canvas for a diagrammatic representation of nodes and their paths in a troubleshooting process.

As a process owner or business analyst, you can configure [decision tree](https://www.servicenow.com/docs/access?context=now-platform-glossary&version=yokohama&pubname=yokohama-glossary&section=gloss-decision-tree&ft:locale=en-US) by adding nodes, defining paths, and attaching guidances through Decision Tree Builder. For more information, see [Decision tree nodes](guided-decision-tree-node-types.md).

You can validate and activate a decision tree with a single action. For more information, see [Activate a decision tree](../task/activate-guided-decision-tree.md).

## Decision Tree Builder canvas

![Decision Tree Builder with a flow chart and a side panel that has node configuration properties.](../image/diagram-canvas-gd-builder.png)

## Accessing Decision Tree Builder

You can access the Decision Tree Builder by selecting the **Open in Builder** button on the decision tree record.

## Configuring question and guidance nodes

You can configure a new node as a question node or a guidance node. When there are multiple questions in a start node or a question node, you can delete a question or change the order of the questions. For more information, see [Add questions or instructions to a decision tree](../task/configure-start-node-gdb.md).

Guidance nodes provide actions to agents to resolve or escalate a customer issue. You can either select a guidance from the list of available guidances or create a guidance in Core UI. You can then configure guidance inputs by entering static values or reuse inputs from prior nodes. For more information, see [Provide actions to agents in a decision tree](../task/configure-guidance-in-gdb.md).

## Linking node

You can configure a new node as a linking node to link a child decision tree to the current decision tree. This linking connects the execution of the primary decision tree to another decision tree when a specific condition is met. For more information, see [Link an activated decision tree to this decision tree](../task/configure-linking-node-dtb.md).

## Creating paths for the next nodes

A path in a decision tree connects one node to another. You can configure a condition to define when the path must be taken. Selecting certain answers can be a condition for the path. The priority order for a path sets the precedence of one path over another.

For more information, see [Determine the next node displayed in a decision tree](../task/configure-path-in-gdb.md).

## Editing a node or a path

When you edit the inputs of nodes and their paths, make sure to update the following nodes as well because they might be reusing data from these inputs.

## Deleting a node or a path

Note the following information about deleting a node or path:

-   You can delete a leaf node if it isn’t connected to any path or a node.
-   Deleting a leaf node removes the node from the decision tree but the configuration of the path before the deleted node remains intact.
-   You can't delete an intermediate node or path.
-   When you delete the question node after a guidance node, both the question node and the path are deleted.

## Linking inputs

You can link inputs from one node to another to reuse input values from prior nodes. You can use linked inputs to create path conditions. For more information about input mapping in the question node or guidance node, see [Linking inputs in decision tree nodes](../reference/guided-decision-tree-input-mapping.md).

For more information, see [Reuse answers at decision points](../task/map-inputs-in-decision-guidance-node.md).

**Related topics**  


[Validation error notifications in Decision Tree Builder](validation-errors-builder.md)

[Activate a decision tree](../task/activate-guided-decision-tree.md)

[Revert to the previous activated decision tree version](../task/discard-latest-changes.md)

