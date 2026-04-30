---
title: Create a decision tree in Core UI
description: Create a decision tree that agents can use to troubleshoot solutions to customer issues.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a decision tree in Core UI

Create a decision tree that agents can use to troubleshoot solutions to customer issues.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

Decision trees are first created in Core UI. You then use Decision Tree Builder to configure the start node and add nodes and paths to build a decision tree.

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  On the Decision Trees page, select **New**.

3.  On the form, fill in the fields.

<table id="table_v1f_pzl_vwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The internal name of the decision tree.

</td></tr><tr><td>

Action Label

</td><td>

The label of the call-to-action button on the Recommended Actions card.

</td></tr><tr><td>

Description

</td><td>

The description of the decision tree to show on the Recommended Actions card.

</td></tr><tr><td>

Title

</td><td>

The external name of the decision tree that end-users or agents see in a workspace.If the **Title** field is empty, the internal name is shown as the external name on the Recommended Actions card.

</td></tr><tr><td>

Question font size

</td><td>

The font size of the questions in the guided decision tree. It reflects in the workspace and service portal.The font size defined in the parent decision tree is inherited by the child decision tree even though the Question font size for the child decision tree has its own Question font size defined.

 You may need to configure the form to add this field.

</td></tr><tr><td>

Show a dismiss button

</td><td>

Shows or hides the **Dismiss** button that cancels the flow of a decision tree. This field is turned on by default.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

A decision tree record and a start node are created.

## What to do next

Configure a start node to [add initial set of questions or instructions to a decision tree](configure-start-node-gdb.md) in Decision Tree Builder.

