---
title: Working with outbound invoice
description: Validate invoice data with an ERP number, process the integration, and move the invoice to payment extraction.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/working-with-outbound-invoice.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations,, invoice capture, invoice processing, invoice management, ERP integration, outbound integration]
breadcrumb: [Accounts Payable Operations integration framework, Integrate, Accounts Payable Operations, Finance and Supply Chain]
---

# Working with outbound invoice

Validate invoice data with an ERP number, process the integration, and move the invoice to payment extraction.

## Before you begin

Role required: sn\_spend\_intg\_admin or sn\_spend\_intg\_procurement\_integrator

## Procedure

1.  Open `sn_spend_intg_outbound_invoice_list.do` staging table.

    The **Invoice record** is verified with ERP number.

2.  Set the **Integration status** to **Processed**.

    The invoice **Status** is automatically set to **Pending payment**. The invoice is extracted for payment, and the invoice status is set to **Paid**.


