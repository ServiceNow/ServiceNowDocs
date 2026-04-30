---
title: Importing data using import sets
description: To import data define a data source and transform map, and run or schedule an import.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Import sets, Imports, Data and Automation]
---

# Importing data using import sets

To import data define a data source and transform map, and run or schedule an import.

![](../image/ImportingDataDataFlow.png "Importing data: data flow")

-   **[Create a data source](c_CreateNewDataSource.md)**  
Create a data source record to define what data an import set should import.
-   **[Data source fields](../reference/r_DataSourceFileTypeFields.md)**  
In addition to common fields, other fields appear on the data source form, depending on the value of the **Type** field.
-   **[Create a transform map](../../../script/server-scripting/task/t_CreateATransformMap.md)**  
Every import operation to a production table requires at least one transform map associated with an import set.
-   **[Mapping options](../../../script/server-scripting/concept/c_MappingOptions.md)**  
You can map fields in a number of ways depending on the circumstances of the import and whether data must be transformed prior to loading onto a production table.
-   **[Create a field map](../../../script/server-scripting/task/t_CreatingAFieldMap.md)**  
Field maps establish a relationship between a field in an import set table and a field in the target table.
-   **[Field map script variables](../reference/r_FieldMapScriptVars.md)**  
Several predefined variables are available in the **Source script** field.
-   **[Run an import](../task/t_RunImport.md)**  
You can manually run an import to immediately import data.
-   **[Importing date/time values](importing-date-time-values.md)**  
Considerations when importing data containing date/time values.
-   **[Review the import set](../task/t_ReviewTheImportSet.md)**  
After an import set completes, you can review the completed import and clean up import set tables. Even if no errors are reported by the progress indicator, review how your data is imported into the new import set.
-   **[Viewing the import log](../../managing-data/concept/c_ViewingTheImportLog.md)**  
The import log is where you can find information about the internal processing that occurs during an import operation.
-   **[Import run history](../reference/r_ImportRunHistory.md)**  
The import history gives status information about individual import operations.
-   **[Schedule a data import](../task/t_ScheduleADataImport.md)**  
Schedule imports to make it possible to specify that certain import operations occur at a regular interval.
-   **[Monitor scheduled data import executions](../task/monitor-sched-import-executions.md)**  
Monitor scheduled data import executions to see the hierarchy and flow of the scheduled chained imports.
-   **[Monitor concurrent import sets](../task/monitor-concurrent-import-sets.md)**  
Monitor concurrent import sets to check the status of import sets and import set jobs, resume or reprocess import sets, and view transform history.
-   **[Monitor concurrent import set jobs](../task/monitor-concurrent-import-set-jobs.md)**  
Check the status of concurrent import set jobs.
-   **[Post CSV or Excel files directly to an import set](../task/t_PostCSVOrExcelFilesToImportSet.md)**  
An administrator can post CSV or Excel files directly to instance.
-   **[Delete import sets](../task/delete-import-sets.md)**  
Delete import sets to clean up your database on a scheduled basis, one time only, or on demand.
-   **[Delete import set tables](../task/delete-import-set-tables.md)**  
Delete import set tables, related transform maps, or data only \(preserving the table structure\) to clean up your database.

**Parent Topic:**[Import sets](../reference/import-sets-landing-page.md)

