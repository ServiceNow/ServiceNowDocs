---
title: Invoice exceptions
description: Invoice exceptions are issues that are identified in an invoice during invoice processing.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Invoice exceptions

Invoice exceptions are issues that are identified in an invoice during invoice processing.

The Accounts Payable Operations exception engine automatically identifies discrepancies in invoices and lists them as invoice exceptions in the Source-to-Pay Workspace workspace. The Accounts Payable Specialist can analyze the identified invoice exceptions and take appropriate action to resolve them.

The Accounts Payable Operations exception engine is run for the PO invoices that are in either the PO matching completed or Exceptions found state.

The Accounts Payable Operations exception engine is run for Non-PO invoices that are in the Accepted or Exceptions found state.

The Accounts Payable Operations exception engine identifies invoice exceptions of the following types.

<table id="table_vlc_hk1_wvb"><thead><tr><th>

Invoice exception

</th><th>

Description

</th><th>

 

</th><th>

Do these steps to resolve the invoice exception

</th><th>

Applicable to

</th></tr></thead><tbody><tr><td>

Invalid or blocked supplier

</td><td>

This exception occurs in one of the following scenarios:-   The supplier information is missing on the invoice.
-   The supplier information on the invoice doesn’t match the information on the purchase order if invoice is of type PO.
-   The Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) table doesn’t have a record with a combination of Invoice.supplier and Invoice.legal\_entity fields
-   In the Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) table, the supplier has one of the following attributes set to true:
    -   Hold Payment: Indicates that the invoice payment is put on hold for the supplier
    -   Hold Posting: Indicates that the invoice posting is put on hold for the supplier

This exception is a header-level exception.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:-   If the supplier information is missing on the invoice, do the following:
    1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
    2.  Populate a valid supplier and legal entity.
-   If the supplier information on the invoice doesn’t match with that on the purchase order, do the following:
    1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
    2.  Update the supplier information on the invoice to match with that on the purchase order.
-   If the Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) table, doesn’t have a record with a combination of Invoice.supplier and Invoice.legal\_entity, do the following:
    1.  Log in with the Supplier Enablement Manager \(sn\_fin.supplier\_payment\_info\_write\) role.

    2.  Add a record with the combination of Invoice.Supplier – Invoice.LegalEntity fields in the Supplier Legal Entity Mapping \(sn\_fin\_supplier\_detail\) table.
-   If the supplier's Hold Payment and Hold Posting attributes are set to true in the Supplier Legal Entity Mapping table, do the following:
    1.  Log in with the Supplier Enablement Manager \(sn\_fin.supplier\_payment\_info\_write\) role.

    2.  Take the necessary actions to remove holds from invoices to enable payment and posting of the invoices.

</td><td>

PO invoice and Non-PO invoice

</td></tr><tr><td>

Insufficient Funds \(Quantity variance\)

</td><td>

This exception occurs when the total quantity of previously billed invoices and the current invoice, which is in-process becomes more than the respective purchase order line quantity.This exception is a line-level exception.

To resolve this invoice exception, you must edit the purchase order. For more information, see [Edit a purchase for an Insufficient Funds invoice exception](../task/edit-purchase-insufficient-funds.md).

</td><td>

 

</td><td>

To resolve this invoice exception, you must edit the purchase order. For more information, see [Edit a purchase for an Insufficient Funds invoice exception](../task/edit-purchase-insufficient-funds.md).

</td><td>

PO invoice

</td></tr><tr><td>

Insufficient Funds \(Line amount variance\)

</td><td>

This exception occurs when purchase order lines don't have sufficient funds left to process the current invoice, which is in-process.This exception is a line-level exception.

</td><td>

 

</td><td>

To resolve this invoice exception, you must edit the purchase order. For more information, see [Edit a purchase for an Insufficient Funds invoice exception](../task/edit-purchase-insufficient-funds.md).

</td><td>

PO invoice

</td></tr><tr><td>

Insufficient Goods Receipt

</td><td>

This exception occurs when one or more lines of an invoice don’t have sufficient receipts to process the invoice.This exception is a line-level exception.

</td><td>

 

</td><td>

-   **Resolving the Insufficient Goods Receipt exception when PSM is installed**

If Sourcing and Procurement Operations \(PSM\) is installed, and if no receipt task exists for the purchase order line, Accounts Payable Invoice Processing creates a receipt task and displays the task in the **Related tasks** tab of the exception form. For more information, see [Invoice exception form](../reference/exception-form-fields.md).

The receipt task is assigned to the user specified in the **Recipient** field on the PO line. The recipient must have the sn\_shop.acknowledgement\_task\_owner role to complete the receipt task from Employee Center.

For more information, see [Confirm receipt of your order from Employee Center](../task/confirm-receipt-task.md).

-   **Resolving the Insufficient Goods Receipt exception when PSM isn’t installed**

If Sourcing and Procurement Operations isn’t installed, then the Accounts Payable Specialist must manually create an exception task, which is assigned to the business owner. The business owner must mark this task as complete in Employee Center. For more information, see [Mark an exception task as complete from Employee Center](../task/complete-exception-task-ec.md).


