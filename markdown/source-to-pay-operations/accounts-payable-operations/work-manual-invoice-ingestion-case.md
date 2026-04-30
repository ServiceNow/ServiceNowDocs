---
title: Work on an invoice processing case
description: Perform different manual actions to process an invoice.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Invoice processing cases, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Work on an invoice processing case

Perform different manual actions to process an invoice.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

An invoice case with a category of Invoice automation and sub-category of Invoice processing is referred to as an invoice processing case.

By default, an invoice processing case is automatically created when you receive an invoice via email. Document Intelligence captures the invoice data and subsequently creates the invoice and invoice line records in Accounts Payable Operations. However, the Accounts Payable Specialist can also manually create an invoice from the Source-to-Pay Workspace. For more information, see [Create an invoice manually](create-invoice.md).

For a description of the field values and information about the available tabs on the invoice processing case form, see [Invoice processing case form](../reference/invoice-processing-case-form.md).

## Procedure

1.  Navigate to **Source-to-Pay Workspace**&gt;**All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Do one of the following:

    -   Navigate to **Lists** &gt; **My work** &gt; **Open cases**.
    -   Navigate to **Lists** &gt; **All work** &gt; **Cases**.
    ![List view](../image/apo-list-view.png)

4.  Open an invoice processing case.

    Typically, the state of the newly created invoice processing case is New and the status of the invoice associated with this case is either Draft or Received, depending on how it was processed by the Accounts Payable Operations integration with Document Intelligence application.

    For more information about invoice statuses, see [Work with invoices](../concept/work-with-invoices.md).

5.  In the **Assigned to** field, specify a user that you want to assign the invoice processing case to.

    The invoice processing case moves to the Assigned state.

6.  Do one of the following:

    -   If you have the Accounts Payable Specialist role, assign the invoice processing case to yourself by selecting **Assign to me**.
    -   If the invoice processing case is assigned to you by the Accounts Payable Specialist, start working on the case by selecting **Accept**.
    The invoice processing case moves to the Work in progress state.

7.  Do one of the following:

<table id="table_mvk_c3r_gwb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Review the invoice in Document Intelligence to create the invoice

</td><td>

If a processing error occurs in Document Intelligence, the invoice processing case displays the following error:

 `Invoice has a data extraction error. Review invoice with automation to continue processing.`

 For more information, see [Review an invoice in Document Intelligence](review-invoice-docintel.md).

</td></tr><tr><td>

Enter the missing required information in the invoice

</td><td>

If a transformation error occurs in Document Intelligence, the invoice processing case displays the following error:

 `Required information for invoice has one or more errors. Review required fields and currency in "Details" tab to continue processing.`

 For more information, see [Enter the missing required invoice information and submit an invoice](enter-missing-docintel.md).

</td></tr></tbody>
</table>8.  Submit the invoice.

    After you submit the invoice, the status of the invoice updates to Received and the invoice processing case remains in the Work in progress state.

    The automated duplicate check process is run and if the process suspects that the invoice is a duplicate, the invoice moves to the Suspected duplicate status, and the invoice processing case displays the following error.

    `Invoice is a potential duplicate. Review invoices in "Potential duplicate invoices" tab to confirm or reject duplicate.`

    The Accounts Payable Specialist must manually confirm whether the invoice is a duplicate.

