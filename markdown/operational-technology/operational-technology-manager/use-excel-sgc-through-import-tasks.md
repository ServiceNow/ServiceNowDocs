---
title: Using the Service Graph Connector for Microsoft Excel through import tasks
description: With the Service Graph Connector for Microsoft Excel, you can create import tasks that handle the upload, validation, and import of staging records for your OT device data into the Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2025-07-14"
reading_time_minutes: 1
breadcrumb: [Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Using the Service Graph Connector for Microsoft Excel through import tasks

With the Service Graph Connector for Microsoft Excel, you can create import tasks that handle the upload, validation, and import of staging records for your OT device data into the Configuration Management Database \(CMDB\).

## Import task overview

Users assigned the OT Excel Import User \[ot\_excel\_import\_user\] role can create import tasks in the Industrial Workspace. Import tasks handle the following tasks.

-   Upload the populated Microsoft Excel spreadsheet into staging table.
-   Validate the staging records created from the Microsoft Excel spreadsheet.
-   Import the valid staging records into the CMDB.
-   Optionally, create remediation tasks for invalid staging records.

-   **[Create an import task](../task/create-import-task-excel-sgc.md)**  
Create an import task for the Service Graph Connector for Microsoft Excel to handle the import of Operational Technology \(OT\) device data from your Microsoft Excel spreadsheet.
-   **[Validate imported staging records](../task/run-validations.md)**  
Validate the imported staging records from your import task to find missing, duplicate, and invalid data.
-   **[Trigger a CMDB import for valid staging records](../task/trigger-cmdb-import.md)**  
Trigger a Configuration Management Database \(CMDB\) import for your valid staging records to directly import them into the CMDB
-   **[Create a remediation task for invalid staging records](../task/create-remediation-task-for-validation-errors.md)**  
After running validations for the Operational Technology \(OT\) device data imported with the Service Graph Connector for Microsoft Excel, optionally create a remediation task to resolve invalid staging records.

**Parent Topic:**[Service Graph Connector for Microsoft Excel](service-graph-connector-for-OT-excel.md)

