---
title: Importing from another ServiceNow instance
description: There are several methods for moving data from one instance to another.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Import sets, Imports, Creating integrations with applications]
---

# Importing from another ServiceNow instance

There are several methods for moving data from one instance to another.

All of these methods assume you need to periodically move a collection of records from a table on one instance to a table on another instance. If you want an action on an individual record to trigger a corresponding action on another instance, consider using a REST web service instead.

## Identifying Needed Related Records

All import processes work by fetching data from one table at a time. This process can produce unexpected results if the incoming data references new records in other tables such as users, locations, or companies. To prevent importing broken references to other tables you must identify the connections between your tables and import the common data prior to importing the application data.

For example, prior to importing incident data, you might want to first import related configuration items, users, and locations. Furthermore you might want to import incidents before importing problems or changes that refer to these incident records.

## Available Import Processes

The system offers the following processes to move data from one instance to another.

-   Export and import XML records directly from lists
-   Create XML import sets and transform data as needed
-   Export and import CSV files from lists

-   **[XML records from lists](c_XMLRecordsFromLists.md#)**  
You can directly export records as XML from any list or form.
-   **[Using XML import sets](c_XMLImportSets.md)**  
Use an XML import set to import data from another instance.
-   **[Retrieving data from a CSV formatted file](../task/t_RetrieveDataFromACSVFormatFile.md)**  
In this method, you import data from another instance using an HTTPS data source to return a CSV formatted file containing the rows to be imported.

**Parent Topic:**[Import sets](../reference/import-sets-landing-page.md)

