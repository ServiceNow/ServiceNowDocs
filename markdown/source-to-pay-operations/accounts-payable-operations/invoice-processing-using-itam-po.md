---
title: Invoice processing using IT Asset Management purchase order
description: The ITAM-APO integration is designed to streamline invoice processing for ITAM-related purchase orders \(POs\), verifying better accuracy, exception handling, and operational efficiency.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IT Asset Management purchase order invoice processing, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice processing using IT Asset Management purchase order

The ITAM-APO integration is designed to streamline invoice processing for ITAM-related purchase orders \(POs\), verifying better accuracy, exception handling, and operational efficiency.

## Before you begin

Role required: Accounts\_payable\_specialist \[sn\_ap\_apm.accounts\_payable\_specialist\]

## Procedure

1.  Navigate to **Source-to-Workspace** &gt; **Accounts Payable Operations**.

2.  Create a purchase order in ITAM.

    For more information on creating purchase order in ITAM, see Create a purchase order.

3.  Create an invoice with the ITAM purchase order.

    For more information on invoices, [Create an invoice manually](create-invoice.md). The Accounts Payable Operations checks whether the received quantity in the ITAM receiving slip matches the invoiced quantity. In case of mismatch, an insufficient goods receipt exception is triggered and automatically the ITAM user is notified through email. For more information on exceptions, see [Invoice exceptions](../concept/work-with-invoice-exceptions.md).

4.  The Accounts Payable Operations automatically verifies and revalidates the invoice.


## Result

The invoice processing of ITAM purchase order is successfully performed.

