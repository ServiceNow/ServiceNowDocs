---
title: Components installed with Workplace Core
description: Several types of components are installed with installation of the Workplace Core application, including user roles, scheduled jobs, tables, and business rules.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Install Workplace Core, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Components installed with Workplace Core

Several types of components are installed with installation of the Workplace Core application, including user roles, scheduled jobs, tables, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Roles installed with Workplace Core

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Workplace admin\[sn\_wsd\_core.admin\]

</td><td>

-   Sets up data about the workplace
-   Has complete access to the application

</td><td>

sn\_wsd\_core.workplace\_manager

</td></tr><tr><td>

Workplace manager\[sn\_wsd\_core.workplace\_manager\]

</td><td>

-   Reserves spaces at the workplace
-   Links employees and shifts to spaces
-   Manages preventive maintenance tasks

</td><td>

-   sn\_wsd\_core.workplace\_exposure\_analyst
-   schedule\_admin
-   template\_editor\_global

</td></tr><tr><td>

Workplace exposure analyst\[sn\_wsd\_core.workplace\_exposure\_analyst\]

</td><td>

Identifies potentially exposed employees in the ServiceNow® Emergency Exposure Management application using workspace reservations.

</td><td>

None

</td></tr><tr><td>

Workplace shift owner\[sn\_wsd\_core.workplace\_shift\_owner\]

</td><td>

-   Has edit access to the shifts that they own.
-   Has edit access to details such as shift schedules, associated users, and spaces of owned shifts.
-   Has read-only access to workplace tasks of owned shifts.
-   Can view workspace requests and reservations for owned shifts

</td><td>

None

</td></tr><tr><td>

Workplace user\[sn\_wsd\_core.workplace\_user\]

</td><td>

-   Requests area or workspace reservations from the Workplace Service Portal or the Now® Mobile app
-   Schedules arrival to workplace locations using the Workplace Service Portal or the Now® Mobile app

 **Note:** From Workplace Core v1.3.2 onwards, this role is required for employees to request reservations from Workplace Service Portal.

</td><td>

None

</td></tr><tr><td>

Workplace core writer\[sn\_wsd\_core.task\_writer\]

</td><td>

-   Create, read, update, and delete Workplace Tasks.
-   Create, read, update, and delete Task templates.

</td><td>

sn\_wsd\_core.task\_reader

</td></tr><tr><td>

Workplace core reader\[sn\_wsd\_core.task\_reader\]

</td><td>

Has permission to read all workplace tasks.

</td><td>

None

</td></tr><tr><td>

Workplace knowledge base writer\[sn\_wsd\_core.kb\_writer\]

</td><td>

-   Create, view, publish, and update knowledge base articles.
-   Retire and republish knowledge base articles.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed with Workplace Core

<table id="table_n1f_t4w_2mb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Find upcoming reservation periodically

</td><td>

Finds upcoming workspace reservations between 4–8 hours from the time when this job is executed and sends email notifications to those employees with reservations.

 By default, this job is set to run every 4 hours.

</td></tr><tr><td>

Reservation check-in &amp; check-out

</td><td>

Performs the following actions.-   Notifies employees via email to check in a reservation.
-   Notifies employees via email to check out a reservation.
-   Auto cancels a reservation if it is not checked in within 30 minutes after the employee is notified.
-   Auto checks out a reservation if it is not checked out an hour after the reservation end time.

</td></tr></tbody>
</table>## Tables installed with Workplace Core

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Area\[sn\_wsd\_core\_area\]

</td><td>

Stores the list of areas on office floors.

</td></tr><tr><td>

Arrival Entry\[sn\_wsd\_core\_arrival\_entry\]

</td><td>

Stores the list of scheduled arrival entries of the employees.

</td></tr><tr><td>

Arrival Schedule\[sn\_wsd\_core\_arrival\_schedule\]

</td><td>

Store the list of scheduled arrival intervals created by the workplace manager.

