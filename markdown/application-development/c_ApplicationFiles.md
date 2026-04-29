---
title: Application files
description: Application files are configuration records that allow developers to extend application functionality.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application files

Application files are configuration records that allow developers to extend application functionality.

Application developers create application files when they add configuration records for application logic such as business rules, workflows, and script includes. Scoped applications do not own these tables, but they do own the records \(files\) within these tables. For example, adding a business rule to check for available rooms from the Conference Room table adds an application file to the Business Rule \[sys\_script\] table. Application developers can view the complete list of application files from the custom application record.

The Application File \[sys\_metadata\] table is the parent table for all tables that contain configuration records. It provides a series of standard fields that define the attributes for a configuration record. Tables that contain configuration records extend the Application File table. For example, the Business Rule \[sys\_script\] table extends the Application File table.

Developers do not create application file records directly from the Application File table. Instead, they create or modify configuration records, and the system creates or modifies the associated application file record. Most configuration record tables do not display a reference field or related list for the Application File table. By default, only Applications \[sys\_scope\] and Tables \[sys\_db\_object\] have a reference to the Application File table.

The system also tracks application file records in Update Sets. Whenever you change an application file record or its related configuration record, the system adds a corresponding record in the Customer Updates \[sys\_update\_xml\] table. The system uses a single update record, ensuring that a configuration record and its application file are kept in sync when transferring applications between instances. To avoid collision, users are warned when they edit an application file that has been previously edited in another Update Set.

Administrators can:

-   View file properties for configuration records.
-   Protect application files from changes during upgrades.
-   View parent-child relationships between configuration records.

**Related topics**  


[Legacy - Add an application file to an application](../task/t_AddAnAppFileToAnApp.md)

