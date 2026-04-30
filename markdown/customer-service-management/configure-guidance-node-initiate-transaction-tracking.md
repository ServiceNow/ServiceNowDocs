---
title: Configure a guidance node to initiate the transaction tracking
description: Configure a guidance node in Decision Tree Builder so that agents can initiate the transaction tracking.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure a guidance node to initiate the transaction tracking

Configure a guidance node in Decision Tree Builder so that agents can initiate the transaction tracking.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

When the customer answers that money is debited after a failed transaction, agents can create a case to initiate the transaction tracking.

![Initiate transaction tracking guidance configuration that includes node name, guidance selected, and input mapping between this guidance and question nodes.](../image/ex-trxn-tracking-guidance.png)

## Procedure

1.  Select **Add node** on the Amount-is-debited path.

    ![the Add node button in the Decision Tree Builder to configure a question or guidance node.](../image/ex-amt-debited-guidance.png)

2.  In the pop-up window, select **Propose a guidance as an outcome** to configure a guidance node.

    A guidance is an outcome of a decision tree.

3.  In the **Node name** field, enter `Initiate transaction tracking`.

4.  In the **Guidance** field, select Initiate transaction tracking guidance.

5.  In the **Set field inputs to pass data into this guidance** section, link the task input from the previous question node.

    ![Linking the task input from the previous question node to this guidance node.](../image/gd-task-input-mapping.gif)

6.  In the **Set more field inputs to show to users** section, link guidance inputs to the inputs from the previous question node.

    1.  Select the Link input icon \(![Link input icon](../image/icon-link-input.png)\) next to the field.

    2.  Select the previous question node and the question from the list.

        The provided answer to the question is mapped to the guidance input during runtime.

7.  Select **Save and close**.


## What to do next

Do the following steps to add the next question node:

1.  Add a new path by selecting the Add path icon \(![Add path icon](../image/icon-add-path.png)\) on the Initiate transaction tracking guidance node.

    You can add a question node only after a guidance node. The execution of the decision tree continues after the guidance is performed. The path configuration isn’t required because there can only be one question node after a guidance node.

2.  [Configure a question node for further assistance](configure-a-question-node-for-further-assistance.md).

