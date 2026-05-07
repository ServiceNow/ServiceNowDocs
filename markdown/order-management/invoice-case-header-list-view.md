---
title: Invoice case details on the Business Portal
description: Field descriptions for invoice case headers and invoice case line list views on the Business Portal.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-10"
reading_time_minutes: 2
breadcrumb: [Business Portal reference, Reference, Sales Customer Relationship Management]
---

# Invoice case details on the Business Portal

Field descriptions for invoice case headers and invoice case line list views on the Business Portal.

## Invoice case header fields

<table id="table_rlf_wkd_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

Customer account associated with the invoice dispute case.

</td></tr><tr><td>

Contact

</td><td>

Name of the customer contact for the invoice case.

</td></tr><tr><td>

Invoice

</td><td>

Unique, system-generated invoice number being disputed, starting with the prefix ARINV.

</td></tr><tr><td>

Invoice date

</td><td>

Date the invoice was issued.

</td></tr><tr><td>

Priority

</td><td>

Urgency level assigned to the invoice case. The available options are:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low \(default\)

</td></tr><tr><td>

Request source

</td><td>

Scope selected when creating the invoice case from the Business Portal using the playbook experience. The available options are:-   Specific invoice line and single invoice
-   Invoice header details and multiple invoices

</td></tr></tbody>
</table>## Invoice case line list view

<table id="table_o4f_nnd_g3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique, system-generated invoice case line starting with the prefix INVCSL.

</td></tr><tr><td>

Invoice

</td><td>

The invoice number associated with this case line. This field is displayed for an invoice case created with **Invoice header details, multiple invoices** as the request source.

</td></tr><tr><td>

Invoice line

</td><td>

The invoice line number associated with one of the invoices in this case line. This field is displayed for an invoice case created with **Specific invoice lines, single invoice** as the request source.

</td></tr><tr><td>

Description or Short description

</td><td>

A brief summary of the invoice case line item.

</td></tr><tr><td>

State

</td><td>

The current status of the invoice case line. The available options are:-   Draft
-   New
-   Work in Progress
-   Awaiting Info
-   Resolved - Accepted
-   Resolved - Denied
-   Canceled

</td></tr><tr><td>

Invoiced quantity

</td><td>

The quantity that was originally billed on the invoice. This field is displayed for an invoice case created with **Specific invoice lines, single invoice** as the request source.

</td></tr><tr><td>

Disputed quantity

</td><td>

The quantity being disputed by the customer. This field is displayed for an invoice case created with **Specific invoice lines, single invoice** as the request source.

</td></tr><tr><td>

Approved quantity

</td><td>

The quantity approved for adjustment or credit after dispute resolution. This field is displayed for an invoice case created with **Specific invoice lines, single invoice** as the request source.

</td></tr><tr><td>

Invoiced billing location

</td><td>

The billing address that appears on the original invoice.

</td></tr><tr><td>

Invoiced shipping location

</td><td>

The shipping address that appears on the original invoice.

</td></tr><tr><td>

Disputed billing location

</td><td>

The billing address that the customer claims should have been used.

</td></tr><tr><td>

Disputed shipping location

</td><td>

The shipping address that the customer claims should have been used.

</td></tr><tr><td>

Expected start

</td><td>

The planned or expected start date for service or product delivery.

</td></tr><tr><td>

Actual start

</td><td>

The actual date when service or product delivery began.

</td></tr><tr><td>

Product offering

</td><td>

The product or service offering associated with this invoice line. This field is displayed for an invoice case created with **Specific invoice lines, single invoice** as the request source.

</td></tr><tr><td>

Sold product

</td><td>

The specific product that was fulfilled and invoiced. This field is displayed for an invoice case created with **Specific invoice lines, single invoice** as the request source.

</td></tr><tr><td>

Contact

</td><td>

Customer contact for the invoice case.

</td></tr></tbody>
</table>**Parent Topic:**[Business Portal reference for Sales Customer Relationship Management](som-business-portal-reference.md)

