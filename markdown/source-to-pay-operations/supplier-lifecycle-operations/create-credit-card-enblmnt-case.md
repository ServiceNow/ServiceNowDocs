---
title: Create a case for supplier credit card enablement
description: Create a supplier case to request for the credit card information from a supplier.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-11-19"
reading_time_minutes: 1
breadcrumb: [Using Supplier Payment Optimization, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create a case for supplier credit card enablement

Create a supplier case to request for the credit card information from a supplier.

## Before you begin

Role required: sn\_slm.manager, sn\_slm.owner, or sn\_slm.admin

**Note:** The sn\_slm.owner role can create cases only for the suppliers they own.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  On the home page, do one of the following:

    -   Under Quick actions, select **Create case**.
    -   Under Quick actions, select **Manage my suppliers** and do the following:
        1.  Select the link to the supplier name under the Legal name column.
        2.  From the **Create** drop-down list, select **Supplier case**.
3.  On the Create New Supplier Case form, fill in the fields.

    In the **Case type** field, select **Credit card enablement**.

    ![Credit card enablement case form](../image/create-credit-card-case.png)

    For more information about the form fields and descriptions, see [Create New Supplier Case form](../reference/new-supplier-case.md).

4.  Select **Save**.

    The case is created in Draft state.

5.  Select **Submit case**.


## Result

The case is created in the **Open** state.

## What to do next

After you submit the case, a playbook for this supplier case opens.

For more information, see [Supplier credit card enablement playbook](../concept/credit-card-enblmnt-playbook.md).

**Parent Topic:**[Using Supplier Payment Optimization](../concept/using-supp-payment-opt.md)

**Related topics**  


[Using Supplier Payment Optimization](../concept/using-supp-payment-opt.md)

[View the Payment Optimization dashboard](view-payment-opt-db.md)

[Case playbook for specific supplier case types](../concept/gen-playbook-cases.md)

[Estimate savings using the saving estimator tool](estimate-savings.md)

