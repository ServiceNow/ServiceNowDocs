---
title: Obligation Management
description: Obligation Management in Contract Management Pro enables you to track and fulfill the responsibilities specified in a contract.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Obligation Management

Obligation Management in Contract Management Pro enables you to track and fulfill the responsibilities specified in a contract.

With Obligation Management, a contract manager can create obligation records to define specific instructions and obligation task types required to fulfill the contract obligation. Obligation tasks are created to track and complete the activities specified in a contract, such as submitting an IT asset invoice every month.

An obligation record may have two types of obligation tasks:

-   **Ad hoc obligation task**

    The obligation task may be required only once or on irregular intervals to fulfill the contract obligations.

-   **Recurring obligation task**

    The obligation task is required at regular intervals to fulfill the contract obligations. Recurring obligation tasks are automatically created based on the defined schedule.


The Obligation Management workflow starts after the signed contract is added to the contract repository record and might progress as follows:

1.  A contract manager reviews the contract in the contract repository and creates obligation records for key obligations.
2.  The contract manager provides the obligation details, including an obligation task schedule, in the obligation record.

    For more information, see [Create obligation records](../task/cncore-create-obligations.md).

3.  Obligation tasks are created.
    -   For an ad hoc schedule, the contract manager creates an obligation task from the **Obligation tasks** tab.
    -   For a recurring schedule, the obligation tasks are automatically created based on the defined schedule.
4.  The assigned user is notified when the obligation task is created.
5.  The assigned user works on the obligation task and submits it for review.

    The state of the obligation task changes from Open to Awaiting approval.

6.  The obligation fulfiller reviews the task and approves or rejects it.
    -   If the obligation task is rejected, the state of the task changes to Open, and the assigned user continues to work on it.
    -   If the obligation task is approved, the state of the task changes to Completed.

-   **[Create obligation records](../task/cncore-create-obligations.md)**  
Create obligation records for signed contracts in Obligation Management to fulfill the responsibilities specified in the contract through obligation tasks. Recurring obligation tasks are automatically created from the record. You can also add ad hoc obligation tasks that are performed only once or at irregular intervals.
-   **[Submit obligation tasks](../task/cncore-work-on-ob-tasks.md)**  
As an obligation user, work on obligation tasks to fulfill the obligation specified in the contract, and submit them for review.
-   **[Cancel an obligation task](../task/cncore-cancel-ob-task.md)**  
Cancel an open obligation task in Obligation Management that is no longer required.
-   **[Approve or reject obligation tasks](../task/cncore-manage-ob-tasks.md)**  
As an obligation fulfiller, review obligation tasks in Obligation Management that have been submitted for approval, and take the appropriate action.

**Parent Topic:**[Using Contract Management Pro](cncore-use-cmpro.md)

