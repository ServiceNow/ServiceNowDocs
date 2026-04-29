---
title: Components installed with Workplace Space Management
description: Several types of components are installed with the Workplace Space Management application, including tables and user roles.
locale: en-US
release: australia
product: Workplace Space Management
classification: workplace-space-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Space Management

Several types of components are installed with the Workplace Space Management application, including tables and user roles.

Demo data is available for this feature.

## Roles installed with Workplace Space Management

<table id="table_rpj_13j_qpb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_wsd\_spcmgmt.admin

</td><td>

As a Workplace Space Management admin, you can access the application completely.

</td><td>

sn\_wsd\_spcmgmt.manager

</td></tr><tr><td>

sn\_wsd\_spcmgmt.manager

</td><td>

As a Workplace Space Manager, you can access the application completely.

</td><td>

None

</td></tr><tr><td>

sn\_wsd\_spcmgmt.space\_planner

</td><td>

As a workplace space planner, you can create a scenario and deploy it

</td><td>

-   sn\_wsd\_core.task\_reader
-   sn\_wsd\_move.reader
-   sn\_wsd\_core.task\_reader
-   sn\_wsd\_core.profile\_writer
-   sn\_wsd\_central.workspace\_user
-   view\_changer
-   sn\_wsd\_spcmgmt.manager
-   sn\_wsd\_core.location\_writer

</td></tr><tr><td>

sn\_wsd\_spcmgmt.scenario\_reader

</td><td>

As a workplace scenario reader, you can view scenarios in a read-only mode.

</td><td>

sn\_wsd\_central.workspace\_user

</td></tr><tr><td>

sn\_wsd\_spcmgmt.schedule\_plan\_reader

</td><td>

As a Schedule Plan reader, you can view schedule plans in the read-only mode.

</td><td>

None

</td></tr><tr><td>

sn\_wsd\_spcmgmt.schedule\_plan\_writer

</td><td>

As a Schedule Plan writer, you can create and edit schedule plans.

</td><td>

sn\_wsd\_spcmgmt.schedule\_plan\_reader

</td></tr><tr><td>

sn\_wsd\_spcmgmt.project\_owner

</td><td>

As a Project Owner, you can create and manage Schedule Plans.

</td><td>

-   sn\_wsd\_spcmgmt.schedule\_plan\_writer
-   sn\_wsd\_core.workplace\_user
-   sn\_wsd\_core.task\_reader
-   sn\_wsd\_core.profile\_reader
-   sn\_wsd\_core.location\_reader
-   sn\_wsd\_central.workspace\_user
-   sn\_wsd\_core.shift\_reader

</td></tr></tbody>
</table>## Tables installed with Workplace Space Management

**Note:** Neighborhood is moved from Workplace Space Management \[version\] to Workplace Core \[version\]. For more information, see [Components installed with Workplace Core](../../workplace-service-delivery/reference/components-installed-with-workplace-service-delivery.md).

<table id="table_t5k_1kj_qpb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allocation\[sn\_wsd\_spcmgmt\_location\_cc\_dept\_map\]

</td><td>

Stores information about all the cost centers and departments that are created in the application.

</td></tr><tr><td>

Workplace Location Status Tracker\[sn\_wsd\_spcmgmt\_location\_status\_tracker\]

</td><td>

Stores information about all the status changes of the locations.

</td></tr><tr><td>

Neighborhood\[sn\_wsd\_spcmgmt\_neighborhood\]

</td><td>

Stores information about a neighborhood allocated to a cost center, department, or a group.This table is deprecated from Workplace Space Management version 1.17.0.

</td></tr><tr><td>

Neighborhood user assignment rule\[sn\_wsd\_spcmgmt\_neighborhood\_user\_assignment\]

</td><td>

Stores information about neighborhood user assignment rule to create and add new users to a neighborhood.This table is deprecated from Workplace Space Management version 1.17.0.

</td></tr><tr><td>

Neighborhood space\[sn\_wsd\_spcmgmt\_neighborhood\_m2m\_space\]

</td><td>

Stores information about a neighborhood space.This table is deprecated from Workplace Space Management version 1.17.0.

</td></tr><tr><td>

View by Configuration\[sn\_wsd\_spcmgmt\_view\_by\_configuration\]

</td><td>

Stores information about the view by configurations created for Scenario Planning or Building Overview.

</td></tr><tr><td>

Schedule Plan\[sn\_wsd\_spcmgmt\_schedule\_plan\]

</td><td>

Stores information such as the start date, end date, and the selected schedule for Schedule Plans.

</td></tr><tr><td>

Schedule Plan Space\[sn\_wsd\_spcmgmt\_schedule\_plan\_space\]

</td><td>

Stores information about the workspaces selected for Schedule Plans.

</td></tr><tr><td>

Schedule Plan User\[sn\_wsd\_spcmgmt\_schedule\_plan\_user\]

</td><td>

Stores information about the users selected for Schedule Plans.

</td></tr><tr><td>

Schedule Plan User Space\[sn\_wsd\_spcmgmt\_schedule\_plan\_user\_space\]

</td><td>

Stores information about the user to space mapping and validation issues for Schedule Plans.

</td></tr><tr><td>

Space Allocation Type Change Tracker\[sn\_wsd\_spcmgmt\_space\_allocation\_type\_change\_tracker\]

</td><td>

Stores information about changes made to types of allocation, which can be reviewed to plan and edit scenarios.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Space Management references](../concept/workplace-space-mgmt-references.md)

**Related topics**  


[Properties installed with Workplace Space Management](properties-installed-with-workplace-space-mgmt.md)

[View by Configuration form](view-by-configuration-form.md)

