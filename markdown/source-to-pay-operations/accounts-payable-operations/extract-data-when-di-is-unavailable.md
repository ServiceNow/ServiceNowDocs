---
title: Extract data when Document Intelligence is unavailable
description: You must manually create an invoice for processing when Document Intelligence is unavailable.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Document Intelligence processing with playbook, Playbook for updating the invoice primary data, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Extract data when Document Intelligence is unavailable

You must manually create an invoice for processing when Document Intelligence is unavailable.

## Before you begin

Role required: Accounts Payable admin, Accounts Payable specialist

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

    A list of options within the workspace is displayed.

3.  Select **Invoices &gt;****All invoices.**

    You can create an invoice manually. For more information on invoices, see [Work with invoices](../concept/work-with-invoices.md).

4.  Select **View invoice processing case**.

    A playbook is created for the invoice processing case.

5.  Select **Validate invoice**&gt;**Capture invoice details** activity card.

    An alert message displays as: `DocIntel is unavailable to process the invoice. To continue processing, manually create an invoice or close the case`.

6.  Select **Create invoice** manually.

    **Note:** You can select **Create invoice** when Document Intelligence is down or still processing in the background. If Document Intelligence is extracting invoice details via email using generative AI skill, then the invoice processing case is created with **Review invoice** option enabled. Thus, prompting the Accounts Payable specialist to manually review the invoice details.

    For more information on manual creation of invoices, see [Using Invoice Case Management](../concept/use-invoice-case-mgmt.md)

7.  Select **Review header details** to populate the header fields.

8.  Select **Review invoice lines** and add the invoice line fields or populate the required fields.

9.  Select **Submit**.

    If no further processing is required, then you can close the invoice case. A pop-up window prompts you to enter the reason for closing the invoice processing case. The playbook is canceled and the supplier is notified about the closure of the invoice processing case. The **Notify supplier** card is activated by default and displays the email sent to the supplier.

    **Note:** Invoices ingested through integration or manually, the **Capture invoice details** activity card isn’t displayed under **Validate invoice**.


## Result

The invoice is manually created for processing when Document Intelligence is unavailable.

**Parent Topic:**[Document Intelligence processing with playbook](../concept/use-di-with-playbook.md)

