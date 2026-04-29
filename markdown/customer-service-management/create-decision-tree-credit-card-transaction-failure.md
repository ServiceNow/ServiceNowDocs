---
title: Create a decision tree for troubleshooting a failed transaction
description: Help Anita create a decision tree that agents can use to troubleshoot a failed credit card transaction. After this step, the decision tree can be configured in Decision Tree Builder.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a decision tree for troubleshooting a failed transaction

Help Anita create a decision tree that agents can use to troubleshoot a failed credit card transaction. After this step, the decision tree can be configured in Decision Tree Builder.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Decision Trees**.

    ![Navigation to decision tree in the navigation side bar.](../image/nav-decision-tree.png)

2.  Select **New** on the Decision Trees list.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Type `Troubleshoot credit card transaction failure`.|
    |Action Label|Type `Troubleshoot`.|
    |Description|Type `Decision tree to help agents troubleshoot a credit card transaction failure`.|
    |Title|Type `Troubleshoot credit card transaction failure`.|
    |Question font size|Enter the desired font size for the questions in the guided decision tree. Example: `14`|
    |Show a dismiss button|Select this check box if you want the Dismiss button to appear on recommendation for the agent.|

    ![The new record form to fill in the decision tree details.](../image/create-decision-tree-example.png)

4.  Select **Submit**.

    The **Open in Builder** button is shown.


## What to do next

[Configure the start node](ask-card-holder-and-transaction-details.md) to ask for the user, card, and transaction details and determine if any amount was debited.

