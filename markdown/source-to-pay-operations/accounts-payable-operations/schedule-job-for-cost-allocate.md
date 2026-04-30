---
title: Run scheduled job for cost allocation
description: Run a scheduled job to copy cost allocations from invoice line to purchase order line when upgrading Accounts Payable Operations from lower to higher version.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Post upgrade tasks for APO, Upgrade Accounts Payable Operations, Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Run scheduled job for cost allocation

Run a scheduled job to copy cost allocations from invoice line to purchase order line when upgrading Accounts Payable Operations from lower to higher version.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Scheduled Jobs** &gt; **Update Cost Allocation for the invoice**.

2.  Select the **Active** check box.

3.  In the script, add the following encodedQuery:

    ```
    var encodedQuery = sn_shop.InvoiceLine.ORDER_LINE + 'ISNOTEMPTY^' + sn_shop.InvoiceLine.INVOICE + '.' + sn_shop.Invoice.STATE + 'IN' + sn_shop.Invoice.STATE_DRAFT + ',' + sn_shop.Invoice.STATE_PO_MAPPING_ERROR + "," + sn_shop.Invoice.STATE_SUSPECTED_DUPLICATE;
    ```

4.  Select **Save** and **Execute Now**.

    During the upgrade Accounts Payable Operations, cost allocation is auto-updated when purchase order lines are mapped to invoice lines.


