---
title: Import project tasks for multiple projects
description: Import project tasks for multiple projects from an external file system or data source using import sets and transform maps.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Importing and exporting projects, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Import project tasks for multiple projects

Import project tasks for multiple projects from an external file system or data source using import sets and transform maps.

## Before you begin

Role required: import\_transformer, import\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Select the **Existing table** option.

3.  From the Import set table list, select the **Import planned task \[imp\_planned\_task\]** option.

4.  In the **Source of the import** field, select File, and then select **Choose File** to select the source Excel spreadsheet.

5.  If required, specify the Work sheet and Header row number.

6.  Select **Submit**

    The imported data is available in the selected Import Set table.

7.  Create field mappings for custom columns.

    For more information, see Create field mappings.

8.  Transform the data from the import set table to the target table.

    For more information, see Run an import.


**Parent Topic:**[Importing and exporting projects](../concept/c_ProjectImportAndExport.md)

**Related topics**  


[Project field mapping](../reference/r_ProjectFieldMapping.md)

[Create custom field mapping for Microsoft Project file import](map-custom-fields-msp-project.md)

[Project import from Microsoft Project](../concept/project-import-msp.md)

[Project export to Microsoft Project](../concept/c_ProjectExportToMicrosoftProject.md)

[Calendars and schedules- Limitations](../concept/c_CalendarsAndSchedules.md)

[Importing and exporting projects](../concept/c_ProjectImportAndExport.md)

