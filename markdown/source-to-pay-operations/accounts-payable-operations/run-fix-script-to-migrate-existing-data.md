---
title: Run a glide fix script to migrate existing data
description: When you update the instance from Washington DC to Yokohama release, you must manually run the glide fix to update the invoice and invoice line tables to their respective base tables.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Post upgrade tasks for APO, Upgrade Accounts Payable Operations, Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configuring Accounts Payable Operations, Accounts Payable Operations, Finance and Supply Chain]
---

# Run a glide fix script to migrate existing data

When you update the instance from Washington DC to Yokohama release, you must manually run the glide fix to update the invoice and invoice line tables to their respective base tables.

## Before you begin

Role required: maint

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Select **New**.

    A new Fix script record opens.

3.  Open the fix script record.

4.  Enter **Name** as re-parent invoice table.

5.  Deselect the **Record for rollback** check box.

6.  In the **Script** field, add the following code for the invoice line:

    ```
    (function() {
                const invoiceLinetableToReparent = "sn_shop_invoice_line";
                const invoiceLineNewExtends = "sn_fin_base_invoice_line";
                const oldExtends = "";
    var invoiceLineGr = new GlideRecord("sys_db_object");
            invoiceLineGr.get("name", invoiceLinetableToReparent);
            if(invoiceLineGr.super_class.name == invoiceLineNewExtends) {
                gs.info("{0} table already reparented to {1}. No reparenting required.", invoiceLinetableToReparent, invoiceLineNewExtends);
                return;
            }
    try {
                
                var invoiceLinetpc = new GlideTableParentChange(invoiceLinetableToReparent);
                var reparentInvoiceLineResult = invoiceLinetpc.change(oldExtends, invoiceLineNewExtends);
    
            } catch (e) {
                gs.warn("Table parent change for sn_shop_invoice_line did not complete. Error: {0}", e);
            } 
    })();
    
    ```

7.  In the **Script** field, add the following code for invoice:

    ```
     (function() {
            const invoiceTableToReparent = "sn_shop_invoice";
            const oldExtends = "";
            const invoiceNewExtends = "sn_fin_base_invoice";
    var invoiceGr = new GlideRecord("sys_db_object");
            invoiceGr.get("name", invoiceTableToReparent);
            if(invoiceGr.super_class.name == invoiceNewExtends){
                gs.info("{0} table already reparented to {1}. No reparenting required.", invoiceTableToReparent, invoiceNewExtends);
                return;
            }
     try {
                var tpc = new GlideTableParentChange(invoiceTableToReparent);
                var reparentResult = tpc.change(oldExtends, invoiceNewExtends);
            } catch (e) {
                gs.warn("Table parent change for sn_shop_invoice did not complete. Error: {0}", e);
            } 
     })();
    
    ```

8.  Select**Save**.

9.  Select **Submit**.

    The Fix script is created.

10. Select **Run Fix Script**.

    The parent invoice and invoice line tables are changed to respective base tables.


