---
title: Example: Troubleshoot a failed credit card transaction
description: Learn how process analysts or business owners configure a recommended action that uses a decision tree to troubleshoot a failed credit card transaction.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example configurations, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Example: Troubleshoot a failed credit card transaction

Learn how process analysts or business owners configure a recommended action that uses a decision tree to troubleshoot a failed credit card transaction.

## Problem scenario

Paul was trying to purchase a smart watch using his StellarVest bank credit card. But the transaction failed at the time of payment. Paul created a case in the StellarVest bank customer support portal seeking assistance.

In this scenario, the agent assigned to the Paul’s case is recommended to use a decision tree to troubleshoot the failed credit card transaction. The decision tree collects user, credit card, and transaction details. If money was debited, transaction tracking is initiated. However, if no money was debited, the agent provides a failure code, which determines what guidance is provided. Examples of potential guidances include: reassigning the case, creating a work order, or assigning the case to an IT technician.

## Configuring a recommended action for troubleshooting a failed credit card transaction

Help process analysts configure a recommended action of type decision tree that enables agents to troubleshoot a failed credit card transaction reported by customers.

|Task|Description|
|----|-----------|
|Creating a decision tree|Create a decision tree that enables agents to ask a series of questions to customers. Based on the answers provided, agents can troubleshoot and provide resolution to customer issues. For more information about how to configure a decision tree in Decision Tree Builder, see [Troubleshoot a failed credit card transaction decision tree](example-decision-tree.md).|
|[Create a rule from the Case context record](../task/ex-create-rule.md)|Create a rule to show recommendations for active cases that meet the condition specified in this rule.|
|[Create a recommendation with the decision tree as an action type](../task/ex-create-recommendation.md)|Create a recommendation that uses decision tree to troubleshoot a failed credit card transaction.|

