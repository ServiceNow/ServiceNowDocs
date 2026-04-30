---
title: Retrieve a credit assessment and evaluate the risks for a customer
description: Retrieve a credit assessment and evaluate the risks for a customer. You can approve or reject the credit card request based on your findings.
locale: en-US
release: yokohama
product: Financial Services Card Operations
classification: financial-services-card-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up a new credit card account, Managing credit card service requests, Card Operations, Using banking applications, Financial Services Operations \(FSO\)]
---

# Retrieve a credit assessment and evaluate the risks for a customer

Retrieve a credit assessment and evaluate the risks for a customer. You can approve or reject the credit card request based on your findings.

## Before you begin

Role required: sn\_bom\_credit\_asmt.b2c\_agent or sn\_bom\_credit\_asmt.b2c\_agent\_connector

**Important:** For the agent connector role to work, it must be combined with one of the CSM industry data model roles. For more information, see [Roles and Personas](../../fso-common/concept/fso-combine-csm-industry-roles.md).

## About this task

This credit assessment task is automatically created in one of the following conditions:

-   On completion of the [evaluate product eligibility task](evaluate-product-eligibility.md) for a new credit card case
-   With a credit card service case for [increasing credit limit request](../concept/work-increase-credit-limit-case.md)

## Procedure

1.  Navigate to **All** &gt; **Financial Services Operations** &gt; **Workspace**.

2.  Click the lists icon \(![lists icon.](../image/list-icon.png)\).

3.  In the **Lists** tab, under **Credit Assessment** and then open the task list.

    -   For your assigned tasks, click **Assigned to me**.
    -   For all credit assessment tasks, click **All**.
4.  In the list, select the task that you want to work on.

    To work on a task that is not assigned to you yet, assign it to yourself by clicking **Assign to me**.

5.  In the **State** field, change the state of the task to **Work in Progress**.

6.  In the **Risk score** field, select a risk score that is based on your findings.

7.  In the **Credit approved** field, select **Yes** to approve or **No** to reject the credit card request.

8.  In the **Approved credit limit** field, enter a credit limit that is based on your assessment for the customer.

9.  In the **Work notes** field, enter any comments.

10. Click **Close**.


## Result

-   The credit assessment task moves to the Closed – Complete state.
-   If you approved the credit request, the following occurs:
    -   **For a new credit card request**
        -   The stage of the associated credit card service case changes from Credit Risk Assessment to Customer Agreement.
        -   A document task to check the completeness of the customer's supporting documents is automatically generated in the **Tasks** tab of the associated case. The task is created in the Open state and assigned to an assignment group or a document agent in the document services department. The assignment group or user that the task is assigned to is based on the assignment rule.
    -   **For an increase credit limit request**
        -   The stage of the associated credit card service case changes from Credit Risk Assessment to Update Account.
        -   A credit card task that increases the credit limit is automatically generated in the **Tasks** tab of the associated case. The task is created in the Open state and assigned to an assignment group or a credit card agent in the credit card services department. The assignment group or user that the task is assigned to is based on the assignment rule.
-   If you rejected the credit request, the associated credit card service case is automatically closed and the stage of the case changes from Credit Risk Assessment to Closed – Rejected.

