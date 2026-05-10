---
title: Components installed with Workplace Core
description: Several types of components are installed with installation of the Workplace Core application, including user roles, scheduled jobs, tables, and business rules.
locale: en-US
release: australia
product: Workplace Core
classification: workplace-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Workplace Core references, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Core

Several types of components are installed with installation of the Workplace Core application, including user roles, scheduled jobs, tables, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

Demo data is available for this feature.

## Roles

<table id="table_dqg_gb5_prb"><thead><tr><th>

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
-   Manages planned maintenance tasks

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
-   Read Task templates.

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

</td></tr><tr><td>

Workplace entity reader\[sn\_wsd\_core.workplace\_entity\_reader\]

</td><td>

Has permission to read the Workplace Entity \[sn\_wsd\_core\_workplace\_entity\] and Entity Type \[sn\_wsd\_core\_entity\_type\] tables.This role is required by workplace users to create any requests based on Workplace Entities.

</td><td>

None

</td></tr><tr><td>

Workplace entity writersn\_wsd\_core.workplace\_entity\_writer

</td><td>

Has permissions to create and edit records in the Workplace Entity \[sn\_wsd\_core\_workplace\_entity\] and Entity Type \[sn\_wsd\_core\_entity\_type\] tables.

</td><td>

sn\_wsd\_core.workplace\_entity\_reader

</td></tr><tr><td>

Workplace core neighborhood readersn\_wsd\_core\_neighborhood\_reader

</td><td>

Any user with workplace manager role and space planner role has permission to read neighborhood.

</td><td>

None

</td></tr><tr><td>

Workplace core neighborhood writersn\_wsd\_core\_neighborhood\_writer

</td><td>

Any user with workplace manager role and space planner role has permission to read and write neighborhood.

</td><td>

None

</td></tr></tbody>
</table>## Tables

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Space Suggestions \[sn\_wsd\_core\_user\_space\_suggestions\]

</td><td>

Cache table for user preferred or recommended spaces. Has list view fields \(User, Building, and Suggestions\)**Note:** The sn\_wsd\_concierge.admin role can read, create, edit, and delete records in the table in both form and list views.The sn\_wsd\_core.workplace\_user has READ configuration used when receiving suggestions. Users with sn\_wsd\_core.workplace\_user role can only see the records created for them, and the records are read-only.

For more information, see [User Space Suggestions](../../workplace-concierge/task/userspace-suggestions.md).

</td></tr><tr><td>

Space Suggestions

</td><td>

Cache table for space suggestions for employees. The suggestion type field contains the drop down in the form view fields \(Location, Favorites, Past and Future reservations, Collaborator location and Standard services\). Weight should be a positive number \(integer\). If a negative number is entered and saved, application shows an error message. For more information, see [Space suggestion Configuration](../../workplace-concierge/task/space-suggestion-configuration.md).**Note:** The sn\_wsd\_concierge.admin role can read, create, edit, and delete records in the table in both form and list views.The sn\_wsd\_core.workplace\_user has READ configuration used when receiving suggestions. Users with sn\_wsd\_core.workplace\_user role can only see the records created for them, and the records are read-only.

</td></tr><tr><td>

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

Location Migration Configurationsn\_wsd\_core\_location\_migration

</td><td>

Stores information about all the location migration configurations.

</td></tr><tr><td>

Planned Task Definition\[sn\_wsd\_core\_planned\_task\_def\]

</td><td>

Stores the planned task definitions that workplace managers create for workplace tasks.

</td></tr><tr><td>

QR Code\[sn\_wsd\_core\_qr\]

</td><td>

Stores information about all the QR codes generated in the application.

</td></tr><tr><td>

Region\[sn\_wsd\_core\_region\]

</td><td>

Stores the list of regions of workplace locations.

</td></tr><tr><td>

Room\[sn\_wsd\_core\_room\]

</td><td>

Stores information about all the rooms.

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

Stores the relationship between shifts and employees.For existing users who are upgrading from the first version of the app, ensure that you have the **User** field as the display value. For more information, see [Select a field as the table display value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_SelectTheDisplayValue.md).

</td></tr><tr><td>

User Workplace Profile\[sn\_wsd\_core\_workplace\_profile\]

</td><td>

Stores the relationship between employees and their designated workspaces.

</td></tr><tr><td>

Workplace Safety User\[sn\_wsd\_core\_workplace\_user\]

</td><td>

Stores information about all the Workplace Service Delivery users.

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

 If you are upgrading from version 1.1.1 or earlier of the app, ensure that the **Default Value** field is empty for the workplace\_task\_type column of this table. For more information on how to modify the default display value of a table column, see [Specify a default field value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_SpecifyingADefaultValue.md).

</td></tr><tr><td>

Workplace rooms\[sn\_wsd\_core\_room\]

</td><td>

Extends the Space \[sn\_wsd\_core\_space\] table. It holds the reservable items of a room that are available to reserve.

</td></tr><tr><td>

Workplace Performer Criteria\[sn\_wsd\_core\_performer\_criteria\]

</td><td>

Extends the Application file table. Stores information about all the performer criteria created in the application. The performer criteria stores the list of users who are eligible to perform approval-related actions.

</td></tr><tr><td>

Workplace Approval Definition\[sn\_wsd\_core\_approval\_definition\]

</td><td>

Extends the Application file table. Stores information about all the approval definitions. The tables store information such as which entities require approval.

</td></tr><tr><td>

Workplace Approval Configuration\[sn\_wsd\_core\_approval\_configuration\]

</td><td>

Extends the Application file table. Stores information about all the workplace approval configurations.

</td></tr><tr><td>

Workplace space type\[sn\_wsd\_core\_space\_type\]

</td><td>

Stores information about Workplace space types that are referenced to Indoor Mapping place types for indoor navigation.

</td></tr><tr><td>

Workplace core neighborhood\[sn\_wsd\_core\_neighborhood\]

</td><td>

Stores information about neighborhood.

</td></tr><tr><td>

Workplace core neighborhood space association\[sn\_wsd\_core\_neighborhood\_m2m\_space\]

</td><td>

Stores information about neighborhood space association.

</td></tr><tr><td>

Workplace core neighborhood space user assignment\[sn\_wsd\_core\_neighborhood\_user\_assignment\]

</td><td>

Stores information about neighborhood user assignment rule.

</td></tr><tr><td>

Workplace Card Configuration\[sn\_wsd\_core\_card\_configuration\]

</td><td>

Stores configurations for the cards that are used across Workplace applications.

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Core references](../concept/wsd-references.md)

**Related topics**  


[Properties installed with Workplace Core](properties-installed-with-workplace-service-delivery.md)

[Workplace Profile Location Assignment form](wsd-location-assignment-form.md)

[Workplace location assignment anomaly types](location-assignment-anomaly-types.md)

[Reserve a space form](reserve-space-form.md)

[Card Configuration examples](card-configuration-examples.md)

