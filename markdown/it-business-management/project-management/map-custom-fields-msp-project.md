---
title: Create custom field mapping for Microsoft Project file import
description: Map custom fields from Microsoft Project to ServiceNow fields before importing a project.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Importing and exporting projects, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create custom field mapping for Microsoft Project file import

Map custom fields from Microsoft Project to ServiceNow fields before importing a project.

## Before you begin

Create custom fields in your ServiceNow instance before mapping them with Microsoft Project. For more information, see Add and customize a field in a table.

Role required: it\_pps\_admin

## About this task

Map the custom fields that you create in your ServiceNow instance with custom fields in the Microsoft Project file you plan to import.

The supported data types for field mapping between Microsoft Project and ServiceNow instances are:

-   True/False
-   Calendar
-   Date/Time
-   Choice
-   Color
-   Currency
-   Decimal
-   Due Date
-   Floating Point Number
-   Date
-   Date/Time
-   Duration
-   List
-   Time
-   HTML
-   Integer
-   Long
-   Percent Complete
-   Phone Number \(E164\)
-   Reference
-   Name -Value Pairs
-   String
-   Translated HTML
-   Translated Text
-   URL
-   Wiki

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Project - MSP Import Field Mappings**.

2.  Select **New**.

3.  From the Table list, select the table in which you created the custom field.

    |Task|Steps|
    |----|-----|
    |**If you created a field in the project table**|Select **Project** from the Table list.|
    |**If you created a field in the project task table**|Select **Project Task** from the Table list.|

4.  In the **Microsoft Project Column** field, enter the name of the custom field in your Microsoft Project file that you want to map.

5.  In the Destination Column list, select the custom ServiceNow field that you want to map to the Microsoft Project field while importing a project.

6.  Select **Submit**.


## What to do next

-   Import the Microsoft Project file. For more information, see [Import a Microsoft Project file with the Import module](t_ImportMicrosoftProjectFiles.md).
-   Configure the Project form to add the custom fields that you want to see. For more information, see Form configuration.

**Parent Topic:**[Importing and exporting projects](../concept/c_ProjectImportAndExport.md)

**Related topics**  


[Project field mapping](../reference/r_ProjectFieldMapping.md)

[Project import from Microsoft Project](../concept/project-import-msp.md)

[Import project tasks for multiple projects](import-project-tasks-multiple-projects.md)

[Project export to Microsoft Project](../concept/c_ProjectExportToMicrosoftProject.md)

[Calendars and schedules- Limitations](../concept/c_CalendarsAndSchedules.md)

[Importing and exporting projects](../concept/c_ProjectImportAndExport.md)

