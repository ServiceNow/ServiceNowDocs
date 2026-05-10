---
title: Exporting and importing data via XML
description: Migrate data from one instance to another by exporting and importing XML files.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Exporting and importing data via XML

Migrate data from one instance to another by exporting and importing XML files.

## Key benefits

-   Directly export records as XML from any list or form.
-   Transfer all fields and values exactly from one instance to another.
-   Perform unscheduled data imports as needed.
-   Save time by not building import sets or transform maps.

## Use cases

-   Export smaller batches of records on an infrequent basis by exporting and importing data via XML.
-   Export and import data using XML files for records created in a development instance that must be migrated with an update set as part of a migration procedure. Examples of these records include lookup tables, unit test records, and other information required to support production. Typically, this information is only migrated once and the overhead of an import set is not justified.

## Important considerations

-   The XML export preserves all record field values including system generated field values such as:
    -   Sys ID
    -   Creation date
    -   Update date
-   Image field data is not preserved when exporting to XML.
-   The XML import directly inserts records into the target table. During the import the system:
    -   Ignores any business rules that normally apply to the table.
    -   Does not provide any opportunity to transform incoming data.
    -   Automatically matches a reference field's display value to the local Sys ID for some tables.
-   Data export and import via XML is helpful for copying records from one system to another but does not remove the need to know the relationships between tables. If you need validate or transform data or reconcile the sys ID values of reference fields, use an XML import set instead. See [Export sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-export-sets/c_ExportSets.md).

