---
title: Table extension and classes
description: Enable one or more child tables to share fields and records with a parent table. Administrators and application developers can only extend tables during table creation.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Exploring ServiceNow AI Platform tables, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Table extension and classes

Enable one or more child tables to share fields and records with a parent table. Administrators and application developers can only extend tables during table creation.

Administrators and application developers typically extend tables to create a set of related records that share information. For example, in the base system, the Task and the Configuration Item tables have multiple extensions:

<table id="table_v34_p1d_ty"><thead><tr><th>

Original table

</th><th>

Related tables extended from original table

</th></tr></thead><tbody><tr><td>

Task \[task\]

</td><td>

-   Incident \[incident\]
-   Problem \[problem\]
-   Change Request \[change\_request\]

</td></tr><tr><td>

Configuration Item \[cmdb\_ci\]

</td><td>

-   Application \[cmdb\_ci\_appl\]
-   Computer \[cmdb\_ci\_computer\]
-   Database \[cmdb\_ci\_database\]

</td></tr></tbody>
</table>A table that extends another table is called a child class, and the table it extends is the parent class. A table can be both a parent and child class both extending and providing extensions for other tables. A parent class that is not an extension of another table is called a base class.

Administrators can use these tools to see the relationships between classes.

-   Schema map
-   System dictionary
-   Tables module

Extending a table:

-   Links the new table to the extending table.
-   Creates system fields in the new table.
-   Creates one or more database tables to store the parent and child classes. The number of tables the system creates depends upon the extension model selected during table creation.

## Extension models

The ServiceNow AI Platform offers these extension models.

-   Table per class
-   Table per hierarchy
-   Table per partition

The extension model determines these attributes.

-   The number of database tables created
-   The derivation of fields from parent classes
-   The replication of records from child classes

## Table per class

-   **Tables created**

    Creates a separate database table for the parent class and each child class.

-   **Fields derived from parent class**

    Child classes derive fields from parent classes.

-   **Dictionary records created for parent class**

    A parent class has a Dictionary record for the collection and for each field that can be derived from it. For example, the Contract \[ast\_contract\] table has 59 Dictionary records, which define the table and its fields.

-   **Dictionary records created for child classes**

    Each child class only has Dictionary entries for fields unique to the class.

-   **Records replicated**

    The parent class replicates each record stored in its child classes. Each child class only stores records unique to the class. Replicated records have the same Sys ID value in each table. The system replicates any change you make to a child record to the matching record in the parent table. For example, Contract \[ast\_contract\] table replicates records from the Lease \[ast\_lease\] and Warranty \[ast\_warranty\] tables.


## Table per hierarchy

-   **Tables created**

    Creates one database table for the parent class, which stores all records for the parent and child classes. Child classes do not have separate database tables.

-   **Fields derived from parent class**

    Child classes derive fields from parent classes. For example, the Incident table derives fields from the Task table.

-   **Dictionary records created for parent class**

    A parent class has a Dictionary record for the collection and for each field that can be derived from it. For example, the Task table is a parent class that has 66 Dictionary records, which define the table and its fields.

    The Dictionary entry for the parent class contains a sys\_class\_name column whose value indicates which child class each record belongs to. For example, Incident records have a sys\_class\_name value of incident, and change records have a sys\_class\_name value of change.

-   **Dictionary records created for child classes**

    Each child class only has Dictionary entries for fields unique to the class. For example, the Incident table only has 22 Dictionary records, which are not already defined in the Task table.

-   **Records replicated**

    Record replication is not needed, because the parent class stores all records that belong to the hierarchy. For example, the Task table contains all records from its child classes such as the Change, Incident, and Problem tables.


## Table per partition

-   **Tables created**

    Creates one database table for the parent class, which stores all records for the parent and child classes. Child classes do not have separate database tables. As the database table reaches a storage limit, the system dynamically adds storage tables \(partitions\) to store additional records.

-   **Fields derived from parent class**

    Child classes do not derive fields from parent classes. Instead each child class has its own list of fields. For example, the Base Configuration Item \[cmdb\], Configuration Item \[cmdb\_ci\], and Hardware \[cmdb\_ci\_hardware\] tables all have their own field definitions.

-   **Dictionary records created for parent class**

    A parent class has a Dictionary record for the collection and for each field relevant to it. For example, the Base Configuration Item \[cmdb\] table is a parent class that has 48 Dictionary records.

    The system replicates changes made to parent class Dictionary entries to child class Dictionary entries. For example, when you change the name column in the parent class Base Configuration Item \[cmdb\] table, the system replicates it to child class Dictionary entries such as the Configuration Item \[cmdb\_ci\] and Hardware \[cmdb\_ci\_hardware\] tables.

    The Dictionary entry for the parent class contains columns for sys\_class\_name and sys\_class\_path whose values indicate which child class each record belongs to. For example, Hardware records have a sys\_class\_name value of cmdb\_ci\_hardware, and computer records have a sys\_class\_name value of cmdb\_ci\_computer.

    When the database table reaches a storage limit, the system updates the Dictionary entry for the parent class to include columns for sys\_storage\_alias and storage\_table\_name. These storage column Dictionary entries allow administrators to manage the parent class and its storage tables as a single logical unit.

-   **Dictionary records created for child classes**

    Each child class has a Dictionary record for the collection and for each field relevant to it. For example, the Hardware table has 73 Dictionary records with some records duplicating columns in the parent class.

-   **Records replicated**

    Record replication is not needed, because the parent class stores all records that belong to the hierarchy. For example, the Base Configuration Item \[cmdb\] table contains all records from its child classes such as the Application \[cmdb\_ci\_appl\], Computer \[cmdb\_ci\_computer\], and Hardware \[cmdb\_ci\_hardware\] tables.


**Parent Topic:**[Exploring ServiceNow AI Platform tables](exploring-table-administration.md)

