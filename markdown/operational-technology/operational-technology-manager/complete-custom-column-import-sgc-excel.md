---
title: Complete the custom column import
description: Upload an updated Microsoft Excel spreadsheet to populate the custom column and complete the import.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/operational-technology-manager/complete-custom-column-import-sgc-excel.html
release: brazil
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 1
breadcrumb: [Add a custom column to the staging table, Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Complete the custom column import

Upload an updated Microsoft Excel spreadsheet to populate the custom column and complete the import.

## Before you begin

Role required: ot\_excel\_import\_user

## Procedure

1.  Create a record in the OT Excel SGC Import Task table.

2.  From the record, download the attached **sg\_ot\_excel\_staging.xlsx** file.

3.  In the Microsoft Excel file, add your custom column and fill in the data for your configuration item \(CI\) records.

4.  Upload the updated Excel file to the OT Excel SGC Import Task record.

    For more information about completing the custom column import with an import task and validating the imported staging records, see [Create an import task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/create-import-task-excel-sgc.md) and [Validate imported staging records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/run-validations.md).


## What to do next

Update the column mapping script with the custom column. For more information, see [Update the column mapping script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/update-column-mapping-script-sgc-excel.md).

**Parent Topic:**[Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/add-custom-column-staging-table.md)

