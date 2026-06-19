---
title: Invoice inquiry cases
description: Invoice inquiry cases help resolve invoice-related issues raised by suppliers or employees through structured case workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/work-with-inquiry-cases.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [APO, Accounts Payable Operations, invoice management, supplier, invoice inquiry case]
breadcrumb: [Using Invoice Case Management, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice inquiry cases

Invoice inquiry cases help resolve invoice-related issues raised by suppliers or employees through structured case workflows.

When you receive an email for an inquiry, the application automatically creates an invoice case with a category of **Inquiry** and one of the following sub-categories:

-   **Payment inquiry**
-   **Invoice inquiry**
-   **Expedite payment request**
-   **Payment terms issue**
-   **Invoice entry assistance**
-   **Other**

**Note:** An invoice case with a category of **Inquiry** is referred to as an invoice inquiry case.

However, an agent \[sn\_ap\_cm.agent\] can manually create invoice inquiry cases and work on them or create Accounts Payable tasks for those cases and assign them to a user or group. For more information, see [Create an invoice inquiry case manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-inquiry-case.md).

## Invoice inquiry case life cycle

The following figure illustrates the various states that the invoice inquiry case goes through during its life cycle, from its creation to closure.

\[Omitted image "inquiry-case-lifecycle-apm.png"\] Alt text: Invoice inquiry case life cycle

|State|Description|
|-----|-----------|
|New|The case is created.|
|Assigned|The case is assigned.|
|Work in progress|The case is being worked on.|
|Awaiting requester info|The agent needs more information from the requester to continue working on the case.|
|Awaiting internal info|The agent is waiting for the internal review on the case to complete.|
|Closed complete|The case is closed by entering the closure code.|
|Closed incomplete|The case is marked as incomplete by entering the closure code. Providing the closure details is required when you mark a case as **Close incomplete**.|
|Canceled|The case is a duplicate, created in error, or no longer required.|

-   **[Work on an invoice inquiry case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-inquiry-case.md)**  
Work on an invoice inquiry case to resolve an issue raised by the suppliers or employees.
-   **[Create an invoice inquiry case manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-inquiry-case.md)**  
Create invoice inquiry cases to address and respond to questions related to invoices and payment.
-   **[Create an invoice task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-apm-task.md)**  
Create an invoice task and assign it to a user or group to resolve an invoice inquiry case.
-   **[Request additional information from the requester for an invoice inquiry case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/request-caller-info-inquiry-case.md)**  
Request additional information from the requester to continue working on the case.
-   **[Submit an invoice inquiry case for an internal review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/submit-inquiry-case-internal-review.md)**  
Submit an invoice inquiry case for an internal review by creating a review task and assigning it to the reviewers.
-   **[Close an invoice inquiry case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/close-inquiry-case.md)**  
Mark an invoice inquiry case as resolved after completing all necessary activities and tasks.

**Parent Topic:**[Using Invoice Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-invoice-case-mgmt.md)

