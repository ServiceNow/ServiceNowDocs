---
title: Work on an invoice inquiry case
description: Work on an invoice inquiry case to resolve an issue raised by the suppliers or employees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/work-inquiry-case.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, invoice management, supplier, invoice inquiry case, admin]
breadcrumb: [Invoice inquiry cases, Using Invoice Case Management, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Work on an invoice inquiry case

Work on an invoice inquiry case to resolve an issue raised by the suppliers or employees.

## Before you begin

Role required: sn\_ap\_cm.agent or sn\_ap\_cm.admin

## About this task

An invoice case with a category of Inquiry is referred to as an invoice inquiry case.

Typically, an invoice inquiry case is automatically created when you receive an inquiry email. However, the agent can also manually create an invoice inquiry case from the Source-to-Pay Workspace. For more information, see [Create an invoice inquiry case manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-inquiry-case.md).

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(\[Omitted image "cases-list-icon.png"\] Alt text: List icon\).

3.  Do one of the following:

    -   Navigate to **Lists** &gt; **My Work** &gt; **Open cases**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **Cases**.
4.  Open an invoice inquiry case to work on.

5.  Do one of the following:

    -   To assign the case to yourself, select **Assign to me**.
    -   If the case is assigned to you by the Accounts Payable Specialist, you can start working on the case by selecting **Accept**.
    The case moves to the **Work in progress** state.\[Omitted image "inquiry-case.png"\] Alt text: Inquiry case

6.  Do one of the following:

    -   Request more information about the invoice inquiry case from the requester. For more information, see [Request additional information from the requester for an invoice inquiry case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/request-caller-info-inquiry-case.md).

        The state of the case updates to Awaiting requester info.

    -   Submit the invoice inquiry case for an internal review. For more information, see [Submit an invoice inquiry case for an internal review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/submit-inquiry-case-internal-review.md).

        The state of the case updates to Awaiting internal info.

    -   Create an invoice task and assign it to a user or group to resolve the invoice inquiry case. For more information, see [Create an invoice task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-apm-task.md).
    -   AP specialist closes the inquiry case and if the system property **sn\_ap\_cm.awaiting\_acceptance\_enabled**is enabled, then the invoice inquiry state changes to awaiting acceptance, and the supplier receives an inquiry task in the Supplier Collaboration portal. If the supplier confirms the state of the invoice inquiry changes then the invoice is closed, otherwise the state of the invoice inquiry changes to **Work in Progress**.
    -   The state of an inquiry case changes from**Awaiting requester info** and**Awaiting internal info** to **Work in progress** in the following scenarios:
        -   An email reply from a requester triggers an action to move the inquiry case state to Work in progress.
        -   When all inquiry tasks are closed, the inquiry case state is automatically changed to Work in progress.
        -   An agent can manually change the inquiry state from Awaiting requester info to Work in progress.
7.  Close an invoice inquiry case when all the activities and tasks for resolving the case are completed.

    For more information, see [Close an invoice inquiry case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/close-inquiry-case.md).

    The inquiry case and related tasks are closed successfully.


**Parent Topic:**[Invoice inquiry cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-inquiry-cases.md)

**Related topics**  


[Using Supplier Collaboration Portal in APO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/using-supplier-collaboration-portal.md)

