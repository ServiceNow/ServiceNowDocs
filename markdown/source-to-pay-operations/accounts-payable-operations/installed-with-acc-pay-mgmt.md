---
title: Components installed with Accounts Payable Invoice Processing
description: Several types of components are installed with activation of the Accounts Payable Invoice Processing plugin, including user roles, flows, and tables.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Components installed with Accounts Payable Invoice Processing

Several types of components are installed with activation of the Accounts Payable Invoice Processing plugin, including user roles, flows, and tables.

## Roles installed

**Note:** The following roles are installed with Finance Common Architecture \(com.sn\_fin\), which is installed as a dependent plugin:

-   sn\_fin.supplier\_payment\_info\_read: Provides read access to supplier details and supplier payment information tables
-   sn\_fin.supplier\_payment\_info\_write: Provides write access to supplier details and supplier payment information tables

The sn\_shop.invoice\_owner role is installed with Source-to-Pay Common Architecture \(com.snc.sn\_shop\), which is installed as a dependent plugin.

For information about the components installed with Invoice Case Management, see [Components installed with Invoice Case Management](installed-with-invoice-case-mgmt.md).

<table id="table_o4b_sbc_gvb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Accounts Payable Invoice Processing Administrator \[sn\_ap\_apm.admin\]

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

</td></tr></tbody>
</table>## Flows installed

<table id="table_vgb_25n_fwb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Invoice Processing Case for Invoice

</td><td>

Creates an invoice processing case for an invoice that is received via email.**Note:** If you receive an email with N attachments, the application creates N invoice processing cases — a new invoice processing case for each attached invoice, where N is a positive number. If you receive an email with no attachment, then the application does not create an invoice processing case.

</td></tr><tr><td>

Start Invoice Processing for Orphan Invoices

</td><td>

Picks up all the invoice records in Draft state that do not have an invoice case associated to them and starts their processing.You must activate the flow to use it. For information on how to activate the flow, see [Activate the Start Invoice Processing for Orphan Invoices flow](../task/activate-start-invoice-processing-flow.md).

</td></tr></tbody>
</table>|Job|Description|
|---|-----------|
|Exception Monitoring scheduler|Runs on a regular schedule every five minutes to identify exceptions for the PO and Non-PO invoices that are in **PO matching completed/Accepted** or **Exceptions found** state.|

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

Extends the Application File table. Stores the exception definitions for an exception.

</td></tr><tr><td>

Invoice processing detailsn\_ap\_apm\_invoice\_attribute

</td><td>

Stores invoice processing information

</td></tr></tbody>
</table>