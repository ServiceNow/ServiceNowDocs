---
title: Export product catalog entities
description: Export product catalog entities as a JSON file and save the file to your local download directory so that it can be imported to another ServiceNow instance.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exporting and importing product catalog entities, Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Export product catalog entities

Export product catalog entities as a JSON file and save the file to your local download directory so that it can be imported to another ServiceNow instance.

## Before you begin

After upgrading to the Yokohama release, check with your administrator that the **Code** field values are available for the main product catalog entities in your source and target instances. For more information, see [Add Code field values to catalog entities after upgrading](run-fix-script-sched-job-export.md).

Role required: product\_catalog\_admin

## About this task

You can export catalog entities in any sequence, but they must be imported to a target instance in a certain order. You import base entities \(characteristics and characteristic options, template, and unit of measure\) first, followed by the product catalog, product offerings, and product specifications.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Export** &gt; **Export Entities**.

    The Export Entities list shows the previous export jobs.

3.  Start an export job by selecting **Export Hierarchy**.

    The **Catalog Export** form opens in the **Export-UI** tab.

4.  In **Entity Type**, select the product catalog entity to be exported from your source instance.

    The product catalog entities are: Product Offering, Product Specification, Service Specification, Product Offering Catalog, Characteristic, Unit of Measure, and Template.

5.  Select the items that you want to export and select **Export**.

6.  Give the export job a file name and description, then select **Submit**.

    The export process begins and a message displays the catalog export ID.

7.  Find and view the exported JSON file by refreshing the **Export Entities** list and selecting the export job.

    The exported file appears in the **Attachments** pane.

    ![The Catalog Export Request page with an exported JSON file in the Attachments pane.](../image/e-i-attachment-screen.png)

8.  Select the attachment to download the exported file.

    The file is downloaded as a JSON file and saved to your local download directory.


## What to do next

-   [Import product catalog entities](import-product-catalog-entities.md)
-   [View export job status](view-export-job-status.md)

