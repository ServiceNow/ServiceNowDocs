---
title: Import your equipment model data using the data source and scheduled import
description: After you complete your Microsoft Excel spreadsheet with your equipment model data, import it into the ServiceNow AI Platform by using the data source and scheduled import.
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Importing equipment model data, Configure, Industrial Process Manager, Operational Technology]
---

# Import your equipment model data using the data source and scheduled import

After you complete your Microsoft Excel spreadsheet with your equipment model data, import it into the ServiceNow AI Platform by using the data source and scheduled import.

## Before you begin

Before you perform this process, you must prepare a Microsoft Excel spreadsheet for import. To learn more, see [Populating your Microsoft Excel spreadsheet with equipment model data](../concept/populate-excel-spreadsheet-with-isa-equipment-model-data.md).

Role required: cmdb\_inst\_admin, import\_admin

## About this task

By running this process, you create unique Equipment Model Entity CI class records in the Configuration Management Database \(CMDB\) for the equipment model records that are included in your spreadsheet.

## Procedure

1.  Navigate to **All** &gt; **Equipment Model - ISA** &gt; **Import Equip. Model - Data Source**.

2.  In the **SG Equipment Model** data source record, attach the Microsoft Excel spreadsheet that you created:

    1.  Select **Manage Attachments**.
    2.  In the Attachments dialog box, select **Choose File**.
    3.  Select the Microsoft Excel spreadsheet that you created, and then close the Attachments dialog box.
    4.  After attaching the spreadsheet, select the **Load All Records** related link to load all records from the spreadsheet to the import table. Once the operation is complete, you should see the following confirmation message with the **Success** completion code if the data is loaded without any errors.![Confirmation message that says State Complete and Completion Code Success if the record loading completed without any errors.](../image/load-records-success.png)
    5.  In the confirmation message, select the **Run Robust Transform** related link.
    6.  Select **Transform**. If the import is successful, you should see the following confirmation message with the **Success** completion code.![Confirmation message that says State Complete and Completion Code Success if the import is completed without any errors.](../image/run-rte-success.png)

**Parent Topic:**[Importing equipment model data](../concept/importing-isa95-equipment-model-etl.md)

