---
title: Update the column mapping script
description: To transfer the custom column data to the Configuration Management Database \(CMDB\), update the column mapping script to add the corresponding entry to the importSetColumnsVsStagingColumnsMap object.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/operational-technology/operational-technology-manager/update-column-mapping-script-sgc-excel.html
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 1
breadcrumb: [Add a custom column to the staging table, Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Update the column mapping script

To transfer the custom column data to the Configuration Management Database \(CMDB\), update the column mapping script to add the corresponding entry to the **importSetColumnsVsStagingColumnsMap** object.

## Before you begin

Role required: ot\_excel\_import\_user

## About this task

The **importSetColumnsVsStagingColumnsMap** object in the **SGOTAssetImportExcelConstants** script controls which columns from the SG OT Excel Stagings \(sg\_ot\_excel\_staging\) table are included when you trigger the CMDB import process. If you add a custom column to the staging table, you must add a corresponding entry to the **importSetColumnsVsStagingColumnsMap** object. Otherwise, the custom column is ignored during import. For more information about triggering the CMDB import process, see [Trigger a CMDB import for valid staging records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/operational-technology-manager/trigger-cmdb-import.md).

Each entry in **importSetColumnsVsStagingColumnsMap** object is a key-value pair with the following format:

`"<import set column name>": "<staging table column name>"`

The key is the field name that appears in the JSON payload sent to the CMDB import \(sn\_otsm\_sgc\_sg\_ot\_excel\_import\) set. The value is the name of the corresponding column on the SG OT Excel Stagings table.

When you create a key and value, they're typically identical. For example, a custom staging column named **u\_my\_custom\_field** maps to itself. Only use a different name if you need the import set field name to differ from the staging table column name.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Import OT Devices - Script Includes**.

2.  Select the **SGOTAssetImportExcelConstants** record.

3.  In the **importSetColumnsVsStagingColumnsMap** object, add a line in the following format:

    `"ETL Column Name": "Staging Table Column Name"`

    For example: `"u_my_custom_field": "u_my_custom_field"`

4.  Before your new entry, add a comma at the end of the line so that the object remains valid JavaScript.

5.  Select **Update**.


## What to do next

Configure the Robust Transform Engine \(RTE\) mapping for the Extract Transform Load \(ETL\). For more information, see [Configure the RTE mapping for ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/operational-technology-manager/complete-rte-mapping-etl-sgc-excel.md).

**Parent Topic:**[Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/operational-technology-manager/add-custom-column-staging-table.md)

