---
title: Service Graph Connector for Microsoft Excel
description: The Service Graph Connector for Microsoft Excel function enables you to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet. You use it in the Integration Hub Extract Transform Load \(ETL\) to upload this data to the Configuration Management Database \(CMDB\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/operational-technology/operational-technology-manager/service-graph-connector-for-OT-excel.html
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use, Operational Technology Manager, Operational Technology]
---

# Service Graph Connector for Microsoft Excel

The Service Graph Connector for Microsoft Excel function enables you to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet. You use it in the Integration Hub Extract Transform Load \(ETL\) to upload this data to the Configuration Management Database \(CMDB\).

Before you can run the import process, you must populate the Microsoft Excel spreadsheet with your existing Operational Technology data. When you import your Microsoft Excel spreadsheet using the Integration Hub ETL, it creates the correct configuration item \(CI\) records in the Configuration Management Database \(CMDB\). To learn more, see [Operation Technology \(OT\) extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-ci-class-models-operation-technology.md).

-   **[Configuring Service Graph Connector for Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/configuring-service-graph-connector-for-excel.md)**  
Configure the Service Graph Connector for Microsoft Excel to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet.
-   **[Easy import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/easy-import.md)**  
Easy import is a simplified import process that enables you to import only the columns that you want.
-   **[Managing Validations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/managing-validations.md)**  
Validation enables you to review and manage the imported data in the staging table.
-   **[Schedule the time interval to import data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/schedule-import.md)**  
Schedule the time interval to import the data from the staging table to the CMDB.
-   **[Import your Microsoft Excel spreadsheet using the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/import-excel-spreadsheet-service-graph-connector.md)**  
Import your Microsoft Excel spreadsheet into the staging table using easy import to create the required data in the staging table from the spreadsheet.
-   **[Add a custom field mapping in the staging table for Service Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/add-new-column-mappings-excel-service-graph.md)**  
Add a custom field to the staging table and map the custom field from the staging table to the CI field through Excel SGC.
-   **[Add a custom implementation for device classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/adding-custom-implementation-for-asset-classification.md)**  
Customize the base system classification of an device based on the type, os\_version, and firmware\_version.
-   **[Add a custom validation for devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/add-custom-validation-for-devices.md)**  
Customize the validation for your OT devices.
-   **[Test the Excel Service Graph connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/excel-service-graph-connector-troubleshooting.md)**  
The troubleshooting actions can help resolve common issues when importing your Operational Technology devices or data. Access the System Log to troubleshoot for these errors.
-   **[View script includes used by the Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/view-script-includes-used-by-service-graph-connector.md)**  
As an admin, view the script includes related to the Service Graph Connector.
-   **[Access system properties used by the Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/access-system-properties-used-by-service-graph-connector.md)**  
As an admin, view system properties related to the Service Graph Connector.

**Parent Topic:**[Using the Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/using-operational-technology-manager.md)

**Related topics**  


[IntegrationHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/integrate-applications/integration-hub/integrationhub.md)

[IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md)

