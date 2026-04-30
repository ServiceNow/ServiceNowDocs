---
title: Using Playbook in Accounts Payable Operations
description: Configure a playbook and visualize the step-by-step actions performed by an Accounts Payable specialist while processing an invoice.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Playbook for updating the invoice primary data, Using Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Using Playbook in Accounts Payable Operations

Configure a playbook and visualize the step-by-step actions performed by an Accounts Payable specialist while processing an invoice.

## Before you begin

Role required: Accounts Payable specialist

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

    A list of options within the workspace is displayed.

3.  Select **Invoices &gt;****All invoices.**

    You can create an invoice manually. For more information on invoices, see [Work with invoices](../concept/work-with-invoices.md).

4.  Select **View Invoice processing case**.

    A playbook is available for the Invoice processing case. You can view the stages and activities of Invoice processing in the **Playbook** tab.

5.  Select **Validate invoice**.

    The invoice opens and you must verify the invoice details.

    1.  Select the **Review header** details.

        Review the invoice header details and make any required changes.

    2.  Select **Save**.

    3.  Select **Continue** to move to the next activity in the playbook.

    4.  Select the **Review invoice lines** activity.

        Manually review the invoice lines associated with the invoice processing case.

    5.  Select **Add new invoice lines** to create invoice lines.

    6.  Select **Continue** to move to the next activity in the playbook.

    7.  Select the **Review invoice tax line details** activity.

        The **Review invoice tax line details** displays the list of invoice tax lines.

    8.  Select **Add tax**.

        The **Add tax lines to the invoice** pop-up box displays. You can choose to add tax lines associated with invoice line. For more information on the fields of tax lines, see [Invoice Tax lines fields](../reference/tax-lines.md).

    9.  Select an **Invoice line** in which you would like to add the tax lines.

    10. Select the **Apply to all invoice lines** check box if you want to add the tax lines to all the invoice lines.

    11. In the **Enter tax details** area, perform the following steps.

    12. Select the **Tax type** to be associated with the invoice line.

    13. Enter the **Supplier tax rate** details.

    14. Enter the **Taxable amount** details.

    15. Enter the **Supplier tax** details.

    16. Select **Add tax**.

        The tax lines are added to the invoice line.

    17. Select **Submit invoice**.

        The invoice is submitted with tax lines.

6.  Select **Check Duplicates**.

    1.  The **Check Duplicates** activity enables you to check if the invoice processing case is a suspected duplicate.

        The **Review Duplicates** activity is auto-selected if the invoice is a suspected duplicate. If the invoice isn't a suspected duplicate, then the activity is set to auto-complete.

    2.  Select **Confirm duplicate**.

        If the invoice is found to be duplicate, then select confirm duplicate. The invoice moves to a confirmed duplicate State and the playbook is set to **Cancelled**

    3.  Select **Notify supplier**.

    4.  Select **Not a duplicate** if the invoice isn’t duplicate.

        A pop-up box displays prompting the user to enter the reason for the non-duplicate invoice.

    5.  To reset the invoice to the received state after setting, it as confirmed duplicate follow the steps from [Reset an invoice to the Received status](reset-invoice-to-received.md).

7.  Select the **Match lines** card.

    If the invoice is a PO invoice or credit memo invoice of type PO and the invoice doesn't run into a matching error, then the **Match lines** card is set to auto-complete. However, if the invoice is of type Non-PO invoice or a credit memo invoice of type Non-PO, the stage is skipped.

    1.  Verify the **Match invoice lines** card.

    2.  You can edit the changes to the purchase order form and select **Update**.

    3.  Select **Continue** after you save the changes.

    4.  In the **Review the PO Lines** card, review the PO lines associated with the purchase order to identify the lines that is mapped to the invoice line.

    5.  You can edit the invoice lines and match the invoice lines with the corresponding purchase order lines.

    6.  Verify the **Verify Purchase Order** card.

        Verify the purchase order details associated with an invoice.

8.  Select **Review exceptions**.

    The list of exceptions raised for the invoice is listed. For more information on exceptions, see [Invoice exceptions](../concept/work-with-invoice-exceptions.md). This stage is set to auto-complete if the invoice doesn't run into exceptions.

    1.  Review the exceptions generated for the invoice using the **Resolve exceptions** card, and resolve exceptions if any.

    2.  Select an **Check exceptions** action to reevaluate the exceptions.

    3.  Select **Review exception tasks** to resolve exception tasks if any.

    4.  Select **Create new task** to create an exception task.

        For more information on exception tasks, [Work on an invoice exception](work-invoice-exception-case.md).

9.  Select the **Await approval** card.

    This stage is set to auto-complete after the invoice is approved.

    **Note:** Use **Review approvals** generated for the invoice. In the **Notify supplier** activity, you can review the emails sent to the supplier when an invoice is rejected.

10. Select the **Pay Invoice** card.

    1.  In the **Review Integration errors** activity, review the integration errors generated for the invoice.

        For more information on integration errors, see [Integration errors](../concept/integration-errors-during-erp-posting.md).

    2.  The playbook auto-selects a **Review payments** activity.

        You can view the payment details of the invoice. For more information on the payment form, see [Payment terms](../reference/payment-terms.md)

    The invoice processing case is completed with status set to **Paid**.


**Parent Topic:**[Playbook for updating the invoice primary data](../concept/playbooks.md)

