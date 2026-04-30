---
title: Using Playbook in Accounts Payable Operations
description: Configure a playbook and visualize the step-by-step actions performed by an Accounts Payable specialist while processing an invoice.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Playbook for updating the invoice primary data, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Using Playbook in Accounts Payable Operations

Configure a playbook and visualize the step-by-step actions performed by an Accounts Payable specialist while processing an invoice.

## Before you begin

Role required: Accounts Payable specialist

## Procedure

1.  Navigate to **Source-to-Pay Workspace** &gt; **All** &gt; **Accounts Payable Operations**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

    A list of options within the workspace is displayed.

3.  Select **Invoices &gt;****All invoices.**

    You can create an invoice manually. For more information on invoices, see [Work with invoices](../concept/work-with-invoices.md).

4.  Select **View Invoice processing case**.

    A playbook is available for the Invoice processing case. You can view the stages and activities of Invoice processing in the **Playbook** tab.

5.  Select **Validate invoice**.

    The invoice opens and you must verify the invoice details. The **Classify documents** swim lane appears and prompts you to verify the invoice classification. The Classify documents swim lane appears if the document classification skill is activated. For more information on document classification, see [Configure Accounts payable document classification skill](config-doc-classification-skill-apo.md).

    1.  Select the **Review header** details.

        Review the invoice header details and make any required changes.

    2.  Select **Save**.

    3.  Select **Continue** to move to the next activity in the playbook.

    4.  Select the **Review invoice lines** activity.

        Manually review the invoice lines associated with the invoice processing case.

    5.  When tax integration is disabled, you can create tax lines from related list of invoice lines or invoice case.

    6.  Select **Add new invoice lines** to create invoice lines.

    7.  Select **Continue** to move to the next activity in the playbook.

    8.  Select **Add tax**.

        The **Add tax lines to the invoice** pop-up box displays. You can choose to add tax lines associated with invoice line. For more information on the fields of tax lines, see [Invoice Tax lines fields](../reference/tax-lines.md).

    9.  Select an **Invoice line** in which you would like to add the tax lines.

    10. Select the **Apply to all invoice lines** check box if you want to add the tax lines to all the invoice lines.

    11. In the **Enter tax details** area, perform the following steps.

    12. Select the **Tax type** to be associated with the invoice line.

    13. Enter the **Supplier tax rate** details.

    14. Enter the **Supplier tax** details.

    15. Select **Add tax**.

        The tax lines are added to the invoice line.

    16. Select **Submit invoice**.

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

7.  Select the **Map invoice lines** card.

    If the invoice is a PO invoice or credit memo invoice of type PO and the invoice doesn't run into a matching error, then the **Map invoice lines** card is set to auto-complete. However, if the invoice is of type Non-PO invoice or a credit memo invoice of type Non-PO, the stage is skipped.

    1.  Verify the **Map invoice lines** card.

    2.  Verify the **Verify Purchase Order** card.

        Verify the purchase order details associated with an invoice.

    3.  You can edit the changes to the purchase order form and select **Update**.

    4.  Select **Continue** after you save the changes.

    5.  In the **Review PO line mapping** card, review the PO lines associated with the purchase order to identify the lines that is mapped to the invoice line.

    6.  You can edit the invoice lines and match the invoice lines with the corresponding purchase order lines.

    The swim lane moves to **Review compliance**. For more details on tax compliance, see [Tax integration in playbook](tax-integration-in-playbook.md).

8.  Select **Review exceptions**.

    The list of exceptions raised for the invoice is listed. For more information on exceptions, see [Invoice exceptions](../concept/work-with-invoice-exceptions.md). This stage is set to auto-complete if the invoice doesn't run into exceptions.

    1.  Review the exceptions generated for the invoice using the **Resolve exceptions** card, and resolve exceptions if any.

    2.  Select an **Check exceptions** action to re-evaluate the exceptions.

        For Valid coding required exception, the exception engine is trained to provide recommendations from Agentic AI. The status of the exception is set to **Review needed**.

    3.  The APS manually reviews and verifies the suggestion by selecting **Accept suggestion** and **Save**.

    4.  After all the exceptions are resolved in an invoice line, the status of the exception changes to **Complete**.

    5.  Select **Review exception tasks** to resolve exception tasks if any.

    6.  Select **Create new task** to create an exception task.

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

