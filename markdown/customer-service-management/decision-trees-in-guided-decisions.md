---
title: Decision trees in Guided decision
description: Decision trees and guidances enable agents to work through a structured troubleshooting process to resolve customer issues faster and provide standardized resolution.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-03-27"
reading_time_minutes: 2
breadcrumb: [Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Decision trees in Guided decision

Decision trees and guidances enable agents to work through a structured troubleshooting process to resolve customer issues faster and provide standardized resolution.

-   **Decision trees**

    A decision tree is a multi-step process that includes a series of questions, answers, and a guidance for an agent to follow. This process is made up of different decision tree elements, including nodes, inputs, and paths. For more information, see [Decision tree elements](../reference/guided-decision-tree-elements.md).

    Decision trees contain different types of nodes. Decision nodes represent one or more questions. Guidance nodes provide recommendations to agents. Each decision tree has a root node called the start node. Each node includes a path to the next node. Based on the answers to the questions, each decision node leads to an outcome, which can be a guidance, a follow-up question, or another decision tree.

-   **Guidances**

    A guidance is an action that an agent can take or information that an agent can share. For example, a guidance can recommend that the agent can share a knowledge article or create a work order. Agents can perform the action by clicking a button on the card.


## Decision tree example

The following example uses a flowchart to show the structure of a decision tree that determines customer eligibility for a promotion. This promotion is available to customers who opened their accounts within the last 30 days.

![Decision tree that asks questions to determine if a customer is available for a promotion. Accounts open less than thirty days are eligible.](../image/decision-tree-basic-diagram1.png "Decision tree for evaluating customer eligibility")

The agent can select one of two paths to answer the question "Is this a new customer?"

-   The **No** path indicates that the customer isn’t eligible for the promotion.
-   The **Yes** path asks an additional question to determine if the account has been open for more than 30 days.
    -   If **Yes**, the customer isn’t eligible for the promotion.
    -   If **No**, the customer is eligible to receive the promotion.

![Decision tree nodes include configuration details such as name, type, and input.](../image/decision-tree-diagram-detailed.png "Decision tree configuration details")

For more information about creating a decision tree, see the following topics:

-   [Configuring decision trees in Decision Tree Builder](decision-trees-in-gdb.md)
-   [Create a decision tree in Core UI](../task/configure-decision-trees-gdb.md)

