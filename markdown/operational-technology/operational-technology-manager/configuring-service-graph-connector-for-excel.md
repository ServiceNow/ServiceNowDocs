---
title: Configuring Service Graph Connector for Microsoft Excel
description: Configure the Service Graph Connector for Microsoft Excel to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/operational-technology/operational-technology-manager/configuring-service-graph-connector-for-excel.html
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Configuring Service Graph Connector for Microsoft Excel

Configure the Service Graph Connector for Microsoft Excel to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet.

Use the Service Graph Connector for Microsoft Excel guided setup and complete tasks in sequence to configure the Service Graph Connector for Microsoft Excel.

Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Guided Setup**, open the following guided setups, and complete the tasks.

For more information on using guided setup, see Guided Setup.

<table id="table_dfl_3jt_5xb"><thead><tr><th>

Task

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

Users

</td><td>

Assigns roles to control the actions that are available for each user.

</td></tr><tr><td>

Review class mappings

</td><td>

Review and update the class mappings available for the Service Graph Connector for Microsoft Excel.**Note:** To review the class mappings available, you need to install the Industrial Core plugin that contains the class mapping template tables for the OT Service Graph Connectors. For more information about the Industrial Core plugin, see .

</td></tr><tr><td>

Staging table configuration

</td><td>

Configure to determine which factors constitute in identifying a unique name for a CI.

 For more information on system properties, see [System properties that impact SG-OT Device Excel Import processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/system-properties-sg-ot-asset-excel-import.md).

</td></tr><tr><td>

Prepare Data

</td><td>

Create and prepare the spreadsheet by positioning your existing data in the correct columns.

 For more information to prepare the data, see [Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/preparing-your-pre-import-ot-worksheet-entry-review-tool-for-sgc-import.md).

</td></tr><tr><td>

Create new OT devices

</td><td>

Create a new OT Device manually by clicking on the New button from the list view of the Staging table. For more information about creating new OT devices, see

</td></tr><tr><td>

Validate records

</td><td>

Run validations against the imported data to update the Validation stage of the records and provide validation comments.

**Note:** You don't need to select any records on the list to run validations. Validations are run on all the records present in the staging table.

 For more information about validating records, see [Managing Validations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/managing-validations.md).

</td></tr><tr><td>

Schedule Import

</td><td>

Import data from the staging table to the import set table and review it in the OT list views and Workspace.

</td></tr></tbody>
</table>-   **[Assign Pre-import OT Worksheet Entry Review roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/assign-pre-import-ot-worksheet-entry-review-tool-for-sgc-import-roles.md)**  
Assign roles to the users  or user groups so that you can manage the Excel Service Graph Connector staging table and ETL.
-   **[Preview existing OT records in the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/preview-existing-asset-records.md)**  
Preview existing Operational Technology \(OT\) device records in the Configuration Management Database \(CMDB\) before you import any new records from the staging table. By previewing existing records, you can avoid reconciling or merging unrelated records.
-   **[Review class mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/review-class-mappings-sgc-excel.md)**  
Review and update the class mappings available for the Service Graph Connector for Microsoft Excel.

**Parent Topic:**[Service Graph Connector for Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/service-graph-connector-for-OT-excel.md)

