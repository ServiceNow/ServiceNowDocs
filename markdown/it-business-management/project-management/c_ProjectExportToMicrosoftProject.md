---
title: Project export to Microsoft Project
description: If you are using Microsoft Project to manage project activities, you can export a project to Microsoft Project \(mpp\) file, an XML file, or a CSV file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/c\_ProjectExportToMicrosoftProject.html
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Importing and exporting projects, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
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

-   **[Export project data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/t_ExportAProjectWithTheProjectForm.md)**  
Export the project data using the Export module, Project form, or Planning Console. Save the export file to a folder on your system in the Microsoft Project \(MPP\), XML, or CSV format.

**Parent Topic:**[Importing and exporting projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectImportAndExport.md)

**Related topics**  


[Project field mapping]()

[Create custom field mapping for Microsoft Project file import]()

[Project import from Microsoft Project]()

[Import project tasks for multiple projects]()

[Calendars and schedules- Limitations]()

[Importing and exporting projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_ProjectImportAndExport.md)

