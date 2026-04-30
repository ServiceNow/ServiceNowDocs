---
title: Export the configuration BOM to a CSV file
description: Export the configuration bill of materials \(BOM\) to a customizable CSV file before the quote is finalized.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-10-27"
reading_time_minutes: 1
breadcrumb: [ProductList.Type options: Accessory and Component, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Export the configuration BOM to a CSV file

Export the configuration bill of materials \(BOM\) to a customizable CSV file before the quote is finalized.

## Before you begin

Role required: Admin

## Enhanced shopping cart with CSV export

ServiceNow CPQ lets you export the configuration bill of materials \(BOM\) before the quote is finalized by exporting the BOM to a CSV file. The BOM UI has been enhanced to enable on-screen manipulation of fields, such as resizing of columns, pinning of fields, and hiding of fields.

## Procedure

1.  In your blueprint, navigate to Layouts.

2.  In your layout, scroll to Product List and select Product List Settings.![Product List](../images/cpq-product-list.png)

3.  In Settings, scroll to Raw Value and insert the following code block:

    ```
    "advanced": {
        "export": true
    }
    ```

    `advanced` enables the enhanced shopping cart, and `export` enables the BOM export. `advanced` must be enabled to use `export`. The final code block should resemble the following:

    ```
    {
      "location": "bottom",
      "type": "sales",
      "hierarchyColumn": "displayName",
      "advanced": {
        "export": true
      }
    }  
    ```

4.  When the blueprint is enabled, deploy it and launch the configurator experience.

    In the UI, you see two new icons on the far right of the product list:

    ![Product List](../images/cpq-product-list-new-items.png)

    The icon to the left of **Export** lets you manipulate the columns via the UI, such as hiding and pinning certain columns. You can also manually resize columns as you would in a spreadsheet.

    The **Export** icon lets you export the current BOM to a CSV file. This will export all contents that are visible in the BOM at the time of export.

    **Note:** The process requires the Quoting tool.


