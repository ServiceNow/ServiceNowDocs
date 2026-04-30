---
title: Allocate costs using distribution set
description: Define a distribution set to split cost allocations automatically for invoice lines with allocation type as cost center or general ledger account.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 2
breadcrumb: [Invoice cost allocation, Create an invoice manually, Work with invoices, Using Accounts Payable Invoice Processing, Use, Accounts Payable Operations, Finance and Supply Chain]
---

# Allocate costs using distribution set

Define a distribution set to split cost allocations automatically for invoice lines with allocation type as cost center or general ledger account.

## Before you begin

Role required: sn\_ap\_apm.admin

## Procedure

1.  Navigate to **Source-to-Pay workspace** &gt; **All** &gt; **Accounts Payable Operations** &gt; **Distribution Sets**.

2.  Select **New**.

    The distribution set form view appears. For more information on the form, see [Distribution set form](../reference/distribution-set-form.md)

3.  Select the **Template** check box if you want the distribution set to be applied as a template to the cost allocation record.

4.  Select **Save**.

    The **Convert Template** pop-up appears. You’ll be prompted with a message "Converting this distribution setup to a template removes all allocation percentage from the distribution line. This action can’t be undone".

5.  Select **Create template**.

    For distribution set with template, if there’s distribution lines created, by default, the distribution set is active. For non-template, if the allocation percentage doesn't sum upto 100%, then the distribution set remains inactive else it is saved as active.

6.  Select **Submit**.

    The distribution set is created.![Distribution set](../image/distribution-set-ws.png)

7.  Select the distribution set for which you want to create distribution lines.

    1.  Select **New**.

        A distribution line form appears. For more information on the distribution line form, see [Distribution set form](../reference/distribution-set-form.md).![Distribution line](../image/distribution-line-record.png)

    2.  Allocate the cost and split the invoice line amount by cost center or general ledger account.

    3.  Select **Submit**.

        After a distribution line is submitted, it’s applicable for new invoices only and unavailable for existing invoices.

8.  To apply distribution set manually for an invoice line, select **Invoice line**&gt; **Cost allocation**&gt; **New**.

    Create a New Invoice cost allocation form appears. You can choose **Allocation type** as Distribution set. For more information on the form, see [Create invoice cost allocation form](../reference/create-invoice-cost-allocation-form.md).![Distribution set in invoice line](../image/distribution-set-cost-alloc.png)

    If a distribution set is created for cost center, then for subsequent cost allocation, the allocation type is cost center by default.

    If a distribution set is created for general ledger account, then for subsequent cost allocation, the allocation type is general ledger account by default.

9.  Select **Save**.


## Result

Distribution set automates cost allocations. Each cost allocation record displays the source whether it’s entered manually, derived from a purchase order, or associated with a specific distribution set number confirming complete traceability.

**Parent Topic:**[Invoice cost allocation](../concept/invoice-line-cost-allocation.md)

**Related topics**  


[Create invoice cost allocation form](../reference/create-invoice-cost-allocation-form.md)

