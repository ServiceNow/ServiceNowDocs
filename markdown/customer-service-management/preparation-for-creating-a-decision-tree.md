---
title: Preparation for creating a decision tree
description: Before configuring a decision tree, process analysts should document the flow of the decision tree using a flow chart including the questions, answers, associated paths, and guidance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Preparation for creating a decision tree

Before configuring a decision tree, process analysts should document the flow of the decision tree using a flow chart including the questions, answers, associated paths, and guidance.

Anita, who is a process analyst at the StellarVest bank wants to create a decision tree that enables agents to troubleshoot a failed credit card transaction.

Anita first creates a flowchart to document the flow of a decision tree to determine the questions, answers, and possible guidance to configure.

![A flow chart depicting the flow of the decision tree that the admin wants to configure.](../image/ex-decision-tree-flow-chart.png)

|No.|Element|Name|Description|
|---|-------|----|-----------|
|1|Start node|[Card holder and transaction details](../task/ask-card-holder-and-transaction-details.md)|Start node that collects customer, credit card, and transaction details.|
|2|Path|[Amount is debited](configuring-paths-for-next-nodes.md#)|Path with condition: Amount is debited.|
|3|Guidance node|[Initiate transaction tracking](../task/configure-guidance-node-initiate-transaction-tracking.md)|Guidance to initiate transaction tracking when amount is debited.|
|4|Question node|[Further assistance needed](../task/configure-a-question-node-for-further-assistance.md)|Ask whether the customer needs further assistance.|
|5|Guidance node|Provide more options|Guidance to provide more options such as talk to an agent or request a new card.|
|6|Path|[Amount is not debited](configuring-paths-for-next-nodes.md#)|Path with condition: amount isn’t debited.|
|7|Question node|[Failure codes](../task/configure-question-node-to-ask-failure-codes.md)|Collect transaction failure codes when amount isn’t debited.|
|8|Path|[Error 200](../task/configure-path-for-200-failure-code.md)|Error code received is 200.|
|9|Guidance node|[Reassign case](../task/associate-guidances-for-different-failure-codes.md)|Guidance to reassign the case to someone else.|
|10|Path|[Error 300](../task/configure-path-for-200-failure-code.md)|Error code received is 300.|
|11|Guidance node|[Create work order](../task/associate-guidances-for-different-failure-codes.md)|Guidance to create a work order for dispatching a new credit card.|
|12|Path|[Error 500](../task/configure-path-for-200-failure-code.md)|Error code received is 500.|
|13|Guidance node|[Assign IT technician](../task/associate-guidances-for-different-failure-codes.md)|Guidance to assign an IT technician to resolve the issue.|

