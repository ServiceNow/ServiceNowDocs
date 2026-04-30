---
title: Edit a decision tree
description: Edit a decision tree that you created using Core UI to improve or extend a troubleshooting process.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Editing decision trees in Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Edit a decision tree

Edit a decision tree that you created using Core UI to improve or extend a troubleshooting process.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

You can edit or extend existing decision trees in the Core UI but you can no longer create them. Use Decision Tree Builder to create new decision trees. For more information, see [Configuring decision trees in Decision Tree Builder](../concept/decision-trees-in-gdb.md).

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  On the form, edit the fields, as necessary.

<table id="table_v1f_pzl_vwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The internal name of the decision tree.**Note:** A start node is created for the decision tree with this name.

</td></tr><tr><td>

Action Label

</td><td>

The label of the call-to-action button on the Recommended Actions card.

</td></tr><tr><td>

Description

</td><td>

The description of the decision tree to show on the Recommended Actions card.

</td></tr><tr><td>

Start Node

</td><td>

The reference of the start node.

</td></tr><tr><td>

Title

</td><td>

The external name of the decision tree that end-users or agents can see in a workspace.If the **Title** field is empty, the internal name is shown as the external name on the Recommended Actions card.

</td></tr><tr><td>

Show a dismiss button

</td><td>

Shows or hides the **Dismiss** button that cancels the flow of a decision tree. This field is turned on by default.

</td></tr></tbody>
</table>4.  Select **Update**.


## What to do next

[Add questions or instructions to a decision input](create-decision-input.md)

