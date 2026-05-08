---
title: Import data from XML
description: After you have successfully exported data from the source instance to XML, import the XML file directly to the target instance.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exporting and importing data via XML, Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Import data from XML

After you have successfully exported data from the source instance to XML, import the XML file directly to the target instance.

## Before you begin

Role required: admin

## About this task

Importing XML doesn't trigger business rules or update the instance cache.

## Procedure

1.  Log in to the target instance \(the instance that should receive the data\).

2.  Navigate to any list in the system.

    Any list can be used because the XML file contains the destination table name for the records.

3.  Select and hold \(or right-click\) any column title and select **Import XML**.

4.  In the Import XML form, select **Choose File** and select the previously exported XML file.

5.  Select **Upload**.


## Result

Data is imported into the target instance.

If the data doesn't import, navigate to **System Definition** &gt; **Tables &amp; Columns** and verify that the table from which the data was exported also exists in the target instance. If the table doesn't exist, you can move it using an update set. For details on using update sets, see Get started with update sets.

