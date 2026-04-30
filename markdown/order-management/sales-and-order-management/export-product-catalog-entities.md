---
title: Export product catalog entities
description: Export product catalog entities as a JSON file and save the file to your local download directory so that it can be imported to another ServiceNow instance.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Export and import product catalog, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Export product catalog entities

Export product catalog entities as a JSON file and save the file to your local download directory so that it can be imported to another ServiceNow instance.

## Before you begin

Role required: product\_catalog\_admin

## About this task

You can export catalog entities in any sequence, but you must import them to a target instance in a certain order. You import base entities \(characteristics and characteristic options, template, and unit of measure\) first, followed by the product catalog, product offerings, and product specifications.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![image.Lists] view.

2.  Navigate to **Export** &gt; **Export Entities**.

    The Export Entities list shows the previous export jobs.

3.  Start an export job by selecting **Export Hierarchy**.

    The **Catalog Export** form opens in the **Export-UI** tab.

4.  In **Entity Type**, select the product catalog entity to be exported from your source instance.

    The product catalog entities include:

    -   Product offering catalog
    -   Unit of Measure
    -   Template
    -   Product specification
    -   Service specification
    -   Resource specification
    -   Product offering - The product offering characteristics, including complex characteristic hierarchies, related specifications, and distribution channel values are also exported with an offering.
    **Note:** During export, note the following:

    -   Versioned entities can be exported in any order. However, if you have many versioned entities that must be exported, the lowest version of the entity must be exported before exporting higher versions of the entity.
    -   Referenced specifications are also exported. For example, when an attribute mapping is exported, the target service specification in that mapping is also exported.
    -   Exceptions and errors are captured when required plugins aren't installed, to help identify issues with drop-down menus that aren't populated with catalog entities.
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

