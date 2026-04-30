---
title: Download the Excel template
description: Download the Microsoft Excel template to create and populate a Microsoft Excel spreadsheet with your existing Operational Technology data.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Easy import, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Download the Excel template

Download the Microsoft Excel template to create and populate a Microsoft Excel spreadsheet with your existing Operational Technology data.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager** &gt; **Import OT Devices - Staging table**.

2.  Right-click the column heading and select **Import** from the list menu.

3.  Select if you want to **Insert** or **Update** records.

    |Template|Description|
    |--------|-----------|
    |Insert|Use this template to add new records to a table.|
    |Update|Use this template to change values within existing records in a table. This template contains one row for each record in the list. The current list filter determines what records the template contains.|

    ![Download the Excel template.](../image/import-excel-template.png)

4.  Clear the **Include all fields in the template** check box to include only the columns that appear in the list in the template.

    Certain fields in the table are updated by system processes and you cannot import values into them. An example is the **Created by** field, which is populated during import with the logged-in user who performs the import.

    Leave this check box selected to include all columns from the table in the template, even those columns that are hidden in the list.

5.  Select **Create Excel template**.

6.  In the Export Complete page, select **Download** to download the Microsoft Excel spreadsheet.


## What to do next

Open the spreadsheet using your preferred application.

**Note:**

The template contains a **Directions** tab describing how to use the template.

**Parent Topic:**[Easy import](../concept/easy-import.md)

