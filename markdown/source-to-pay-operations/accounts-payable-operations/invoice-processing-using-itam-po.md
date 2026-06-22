---
title: Invoice processing using IT Asset Management purchase order
description: Process invoices for IT Asset Management purchase orders using the ITAM-APO integration to validate received quantities against invoiced quantities and handle exceptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/invoice-processing-using-itam-po.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice exception, invoice processing, purchase order, ITAM, asset management, AP specialist]
breadcrumb: [IT Asset Management purchase order invoice processing, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice processing using IT Asset Management purchase order

Process invoices for IT Asset Management purchase orders using the ITAM-APO integration to validate received quantities against invoiced quantities and handle exceptions.

## Before you begin

Role required: Accounts\_payable\_specialist \[sn\_ap\_apm.accounts\_payable\_specialist\]

## Procedure

1.  Navigate to **Source-to-Workspace** &gt; **Accounts Payable Operations**.

2.  Create a purchase order in ITAM.

    For more information on creating purchase order in ITAM, see [Create a purchase order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/procurement/t_CreateAPurchaseOrder.md).

3.  Create an invoice with the ITAM purchase order.

    For more information on invoices, [Create an invoice manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-invoice.md). The Accounts Payable Operations checks whether the received quantity in the ITAM receiving slip matches the invoiced quantity. In case of mismatch, an insufficient goods receipt exception is triggered and automatically the ITAM user is notified through email. For more information on exceptions, see [Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-invoice-exceptions.md).

4.  The Accounts Payable Operations automatically verifies and revalidates the invoice.


## Result

The invoice processing of ITAM purchase order is successfully performed.

