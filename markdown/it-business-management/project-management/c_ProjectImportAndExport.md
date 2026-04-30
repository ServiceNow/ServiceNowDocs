---
title: Project import and export
description: You can manage projects using both Microsoft Project and the ServiceNow Project Management application.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project import and export

You can manage projects using both Microsoft Project and the ServiceNow Project Management application.

## Project Import

Users with it\_project\_manager role can import projects and project tasks from Microsoft Project into ServiceNow Project Management.

Create a project or update an existing project by importing the project data from Microsoft Project into your ServiceNow instance. For more information, see [Project import from Microsoft Project](project-import-msp.md).

While importing a project into your ServiceNow instance, you can also specify the calculation method for calculating project dates. You can import the project tasks with different constraint types using Manual or Automatic calculation. For information about supported constraints and their conversion, see [Project import from Microsoft Project](project-import-msp.md).

You can create custom fields in your ServiceNow instance and map these fields with your Microsoft Project while importing a project. For more information, see [Create custom field mapping for Microsoft Project file import](../task/map-custom-fields-msp-project.md).

You can import project tasks for multiple projects in one time using data files and transform maps. For more information, see [Import project tasks for multiple projects](../task/import-project-tasks-multiple-projects.md).

Some calendar elements are not imported from Microsoft Project into Project Management. For information about calendar elements and schedules, see [Calendars and schedules- Limitations](c_CalendarsAndSchedules.md).

## Project Export

If you have the it\_project\_manager role, you can export project data. The project data, such as project tasks and task constraints, can be exported as an export file. Use this export file to import the projects into other ServiceNow instances.

If you are managing your projects using Microsoft Project, you can export your ServiceNow projects using the export functionality.

You can choose to export the project data in MPP, XML, or CSV file formats. For more information, see [Project export to Microsoft Project](c_ProjectExportToMicrosoftProject.md).

If your project in the ServiceNow instance contains dates with any of the supported constraint types, then these constraints are also exported when you export the project and project tasks. For more information, see [Project export to Microsoft Project](c_ProjectExportToMicrosoftProject.md).

## Supported versions

Projects created in the following versions of Microsoft Project can be imported into the ServiceNow Project Management application.

-   Microsoft Project 2003
-   Microsoft Project 2007
-   Microsoft Project 2010
-   Microsoft Project 2013
-   Microsoft Project 2016

-   **[Calendars and schedules- Limitations](c_CalendarsAndSchedules.md)**  
Some calendar elements from Microsoft Project are not imported into the Project Management application.
-   **[Project field mapping](../reference/r_ProjectFieldMapping.md)**  
During an import, values from Microsoft Project overwrite fields in project records.
-   **[Create custom field mapping for Microsoft Project file import](../task/map-custom-fields-msp-project.md)**  
Map custom fields from Microsoft Project to ServiceNow fields before importing a project.
-   **[Project import from Microsoft Project](project-import-msp.md)**  
Import Microsoft project files into the ServiceNow Project Management application.
-   **[Import project tasks for multiple projects](../task/import-project-tasks-multiple-projects.md)**  
Import project tasks for multiple projects from an external file system or data source using import sets and transform maps.
-   **[Project export to Microsoft Project](c_ProjectExportToMicrosoftProject.md)**  
If you are using Microsoft Project to manage project activities, you can export a project to Microsoft Project \(mpp\) file, an XML file, or a CSV file.

**Parent Topic:**[Project Management](c_ProjectApplicationOverview.md)

