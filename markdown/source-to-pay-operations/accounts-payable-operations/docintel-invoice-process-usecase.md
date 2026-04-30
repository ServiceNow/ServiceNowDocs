---
title: Invoice Processing use case
description: Accounts Payable Operations integration with Document Intelligence provides the DO NOT USE - Invoice Processing use case.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Install Accounts Payable Operations integration with Document Intelligence, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice Processing use case

Accounts Payable Operations integration with Document Intelligence provides the **DO NOT USE - Invoice Processing** use case.

The **DO NOT USE - Invoice Processing** use case identifies the information to extract invoice documents received as email attachments and determines how a user with the Accounts Payable Specialist role interacts with the extracted values in the Document Intelligence workspace.

**Note:** The **DO NOT USE - Invoice Processing** use case is read-only and cannot be edited.

The **DO NOT USE - Invoice Processing** use case contains the list of invoice fields to extract data from invoice attachments and stores this data in the invoice stage record. It also contains an extraction flow that populates the extracted invoice data into the invoice stage and invoice line stage records and updates the Invoice stage status to Processing completed.

You can access this use case by navigating to **All** &gt; **Document Intelligence** &gt; **Use Cases** &gt; **DO NOT USE - Invoice processing**.

The **DO NOT USE - Invoice Processing** use case includes the following information.

<table id="table_sgb_3d2_zwb"><thead><tr><th>

Use case information

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fields

</td><td>

Contains the list of invoice and invoice line fields to extract information from an invoice document. A field is a single piece of information to extract from an invoice document. In the use case, invoice date is of data type "Date field". For example, in case of ambiguous date format such as 01-02-2024, the use case \(the current use case\) interprets the date as month followed by day or vice versa through the DI administration configuration menu. The platform admin \[platform\_ml\_di.admin\] manually configures the use case in the DI administration menu. For more information on the DocIntel fields used to extract data, see [.](https://www.servicenow.com/docs/access?context=single-field-form&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)For the list of invoice and invoice line fields included in the **DO NOT USE - Invoice Processing** use case, see [List of invoice and invoice line fields included in the use case for Accounts Payable Operations integration with Document Intelligence](../reference/use-case-field-list.md).

</td></tr><tr><td>

Field Groups

</td><td>

Includes the **Invoice Lines** field group that maps to the Invoice Line Stage \[sn\_ap\_ic\_invoice\_line\_stage\] target table where the extracted invoice line information from the invoice document is stored.

</td></tr><tr><td>

Document tasks

</td><td>

Includes a document task to train the Document Intelligence model to identify the correct information to extract from an invoice document.

</td></tr><tr><td>

Integration

</td><td>

Maps to the **DO NOT USE - Invoice processing** use case that contains the **DocIntel Extract Values Flow - Invoice processing v1.2 - Invoice Processing v1.2** extraction flow, which populates the extracted invoice data into the invoice stage and invoice line stage records. It also updates the Invoice stage status to Processing completed.

</td></tr></tbody>
</table>-   **[List of invoice and invoice line fields included in the use case for Accounts Payable Operations integration with Document Intelligence](../reference/use-case-field-list.md)**  
The **DO NOT USE - Invoice Processing** use case includes the following set of invoice and invoice line fields from which to extract information from your invoice documents.

**Parent Topic:**[Install Accounts Payable Operations integration with Document Intelligence](apm-integration-docintel.md)

