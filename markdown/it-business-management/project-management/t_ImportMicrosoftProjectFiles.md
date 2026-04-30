---
title: Import a Microsoft Project file with the Import module
description: Use the Import module to import a Microsoft project file as a new project into the Project Management application.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Project import from Microsoft Project, Importing and exporting projects, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Import a Microsoft Project file with the Import module

Use the Import module to import a Microsoft project file as a new project into the Project Management application.

## Before you begin

Role required: it\_project\_manager

## About this task

Before importing a Microsoft Project file into the ServiceNow instance, consider the following information.

-   Microsoft Project project imported into a teamspace is only available to users who can access the teamspace.
-   To import custom fields in your Microsoft project, create those custom fields in your ServiceNow instance first, and then create mapping between these fields before importing the project. For more information, see [Create custom field mapping for Microsoft Project file import](map-custom-fields-msp-project.md).

    **Note:** You can also use the Scripted Extension Points for importing custom fields without creating and mapping the custom fields manually. Use the MSProjectImportTaskFormatter Extension Point to create a script include and map custom fields in Microsoft Project and ServiceNow. You can also use this Extension Point to modify the data while importing a project.

-   If the calculation type is set as **Manual**, recalculation does not happen on project tasks when they are imported from the Microsoft Project file. Once the project is in the ServiceNow system, it would be treated as a manual project.
-   Importing a Microsoft Project project with inter-project dependencies, does not import the shadow tasks.
-   Only the subprojects \(header and parent task\) get imported into the ServiceNow instance, the child tasks are not imported.
-   While importing a Microsoft Project file into ServiceNow, the import fails:
    -   If the project with tasks was created in ServiceNow instance before the import.
    -   If you reimport a project that was imported from Microsoft Project file earlier and you create and add tasks in ServiceNow instance.

        **Note:** To retain the project tasks that were created in the ServiceNow instance, you must export that project first into the Microsoft Project file. Then, reimport the file back into ServiceNow instance.

    -   If the task being deleted due to import has any of the related entities: Cost plan, Benefit plan, Resource plan, Time card, or Expense lines.
    -   If the values for lag or lead time dependencies are not in the supported format.
        -   Positive lag time dependency values for days, hours, and minutes are allowed. Negative lag time dependencies are allowed only for days.
        -   All other elapsed duration types from Microsoft Project such as emin, eday, eweek, emon, eyr, or % are not allowed for import.

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Projects** &gt; **Import**.

2.  Select **Choose File** to select a Microsoft Project \(mpp\) file.

3.  To import the Microsoft project as a new project, select the **Create new project** option.

4.  In the **Project name** field, specify a name for the new project.

5.  To import the Microsoft project as a subset of an active, existing project:

    1.  Select **Update an existing project**.

    2.  Select the reference lookup icon \(![Lookup icon](../image/IconReferencelookup.png)\) and select a project or task.

        Only active projects appear in the list.

6.  Select one of the following options to specify the method for calculating schedule:

    -   **Automatic**: Select this option to apply the scheduling engine while importing the project tasks. The supported constraint types are imported with same constraints applied to them while other constraint types are converted to **Start on specific date**.
    -   **Manual**: Select this option to import all project tasks with **Start on specific date** constraint type irrespective of their constraint type in Microsoft Project.
    For more information about supported constraint types, see [Project import from Microsoft Project](../concept/project-import-msp.md#ul_gsp_tlz_bq).

7.  Select **Import**.


## Result

-   A project task that was imported in ServiceNow instance earlier and has associated time cards, resource plans, cost plan, benefit plan, or expense lines is retained on reimport even if it is deleted from Microsoft Project.
-   Dates in the ServiceNow project remain same as the dates in the Microsoft Project file.
-   In a ServiceNow project with subprojects, the following details change:
    -   The WBS order of imported tasks is regenerated after import.
    -   The **Planned Start Date** and **Planned End Date** of the parent project are rolled up.
    -   The **State** of the parent project and tasks are rolled up.
    -   The % Complete on the top task is rolled up.

**Parent Topic:**[Project import from Microsoft Project](../concept/project-import-msp.md)

**Related topics**  


[Importing and exporting projects](../concept/c_ProjectImportAndExport.md)

