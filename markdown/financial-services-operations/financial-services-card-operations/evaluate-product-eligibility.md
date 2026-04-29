---
title: Evaluate the product eligibility for a customer
description: Evaluate the eligibility of the requested product for the customer.
locale: en-US
release: australia
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up a new credit card account, Use, Card Operations, Banking applications, Financial Services Operations \(FSO\)]
---

# Evaluate the product eligibility for a customer

Evaluate the eligibility of the requested product for the customer.

## Before you begin

Role required: sn\_bom\_credit\_card.agent or sn\_bom\_credit\_card.agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

A credit card task to evaluate the product eligibility is automatically created in the credit card service case for a new card request.

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Select the lists icon \(![lists icon](../../../use/reporting/image/inline-data-vis-96px-list.png)\).

3.  Open the task from a credit card service case or from the Credit Card Task list.

<table id="choicetable_lgv_1db_hmb"><thead><tr><th align="left" id="d75252e120">

Option

</th><th align="left" id="d75252e123">

Steps

</th></tr></thead><tbody><tr><td id="d75252e129">

**From a credit card service case**

</td><td>

1.  In the **Lists** tab, under **Credit Card Service Cases**, click **Assigned to me**.
2.  In the list, click the case that you want to open.
3.  In the case, click the **Tasks** tab and select the credit card task.


</td></tr><tr><td id="d75252e162">

**From the Credit Card Task list**

</td><td>

1.  In the **Lists** tab, under **Credit Card Task**, click **All**.
2.  In the list, click the task that you want to open.


</td></tr></tbody>
</table>4.  In the **State** field, change the state of the task to **Work in Progress**.

5.  Evaluate the eligibility of the requested product for the customer.

6.  In the **Work notes** field, enter any comments that are related to your findings.

7.  To close the task, in the **State** field, change the state of the task to **Closed Complete**.

8.  Click **Save**.


## Result

-   The stage of the associated credit card service case changes from Product Eligibility to Credit Risk Assessment.
-   A credit assessment task to retrieve a credit assessment and evaluate the risk for the customer is automatically generated in the **Tasks** tab of the associated case. The task is created in the Open state and assigned to an assignment group or a credit agent in the credit assessment department. The assignment group or user to whom the task is assigned is based on the assignment rule.

