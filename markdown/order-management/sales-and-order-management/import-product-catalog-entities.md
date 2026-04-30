---
title: Import product catalog entities
description: Import product catalog entities by using the ServiceNow Platform import function.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exporting and importing product catalog entities, Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Import product catalog entities

Import product catalog entities by using the ServiceNow Platform import function.

## Before you begin

Role required: product\_catalog\_admin

## Procedure

1.  Go to the target instance where you want to import the data.

2.  Navigate to **All** &gt; **Product Catalog Management** &gt; **Catalog Import** &gt; **Import**.

    The Catalog Import Data Source window opens.

3.  If the following message appears, select the link to change the application scope to Product Catalog Management.

    ![](../image/e-i-import-edit-message-screen.png)

4.  Attach the JSON file by selecting the **Attachments** \(![](../../../reuse/icons/product-icons/paperclip-fill-24.svg)\) icon.

5.  Select **Choose file** and select the file you want to import.

    **Note:** When you're importing files to a target instance, import the files in a certain order, based on the type of entity:

    1.  Import the exported base entities first, for example characteristics, characteristic options, template, and Unit of Measure \(UOM\).
    2.  Import the product offering catalog if you're exporting product offerings.
    3.  Import product offerings, product specifications, and service specifications.
6.  When the file is uploaded, close the Attachments window.

7.  Under Related Links, select **Load All Records**.

    The data from the imported file loads, and a Progress window opens showing the imported job.

8.  Select **Run Robust Transform**, then select the **Transform** button.

9.  In the Progress window under the Next Steps section, select the imported file name to view the results.

    The imported data is loaded into the correct tables.

10. Navigate to the Entity list view of the entity that you imported to check the imported data.


## What to do next

-   [View export job status](view-export-job-status.md)
-   [View import job status](view-import-job-status.md)

