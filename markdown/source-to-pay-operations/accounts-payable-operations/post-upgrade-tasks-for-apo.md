---
title: Post upgrade tasks for APO
description: Review and complete required post-upgrade tasks after upgrading Accounts Payable Operations.Complete post-upgrade tasks after upgrading Accounts Payable Operations, including upgrading copied use cases to the latest Document Intelligence model.The invoice and invoice line tables are restructured in the Xanadu release.When you update the instance from Washington DC to Australia release, you must manually run the glide fix to update the invoice and invoice line tables to their respective base tables.Run a scheduled job to copy cost allocations from invoice line to purchase order line when upgrading Accounts Payable Operations from lower to higher version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/post-upgrade-tasks-for-apo.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [APO, Accounts Payable Operations, upgrade, migration, invoice automation, APO, Accounts Payable Operations, DocIntel, Document Intelligence, AP case, integration, upgrade, migration, APO, Accounts Payable Operations, invoice management, invoice automation, AP automation, APO, Accounts Payable Operations, invoice management, upgrade, migration, APO, Accounts Payable Operations, invoice management, purchase order, PO, cost allocation, GL coding, admin]
breadcrumb: [Upgrade Accounts Payable Operations, Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Post upgrade tasks for APO

Review and complete required post-upgrade tasks after upgrading Accounts Payable Operations.

## Upgrade configuration for Accounts Payable Operations integration with Document Intelligence

Complete post-upgrade tasks after upgrading Accounts Payable Operations, including upgrading copied use cases to the latest Document Intelligence model.

### Before you begin

Role required: admin

Install the Document Intelligence for Accounts Payable Operations Content Pack from the ServiceNow® Store.

### Procedure

1.  Select the DO NOT USE- Invoice processing V7 use case as source.

2.  Navigate to **All** &gt; **Document Data Extraction Administration** &gt; **Use Cases**.

3.  Search for DO NOT USE- Invoice processing V7 and create a duplicate copy using the \[Omitted image "duplicate-di-usecase.png"\] Alt text: duplicate icon icon.

4.  Save the copied use case.

    Use the copied use case in flows and task definitions.

5.  To upgrade the copied use case to the latest Document Intelligence model, perform the following steps:

    1.  Navigate to **All** &gt; **Fix Scripts**.

    2.  Search for Update DocIntel base\_trained\_model and select **Run Fix Script**.

        The existing copied use case is updated to the latest DI base model.


## Restructured Invoice table

The invoice and invoice line tables are restructured in the Xanadu release.

Before Washington DC release, invoice and invoice line tables were standalone tables. With Xanadu release, the following changes are done:

-   The invoice table \[sn\_shop\_invoice\] extends the base invoice table \[sn\_fin\_base\_invoice\].
-   The invoice line table \[sn\_shop\_invoice\_line\] extends the base invoice line table \[sn\_fin\_base\_invoice\_line\].

\[Omitted image "invoice-reparenting.png"\] Alt text: Invoice table structure explaining the invoice table and invoice table line extending to base tables.

After you upgrade from Washington DC to Australia release, verify that your existing invoice and invoice line data has been migrated correctly. If you notice that your invoice and invoice line tables didn’t migrate properly, use the [Now Support Portal](https://support.servicenow.com/now) to raise a case with the Technical Support team.

## Run a glide fix script to migrate existing data

When you update the instance from Washington DC to Australia release, you must manually run the glide fix to update the invoice and invoice line tables to their respective base tables.

### Before you begin

Role required: maint

### Procedure

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


## Run scheduled job for cost allocation

Run a scheduled job to copy cost allocations from invoice line to purchase order line when upgrading Accounts Payable Operations from lower to higher version.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Scheduled Jobs** &gt; **Update Cost Allocation for the invoice**.

2.  Select the **Active** check box.

3.  In the script, add the following encodedQuery:

    ```
    var encodedQuery = sn_shop.InvoiceLine.ORDER_LINE + 'ISNOTEMPTY^' + sn_shop.InvoiceLine.INVOICE + '.' + sn_shop.Invoice.STATE + 'IN' + sn_shop.Invoice.STATE_DRAFT + ',' + sn_shop.Invoice.STATE_PO_MAPPING_ERROR + "," + sn_shop.Invoice.STATE_SUSPECTED_DUPLICATE;
    ```

4.  Select **Save** and **Execute Now**.

    During the upgrade Accounts Payable Operations, cost allocation is auto-updated when purchase order lines are mapped to invoice lines.


