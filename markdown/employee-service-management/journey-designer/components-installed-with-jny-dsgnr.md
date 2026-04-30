---
title: Components installed with Journey designer
description: Several types of components install with the activation of the Journey designer application, including user roles and tables.
locale: en-US
release: zurich
product: Journey Designer
classification: journey-designer
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Components installed with Journey designer

Several types of components install with the activation of the Journey designer application, including user roles and tables.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Demo data is available for the Journey designer application. If you want to install the demo data, click **Load demo data** when installing this application. Demo data includes sample records and configurations for common use cases.

There are also dependencies on other features or apps.

## Roles

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Inherits

</th><th>

Inherited by

</th></tr></thead><tbody><tr><td>

Administrator \[sn\_jny.admin\]

</td><td>

Grants access to create and manage all Journey designer and Journey Accelerator configurations and features.

</td><td>

-   \[sn\_ja.admin\]
-   \[sn\_jny.writer\]
-   \[taxonomy\_admin\]
-   \[sn\_hr\_le.admin\]
-   \[user\_criteria\_admin\]

</td><td>

sn\_hr\_core.admin

</td></tr><tr><td>

Modifier\[sn\_jny.writer\]

</td><td>

Grants access to create and modify Journey components, such as plans, stages, and to-dos.

</td><td>

-   \[sn\_jny.reader\]
-   \[sn\_ja.modifier\]

</td><td>

\[sn\_jny.admin\]

</td></tr><tr><td>

Reader\[sn\_jny.reader\]

</td><td>

Grants access to view journeys and complete tasks assigned to them.

</td><td>

\[sn\_ja.reader\]

</td><td>

sn\_hr\_core.case\_reader

</td></tr></tbody>
</table>You can assign these roles to the appropriate roles, groups, or users in your application.

-   To assign a role to another role, see [Add a role to an existing role](https://www.servicenow.com/docs/access?context=t_AddARoleToAnExistingRole&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Modules with Role

|Module|Table|Role|
|------|-----|----|
|Journeys Guided Setup|Journey Configuration \[sn\_jny\_journey\_config\]|sn\_jny.admin|
|Manage Journey Configurations|Journey Configuration \[sn\_jny\_journey\_config\]|sn\_jny.admin|
|Manage Journey Types|Journey Type \[sn\_jny\_journey\_type\]|sn\_jny.admin|
|Manage Heading Configurations|Heading Configuration \[sn\_jny\_journey\_heading\_config\]|sn\_jny.admin|
|Manager Journey Type Links|Journey Type Quick Link \[sn\_jny\_m2m\_journey\_type\_quick\_link\]|sn\_jny.admin|
|Manage Roles|User Role \[sys\_user\_has\_role\]|sn\_jny.admin|
|Journeys|Journey \[sn\_jny\_journey\]|sn\_jny.reader|
|Active Journeys Dashboards|\(no table\)|sn\_jny.reader|
|Journey Usage Dashboard|\(no table\)|sn\_jny.reader|
|Reports|Reports \[sys\_report\]|sn\_jny.reader|

## Tables

<table><thead><tr><th>

Table name \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Available For \[sn\_jny\_m2m\_journey\_config\_user\_criteria\]

</td><td>

Contains and tracks users that meet the criteria to access recommended learning courses.

</td></tr><tr><td>

Field Mapping \[sn\_jny\_journey\_field\_mapping\]

</td><td>

Map fields, custom text, or custom scripts to fields used in a journey. These field mappings are from HR tables and fields to Journey designer or Journey Accelerator tables and fields.

</td></tr><tr><td>

Heading Configuration \[sn\_jny\_journey\_heading\_config\]

</td><td>

Contains details about Journey designer header configurations.

</td></tr><tr><td>

Heading Field \[sn\_jny\_journey\_heading\_field\_config\]

</td><td>

Contains details about Journey designer heading fields and tracks changes related to field labels.

</td></tr><tr><td>

Journey \[sn\_jny\_journey\]

</td><td>

Contains and manages Journey designer plans and journeys relation to other tables.

</td></tr><tr><td>

Journey Audit \[sn\_jny\_journey\]

</td><td>

Tracks CRUD actions on plan configurations and who made them.

</td></tr><tr><td>

Journey bulk request task \[sn\_jny\_bulk\_request\]

</td><td>

Tracks information about bulk updates. Admins can use this table to understand and troubleshoot bulk updates if there are errors or failures.

</td></tr><tr><td>

Journey Configuration\[sn\_jny\_journey\_config\]

</td><td>

Contains details about Journey designer plan and journey configurations.

</td></tr><tr><td>

Journey Configuration Quick Link\[sn\_jny\_m2m\_journey\_config\_quick\_link\]

</td><td>

Manages the relationship of quick links that are added to plans and journeys.

</td></tr><tr><td>

Journey Mobile Carousel \[sn\_jny\_st\_jny\_mobile\_carousel\]

</td><td>

Manages data that is presented in the carousel on the Now Mobile App.

</td></tr><tr><td>

Journey Progress \[sn\_jny\_journey\_progress\]

</td><td>

Manages data related to tracking how a journey is progressing against milestones for tasks completion.

</td></tr><tr><td>

Journey Quick Link \[sn\_jny\_journey\_quick\_link\]

</td><td>

Contains details about quick links in Journey designer.

</td></tr><tr><td>

Journey Quick Links \[sn\_jny\_st\_journey\_quick\_links\]

</td><td>

Manages the data for quick links in journeys.

</td></tr><tr><td>

Journey Tasks \[sn\_jny\_st\_journey\_task\]

</td><td>

Tracks activity for task templates in journey configurations.

</td></tr><tr><td>

Journey Timeline \[sn\_jny\_st\_journey\_timeline\]

</td><td>

Tracks the timeline data for a journey.

</td></tr><tr><td>

Journey Type \[sn\_jny\_journey\_type\]

</td><td>

Tracks the details about the journeys contained in Journey designer

</td></tr><tr><td>

Journey Type Quick Link \[sn\_jny\_m2m\_journey\_type\_quick\_link\]

</td><td>

Manages quick link data related to a journey configuration.

</td></tr><tr><td>

Mobile Journey \[sn\_jny\_st\_journey\]

</td><td>

Tracks journey data activity from the Now Mobile app.

</td></tr><tr><td>

Mobile Journey Overview \[sn\_jny\_st\_mobile\_journey\_overview\]

</td><td>

Tracks data used in the Now Mobile app for user journeys.

</td></tr><tr><td>

Not Available For \[sn\_jny\_m2m\_journey\_config\_user\_criteria\_no\]

</td><td>

List users that met the criteria not to be added to a recommended course.

</td></tr></tbody>
</table>**Parent Topic:**[Journey designer reference](jny-dsnr-reference.md)

