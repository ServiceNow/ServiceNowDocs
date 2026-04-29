---
title: Increase the credit limit for a customer
description: Increase the credit limit for a customer to the approved credit limit that was set by the credit assessment agent.
locale: en-US
release: australia
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Increasing the credit limit, Use, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Increase the credit limit for a customer

Increase the credit limit for a customer to the approved credit limit that was set by the credit assessment agent.

## Before you begin

[Retrieve a credit assessment and evaluate the risks for a customer](retrieve-credit-assessment-evaluate-risk.md).

Role required: sn\_bom\_credit\_card.agent or sn\_bom\_credit\_card.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

This credit card task is automatically created when the credit assessment task has approved the request via the retrieve credit assessment and evaluate risk task.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Open the task from a credit card service case or from the Credit Card Task list.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d122979e126">

Option

</th><th align="left" id="d122979e129">

Steps

</th></tr></thead><tbody><tr><td id="d122979e135">

**From a credit card service case**

</td><td>

1.  In the **Lists** tab, under **Credit Card Service Cases**, click **Assigned to me**.
2.  In the list, click the case that you want to open.
3.  In the case, click the **Tasks** tab and select the credit card task.


</td></tr><tr><td id="d122979e168">

**From the Credit Card Task list**

</td><td>

1.  In the **Lists** tab, under **Credit Card Task**, click **All**.
2.  In the list, click the task that you want to open.


</td></tr></tbody>
</table>4.  In the **State** field, change the state of the task to **Work in Progress**.

5.  Based on the value in the **Approved credit limit** field, increase the credit limit for the customer's credit card.

6.  In the **Work notes** field, enter any comments.

7.  To close the task, in the **State** field, change the state of the task to **Closed Complete**.

8.  Click **Save**.


## Result

-   The stage of the associated credit card service case changes from Update Account to Closed – Complete.

    **Important:** If the request is for a temporary increase in the credit limit, the state of the case remains in the Work in Progress state and in the Update Account stage until the end date that is specified in the case. The system automatically creates a new credit card service case on the specified end date to reset the credit limit.

-   The customer receives a pre-configured email notification about the case closure.

## What to do next

If the associated case is for a temporary increase in the credit limit, work on the new case to [revert the credit limit](reset-credit-limit.md) to the original limit on the end date.

