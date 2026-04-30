---
title: Working with outbound invoice
description: ERP integrator validates the invoice with ERP number, processes the integration, and the moves the invoice for payment extraction.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Accounts Payable Operations integration framework, Integrating APO with other applications, Accounts Payable Operations, Finance and Supply Chain]
---

# Working with outbound invoice

ERP integrator validates the invoice with ERP number, processes the integration, and the moves the invoice for payment extraction.

## Before you begin

Role required: sn\_spend\_intg\_admin or sn\_spend\_intg\_procurement\_integrator

## Procedure

1.  Open `sn_spend_intg_outbound_invoice_list.do` staging table.

    The **Invoice record** is verified with ERP number.

2.  Set the **Integration status** to **Processed**.

    The invoice **Status** is automatically set to **Pending payment**. The invoice is extracted for payment, and the invoice status is set to **Paid**.


