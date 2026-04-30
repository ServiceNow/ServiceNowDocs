---
title: Run the fix script for Accounts Payable Operations
description: Run the fix script for successful installation of Accounts Payable Operations.
locale: en-US
release: xanadu
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Run the fix script for Accounts Payable Operations

Run the fix script for successful installation of Accounts Payable Operations.

## Before you begin

-   Install`Accounts Payable Invoice Processing` plugin.
-   Run fix script for Insufficient funds \(header amount variance\) exception to work.
-   Set the **Application scope** to **Source-to-Pay Common Architecture**.
-   All the invoices associated with purchase order must be available in the system for Insufficient funds \(header amount variance\) exception to work.
-   Ensure that invoices have same currency as that of associated with purchase order currency for exception to run successfully.
-   You can run the fix script in batches by adding the command `gr.setLimit(100000)` after the command line `gr.addEncodedQuery("in_process_invoiced_amountISEMPTY"`. Run the script in batches of 100k or 200k.
-   Ensure POs are updated with **In process invoice amount**and **Invoice amount** fields.

    **Note:** If fix script is not executed for POs, then Insufficient funds \(header amount variance\) exception associated with a invoice will not work.


Role required: maint

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix scripts**.

2.  Click **New**.

    A new Fix script record opens.

3.  In the **Name** field, enter name as `Update PO Invoiced Amounts for APO`.

4.  In the **Script** field, copy paste the below mentioned script.

5.  ```
updatePOInvoicedAmounts();

function updatePOInvoicedAmounts() {
    var sessionCurrency = new sn_currency.GlideCurrencyConfig().getSessionCurrency();
    var gr = new GlideRecord("sn_shop_purchase_order");
    gr.addEncodedQuery('in_process_invoiced_amountISEMPTY');
    gr.query();
    while (gr.next()) {
        var poSysID = gr.getValue('sys_id');
        var inProcessInvoiceAmt = getInProcessInvoicedAmount(poSysID);
        var invoicedAmount = getInvoicedAmount(poSysID);
        var poCurrency = !gs.nil(gr.total_amount) ? gr.total_amount.currency : sessionCurrency;
        var amtUpdated = false;
        if (!gs.nil(inProcessInvoiceAmt)) {
            inProcessInvoiceAmt = poCurrency + ';' + inProcessInvoiceAmt;
            gr.getElement('in_process_invoiced_amount').setDisplayValue(inProcessInvoiceAmt);
            amtUpdated = true;
        }
        if (!gs.nil(invoicedAmount)) {
            invoicedAmount = poCurrency + ';' + invoicedAmount;
            gr.getElement('invoiced_amount').setDisplayValue(invoicedAmount);
            amtUpdated = true;
        }
        if (amtUpdated)
            gr.update();
    }
}
 
function getInProcessInvoicedAmount(poSysId) {
    var query = 'invoice_amountISNOTEMPTY,^invoice_amount.amount!=0^stateINpo_matching_completed,exceptions_found,no_exceptions_found,pending_approval,approval_recalled,approved';
    var gr = new GlideAggregate('sn_shop_invoice');
    gr.addNotNullQuery('purchase_order');
    gr.addQuery('purchase_order', poSysId);
    gr.addEncodedQuery(query);
    gr.addAggregate('SUM', 'invoice_amount.amount');
    gr.groupBy('purchase_order');
    gr.query();
    if (gr.next()) {
        var inProcessInvoicedAmt = gr.getAggregate('SUM', 'invoice_amount.amount');
        return inProcessInvoicedAmt;
    }
    return 0;
}
 
function getInvoicedAmount(poSysId) {
    var query = 'invoice_amountISNOTEMPTY,^invoice_amount.amount!=0^stateINpending_payment,paid';
    var gr = new GlideAggregate('sn_shop_invoice');
    gr.addNotNullQuery('purchase_order');
    gr.addQuery('purchase_order', poSysId);
    gr.addEncodedQuery(query);
    gr.addAggregate('SUM', 'invoice_amount.amount');
    gr.groupBy('purchase_order');
    gr.query();
    if (gr.next()) {
        var invoicedAmt = gr.getAggregate('SUM', 'invoice_amount.amount');
        return invoicedAmt;
    }
    return 0;
}
```

6.  Click **Submit**.

7.  In the fix script list view, search and select `Update PO Invoiced Amounts for APO` fix script.

    The `Update PO Invoiced Amounts for APO` fix script opens.

8.  Select **Run Fix Script**.

    A pop-up window appears with options to **Cancel**, **Proceed**, and **Proceed in Background**.

9.  Click **Proceed in Background**.


