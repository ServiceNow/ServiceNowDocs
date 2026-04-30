---
title: Update a project using a Microsoft Project file
description: Import project data, from a Microsoft Project file, into an existing project in your ServiceNow instance using the Project form or Planning Console.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Project import from Microsoft Project, Importing and exporting projects, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Update a project using a Microsoft Project file

Import project data, from a Microsoft Project file, into an existing project in your ServiceNow instance using the Project form or Planning Console.

## Before you begin

Create a [project](t_CreateAProject.md).

Role required: it\_project\_manager

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **All**.

2.  Open the project which you want to update.

3.  Import the Microsoft Project file to update the selected project from any of the following screens:

    -   In the Project form, select **Import from MS Project** from the context menu.
    -   In the Planning Console, select the more actions icon \(![More actions icon](../image/elipsis_icon.png)\) and select the **Import from MS Project** option.
4.  In the Microsoft Project Import dialog box, select the Microsoft Project file and calculation type:

    1.  Select **Choose File** to select a Microsoft Project \(mpp\) file.

    2.  Select one of the following options to specify the method for calculating the schedule:

        -   **Automatic**: Select this option to apply the scheduling engine while importing the project tasks. The supported constraint types are imported with the same constraints applied to them while other constraint types are converted to **Start on specific date**.
        -   **Manual**: Select this option to import all project tasks with the **Start on specific date** constraint type irrespective of their constraint type in Microsoft Project.
        For more information about the supported constraint types, see [Project import from Microsoft Project](../concept/project-import-msp.md#ul_gsp_tlz_bq).

5.  Select **Import**.


## Result

-   A project task that was imported in the ServiceNow instance earlier and has associated time cards, resource plans, cost plan, benefit plan, or expense lines is retained on reimport even if it is deleted from Microsoft Project.
-   Dates in the ServiceNow project remain same as the dates in the Microsoft Project file.
-   In a ServiceNow project with subprojects, the following details change:
    -   The WBS order of imported tasks is regenerated after import.
    -   The **Planned Start Date** and **Planned End Date** of the parent project are rolled up.
    -   The **State** of the parent project and tasks are rolled up.
    -   The **% Complete** on the top task is rolled up.

**Parent Topic:**[Project import from Microsoft Project](../concept/project-import-msp.md)

**Related topics**  


[Importing and exporting projects](../concept/c_ProjectImportAndExport.md)

