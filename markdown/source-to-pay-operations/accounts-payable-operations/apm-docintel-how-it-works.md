---
title: How Accounts Payable Operations integration with Document Intelligence works
description: Accounts Payable Operations integration with Document Intelligence uses automated workflows to extract the required information from the invoice document received as an email attachment, creates an invoice record in Accounts Payable Operations, and adds the extracted information into the newly created invoice record.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Install Accounts Payable Operations integration with Document Intelligence, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# How Accounts Payable Operations integration with Document Intelligence works

Accounts Payable Operations integration with Document Intelligence uses automated workflows to extract the required information from the invoice document received as an email attachment, creates an invoice record in Accounts Payable Operations, and adds the extracted information into the newly created invoice record.

## Invoice ingestion process flow when extraction confidence is high

When you receive an invoice as an attachment via email from a supplier or an employee, the following occurs:

1.  An invoice case is created with category **Invoice automation** and subcategory **Invoice processing** in Accounts Payable Operations.
2.  If Document Intelligence determines that the extraction confidence is higher than the threshold value, it extracts the invoice data and stores the data in temporary staging tables.
3.  The Document Intelligence transformation process imports the invoice data from the staging tables, creates an invoice in the Draft state, and associates the invoice with the invoice processing case.
4.  The application verifies the following:

    -   The required fields are populated on the invoice.
        -   If the required fields aren’t populated on the invoice, the Accounts Payable Specialist is required to open the invoice, manually enter the required values in the required fields, and submit the invoice.
        -   If the required fields are populated on the invoice, the invoice is auto-submitted.
    -   At least one invoice line record exists for the invoice. If not, the Accounts Payable Specialist must add an invoice line record and submit the invoice.
    -   If a unique currency code isn’t identified during currency transformation, the process uses the currency mentioned in the purchase order. If the currency is missing in the purchase order, the transformation process uses the session currency based on the user's locale. In this case, the Accounts Payable Specialist is required to open the invoice processing case, and enter the correct currency code in the invoice fields and submit the invoice. For more information, see [Invoice data transformation logic](invoice-data-trans-logic.md).
    For more information about the required fields for invoice and invoice lines, see [Required fields for creating an invoice](../reference/mandatory-fields-docintel.md).

    After the invoice is submitted, its state changes to Received. The invoice processing begins from this point. For more information, see [Work on an invoice processing case](../task/work-manual-invoice-ingestion-case.md).


## Invoice ingestion process flow when extraction confidence is low

When you receive an invoice as an attachment via email from a supplier or an employee, the following occurs:

1.  An invoice case is created with category **Invoice automation** and subcategory **Invoice processing** in Accounts Payable Operations.
2.  If Document Intelligence determines that the extraction confidence is lower than the threshold value, it doesn’t extract the invoice data and as a consequence an invoice isn’t created.
3.  In this scenario, the Accounts Payable Specialist must do the following:
    1.  Open the invoice processing case created in [step 1](apm-docintel-how-it-works.md#ip-case-low).

        The case displays the following error message: Invoice has a data extraction error. Review invoice with automation to continue processing.

    2.  Select **Review invoice**, which opens Document Intelligence and displays the invoice fields.
    3.  Enter the required values into the invoice fields, and select **Submit**.
4.  The Document Intelligence transformation process imports the invoice data from the staging tables, creates an invoice in the Draft state, and associates the invoice with the invoice processing case.
5.  The application verifies the following:

    -   The required fields are populated on the invoice.
        -   If the required fields aren’t populated on the invoice, the Accounts Payable Specialist is required to open the invoice, manually enter the required values in the required fields, and submit the invoice.
        -   If the required fields are populated on the invoice, the invoice is auto-submitted.
    -   At least one invoice line record exists for the invoice. If not, the Accounts Payable Specialist must add an invoice line record and submit the invoice.
    -   A unique currency code exists on the invoice. If a unique currency code isn’t identified during currency transformation, the process uses the currency mentioned in the purchase order. If the currency is missing in the purchase order, then the transformation process uses the session currency based on the user's locale. In this case, the Accounts Payable Specialist is required to open the invoice processing case and enter the correct currency code in the invoice fields and submit the invoice. For more information, see [Invoice data transformation logic](invoice-data-trans-logic.md).
    For more information about the required fields for invoice and invoice lines, see [Required fields for creating an invoice](../reference/mandatory-fields-docintel.md).

    After the invoice is submitted, its state changes to Received. The invoice processing begins from this point. For more information, see [Work on an invoice processing case](../task/work-manual-invoice-ingestion-case.md).


## Invoice ingestion process flow when the entire transformation process fails

When the Document Intelligence transformation process fails entirely, the following error message is displayed on the invoice processing case:

Invoice automation is experiencing issues. Please contact the administrator.

You must collaborate with the administrator to resolve this issue.

## Localization information

Accounts Payable Operations supports multiple languages. The current DocIntel model is trained to extract invoices in the English language only. If you want to process the invoice in multi-lingual languages supported by DocIntel, you must train the DocIntel model on your own.

For more information on Document Intelligence, see Document Intelligence.

-   **[Required fields for creating an invoice](../reference/mandatory-fields-docintel.md)**  
The Accounts Payable Operations integration with Document Intelligence application checks whether the required fields are populated on the invoice and invoice lines for creating the invoice.
-   **[Invoice data transformation logic](invoice-data-trans-logic.md)**  
Accounts Payable Operations integration with Document Intelligence converts the invoice and invoice line field values from the invoice document to a format supported by the system that processes the invoice.

**Parent Topic:**[Install Accounts Payable Operations integration with Document Intelligence](apm-integration-docintel.md)