9.  Confirm whether the invoice is a duplicate.

    For more information, see [Confirm whether an invoice is a duplicate](confirm-duplicate-invoice.md).

    If you confirm that the invoice is a duplicate, the invoice moves to the Confirmed duplicate status and the invoice processing case moves to the Closed incomplete state.

    **Note:** When the invoice is in the Confirmed duplicate status, the **Reset to Received** option becomes available. If you've confirmed an invoice as duplicate by mistake, you can reset the status back to the Received status. For more information, see [Reset an invoice to the Received status](reset-invoice-to-received.md).

    If you confirm that the invoice is not a duplicate, the invoice moves to the Accepted status, and the invoice processing case remains in the Work in progress state.

    After the invoice moves to the Accepted status, the automated PO matching process is run and one of the following occurs:

    -   If the invoice matches with the PO, then the invoice moves to the PO matching completed status.
    -   If the invoice doesn't match with the PO, then the invoice moves to the PO matching error status and the invoice processing case displays the following error:

        `Invoice needs to match Purchase order. Match "invoice lines" to "Purchase order lines" to continue processing.`

        The Accounts Payable Specialist must manually match the invoice and invoice lines with the PO and the PO lines, respectively. The invoice moves to the PO matching completed status only after all the invoice lines move to the PO matching completed status.

        The invoice processing case remains in the Work in progress state.

        **Note:** After the invoice moves to the PO matching completed status, the exception engine is run via a scheduled job at a specific time on a recurring basis. The exception engine runs on all the invoices that are in the PO matching completed status.

        At this stage, however, you can also manually run the exception engine to identify invoice exceptions on the invoice.

    **Note:** The **Check for exceptions** option enables you to instantly run the exception engine on a single, selected invoice that is in the PO matching completed status, whereas the scheduled job periodically runs the exception engine on all the invoices that are in the PO matching completed status.

10. Check for exceptions on the invoice.

    For more information, see [Check for invoice exceptions on a single invoice](identify-exceptions-manually.md).

    If no exceptions are found, the invoice moves to the No exceptions found status.

    If exceptions are found on the invoice, the invoice moves to the Exceptions found status, and the invoice processing case displays the following error:

    `Invoice has one or more exceptions. Resolve all issues in "Invoice exceptions" to continue processing.`

    The Accounts Payable Specialist can work on the exceptions or create exception tasks and assign them to other users to resolve the exceptions. For more information, see [Invoice exceptions](../concept/work-with-invoice-exceptions.md).

    After all the exception tasks are completed and the exceptions are resolved, the invoice moves to the No exceptions found status. The invoice processing case remains in the Work in progress state.

    At this stage, the automated invoice approval process runs and submits the invoice for approval.

    The invoice moves to the Pending approval status and the invoice processing case remains in the Work in progress state.

    Typically, an invoice that is in the No exceptions found status is automatically picked by the approval engine and submitted for approval. However, in a few scenarios, you may have to manually submit an invoice for approval. For more information, see [Invoice approvals](../concept/invoice-approvals.md).

    After you submit the invoice, the invoice moves to the Pending approval status, and the invoice processing case remains in the Work in progress state.

    At this stage, one of the following occurs:

    -   If the invoice is rejected, the invoice moves to the Rejected status and the rejection comments are copied over to the invoice processing case.

        To resubmit the invoice, you must cancel the rejected invoice using the **Cancel invoice** option and submit a new invoice.

    -   If the invoice is approved, the invoice moves to the Approved status and the invoice processing case moves to the Closed complete state.

## Result

The different manual actions are performed to process an invoice.

-   **[Accounts Payable Specialist manual tasks](../concept/aps-manual-tasks.md)**  
Accounts Payable Operations performs invoice processing using automated workflows, with minimal manual intervention. In some situations, however, the Accounts Payable Specialist is required to perform a few manual tasks to move the invoice to the next stage of processing.

**Parent Topic:**[Invoice processing cases](../concept/working-with-ingestion-cases.md)

**Related topics**  


[Accounts Payable Invoice Processing](../concept/acc-pay-invoice-processing.md)

[Invoice Case Management](../concept/acc-pay-case-mgmt-overview.md)

[Source-to-Pay Workspace](../concept/acc-pay-workspace.md)

[Invoice processing cases](../concept/working-with-ingestion-cases.md)

[Tolerance Rules and Variances for invoices](../concept/tolerance-rules-and-variance.md)

[Invoice approvals](../concept/invoice-approvals.md)

