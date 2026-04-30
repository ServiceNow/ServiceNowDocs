---
title: Importing equipment model data
description: The scheduled import function enables you to import your existing equipment model data from a populated Microsoft Excel flat-file spreadsheet. You can use it to import your ISA-95 Equipment Model data to the Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Industrial Process Manager, Operational Technology]
---

# Importing equipment model data

The scheduled import function enables you to import your existing equipment model data from a populated Microsoft Excel flat-file spreadsheet. You can use it to import your ISA-95 Equipment Model data to the Configuration Management Database \(CMDB\).

You must install the Industrial Process Manager before importing equipment model data.

Several methods are available for importing the equipment model data into the ServiceNow AI Platform:

1.  If you use the spreadsheet to import the data, you must populate the Microsoft Excel spreadsheet with your existing ISA-95 Equipment Model data and run the **SG-Equipment Model Scheduled Import Using Spreadsheet** scheduled import. Many legacy record systems contain functions that enable you to export this data to an Excel spreadsheet, which means that you don't have to populate it manually.
2.  Several ServiceNow partners are also developing integrations to third-party legacy record systems that store equipment model data.
    -   When these integrations become available, you can find them on the ServiceNow Store by searching for Operational Technology certified integrations for the Industrial Process Manager.
    -   Install those integrations that are applicable to your environment, and run them as needed.

By using these import methods, you can update existing equipment models in the ServiceNow AI Platform with the data that is stored in your authoritative source when needed. For newly imported data, the ServiceNow AI Platform automatically creates Equipment Model Entity CI class records in the Configuration Management Database \(CMDB\).

## System properties that affect import processing

The following system properties affect how you populate your Microsoft Excel spreadsheet with the equipment model data and how the Import Equipment Model - ETL process functions.

-   **sn\_isa\_model.cmdb\_relationships\_sync\_levels**

    Determines how many levels of an equipment model can be imported into the ServiceNow AI Platform and then are synchronized in the Configuration Management Database \(CMDB\). The default value is 8.

-   **sn\_isa\_model.short\_code\_validation\_max\_length**

    Sets the maximum length for the Short Code column on your spreadsheet. The default value is 3.

-   **sn\_isa\_model.user\_search\_matching\_attribute**

    Matches the user data references that are imported from your populated spreadsheet to the corresponding user records that are stored in the System Users \[sys\_user\} table. The default is the user's email address, because the email address is unique to each user record.

-   **glide.scriptable.excel.max\_file\_size**

    Sets the maximum size of an Excel file, expressed in bytes. This property is global.


**Note:** To learn more about adding or creating system properties to control system behavior, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

-   **[Populating your Microsoft Excel spreadsheet with equipment model data](populate-excel-spreadsheet-with-isa-equipment-model-data.md)**  
Create and populate a Microsoft Excel spreadsheet with your existing ISA equipment model data. Positioning your existing data in the correct columns is crucial to the success of your upload.
-   **[Import your equipment model data using the data source and scheduled import](../task/import-equipment-model-data-using-data-source-and-scheduled-import.md)**  
After you complete your Microsoft Excel spreadsheet with your equipment model data, import it into the ServiceNow AI Platform by using the data source and scheduled import.

**Parent Topic:**[Configuring the Industrial Process Manager](configuring-manufacturing-process-mgr.md)

