---
title: Import product catalog entities
description: Import product catalog entities by using the ServiceNow Platform import function.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exporting and importing product catalog entities, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Import product catalog entities

Import product catalog entities by using the ServiceNow Platform import function.

## Before you begin

The application scope must be set to Product Catalog Management core. You can change the application scope using the application picker ![](../../../reuse/icons/product-icons/globe-outline-24.svg) in the Unified Navigation bar.

Role required: product\_catalog\_admin

## About this task

You import certain product catalog entities to your target instance in the following order:

-   Import the exported base entities.
-   Import the product offering catalog if you're exporting product offerings.
-   Import product offerings and product specifications.

## Procedure

1.  Go to the target instance where you want to import the data.

2.  Navigate to **All** &gt; **Product Catalog Management** &gt; **Catalog Import** &gt; **Import**.

    The Catalog Import Data Source window opens.

3.  Attach the JSON file by selecting the **Attachments** ![](../../../reuse/icons/product-icons/paperclip-fill-24.svg) icon.

4.  Select **Choose file** and select the file you want to import.

    Versioned entities can be imported in any order. However, if you have many versioned entities that must be imported, the lowest version of the entity must be imported before higher versions of the entity.

    **Note:** When you're importing files to a target instance, import the files in a certain order, based on the type of entity:

    1.  Import the exported base entities first, for example characteristics, characteristic options, template, and Unit of Measure \(UOM\).
    2.  Import the product offering catalog if you're exporting product offerings.
    3.  Import service specifications, product specifications, and then product offerings.
5.  When the file is uploaded, close the Attachments window.

6.  Under Related Links, select **Load All Records**.

    The data from the imported file loads, and a Progress window opens showing the imported job.

7.  Select **Run Robust Transform**, then select the **Transform** button.

8.  In the Progress window under the Next Steps section, select the imported file name to view the results.

    The imported data is loaded into the correct tables.

9.  Navigate to the Entity list view of the entity that you imported to check the imported data.


## What to do next

-   [View export job status](view-export-job-status.md)
-   [View import job status](view-import-job-status.md)

