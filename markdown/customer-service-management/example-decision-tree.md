---
title: Example configuration of a decision tree
description: This example demonstrates an end-to-end configuration of a decision tree to help you get started with Guided Decisions. After you configure the decision tree, you can either embed it in a playbook or use it as a recommendation in Recommended Actions.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Example configuration of a decision tree

This example demonstrates an end-to-end configuration of a decision tree to help you get started with Guided Decisions. After you configure the decision tree, you can either embed it in a playbook or use it as a recommendation in Recommended Actions.

For more information about decision trees, see [Decision trees in Guided decision](decision-trees-in-guided-decisions.md) and [Configuring guidances and decision trees](configuring-guided-decisions.md).

## Troubleshooting a failed credit card transaction

Paul, who holds an account with the StellarVest bank is trying to purchase a smart watch using their credit card. But the transaction failed at the time of payment. Paul created a case in the StellarVest bank portal seeking assistance. Agents from the StellarVest bank work on the cases created by customers to resolve their issues.

In this scenario, the agent assigned to the Paul’s case uses a decision tree to troubleshoot the failed credit card transaction. The decision tree collects user, credit card, and transaction details. If money was debited, transaction tracking is initiated. However, if no money was debited, the agent provides a failure code which determines what guidance is provided. Examples of potential guidances include: reassigning the case, creating a work order, or assigning the case to an IT technician.

![A completed decision tree for troubleshooting a failed credit card transaction in Decision Tree Builder. The tree includes start node, question nodes, and guidance nodes.](../image/example-complete-decision-tree.png)

## Creating the decision tree to troubleshoot the failed transaction

Learn how process analysts or business owners create a decision tree, and configure various decision tree nodes in the [next pages](preparation-for-creating-a-decision-tree.md).