</td></tr><tr><td>

Building\[sn\_wsd\_core\_building\]

</td><td>

Stores the list of office buildings.

</td></tr><tr><td>

Campus\[sn\_wsd\_core\_campus\]

</td><td>

Stores the list of office campuses.

</td></tr><tr><td>

Floor\[sn\_wsd\_core\_floor\]

</td><td>

Stores the list of office floors.

</td></tr><tr><td>

Html Signing Template\[sn\_wsd\_core\_html\_signing\_template\]

</td><td>

Stores the templates to sign off on a planned task and generate a PDF.

</td></tr><tr><td>

Location Shift\[sn\_wsd\_core\_m2m\_location\_shift\]

</td><td>

Stores the relationship between shifts and workspace locations.

</td></tr><tr><td>

Planned Task Definition\[sn\_wsd\_core\_planned\_task\_def\]

</td><td>

Stores the planned task definitions that workplace managers create for workplace tasks.

</td></tr><tr><td>

Region\[sn\_wsd\_core\_region\]

</td><td>

Stores the list of regions of workplace locations.

</td></tr><tr><td>

Reservation\[sn\_wsd\_core\_reservation\]

</td><td>

Stores the relationship between shifts, employees, and workspaces.

</td></tr><tr><td>

Shift\[sn\_wsd\_core\_shift\]

</td><td>

Stores the list of shifts.

</td></tr><tr><td>

Site\[sn\_wsd\_core\_site\]

</td><td>

Stores the list of sites of the organization.

</td></tr><tr><td>

Space\[sn\_wsd\_core\_space\]

</td><td>

Stores the list of workspaces of the organization.

</td></tr><tr><td>

Space Type\[sn\_wsd\_core\_space\_type\]

</td><td>

Stores the list of space type configuration created by the workplace manager.

</td></tr><tr><td>

Space Staging\[sn\_wsd\_core\_space\_staging\]

</td><td>

Acts as an interim placeholder table for imported data about spaces.

</td></tr><tr><td>

User Shift\[sn\_wsd\_core\_m2m\_user\_shift\]

</td><td>

Stores the relationship between shifts and employees.For existing users who are upgrading from the first version of the app, ensure that you have the **User** field as the display value. For more information, see [Select a field as the table display value](https://www.servicenow.com/docs/access?context=t_SelectTheDisplayValue&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

User Workplace Profile\[sn\_wsd\_core\_workplace\_profile\]

</td><td>

Stores the relationship between employees and their designated workspaces.

</td></tr><tr><td>

Workplace Client Role Rule\[sn\_wsd\_core\_client\_role\_rule\]

</td><td>

Stores the workplace client role assignment rules created for employees.

</td></tr><tr><td>

Workplace Location\[sn\_wsd\_core\_workplace\_location\]

</td><td>

Parent table for all workspace entity tables such as Regions, Sites, Campuses, Buildings, Floors, Areas, and Spaces.

</td></tr><tr><td>

Workplace Request\[sn\_wsd\_core\_workplace\_request\]

</td><td>

Stores the workplace reservation requests created by employees.

</td></tr><tr><td>

Workplace Task\[sn\_wsd\_core\_workplace\_task\]

</td><td>

Stores all the workplace tasks created for shifts.

 If you are upgrading from version 1.1.1 or earlier of the app, ensure that the **Default Value** field is empty for the workplace\_task\_type column of this table. For more information on how to modify the default display value of a table column, see [Specify a default field value](https://www.servicenow.com/docs/access?context=t_SpecifyingADefaultValue&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Workplace rooms\[sn\_wsd\_core\_room\]

</td><td>

Extends the Space \[sn\_wsd\_core\_space\] table. It holds the reservable items of a room that are available to reserve.

</td></tr></tbody>
</table>**Parent Topic:**[Install Workplace Core](../task/install-workplace-safety-mgmt-hr.md)

