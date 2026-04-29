---
title: Provide actions to agents in a decision tree
description: Configure a guidance node in Decision Tree Builder so agents can view a recommendation on what to do next.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring decision trees in Decision Tree Builder, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Provide actions to agents in a decision tree

Configure a guidance node in Decision Tree Builder so agents can view a recommendation on what to do next.

## Before you begin

Verify that the guidances you want to use exist or create them. For more information, see [Create a guidance in the Core UI](create-guidances.md).

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

**Note:** If the **Allow users to re-run the guidance** field is selected when creating a guidance, users can re-execute the guidance or go back and modify responses in the previous question nodes in the run-time experience.

You can link guidance inputs and outputs to the next question node.

You can select a guidance from the list of available guidances to link to your guidance node or create a new one in Core UI.

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

2.  Select the decision tree from the list.

3.  Select **Open in Builder**.

4.  In Decision Tree Builder, add a new node by selecting the Add path icon \(![Add path icon](../image/icon-add-path.png)\) on a node.

5.  Select **Add node**.

6.  In the pop-up window, configure a guidance node by selecting **Propose a guidance as an outcome**.

    A guidance is an outcome of a decision tree.

7.  Enter a name for the node.

8.  In the **Guidance** field, select the guidance by starting to type the guidance name and selecting it from the list.

9.  Enter specific values for guidance inputs in the **Set field inputs to pass data into this guidance** section.

    These fields can contain static text, dynamic content such as field values from guidance inputs, or a combination of static text and dynamic content. To use dynamic content, select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) next to the field and select a guidance input from the list.

10. Enter placeholder values for guidance inputs in the **Set more field inputs to show to users** section.

    Agents can substitute their own information for the placeholder values. These fields can contain static text, dynamic content such as field values from guidance inputs, or a combination of static text and dynamic content. To use dynamic content, select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) next to the field and select a guidance input from the list.

11. Select **Save and close**.


## What to do next

[Add a next node that is a question node after a guidance node.](configure-start-node-gdb.md)

