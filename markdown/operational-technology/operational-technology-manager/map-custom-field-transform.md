---
title: Map the custom field in the transform map
description: Map the custom source field on the pre-import table to the target field on the sta table so the imported value transforms into the correct staging column.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/operational-technology-manager/map-custom-field-transform.html
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-06-29"
reading_time_minutes: 1
keywords: [transform map, field map, field mapping]
breadcrumb: [Add a custom column to the staging table, Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Map the custom field in the transform map

Map the custom source field on the pre-import table to the target field on the sta table so the imported value transforms into the correct staging column.

## Before you begin

The custom column must be added to both the staging table and the pre-import table before completing this task. For more information, see [Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/add-custom-column-staging-table.md) and [Add a matching column to the pre-import table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/add-column-pre-import-table.md).

Role required: ot\_excel\_import\_user

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager Admin** &gt; **Import OT Devices - Data Sources**.

2.  Select the **SG OT Excel Staging Import** record.

3.  Under the **Transforms** tab, select the sn\_otsm\_sgc\_sg\_ot\_excel\_pre\_import transform map record.

4.  Under the **Field Maps** tab, select **New**.

5.  Set the **Source field** value to the same column you created in the SG-OT Excel Pre Import Staging table.

6.  Set the **Target** value to the same column you created in the SG OT Excel Stagings \[sg\_ot\_excel\_staging\] table.

7.  Select **Submit**.


## Result

The field map is added to the SG-OT Excel Pre Import \[sn\_otsm\_sgc\_sg\_ot\_excel\_pre\_import\] table transform map record.

## What to do next

Upload an updated Microsoft Excel spreadsheet to populate the custom column. For more information, see the following tasks:

-   [Create an import task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/create-import-task-excel-sgc.md)
-   [Validate imported staging records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/run-validations.md)
-   [Trigger a CMDB import for valid staging records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/trigger-cmdb-import.md)

**Parent Topic:**[Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/add-custom-column-staging-table.md)

