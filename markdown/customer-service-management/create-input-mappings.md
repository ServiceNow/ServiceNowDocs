---
title: Reuse answers at decision points
description: Create input mapping to reuse answers from prior nodes. For example, in a decision tree that deals with loan application, you can reuse the input related to the customer’s salary at multiple decision points to determine the loan eligibility.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Editing decision trees in Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Reuse answers at decision points

Create input mapping to reuse answers from prior nodes. For example, in a decision tree that deals with loan application, you can reuse the input related to the customer’s salary at multiple decision points to determine the loan eligibility.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

For more information about input mapping in a decision node or a guidance node, see [Linking inputs in decision tree nodes](../reference/guided-decision-tree-input-mapping.md).

Mapped inputs can be used to create path conditions.

You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create new decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision node or the guidance node that must reuse inputs.

3.  Click **Create Input Mapping**.

4.  In the **Source Node** field, select the node you want to copy from.

5.  In the **Source Input** field, select the node input to copy.

6.  In the **Destination Input** field, select the node input you want to copy the values to.

    **Note:** The **Destination Node** is automatically filled with the value of the node that you're creating the input mapping for.

7.  Select **Submit**.


