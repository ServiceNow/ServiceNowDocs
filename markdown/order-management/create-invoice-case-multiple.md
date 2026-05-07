---
title: Dispute multiple invoices against your account using the Business Portal
description: Challenge discrepancies in billing or shipping locations that affect multiple invoices via the Business Portal using the playbook experience.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Business Portal, Use, Sales Customer Relationship Management]
---

# Dispute multiple invoices against your account using the Business Portal

Challenge discrepancies in billing or shipping locations that affect multiple invoices via the Business Portal using the playbook experience.

## Before you begin

Role required: sn\_customerservice.customer

## About this task

This task describes how to create an invoice case using the playbook experience in the Business Portal. The playbook experience enables you to dispute various invoice discrepancies depending on the scope you select. For multiple invoices, you can report billing location and shipping location issues.

Creating invoice cases using the Now Assist panel limits disputes to quantity issues only. For more information, see [Dispute invoice issues using Now Assist Virtual Assistant](../../now-assist-order-mgmt/task/dispute-invoice-issues-now-assist.md).

## Procedure

1.  Log in to the Business Portal.

2.  Navigate to **Requests** &gt; **Submit a request** &gt; **Submit a case** &gt; **Submit an invoice case**.

3.  Create an invoice case.

    1.  On the form, fill in the fields.

<table id="table_kph_1wl_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

The account for which you’re creating the case.

</td></tr><tr><td>

Request source

</td><td>

This option should be set to **Invoice header details, multiple invoices** to dispute multiple invoices against your account.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact for this case.

</td></tr><tr><td>

Priority

</td><td>

The urgency level assigned to the invoice case. The available priorities are:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low \(default\)


</td></tr><tr><td>

Short description

</td><td>

Optional brief description.

</td></tr></tbody>
</table>    2.  Select **Next**.

        An invoice case is created with its state as Draft.

4.  Select the invoices that you want to add to the invoice case.

    1.  Select **Add** on the Add and specify changes form on the invoice case page.

    2.  On the Add invoices to case window, select the invoices for which you want to create a case and select **Add**.

        For a description of the Add invoices to case list view, see [Add invoices to case list](../reference/add-invoices-to-case-list.md).

        Invoice case lines are created corresponding to the invoices that you selected.

    3.  Select the invoice case lines that you want to edit and select **Edit**.

        If you no longer want to change an invoice case line item, select it, select the drop-down button next to **Edit** and select **Delete** to remove it from the list of items to be modified.

    4.  Modify the billing or shipping location, or both, on the Edit item dialog box.

        |Field|Description|
        |-----|-----------|
        |Disputed billing location|The correct billing location if the Invoiced billing location is incorrect.|
        |Disputed shipping location|The correct shipping location if the Invoiced shipping location is incorrect.|

    5.  Select **Update**.

    6.  Select **Next** on the Add and specify changes form.

5.  Verify the requested changes and submit the invoice case on the Review and submit page.

    -   If you need to make more changes, navigate to the required page from the Activities section and repeat the modification process.
    -   If the changes are accurate, select **Submit**.

## Result

The invoice case is created with the invoice case line items corresponding to the invoices you updated, and the state of the invoice case changes to New.

## What to do next

Track the status of your invoice case. For more information, see [View invoice case details in the Business Portal](view-invoice-cases-business-portal.md).

Follow up on your invoice case. For more information, see [Communicate and share supporting documents for an invoice case from Business Portal](manage-invoice-cases-bp.md).

**Related topics**  


[Invoice case details on the Business Portal](../reference/invoice-case-header-list-view.md)

