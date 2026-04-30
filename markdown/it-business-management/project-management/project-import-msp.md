---
title: Project import from Microsoft Project
description: Import Microsoft project files into the ServiceNow Project Management application.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project import and export, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project import from Microsoft Project

Import Microsoft project files into the ServiceNow Project Management application.

Users with the project manager role can import a project using:

-   Import module
-   Project form
-   Planning Console

When you import a project as a new project or into an existing project, the projects are updated as follows:

-   New project: A new record is created in the Project \[pm\_project\] table. The tasks associated with the project are added to the Project Task \[pm\_project\_task\] table.

    Only the common or [mapped fields](../reference/r_ProjectFieldMapping.md) are imported. Imported projects are brought into the instance with both Priority and Risk set to Low.

-   Existing project: The instance checks the Text10 field in the top-level Microsoft Project task. If the Text10 field contains a recognizable sys\_id, it means that the project was previously exported from a ServiceNow instance. In this case, the values from the project overwrite the values for the existing project.

You can also specify the schedule calculation type as **Automatic** or **Manual** for the imported tasks. When you import a project into the instance, project constraints are converted as follows:

-   The time constraint for all imported tasks, when you select calculation type as **Manual**, is set to **Start on specific date** irrespective of their constraint type in Microsoft Project.
-   The following constraint types are supported when you select calculation type as **Automatic**:

    -   **Start on specific date**
    -   **As soon as possible**
    -   **Start no later than**
    -   **Start no earlier than**
    Tasks with other constraint types are converted to **Start on specific date**.


**Note:** The resource name in Microsoft Project should map to the name of the user in the instance.

-   **[Import a Microsoft Project file with the Import module](../task/t_ImportMicrosoftProjectFiles.md)**  
Use the Import module to import a Microsoft project file as a new project into the Project Management application.
-   **[Update a project using a Microsoft Project file](../task/import-prj-pc-pf.md)**  
Import project data, from a Microsoft Project file, into an existing project in your ServiceNow instance using the Project form or Planning Console.

**Parent Topic:**[Project import and export](c_ProjectImportAndExport.md)

**Related topics**  


[Calendars and schedules- Limitations](c_CalendarsAndSchedules.md)

[Project field mapping](../reference/r_ProjectFieldMapping.md)

[Create custom field mapping for Microsoft Project file import](../task/map-custom-fields-msp-project.md)

[Import project tasks for multiple projects](../task/import-project-tasks-multiple-projects.md)

[Project export to Microsoft Project](c_ProjectExportToMicrosoftProject.md)