</td><td>

PO invoice

</td></tr><tr><td>

Valid coding required

</td><td>

This exception occurs when one or more lines of an invoice cost is distributed across multiple cost centers or general ledger accounts. When the cost is split across multiple cost centers, the cost center field on the invoice line is read-only and allows one type of allocation type in the cost. This exception is a line-level exception and applies for general ledger account.

</td><td>

 

</td><td>

To resolve this invoice line exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Populate the ledger account, enter the information for invoice lines or cost allocations. For example: You can enter a ledger account in the invoice lines and add multiple cost allocations on the allocations page, or you can enter a cost center in the invoice lines and include several general ledger account allocations on the cost allocations page. You can also choose to enter general ledger and cost center both in the invoice line.

</td><td>

PO Invoice and Non-PO invoice

</td></tr><tr><td>

Missing required information

</td><td>

This exception occurs when one or more fields of the following are missing on the invoice:-   Payment terms
-   Invoice type
-   Supplier
-   Invoice amount
-   Invoice date
-   Legal entity

This exception is a header-level exception.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Populate the following fields on the invoice:
    -   Payment terms
    -   Invoice type
    -   Supplier
    -   Invoice amount
    -   Invoice date
    -   Legal entity

</td><td>

PO Invoice and Non-PO invoice

</td></tr><tr><td>

Missing or Invalid Business Owner

</td><td>

This exception occurs when the business owner of the invoice is missing or inactive or is different from the business owner mentioned in the purchase order \(if invoice is of type PO\).This exception is a header-level exception.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Update the valid business owner field in the invoice line.

</td><td>

PO Invoice and Non-PO invoice

</td></tr><tr><td>

Over tax amount variance

</td><td>

This exception occurs when the supplier tax amount is greater than the system tax amount.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Make necessary corrections to the supplier tax, system tax on all the invoice lines.
3.  You can choose to either accept system tax or supplier tax.

</td><td>

PO Invoice, Non-PO invoice, and Credit memo

</td></tr><tr><td>

Under tax amount variance

</td><td>

This exception occurs when the supplier tax amount is lesser than the system tax amount.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Make necessary corrections to the supplier tax, system tax on all the invoice lines.
3.  You can choose to either accept system tax or supplier tax.

</td><td>

PO Invoice, Non-PO invoice, and Credit memo

</td></tr><tr><td>

Tax validation failed

</td><td>

This exception occurs when the tax is not validated due to integration error

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) or Tax specialist role.
2.  The system restarts the tax execution

</td><td>

 

</td></tr><tr><td>

Tax validation expired

</td><td>

Tax information is changed after the invoice execution, then Tax validation expired failed exception is raised.

</td><td>

 

</td><td>

1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) or Tax specialist role.
2.  Make necessary corrections to the invoice and selects **Validate tax** to re-calculate the tax

</td><td>

 

</td></tr><tr><td>

Under tax amount variance \(Invoice line\)

</td><td>

Tax amount on an invoice line is lesser than the tax response received for the line item through tax engine

</td><td>

 

</td><td>

1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) or Tax specialist role.
2.  Make necessary corrections to the invoice line item and select either **Accept Supplier tax** or **Accept System tax**

</td><td>

 

</td></tr><tr><td>

Under tax amount variance \(Invoice header\)

</td><td>

Total tax amount on the invoice header is lesser than the total tax for the invoice received through tax engine

</td><td>

 

</td><td>

1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) or Tax specialist role.
2.  Make necessary corrections to the invoice header and select either **Accept Supplier tax** or **Accept System tax**

</td><td>

 

</td></tr><tr><td>

Over tax amount variance \(Invoice header\)

</td><td>

Total tax amount on the invoice header is greater than the total tax of the invoice received through tax engine

</td><td>

 

</td><td>

1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) or Tax specialist role.
2.  Make necessary corrections to the invoice header and select either **Accept Supplier tax** or **Accept System tax**

</td><td>

 

</td></tr><tr><td>

Over tax amount variance \(Invoice line\)

</td><td>

Tax amount on the invoice line is greater than the tax of the invoice line item of the invoice received through tax engine

</td><td>

 

</td><td>

1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) or Tax specialist role.
2.  Make necessary corrections to the invoice line item and select either **Accept Supplier tax** or **Accept System tax**

</td><td>

 

</td></tr><tr><td>

Invoice isn’t balanced

</td><td>

This exception occurs when sum of the subtotals of the invoice lines must match the sub total amount in the header.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Make necessary corrections to the sub total so that the sum of sub totals of invoice lines match with the invoice header amount.

</td><td>

PO Invoice, Non-PO invoice, and Credit memo

</td></tr><tr><td>

Insufficient Funds \(Header amount variance\)

</td><td>

This exception occurs when purchase order doesn’t have sufficient balance left to process the invoice.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Make necessary corrections to invoice amount so that the sum of amount of all invoices related to PO \(in progress or paid\) amount must be less than the total PO amount.

</td><td>

PO invoice

</td></tr><tr><td>

Line unit price variance

</td><td>

