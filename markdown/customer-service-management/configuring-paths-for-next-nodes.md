---
title: Configuring paths with conditions whether the amount is debited or not
description: Configure paths with conditions to determine the next question or guidance node that is displayed in a decision tree.Configure a path for the amount-debited condition for the next guidance node.Configure a path for the amount-not-debited condition for the next question node.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configuring paths with conditions whether the amount is debited or not

Configure paths with conditions to determine the next question or guidance node that is displayed in a decision tree.

-   If any amount is debited during a failed transaction, the path that leads to the Initiate transaction tracking guidance is taken.
-   If no amount is debited during a failed transaction, the path that leads to the next question node is taken.

## Configure the path for the amount-debited condition

Configure a path for the amount-debited condition for the next guidance node.

### Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

### About this task

When a customer answers that the amount is debited from the credit card, the path that leads to the Initiate transaction tracking guidance is taken.

![Path configuration that includes path name, path priority, and condition for the path.](../image/ex-amt-debited-path.png)

### Procedure

1.  In Decision Tree Builder, select the Add path icon \(![Add path icon](../image/icon-add-path.png)\) on the start node.

    A new path and a new node are added to the canvas.

    ![New path and Add node for configuring the new path and node after a question node.](../image/ex-add-path.png)

2.  Select the new path.

3.  In the **Path name** field, enter `Amount is debited`.

4.  In the **Path priority** field, enter `100`.

5.  Select the appropriate fields to set the condition "Has any amount been debited? \| is \| true".

6.  Select **Save and close**.


### What to do next

[Configure a guidance node](../task/configure-guidance-node-initiate-transaction-tracking.md) that allows agents to initiate the transaction tracking for a failed transaction.

## Configure the path for the amount-not-debited condition

Configure a path for the amount-not-debited condition for the next question node.

### Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

### About this task

When a customer answers that the amount isn’t debited from the credit card, the path that leads to the next question node is taken. The question node asks for failure codes that the user received.

![Path configuration that includes path name, path priority, and condition for the path.](../image/ex-amt-not-debited-path.png)

### Procedure

1.  In Decision Tree Builder, select the Add path icon \(![Add path icon](../image/icon-add-path.png)\) on the start node.

    A new path and a new node are added to the canvas.

    ![New path and Add node for configuring the new path and node after a question node.](../image/ex-add-path.png)

2.  Select the new path.

3.  In the **Path name** field, enter `Amount is not debited`.

4.  In the **Path priority** field, enter `200`.

5.  Select the appropriate fields to set the condition "Has any amount been debited? \| is \| false".

6.  Select **Save and close**.


### What to do next

[Configure a question node](../task/configure-question-node-to-ask-failure-codes.md) to ask for the failure codes that customer received after the failed transaction.

