---
title: Set up a credit card account for a customer and close the case
description: Set up a new credit card account for a customer after customer verification is done and the required documents are prepared.
locale: en-US
release: xanadu
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up a new credit card account, Managing credit card service requests, Financial Services Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Set up a credit card account for a customer and close the case

Set up a new credit card account for a customer after customer verification is done and the required documents are prepared.

## Before you begin

Role required: sn\_bom\_credit\_card.agent or sn\_bom\_credit\_card.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

This credit card task is automatically created for a new credit card case when the document service task to [file the customer agreement](file-customer-agreement.md) completes.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  Open the task from a credit card service case or from the Credit Card Task list.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d25658e112">

Option

</th><th align="left" id="d25658e115">

Steps

</th></tr></thead><tbody><tr><td id="d25658e121">

**From a credit card service case**

</td><td>

1.  In the **Lists** tab, under **Credit Card Service Cases**, click **Assigned to me**.
2.  In the list, click the case that you want to open.
3.  In the case, click the **Tasks** tab and select the credit card task.


</td></tr><tr><td id="d25658e154">

**From the Credit Card Task list**

</td><td>

1.  In the **Lists** tab, under **Credit Card Task**, click **All**.
2.  In the list, click the task that you want to open.


</td></tr></tbody>
</table>4.  In the **State** field, change the state of the task to **Work in Progress**.

5.  Based on the values in the **Risk score** and **Approved credit limit** fields, create a new credit card account for the customer as per the request.

6.  In the **Work notes** field, enter any comments.

7.  To close the task, in the **State** field, change the state of the task to **Closed Complete**.

8.  Click **Save**.


## Result

-   The stage of the associated credit card service case changes from Account Creation to Closed – Complete.
-   The customer receives a pre-configured email notification about the case closure.

