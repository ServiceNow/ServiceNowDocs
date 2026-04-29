---
title: Storage aliases
description: Learn about the role storage aliases play in data manipulation and field creation in the ServiceNow AI Platform.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring tables, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Storage aliases

Learn about the role storage aliases play in data manipulation and field creation in the ServiceNow AI Platform.

Understanding storage aliases is important for effective data management and schema customization in the ServiceNow AI Platform, particularly when dealing with complex table hierarchies like those in the Task \[task\] table.

By default, administrators have access to the Storage Column Aliases \[sys\_storage\_alias\] table within an instance. However, transactional processes against this table can't be performed by an administrator from the user interface.

## Table hierarchy and models

Understanding storage aliasing requires knowledge of table hierarchies within the Task \[task\] table, which involves two models: Table per hierarchy and Table per class.

-   **Table per hierarchy**

    This model uses a single physical table, the Task \[task\] table, which features a flattened hierarchy where all columns within the task hierarchy exist only on the task table. For example, fields related to change requests aren't on a separate Change Request \[change\_request\] table but are integrated into the Task \[task\] table. You can verify whether a table is Table per hierarchy by checking the extension model field in the Tables \[sys\_db\_object\] table. If the table's parent is a direct child of the Task \[task\] table, the table uses Table per hierarchy.

    An extended table inherits the hierarchy of its parent. For example, the IMAC \[change\_request\_imac\] table is a child table of the Change Request \[change\_request\] table, which extends the Task \[task\] table. Because the Change Request \[change\_request\] table is Table per hierarchy, the IMAC \[change\_request\_imac\] table model is also Table per hierarchy. Legacy tables such as the Incident \[incident\] table, Change Request \[change\_request\] table, and Problem \[problem\] table are all part of the flattened Task \[task\] table hierarchy.

-   **Table per class**

    This model applies to tables that physically exist in the database. It's used for new tables directly extending from the Task \[task\] table when the task row count exceeds 1 million rows. Unlike Table per hierarchy, Table per class doesn't use glomming because it doesn't operate within a flattened hierarchy.


## Storage alias definition

A storage alias is created for every field on a table within an instance. Familiarize yourself with the key fields on the Storage Column Aliases \[sys\_storage\_alias\] table.

-   **Element Name**

    Indicates how the field appears to users, which is important for user interface interactions and scripting.

-   **Storage Alias**

    Indicates the exact physical column where the data for a field is stored. The storage alias value is used in combination with the table\_name value to identify what data to manipulate. The storage alias value is the actual physical column on the Task \[task\] table.

-   **Storage Table Name**

    Specifies the physical table that houses the element. For Table per hierarchy tables, the value is always task. For Table per class tables, the value is the name of the physical table.

-   **Table**

    Specifies the logical class that each element links to on the physical Task \[task\] table. The Table element holds the table\_name value which is the class discriminator.


![Elements with storage alias a_ref_2 on the Task table.](../image/storage-aliases.png "Storage column aliases")

In this example, the storage alias for the cab\_delegate element is a\_ref\_2 and the physical storage table where the data is stored is task. The example depicts 10 logical elements in different logical classes on the Task \[table\] that all link to the same alias a\_ref\_2 on the physical Task \[task\] table.

The sibling elements are glommed, which means they share one physical column on the Task \[task\] table. You can query data from the logical element cab\_delegate using a query like:

```
SELECT a_ref_2 from task WHERE sys_class_name='change_request' AND a_ref_2 IS NOT NULL
```

The query specifies data in the physical column a\_ref\_2. The class discriminator change\_request is used in combination with the storage alias a\_ref\_2 to query the logical element cab\_delegate from the logical class change\_request on the physical Task \[task\] table.

The naming convention for fields created in the actual physical tables can vary depending on the type of field. In this example, a\_ref\_2 is an alias on the Task \[task\] table that holds values for reference fields.

## Functionality and usage

Storage aliases serve multiple purposes.

-   **Mapping**

    Aliases map logical elements \(Table per hierarchy\) or physical elements \(Table per class\) to the actual physical columns in the backend database. The logical element can be glommed to a physical column that is larger than the logical element's max\_length.

-   **Glomming**

    Aliases allow multiple sibling elements to share a single physical column in a Table per hierarchy model.

-   **Label mapping**

    Aliases associate sys\_documentation \(label\) records with their respective elements, enhancing visibility in forms, reports, and list views.


## Restrictions and rules

-   Two logical elements within the same class can't share a physical column. For example, two string fields created on the Incident \[incident\] table can't map to the same physical column in the database.
-   A parent element and its child can't share a physical column. For example, a field created on the Incident \[incident\] table can't be mapped to a physical column when that physical column is already mapped to a field on the Task \[task\] table.
-   Only sibling elements can share a physical column. For example, a reference field on the Change Request \[change\_request\] table and a reference field on the Incident \[incident\] table and can both map to the same physical column.
-   Fields created directly on the Task \[task\] table \(where sys\_class\_name is 'task'\) can't be glommed.

**Parent Topic:**[Exploring ServiceNow AI Platform tables](exploring-table-administration.md)

