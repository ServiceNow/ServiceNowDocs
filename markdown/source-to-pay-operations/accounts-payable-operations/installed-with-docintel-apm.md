---
title: Components installed with Accounts Payable Operations integration with Document Intelligence
description: Several types of components are installed with activation of the Accounts Payable Operations integration with Document Intelligence \(com.sn\_ap\_ic\) application plugin, including user roles, flows, and tables.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Accounts Payable Operations integration with Document Intelligence, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Components installed with Accounts Payable Operations integration with Document Intelligence

Several types of components are installed with activation of the Accounts Payable Operations integration with Document Intelligence \(com.sn\_ap\_ic\) application plugin, including user roles, flows, and tables.

## Roles required

You must have the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role to review an invoice in Document Intelligence and enter values in the invoice fields.

For more information about the roles that are installed with Document Intelligence, see [Components installed with Document Intelligence](https://www.servicenow.com/docs/access?context=installed-with-document-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Flows installed

<table id="table_ydv_ykm_4wb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invoice processing case for Invoice email

</td><td>

Creates an invoice processing case after receiving an inbound email that contains at least one attachment, and then copies the email attachment to the invoice processing case.

 **Note:** This flow is installed when you install the Accounts Payable Operations integration with Document Intelligence application.

</td></tr><tr><td class="sub-head" colspan="2">

Flows installed only when you install the Document Intelligence application

</td></tr><tr><td>

Invoice attachment DI processing

</td><td>

Creates the DocIntel task for processing the invoice attachment and creates the invoice stage record for storing the extracted data from the invoice attachment.

</td></tr><tr><td>

DocIntel Extract Values Flow - Invoice Processing v1.2 - Invoice Processing v1.2 v1.2 - Invoice Processing v1.2

</td><td>

Populates the extracted data from the DocIntel task to the invoice stage and invoice line stage records and updates Invoice stage status to Processing completed.

</td></tr><tr><td>

Invoice Stage to Invoice Transformation

</td><td>

This flow does the following:-   Runs the transformation logic for the invoice stage and the invoice line stage records
-   Updates the invoice to **Received** state and associates the invoice with the invoice processing case if all the prerequisite conditions for the transformation are met
-   Updates the invoice processing case’s DocIntel Status to Processed \(STP completed\) if the DocIntel status is still in Processing

</td></tr><tr><td>

DI STP Failed

</td><td>

Processes the DocIntel task that does not fail or that does not undergo straight through processing. This flow updates its associated invoice stage to Processing error and updates the invoice processing case’s DocIntel status to Processed \(STP failed\) or Failed, respectively.

</td></tr></tbody>
</table>## Tables installed

<table id="table_s4y_nmv_ywb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invoice Stage

 \[sn\_ap\_ic\_invoice\_stage\]

</td><td>

Stores the invoice data extracted from the invoice.

</td></tr><tr><td>

Invoice Line Stage

 \[sn\_ap\_ic\_invoice\_line\_stage\]

</td><td>

Stores the invoice line data extracted from the invoice.

</td></tr></tbody>
</table>**Parent Topic:**[Install Accounts Payable Operations integration with Document Intelligence](../concept/apm-integration-docintel.md)

