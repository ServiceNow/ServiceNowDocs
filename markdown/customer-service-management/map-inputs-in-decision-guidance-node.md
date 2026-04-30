---
title: Reuse answers at decision points
description: Link inputs to reuse answers from prior nodes in Decision Tree Builder. For example, in a decision tree that deals with a loan application, you could reuse the input related to the customer’s salary at multiple decision points to determine the loan eligibility.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring decision trees in Decision Tree Builder, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Reuse answers at decision points

Link inputs to reuse answers from prior nodes in Decision Tree Builder. For example, in a decision tree that deals with a loan application, you could reuse the input related to the customer’s salary at multiple decision points to determine the loan eligibility.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

Linked inputs can be used to create path conditions.

For more information about input mapping and exceptions related to input mapping, see [Linking inputs in decision tree nodes](../reference/guided-decision-tree-input-mapping.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select **Open in Builder**.

4.  In Decision Tree Builder, select the node you want to map inputs to.

<table id="table_tqp_hlz_qwb"><thead><tr><th>

Node type

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Question node

</td><td>

1.  Enter a question and select the type of answer.
2.  Select **Link inputs to reuse prior data**.
3.  Use the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to select a prior node and an input that you want to reuse in this question.
 **Note:** The question with a reused answer is answered automatically during runtime.

</td></tr><tr><td>

Guidance node

</td><td>

1.  Select a guidance from the list.
2.  Select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to select a prior node and the input that you want to reuse in the guidance input.


</td></tr><tr><td>

Linking node

</td><td>

1.  Select a child tree from the list.
2.  Select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) to select a prior node and the input that you want to reuse in the start node of the child tree.


</td></tr></tbody>
</table>5.  Select **Save and close**.


