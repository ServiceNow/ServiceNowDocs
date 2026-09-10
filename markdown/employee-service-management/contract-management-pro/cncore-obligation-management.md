---
title: Obligation Management
description: Obligation Management in Contract Management Pro enables you to track and fulfill contractual responsibilities by creating obligation records and managing associated tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-obligation-management.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Obligation Management]
audience: [sn\_cm\_obligation.obligation\_fulfiller, sn\_cm\_obligation.obligation\_user]
breadcrumb: [Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Obligation Management

Obligation Management in Contract Management Pro enables you to track and fulfill contractual responsibilities by creating obligation records and managing associated tasks.

With Obligation Management, a contract manager can create obligation records to define specific instructions and obligation task types required to fulfill the contract obligation. Obligation tasks are created to track and complete the activities specified in a contract, such as submitting an IT asset invoice every month.

An obligation record can have two types of obligation tasks:

-   **Ad hoc obligation task**

    Obligation task required only once or at irregular intervals to fulfill the contract obligations.

-   **Recurring obligation task**

    Obligation task required at regular intervals to fulfill the contract obligations. Recurring obligation tasks are automatically created based on the defined schedule.


You can create obligations using one of the following methods:

-   **Create obligations using AI**

    The AI agent uses contract obligation extraction skill to extract key contractual obligations from contracts. Once extracted, you can review the obligations within the contract playbook and choose to accept or reject them. Accepted obligations are added as records in the **Obligations** tab of the contract record.

-   **Create obligations manually**

    Contract manager manually reviews the contract and creates obligation records for key obligations.


## AI-powered obligation extraction workflow

The AI-powered obligation extraction process uses the manage contract repository agentic workflow and can progress as follows:

1.  As a contract admin with the AI role, activate the contract obligation extraction skill in the AI Admin Hub console.

    For more information, see [Configure AI capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/confg-na-in-cmpro.md).

2.  As a contract admin, activate the business rules.
3.  The obligation extraction process is automatically initiated when a contract record is created.
4.  Once the extraction is complete, the contract manager with the AI role receives a notification indicating that obligations are ready for review.
5.  The contract manager reviews the extracted obligations within the contract playbook. Each obligation can be accepted or rejected based on relevance.
6.  Approved obligations are automatically added as obligation records in the **Obligations** tab of the contract record.
7.  Obligation tasks are created.
    -   For a recurring schedule, the obligation tasks are automatically created for the obligation record based on the defined schedule.
    -   For an ad hoc schedule, the contract manager creates an obligation task from the **Obligation tasks** tab in the contract record.
8.  The assigned user is notified when the obligation task is created.
9.  The assigned user works on the obligation task and submits it for review.

    The state of the obligation task changes from Open to Awaiting approval.

10. The obligation fulfiller reviews the task and approves or rejects it.
    -   If the obligation task is rejected, the state of the task changes to Open, and the assigned user continues to work on it.
    -   If the obligation task is approved, the state of the task changes to Completed.

## Manual obligation management workflow

The manual Obligation Management workflow starts after the signed contract is added to the contract repository record and can progress as follows:

1.  A contract manager reviews the contract in the contract repository and creates obligation records for key obligations.
2.  The contract manager provides the obligation details, including an obligation task schedule, in the obligation record.

    For more information, see [Create obligation records manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-create-obligations-landing.md).

3.  Obligation tasks are created.
    -   For an ad hoc schedule, the contract manager creates an obligation task from the **Obligation tasks** tab.
    -   For a recurring schedule, the obligation tasks are automatically created based on the defined schedule.
4.  The assigned user is notified when the obligation task is created.
5.  The assigned user works on the obligation task and submits it for review.

    The state of the obligation task changes from Open to Awaiting approval.

6.  The obligation fulfiller reviews the task and approves or rejects it.
    -   If the obligation task is rejected, the state of the task changes to Open, and the assigned user continues to work on it.
    -   If the obligation task is approved, the state of the task changes to Completed.

-   **[Create obligations using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-create-obligations-landing.md)**  
Create obligation records for signed contracts to fulfill the responsibilities specified in the contract. You can create obligations manually or use AI to automatically extract obligations from contract documents.
-   **[Create obligations manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-work-on-ob-tasks.md)**  
As an obligation user, work on obligation tasks to fulfill the obligation specified in the contract, and submit them for review.
-   **[Cancel an obligation task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-cancel-ob-task.md)**  
Cancel an open obligation task in Obligation Management that is no longer required.
-   **[Approve or reject obligation tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-manage-ob-tasks.md)**  
As an obligation fulfiller, review obligation tasks in Obligation Management that have been submitted for approval, and take the appropriate action.

**Parent Topic:**[Using Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-use-cmpro.md)

