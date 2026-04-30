---
title: Project export to Microsoft Project
description: If you are using Microsoft Project to manage project activities, you can export a project to Microsoft Project \(mpp\) file, an XML file, or a CSV file.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project import and export, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project export to Microsoft Project

If you are using Microsoft Project to manage project activities, you can export a project to Microsoft Project \(mpp\) file, an XML file, or a CSV file.

Users with the project manager role can export a project using:

-   Export module
-   Project form
-   Planning Console

You can also specify the format in which you want to export project data, the available options are:

-   **XML**: Suitable, if you want to import the project data into other ServiceNow instance.
-   **CSV**: Suitable for exporting project data from Planning Console as is and viewing project data using other applications.
-   **Microsoft Project**: Suitable, if you want to import the project data into Microsoft Project.

    **Note:** The option for exporting project data in CSV and Microsoft Project format is available when exporting a project from Planning Console.


If tasks in your project contain any of the supported constraints, then the constraints are also exported when you export the project. This export of constraints helps you in maintaining project dates when you import the project to another ServiceNow instance. The following constraints are supported:

-   **Start on specific date**: Mapped with Must start on constraint when exported to Microsoft project.
-   **As soon as possible**
-   **Start no later than**
-   **Start no earlier than**

**Note:** Shadow tasks and external dependencies are not exported when you export the project data.

-   **[Export project data](../task/t_ExportAProjectWithTheProjectForm.md)**  
Export the project data using the Export module, Project form, or Planning Console. Save the export file to a folder on your system in the Microsoft Project \(MPP\), XML, or CSV format.

**Parent Topic:**[Project import and export](c_ProjectImportAndExport.md)

**Related topics**  


[Calendars and schedules- Limitations](c_CalendarsAndSchedules.md)

[Project field mapping](../reference/r_ProjectFieldMapping.md)

[Create custom field mapping for Microsoft Project file import](../task/map-custom-fields-msp-project.md)

[Project import from Microsoft Project](project-import-msp.md)

[Import project tasks for multiple projects](../task/import-project-tasks-multiple-projects.md)

