---
title: Link another decision tree to this decision tree
description: Nest and invoke decision trees from linking nodes when specific conditions are met. Use guidance output and nested trees to execute complex troubleshooting.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Editing decision trees in Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Link another decision tree to this decision tree

Nest and invoke decision trees from linking nodes when specific conditions are met. Use guidance output and nested trees to execute complex troubleshooting.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

Create a linking path first. A linking node is automatically created with the same name as the linking path.

## About this task

The execution of the linked decision tree begins when a specific condition specified in the linking path is met. The linking node holds a reference of the start node in the next decision tree.

You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create new decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select the linking node.

4.  In the **Linked Decision Tree** field, select an available decision tree from the list.

5.  Select **Update**.


