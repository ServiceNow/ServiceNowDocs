---
title: Project field mapping
description: During an import, values from Microsoft Project overwrite fields in project records.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project import and export, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project field mapping

During an import, values from Microsoft Project overwrite fields in project records.

<table id="table_lkh_ldr_z4"><thead><tr><th>

Microsoft Project fields

</th><th>

Project Management fields

</th></tr></thead><tbody><tr><td>

Task Name

</td><td>

Short description. The field is overwritten only while you import the first time.

</td></tr><tr><td>

Note

</td><td>

Description

</td></tr><tr><td>

Start

</td><td>

Planned start date

</td></tr><tr><td>

Finish

</td><td>

Planned end date

</td></tr><tr><td>

Duration

</td><td>

Planned duration

</td></tr><tr><td>

Actual Start

</td><td>

Actual start date

</td></tr><tr><td>

Actual Finish

</td><td>

Actual end date

</td></tr><tr><td>

Actual Duration

</td><td>

Actual duration

</td></tr><tr><td>

% Complete

</td><td>

Percent complete \(personalize the form to add this field\)

</td></tr><tr><td>

Predecessor Lag

</td><td>

Lag time between predecessor and successor

</td></tr><tr><td>

WBS

</td><td>

WBS

</td></tr><tr><td>

Critical

</td><td>

Critical path

</td></tr><tr><td>

Rollup

</td><td>

Rollup

</td></tr><tr><td>

Text10 \(Field used for syncing purposes\)

</td><td>

Task Sys\_Id

</td></tr><tr><td>

Project Header Title

</td><td>

Project name

</td></tr><tr><td>

Project Header Subject \(Field used for syncing purposes\)

</td><td>

Top Task Sys\_Id

</td></tr><tr><td>

Resource

</td><td>

Assigned to \[assigned\_to\]**Note:** During import, if there are multiple resources assigned to a task in Microsoft Project:

-   The first resource is added to the **Assigned to** field.
-   The rest of the resources are added to the **Additional assignee list** field.

</td></tr><tr><td>

Resource Group

</td><td>

Assignment Group

</td></tr></tbody>
</table>**Parent Topic:**[Project import and export](../concept/c_ProjectImportAndExport.md)

**Related topics**  


[Calendars and schedules- Limitations](../concept/c_CalendarsAndSchedules.md)

[Create custom field mapping for Microsoft Project file import](../task/map-custom-fields-msp-project.md)

[Project import from Microsoft Project](../concept/project-import-msp.md)

[Import project tasks for multiple projects](../task/import-project-tasks-multiple-projects.md)

[Project export to Microsoft Project](../concept/c_ProjectExportToMicrosoftProject.md)

