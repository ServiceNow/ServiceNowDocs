---
title: Create an invoice exception definition
description: Create invoice exception definitions to flag PO, Non-PO, and credit memo invoices based on defined conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/define-new-invoice-exception.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, invoice exception, invoice automation]
breadcrumb: [Invoice exceptions, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Create an invoice exception definition

Create invoice exception definitions to flag PO, Non-PO, and credit memo invoices based on defined conditions.

Create an exception definition 

## Before you begin

Role required: sn\_ap\_apm.admin

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Administration** &gt; **Invoice exception definition**.

2.  On the Invoice exception definitions form, select **New**.

3.  On the Invoice exception definition form, fill in the fields.

    For a description of the field values, see [Invoice exception definition form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/invoice-exception-definition-form.md). Example: Missing business owner or legal entity.

4.  Select **Active**.

5.  Select **Applicable to** as PO invoice.

6.  Enter the order number by which the exception must be executed.

7.  Select and hold \(or right-click\) on the form &gt; **Save**.

8.  Configure the subflow that you want to choose from the drop-down list.

    For more information on sub flows, see [Create subflow in workflow studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-subflow-in-workflow-studio.md).

9.  Select **Save**.

10. Open the invoice record with all fields configured and click **View invoice processing case**.

    The exception engine runs and displays exceptions in the **Review exceptions** activity card of the playbook.

11. Click **Resolve exceptions** activity card.

    The exceptions are displayed. Navigate to the invoice details and populate the valid business owner details.

12. Navigate to the invoice details and populate the valid business owner details.

13. Click **Save**.

14. Click **Check exceptions**.

    The exception is raised and resolved successfully.


-   **[Create subflow in workflow studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/create-subflow-in-workflow-studio.md)**  
Use subflows to configure conditions that are applied on the invoice and raise an exception.

**Parent Topic:**[Invoice exceptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/work-with-invoice-exceptions.md)

