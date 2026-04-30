---
title: Bypass an invoice exception
description: Bypass an invoice exception if you find that it is not applicable to the invoice.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work on an invoice exception, Invoice exceptions, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Bypass an invoice exception

Bypass an invoice exception if you find that it is not applicable to the invoice.

## Before you begin

Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_apm.admin

## About this task

The **Bypass exception** option is available for an exception only if the **Allow bypass** option is selected for that exception on the Invoice exception definition form. For more information, see [Invoice exception definition form](../reference/invoice-exception-definition-form.md).

## Procedure

1.  Navigate to **All** &gt; **Accounts Payable Operations** &gt; **Accounts Payable Workspace**.

2.  Select the list icon \(![List icon](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Do one of the following:

<table id="table_crv_zwr_2wb"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

View exceptions from the List page

</td><td>

1.  Do one of the following:
    -   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice exceptions**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice exceptions**.
2.  Select the link to the invoice exception under the Number column to open the exception and view its details.


</td></tr><tr><td>

View exceptions from an invoice processing case

</td><td>

1.  Do one of the following:
    -   Navigate to **Lists** &gt; **My Work** &gt; **My open invoice processing cases**.
    -   Navigate to **Lists** &gt; **All Work** &gt; **All open invoice processing cases**.
2.  Open an invoice processing case that contains exceptions.

**Note:** If an invoice processing case contains exceptions, the following message is shown at the top of the case:

`One or more exceptions have been identified on this invoice. Review the identified invoice exceptions and take appropriate action to resolve them.`

3.  Select the **Exceptions** tab.
4.  Select the link to the invoice exception under the Number column to open the exception and view its details.


</td></tr></tbody>
</table>4.  Select **Bypass exception**.

5.  In the Bypass reason dialog box, enter a reason for bypassing the invoice exception and select **OK**.


## Result

The invoice exception is bypassed and its status changes to Closed-bypassed.

After you bypass an exception, the exception engine re-runs automatically.

**Parent Topic:**[Work on an invoice exception](work-invoice-exception-case.md)

