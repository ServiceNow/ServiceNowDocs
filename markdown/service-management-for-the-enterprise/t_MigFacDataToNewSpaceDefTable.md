---
title: Migrate facilities data to new space definition tables
description: To continue using the image-based floor plans with the new space definition, migrate your data from the old tables to the new space definition tables.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate Facilities Visualization Workbench, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Migrate facilities data to new space definition tables

To continue using the image-based floor plans with the new space definition, migrate your data from the old tables to the new space definition tables.

## Before you begin

Role required: facilities\_admin

## About this task

The migration process only migrates complete data. A space that is not in a level or a level not in a building is not migrated. This behavior can be changed by updating the migration script include. Floors that are not connected to a building are not migrated, nor are spaces that are not part of a floor or building. As part of the migration process, the legacy spaces, floors, and buildings are marked as migrated.

The migration path for the old tables to the new are:

-   \[cmn\_building\] migrates to \[alm\_building\]
-   \[fpv\_floor\] migrates to \[fm\_level\]
-   \[fpv\_element\] migrates to \[fm\_space\]

## Procedure

1.  Navigate to **All** &gt; **Facilities** &gt; **Administration** &gt; **Migrate**.

2.  Click **Migrate**.


## Result

The following results can be expected:

-   Data is migrated to the new facilities management tables for buildings, floors, and spaces.
-   After a building, floor, or space is migrated, it is marked as migrated, and is not able to be migrated again.

    **Note:** Any object that is marked as migrated does not get migrated again, so you can safely run through the migration process multiple times without creating duplicated objects in the space tables. This behavior can be modified in the migration script include or by resetting the migration flag on the original objects.


**Parent Topic:**[Activate Facilities Visualization Workbench](../../facilities-interactive-facility-maps/task/t_ActivateFacVisWorkbench.md)

