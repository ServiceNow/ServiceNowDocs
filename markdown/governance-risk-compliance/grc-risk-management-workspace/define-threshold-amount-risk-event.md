---
title: Define a threshold amount for the risk event response template
description: Define a threshold limit for assigning risk event approvers. A threshold limit is defined to determine if a risk event needs an approver.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a risk event response template, Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Define a threshold amount for the risk event response template

Define a threshold limit for assigning risk event approvers. A threshold limit is defined to determine if a risk event needs an approver.

## Before you begin

Role required: sn\_risk.manager and sn\_risk.admin

## About this task

Based on the risk loss amount, you can decide whether approvers are required for the risk events losses. For example, for any risk event that results in a loss of $1000 or less, an approver is not needed. But for any amount beyond $1000, the risk event must be evaluated and an approver is automatically assigned. There can be multiple levels of approvals depending on your defined thresholds. For a better understanding, see the following image. ![Risk event thresholds for approval](../image/threshold-risk-event.png)

In the previous example, the following rules are applied.

-   If the loss is between $0-$100, approval is not required.
-   If the loss is between $101 – $200, approval is required and approval goes to Caitlin.
-   If the loss is over $201 approval will be required from both Caitlin and the Risk manager.

## Procedure

1.  Navigate to **All** &gt; **Risk Events** &gt; **Administration** &gt; **Response Templates**.

2.  Select and open the risk event response template for which you want to add the financial threshold limit.

3.  In the Financial Impact Approval Thresholds related list, click **New**.

4.  From the **Threshold amount** list, select the currency type and enter the amount that needs an approval.

5.  Select the **Approver required** check box.

6.  From the **Assignment type** list, select either **User** or **Group**.

7.  In the **Approver** field, select the approver to approve the risk event if the threshold amount is exceeded.

8.  Click **Submit**.


## Result

The response template is updated with the threshold limit and approver details.

**Parent Topic:**[Create a risk event response template](create-risk-event-response-template.md)

