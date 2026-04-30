---
title: Create an invoice exception definition
description: You can create invoice exception definition for invoices of types PO, Non-PO, credit memo.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Invoice exceptions, Using Accounts Payable Invoice Processing, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Create an invoice exception definition

You can create invoice exception definition for invoices of types PO, Non-PO, credit memo.

## Before you begin

Role required: sn\_ap\_apm.admin

This video shows you how to perform the following procedure.

Create an invoice exception definition

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Administration** &gt; **Invoice exception definition**.

2.  On the Invoice exception definitions form, select **New**.

3.  On the Invoice exception definition form, fill in the fields.

    For description of the field values, see [Invoice exception definition form](../reference/invoice-exception-definition-form.md). Example: Missing business owner or legal entity.

4.  Select **Active**.

5.  Select **Applicable to** as PO invoice.

6.  Enter the order number by which the exception must be executed.

7.  Select and hold \(or right-click\) on the form and **Save**.

8.  Configure the subflow that you want to choose from the drop-down list.

    For more information on sub flows, see [Create subflow in workflow studio](create-subflow-in-workflow-studio.md).

9.  Select **Save**.

10. Open an invoice record with all fields configured and click **View invoice processing case**.

    For more information on creating an invoice record, see [Create an invoice manually](create-invoice.md). The exception engine runs and displays exceptions in the **Review exceptions** activity card of the playbook.

11. Click **Resolve exceptions** activity card.

    The exceptions are displayed. Navigate to the invoice details and populate the valid business owner details.

12. Navigate to the invoice details and populate the valid business owner details.

13. Click **Save**.

    The form is saved.

14. Click **Check exceptions**.


## Result

The exception is raised and resolved successfully.

-   **[Create subflow in workflow studio](create-subflow-in-workflow-studio.md)**  
Use subflows to configure conditions that are applied on the invoice and raise an exception.

**Parent Topic:**[Invoice exceptions](../concept/work-with-invoice-exceptions.md)

