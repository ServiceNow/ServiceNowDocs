---
title: Record Producer
description: A record producer is a specific type of catalog item that allows end users to create task-based records, such as incident records, from the service catalog.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Record Producer

A record producer is a specific type of catalog item that allows end users to create task-based records, such as incident records, from the service catalog.

Use record producers to provide a better end-user experience instead of using the regular task-based form for creating records. The look and feel of a record producer is similar to that of a catalog item. But the record producer generates a task record such as incident, instead of a requested item.

You can create a record producer for tables and database views that are in the same scope as the record producer. You can also create a record producer for tables that allow create access from applications in other scopes.

Define a record producer in the service catalog or from the table record.

**Note:**

-   Use a record producer to create task-based records only.
-   To ensure that standard service catalog processes are followed, such as initiating workflows as expected, do not create requested item records from record producers. Instead, create requested item using catalog items.
-   If the record producer script aborts the record generation, no record is generated in the Item Produced Record \[sc\_item\_produced\_record\] table.

    **Note:** Do not call the update, setAbortAction method, or set the sys\_class\_name on current record to avoid unexpected behavior.


-   **[Create a record producer](../task/t_DefRecProdInSCat.md)**  
You can create a record producer for tables and database views that are in the same scope as the record producer. Also for tables that allow create access from applications in other scopes.
-   **[Create record producers from tables](../task/t_CreatingRecordProducersFromTables.md)**  
You can create Service Catalog record producers directly from a table record.
-   **[Populate record producer data and redirect users](c_PopulatingRecordData.md)**  
You can enter data for all records created by the record producer, and redirect an end user to a particular page after the record producer is submitted.

**Parent Topic:**[Types of catalog items](../reference/r_ExtendedCatalogItemFunctions.md)

