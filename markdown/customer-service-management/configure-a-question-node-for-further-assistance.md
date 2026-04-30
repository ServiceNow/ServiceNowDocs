---
title: Configure a question node for further assistance
description: Add a question node to ask users whether they need further assistance.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Configure a question node for further assistance

Add a question node to ask users whether they need further assistance.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

![The Further assistance needed question node showing the choice as the answer type with yes and no as the choices.](../image/ex-further-assistance-question.png)

## Procedure

1.  Select **New node** on the path that comes from the Initiate transaction tracking guidance.

2.  In the **Node name** field, enter `Further assistance needed`.

3.  In the **Question or instruction** field, type `Do you need further assistance?`.

4.  Make this question a required question by selecting the **Required question** field.

5.  In the **Type of answer** field, select Choice.

6.  In the **Label** field, enter `Yes` for the first option in the list.

7.  Select **Add choice**.

8.  In the **Label** field, enter `No` for the second option in the list.

9.  Select **Save and close**.


## What to do next

Do the following steps to add the next guidance node:

1.  Configure a path with the condition "Do you need further assistance? \| is \| Yes". For more information and example, see [Determine the next node displayed in a decision tree](configure-path-in-gdb.md) and [Configuring paths with conditions whether the amount is debited or not](../concept/configuring-paths-for-next-nodes.md#).
2.  Add a guidance node and associate the More options guidance to the Yes path. For more information and example, see [Provide actions to agents in a decision tree](configure-guidance-in-gdb.md) and [Configure a guidance node to initiate the transaction tracking](configure-guidance-node-initiate-transaction-tracking.md).

