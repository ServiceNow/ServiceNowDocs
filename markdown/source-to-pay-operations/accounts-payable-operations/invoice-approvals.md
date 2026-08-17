---
title: Invoice approvals
description: Invoice approvals in Accounts Payable Operations route exception-free invoices to approvers using configured rules and track states.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-approvals.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice exception, invoice approval, invoice automation]
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice approvals

Invoice approvals in Accounts Payable Operations route exception-free invoices to approvers using configured rules and track states.

The approval engine picks all invoices with the **No exception found** status. Based on the configured approval rules, it creates approval requests and assigns them to approvers. The invoice status changes to **Pending approval**. After the approver approves the request, the invoice status changes to **Approved**.

-   **[Create an approval rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-approval-rule.md)**  
Create approval rules to ensure that the approval requests are reasonable and fit your organization's budget.
-   **[Monitor an approval plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/view-approval-plan.md)**  
Monitor approval plans to understand how the overall approval process is progressing.
-   **[Approve an invoice approval task from Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/approve-invoice-request-ec.md)**  
Approve or reject invoice approval tasks assigned to you in Employee Center.

**Parent Topic:**[Using Accounts Payable Invoice Processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using the AP Invoice API]()

[Rules based engine]()

[Invoice processing]()

[Invoice processing cases]()

[Invoice exceptions]()

[Tolerance rules and variances for invoices]()

[View invoice documents in the Source-to-Pay Workspace]()

