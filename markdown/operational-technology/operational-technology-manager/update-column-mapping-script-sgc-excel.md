---
title: Update the column mapping script
description: Update the column mapping script with the custom column.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/operational-technology-manager/update-column-mapping-script-sgc-excel.html
release: brazil
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 1
breadcrumb: [Add a custom column to the staging table, Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Update the column mapping script

Update the column mapping script with the custom column.

## Before you begin

Role required: ot\_excel\_import\_user

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Import OT Devices - Script Includes**.

2.  Select the **SGOTAssetImportExcelConstants** record.

3.  In the **importSetColumnsVsStagingColumnsMap** object, add a line in the following format:

    `"ETL Column Name": "Staging Table Column Name"`

    For example: `"u_my_custom_field": "u_my_custom_field"`

4.  Above your new entry, add a comma at the end of the previous line.


## What to do next

[Complete the custom column import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/complete-custom-column-import-sgc-excel.md)

**Parent Topic:**[Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/add-custom-column-staging-table.md)

