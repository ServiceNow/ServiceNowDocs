---
title: Import pricing entities
description: Import pricing entities to a target instance by using the ServiceNow Platform import function.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Pricing entities, Pricing Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Import pricing entities

Import pricing entities to a target instance by using the ServiceNow Platform import function.

## Before you begin

Before you start, check your target instance and verify that certain required entities have been imported. For example, the product offerings and product offering catalogs associated with your pricing entities must have been previously imported to your target instance. Similarly, if you're importing price list lines or cost book lines, the price list or cost book for those lines must have been previously imported to your target instance. And if you're importing a new price list matrix, your admin must have imported the associated decision table to your target instance in a system-generated update set.

Role required: sn\_csm\_pricing\_pricelist\_administrator

## Procedure

1.  Go to the target instance where you want to import the pricing data.

2.  Start the import process.

    -   To import pricing entities, navigate to **All** &gt; **Pricing** &gt; **Export/Import** &gt; **Import**.
    -   To import context rules, navigate to **All** &gt; **Context Rule Management** &gt; **Import**.
    The record for the import data source opens.

3.  Attach the JSON file by selecting the **Attachments** ![](../../../reuse/icons/product-icons/paperclip-fill-24.svg) icon in the header bar.

    The Import Data Source pop-up opens.

4.  Select **Choose file** and select the JSON file you want to import.

5.  When the file is uploaded, close the Attachments pop-up.

6.  Under Related Links, select **Load All Records**.

    The data from the imported file loads, and a Progress bar opens showing the imported job. The imported data is loaded into the import set temporary table sn\_csm\_pricing\_import\_data\_source or sn\_csm\_ctxrul\_mgt\_import\_data\_source if you're importing context rules.

    **Note:** During the import of a pricing matrix on the target instance, an import post script associates the reference entities in the decision table that was imported in an update set to the appropriate pricing matrix.

7.  In the Next steps section, select **Run Robust Transform**, then select **Transform**.

    The progress bar shows the transform status. When the transform is complete, the imported data is loaded into the appropriate pricing tables.

8.  In the Next steps section, select the import set link to view the resulting import set.

    The imported data is available in the appropriate tables.

9.  In the Import Set record, open the **Import Log** tab to check for any errors and verify that the transform was completed successfully.


## What to do next

Certain imported pricing entities, such as price lists or cost books, are in the draft state in the target instance. To make the imported price list or cost book active in the instance, publish them.

