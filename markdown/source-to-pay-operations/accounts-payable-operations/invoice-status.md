---
title: Invoice status messages
description: Invoice-related status messages are displayed in the Accounts Payable Operations application.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create New Invoice case form, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice status messages

Invoice-related status messages are displayed in the Accounts Payable Operations application.

<table id="table_ztk_xj1_dwb"><thead><tr><th>

Invoice status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

No invoice

</td><td>

When an invoice encounters data extraction issue, this status is updated. You must review the invoice details and line items using DocIntel to ingest the required data and submit.

</td></tr><tr><td>

Draft

</td><td>

This status is updated in 2 scenarios:-   When an invoice can extract most of the data from DocIntel, the invoice is being updated with the missing required information and is yet to be submitted.
-   When an invoice is created manually until it’s ready for submission.

</td></tr><tr><td>

Received

</td><td>

The invoice created with options such as manual, digitized or through API is moved to Received state.

</td></tr><tr><td>

Suspected duplicate

</td><td>

After the invoice is updated with required details, Accounts Payable Specialist checks if the same invoice \(supplier invoice number\) is previously submitted by the same supplier. If the invoice is submitted by the supplier, then the invoice is updated with **Suspected duplicate** State.

</td></tr><tr><td>

Accepted

</td><td>

This status is updated in one of the following scenarios: -   As part of invoice processing, the invoice moves from **Received** to **Accepted** State if no duplicate invoices are identified by the system
-   Accounts Payable Specialist confirms the invoice is not duplicate.
-   System recognizes the invoice as duplicate and Accounts Payable Specialist confirms it as non-duplicate.

</td></tr><tr><td>

PO matching error

</td><td>

This status is updated in one of the following scenarios:-   An invoice is updated with PO matching error when PO is missing on the invoice.
-   PO line mapping is missing from invoice lines.
-   The currency on the PO is different from the invoice currency.

</td></tr><tr><td>

PO matching completed

</td><td>

When all the invoice lines are mapped to PO lines and if no discrepancies are found between PO and invoice currency, then the invoice is updated to PO matching completed.

</td></tr><tr><td>

Exceptions found

</td><td>

An invoice is updated with the status Exceptions found, when it finds any one or more of the exceptions that were defined in Accounts Payable Operations. For more information on exceptions, see [Invoice exceptions](../concept/work-with-invoice-exceptions.md).

</td></tr><tr><td>

No exceptions found

</td><td>

This status is updated in one of the following scenarios:-   When there are no exceptions with an invoice or invoice lines.
-   When all the identified exceptions are fixed, then the invoice is moved to No exceptions found state.

</td></tr><tr><td>

Pending approval

</td><td>

After all the invoice exceptions are resolved \(no exceptions found\), then the invoice is submitted for approval and the invoice changes to **Pending approval** State.

</td></tr><tr><td>

Rejected

</td><td>

When an invoice is rejected through email, custom APIs, the invoice status is updated as rejected.

</td></tr><tr><td>

Approved

</td><td>

After the invoice us submitted for approval \(pending approval\), if the user approves the invoice, then the invoice is moved to **Approved** state.

</td></tr><tr><td>

Pending payment

</td><td>

After the invoice is approved, then the invoice is integrated with ERP system. If no integration errors are found, then the invoice status changes to **Pending payment**.

</td></tr><tr><td>

Confirmed duplicate

</td><td>

When the system identifies the invoice as suspected duplicate, and then Accounts Payable Specialist confirms the invoice as duplicate, the status changes to **Confirm duplicate**.

</td></tr><tr><td>

Canceled

</td><td>

When Accounts Payable Specialist cancels the invoice, then State is auto set to **Cancelled**.

</td></tr><tr><td>

Paid

</td><td>

After the invoice is posted to ERP and paid in the ERP, the payment is posted back to Accounts Payable Operations without integration error. Then, the invoice moves to **Paid** State.

</td></tr></tbody>
</table>**Parent Topic:**[Create New Invoice case form](create-new-ap-case-form.md)

