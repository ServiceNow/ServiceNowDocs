---
title: Components installed with Accounts Payable Invoice Processing
description: Several types of components are installed with activation of the Accounts Payable Invoice Processing plugin, including user roles, flows, and tables.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Install Accounts Payable Invoice Processing, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Components installed with Accounts Payable Invoice Processing

Several types of components are installed with activation of the Accounts Payable Invoice Processing plugin, including user roles, flows, and tables.

## Roles installed

**Note:** The following roles are installed with Finance Common Architecture \(com.sn\_fin\), which is installed as a dependent plugin:

-   sn\_fin.supplier\_payment\_info\_read: Provides read access to supplier details and supplier payment information tables
-   sn\_fin.supplier\_payment\_info\_write: Provides write access to supplier details and supplier payment information tables. Tax manager creates tax codes, tax types to be applied on the invoice.
-   sn\_fin.tax\_manager: Provides read, write, update and delete access to tax code and tax type tables.

The sn\_shop.invoice\_owner role is installed with Source-to-Pay Common Architecture \(com.snc.sn\_shop\), which is installed as a dependent plugin.

For information about the components installed with Invoice Case Management, see [Components installed with Invoice Case Management](installed-with-invoice-case-mgmt.md).

<table id="table_o4b_sbc_gvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Accounts Payable Invoice Processing administrator \[sn\_ap\_apm.admin\]

</td><td>

Can access all the features and capabilities of the Accounts Payable Operations application.

</td><td>

-   sn\_ap\_cm.admin
-   sla\_admin
-   sn\_\_ap\_apm.accounts\_payable\_specialist

</td></tr><tr><td>

Accounts Payable Specialist \[sn\_ap\_apm.accounts\_payable\_specialist\]

</td><td>

-   Can view and update all invoices and invoice exceptions.
-   Can view purchase orders, supplier details, and supplier payments.

</td><td>

-   sn\_fin.supplier\_payment\_info\_read
-   sla\_manager
-   workspace\_user
-   canvas\_user
-   sn\_ap\_apm.reader
-   sn\_ap\_cm.task.owner
-   email\_composer

</td></tr><tr><td>

Accounts Payable Invoice Processing Reader \[sn\_ap\_apm.reader\]

</td><td>

Can view all the tables available in the Accounts Payable Operations application.

</td><td>

-   vendor\_reader
-   sn\_shop.procurement\_common\_reader

</td></tr><tr><td>

Invoice tolerance admin\[sn\_ap\_apm.invoice\_tolerance\_admin\]

</td><td>

Can create and manage tolerance rules and tolerance types.

</td><td>

 

</td></tr><tr><td>

Tax specialist\[sn\_ap\_apm.tax\_specialist\]

</td><td>

Can perform actions on invoice tax lines and resolve tax variance exceptions.

</td><td>

-   email composer
-   sn\_ap\_cm.task\_owner
-   sla\_manager

</td></tr><tr><td>

Accounts Payable Specialist\[sn\_ap\_apm.accounts\_payable\_specialist\]

</td><td>

Can allocate invoice line costs by cost center or ledger account.

</td><td>

 

</td></tr></tbody>
</table>## Flows installed

<table id="table_vgb_25n_fwb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Invoice Processing Case for Invoice

</td><td>

Creates an invoice processing case for an invoice that is received via email.**Note:** If you receive an email with N attachments, the application creates N invoice processing cases — A new invoice processing case for each attached invoice, where N is a positive number. If you receive an email with no attachment, then the application doesn’t create an invoice processing case.

</td></tr><tr><td>

Start Invoice Processing for Orphan Invoices

</td><td>

Picks up all the invoice records in Draft state that don’t have an invoice case associated with them and starts their processing.You must activate the flow to use it. For information on how to activate the flow, see [Activate the Start Invoice Processing for Orphan Invoices flow](../task/activate-start-invoice-processing-flow.md).

</td></tr></tbody>
</table>|Job|Description|
|---|-----------|
|Exception Monitoring scheduler|Runs on a regular schedule every five minutes to identify exceptions for the invoices of type PO, Non-PO, credit memo that are in **PO matching completed/Accepted** or **Exceptions found** state. You must activate the schedule job to run.|

## Tables installed

<table id="table_s4b_sbc_gvb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invoice exception \[sn\_ap\_apm\_exception\]

</td><td>

Stores the exceptions found in the invoices.

</td></tr><tr><td>

Invoice exception line\[sn\_ap\_apm\_line\_exception\]

</td><td>

Stores the line exceptions found in the invoices.

</td></tr><tr><td>

Invoice exception definition \[sn\_ap\_apm\_exception\_definition\]

</td><td>

Extends the Application File table. Store the exception definitions for an exception.

</td></tr><tr><td>

Invoice processing detailsn\_ap\_apm\_invoice\_attribute

</td><td>

Stores invoice processing information

</td></tr><tr><td>

Invoice tolerance rule\[sn\_ap\_apm\_invoice\_tolerance\_rule\]

</td><td>

Stores the tolerance rules for each tolerance type. The table extends the application file table.

</td></tr><tr><td>

Invoice tolerance type\[sn\_apm\_apm\_invoice\_tolerance\_type\]

</td><td>

Stores the different types of tolerances. The table extends the application file table.

</td></tr></tbody>
</table>