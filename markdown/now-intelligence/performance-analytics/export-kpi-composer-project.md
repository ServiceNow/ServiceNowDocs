---
title: Export a KPI Composer project
description: To copy a KPI Composer project between instances, first export the project as a JSON file.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [KPI Composer projects, Design your indicator solution, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Export a KPI Composer project

To copy a KPI Composer project between instances, first export the project as a JSON file.

Prerequisites
:   [Create a KPI Composer project](create-kpi-composer-project.md)

## Before you begin

Role required: sn\_kpi\_composer.admin

## About this task

The following fields are not exported with a project:

-   Responsible users
-   Contacts
-   Project journal entries
-   References to knowledge articles

## Procedure

1.  Navigate to **KPI Composer**.

    The page of project cards opens.

2.  From the **Options** menu of the project you want to export, select **Export**.

    ![Options menu on a project card showing Export option.](../image/kpi-comp-export-project.png)

3.  Read the notice about which fields are not exported.

4.  Click **Download**.


## Result

The KPI Composer project is saved in a JSON file in the download destination of your computer. The file name has the format `ProjectExport.[Project_name].[Timestamp].json`. For example, for a project named Incident Cost Project, the export file name is `ProjectExport.Incident_Cost_Project.2021-11-22_19_13_20.json`.

**Parent Topic:**[KPI Composer projects](../concept/kpi-composer-projects.md)

**Previous topic:**[Share a KPI Composer project](share-a-kpi-composer-project.md)

**Next topic:**[Import a KPI Composer project](import-kpi-composer-project.md)

