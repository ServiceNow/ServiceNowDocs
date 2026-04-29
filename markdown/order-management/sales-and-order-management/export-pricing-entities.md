---
title: Export pricing entities
description: Export pricing entities as a JSON file and save the file to your local download directory so that it can be imported to another ServiceNow instance.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exporting and importing pricing entities, Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Export pricing entities

Export pricing entities as a JSON file and save the file to your local download directory so that it can be imported to another ServiceNow instance.

## Before you begin

Before you export a new version of a pricing matrix that has an updated decision table, ask your admin to export the system-generated update set that includes the updated decision table, to the target instance.

Role required: sn\_csm\_pricing\_pricelist\_administrator

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Export** &gt; **Export Entities**.

    The Export Entities list shows the previous export jobs.

3.  Start an export job by selecting **Export Hierarchy**.

    The **Export Entities** form opens in the **Export-UI** tab.

4.  In **Entity Type**, select the pricing entity to be exported from your source instance.

    The pricing entities include: Rule Matrix, Price List, Price List Line, Attribute Adjustment, Cost Book, and Cost Book Line.

5.  Select the items that you want to export and then select **Export**.

    **Note:**

    -   Entities such as pricing matrices may have specific versions. Be sure to select a specific version of the entity to be exported and import that version to the target instance.
    -   If you have new versions of pricing matrices with updated decision tables that reference new product offerings, ask your admin to export the system-generated update set that includes the updated decision tables.
6.  Give the export job a file name and description and select **Submit**.

    The export process begins and a message displays the catalog export ID.

7.  Find and view the exported JSON file by refreshing the **Export Entities** list and selecting the export job.

    The exported file appears in the **Attachments** pane.

8.  Select the attachment to download the exported file.

    The file is downloaded as a JSON file and saved to your local download directory.


## What to do next

[Import pricing entities](import-pricing-entities.md).

