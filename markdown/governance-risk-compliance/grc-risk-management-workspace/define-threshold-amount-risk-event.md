---
title: Define a threshold amount for the risk event response template
description: Define a threshold limit for assigning risk event approvers. A threshold limit is defined to determine if a risk event needs an approver.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Define a threshold amount for the risk event response template

Define a threshold limit for assigning risk event approvers. A threshold limit is defined to determine if a risk event needs an approver.

## Before you begin

Role required: sn\_risk.manager and sn\_risk.admin

## About this task

Based on the risk loss amount, you can decide whether approvers are required for the risk events losses. For example, for any risk event that results in a loss of $1000 or less, an approver isn’t needed. But for any amount beyond $1000, the risk event must be evaluated and an approver is automatically assigned. There can be multiple levels of approvals depending on your defined thresholds. For a better understanding, see the following image. ![Risk event thresholds for approval](../image/threshold-risk-event.png)

In the previous example, the following rules are applied.

-   If the loss is between $0-$100, approval isn’t required.
-   If the loss is between $101 – $200, approval is required and approval goes to Caitlin.
-   If the loss is over $201, approval is required from both Caitlin and the Risk manager.

## Procedure

1.  Navigate to **All** &gt; **Risk Events** &gt; **Administration** &gt; **Response Templates**.

2.  Select and open the risk event response template for which you want to add the financial threshold limit.

3.  In the **Financial Impact Approval Thresholds** related list, select **New**.

4.  On the form, fill in the fields.

    For a description of the field values on the Financial Impact Approval Thresholds form, see [Financial Impact Approval Thresholds](../reference/financial-impact-approval-thresholds-form.md).

5.  Select **Submit**.


## Result

The response template is updated with the threshold limit and approver details.

-   **[Financial Impact Approval Thresholds](../reference/financial-impact-approval-thresholds-form.md)**  
Use the Financial Impact Approval Thresholds form to define monetary thresholds that trigger approval requirements for risk events and to configure how approvers are determined when those thresholds are met.

**Parent Topic:**[Use Risk Events](../concept/use-risk-events.md)

