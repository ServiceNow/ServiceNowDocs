---
title: Service Graph Connector for Microsoft Excel
description: The Service Graph Connector for Microsoft Excel function enables you to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet. You use it in the Integration Hub Extract Transform Load \(ETL\) to upload this data to the Configuration Management Database \(CMDB\).
locale: en-US
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

Before you can run the import process, you must populate the Microsoft Excel spreadsheet with your existing Operational Technology data. When you import your Microsoft Excel spreadsheet using the Integration Hub ETL, it creates the correct configuration item \(CI\) records in the Configuration Management Database \(CMDB\). To learn more, see [Operation Technology \(OT\) extension classes](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

-   **[Configuring Service Graph Connector for Microsoft Excel](configuring-service-graph-connector-for-excel.md)**  
Configure the Service Graph Connector for Microsoft Excel to import your existing Operational Technology data from a populated Microsoft Excel flat-file spreadsheet.
-   **[Easy import](easy-import.md)**  
Easy import is a simplified import process that enables you to import only the columns that you want.
-   **[Managing Validations](managing-validations.md)**  
Validation enables you to review and manage the imported data in the staging table.
-   **[Schedule the time interval to import data](../task/schedule-import.md)**  
Schedule the time interval to import the data from the staging table to the CMDB.
-   **[Import your Microsoft Excel spreadsheet using the staging table](../task/import-excel-spreadsheet-service-graph-connector.md)**  
Import your Microsoft Excel spreadsheet into the staging table using easy import to create the required data in the staging table from the spreadsheet.
-   **[Add a custom field mapping in the staging table for Service Graph](../task/add-new-column-mappings-excel-service-graph.md)**  
Add a custom field to the staging table and map the custom field from the staging table to the CI field through Excel SGC.
-   **[Add a custom implementation for device classification](../task/adding-custom-implementation-for-asset-classification.md)**  
Customize the base system classification of an device based on the type, os\_version, and firmware\_version.
-   **[Add a custom validation for devices](../task/add-custom-validation-for-devices.md)**  
Customize the validation for your OT devices.
-   **[Test the Excel Service Graph connector](../reference/excel-service-graph-connector-troubleshooting.md)**  
The troubleshooting actions can help resolve common issues when importing your Operational Technology devices or data. Access the System Log to troubleshoot for these errors.
-   **[View script includes used by the Service Graph Connector](../task/view-script-includes-used-by-service-graph-connector.md)**  
As an admin, view the script includes related to the Service Graph Connector.
-   **[Access system properties used by the Service Graph Connector](../task/access-system-properties-used-by-service-graph-connector.md)**  
As an admin, view system properties related to the Service Graph Connector.

**Parent Topic:**[Using the Operational Technology Manager](using-operational-technology-manager.md)

**Related topics**  


[IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)

[IntegrationHub ETL](https://www.servicenow.com/docs/access?context=integrationhub-etl&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

