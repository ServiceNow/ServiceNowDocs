---
title: Invoice case resolution using AI worker
description: Mark an invoice inquiry case and payment inquiry as resolved to start an automated workflow that requests supplier confirmation through Supplier Collaboration Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-case-resolution-using-ai-worker.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 1
keywords: [APO, Supplier Collaboration Portal, Case resolution, invoice case, AP specialist, AP supplier services]
breadcrumb: [AI worker case resolution confirmation, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice case resolution using AI worker

Mark an invoice inquiry case and payment inquiry as resolved to start an automated workflow that requests supplier confirmation through Supplier Collaboration Portal.

## Before you begin

-   Case resolution is recorded in the activity stream.
-   The supplier contact email address must be registered in the system.

Role required: admin

## About this task

Mark a supplier invoice case as resolved after completing your investigation and accepting the resolution.

## Procedure

1.  Navigate to **Supplier Collaboration Portal** &gt; **My Tasks** &gt; **Open**.

    A notification appears with a request to Accept resolution. Review the resolution details.

2.  Select the appropriate action button:

    -   Select **Yes** if the resolution resolves your issue. The invoice case is auto-closed.
    -   Select **No** if you need more help or the resolution does not address your concern. The system changes the Assignment group to AP supplier services, and an AP specialist investigates the case.\[Omitted image "ai-worker-invc.png"\] Alt text: AI worker resolution in Supplier Collaboration Portal
    **Note:** When a resolution is provided and the case is in **Awaiting acceptance** state, if there is no activity on the case from supplier for 72 hours, a scheduled job closes the case automatically.


**Parent Topic:**[AI worker case resolution confirmation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/ai-worker-case-resolution-confirmation.md)