This exception occurs due to difference in unit price of invoice line and PO.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Make necessary corrections to unit price on invoice line so that it’s equal to unit price of PO line.

</td><td>

PO invoice, Credit memo

</td></tr><tr><td>

Incomplete credit memo

</td><td>

This exception occurs when any of the following are missing on a credit memo invoice:-   Original invoice number
-   Original invoice
-   Purchase order

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Make necessary corrections on the invoice by populating the Original invoice number, Original invoice, and purchase order fields.

</td><td>

Credit memo

</td></tr><tr><td>

Insufficient billing amount on purchase order

</td><td>

This exception occurs when purchase order doesn't have sufficient billing quantity or amount to process the credit memo invoice.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Make necessary corrections to invoice line amount such that the line amount doesn’t exceed the sum of PO line amount and other credit memo \(approved or pending approval\) related to the PO line.

</td><td>

Credit memo

</td></tr><tr><td>

Missing tax information

</td><td>

This exception occurs when tax line information is missing in an invoice. This is a header level exception.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following:1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Add tax lines details to the invoice using the **Add tax** button.

**Note:** The under tax amount variance and over tax amount variance are dependent on the Missing tax information exception.


</td><td>

PO Invoice, Non-PO invoice, and Credit memo

</td></tr><tr><td>

Missing tax code details

</td><td>

This exception occurs when tax code details are missing in one or more invoice lines. This exception applies to PO invoice, non-PO invoice and credit memo. This is a line level exception.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following: 1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Populate the tax code details.

</td><td>

PO Invoice, Non-PO invoice, and Credit memo

</td></tr><tr><td>

Currency mismatch

</td><td>

This exception occurs when the currency on an invoice does not match the currency on the associated purchase order when purchase order mapping is disabled and the invoice is still in draft state. The cost allocation data is preserved even when the purchase order mapping is turned off.

</td><td>

 

</td><td>

To resolve this invoice exception, do the following: 1.  Log in to the application with the Accounts Payable Specialist \(sn\_ap\_apm.accounts\_payable\_specialist\) role.
2.  Correct the currency details to match the invoice and purchase order.

</td><td>

PO invoice, Credit memo

</td></tr></tbody>
</table>By default, the exception engine is configured to run once every 5 minutes through the **Exception Monitoring Job**. This is a scheduled job, which is inactive in the state by default. For information on how to activate the scheduled job, see [Activate the Exceptions Monitoring Scheduler](../task/activate-exception-flow.md).

However, you can also run the exception engine manually. For more information, see [Check for invoice exceptions on a single invoice](../task/identify-exceptions-manually.md).

When you run the exception engine manually on a single invoice, it checks for exceptions only on that invoice, whereas the automated exception engine checks for exceptions on all the invoices that are valid for exception check.

You can bypass an exception in situations where that exception is not applicable to an invoice. For more information, see [Bypass an invoice exception](../task/bypass-invoice-exception.md).

The Accounts Payable Operations exception engine finds exceptions and lists them in the list page of the Source-to-Pay Workspace. View the list of exceptions by navigating to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

In the workspace, select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and do one of the following:

-   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice exceptions**.
-   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice exceptions**.

The Accounts Payable Specialist can analyze the invoice exceptions, create exception tasks, and assign these tasks to the relevant individuals to fix the exceptions and resolve the case. For more information, see [Work on an invoice exception](../task/work-invoice-exception-case.md).

-   **[Activate the Exceptions Monitoring Scheduler](../task/activate-exception-flow.md)**  
Activate the **Exception Monitoring Scheduler** to run the exception engine on a regular schedule to identify invoice exceptions.
-   **[Work on an invoice exception](../task/work-invoice-exception-case.md)**  
As an Accounts Payable Specialist, analyze the invoice exceptions, create exception tasks, and assign them to the relevant individuals to resolve the invoice exceptions.
-   **[View invoice line details for a line-level invoice exception](../task/view-igr-exception-lines.md)**  
View details about invoice lines to understand why a line-level invoice exception has been created.
-   **[View related tasks for an Insufficient Goods Receipt invoice exception](../task/view-psm-task-inv-exception.md)**  
As an Accounts Payable specialist, view tasks related to Sourcing and Procurement Operations to understand why an Insufficient Goods Receipt invoice exception has been raised for an invoice.
-   **[Create an invoice exception definition](../task/define-new-invoice-exception.md)**  
You can create invoice exception definition for invoices of types PO, Non-PO, credit memo.

**Parent Topic:**[Using Accounts Payable Invoice Processing](use-ap-invoice-processing.md)

**Related topics**  


[Invoice ingestion using Application programming interface \(API\)](invoice-ingestion-using-api.md)

[Rules based engine](rules-based-engine.md)

[Work with invoices](work-with-invoices.md)

[Invoice processing cases](working-with-ingestion-cases.md)

[Tolerance Rules and Variances for invoices](tolerance-rules-and-variance.md)

[Invoice approvals](invoice-approvals.md)

[View invoice documents in the Source-to-Pay Workspace](../task/view-invoice-attachment.md)

