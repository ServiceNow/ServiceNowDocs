---
title: Components installed with Journey Accelerator
description: Several types of components install with the activation of the Journey Accelerator application, including user roles and tables. There are also dependencies on other features or apps.
locale: en-US
release: australia
product: Journey Accelerator
classification: journey-accelerator
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Components installed with Journey Accelerator

Several types of components install with the activation of the Journey Accelerator application, including user roles and tables. There are also dependencies on other features or apps.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Demo data is available for the Journey Accelerator application. If you want to install the demo data, click **Load demo data** when installing this application. Demo data includes sample records and configurations for common use cases.

## Roles installed

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Administrator\[sn\_ja.admin\]

</td><td>

Grants access to create and manage all Journey Accelerator components, tables, and data.

</td><td>

-   \[sn\_ja.modifier\]
-   \[sn\_cd.content\_manager\]

</td></tr><tr><td>

Modifier\[sn\_ja.modifier\]

</td><td>

Grants access to modify all Journey Accelerator plans, stages, and to-dos.

</td><td>

\[sn\_ja.reader\]

</td></tr><tr><td>

Reader\[sn\_ja.reader\]

</td><td>

Grants access to read all Journey Accelerator plans, stages, to-dos, and dashboards.

</td><td>

none

</td></tr></tbody>
</table>You can assign these roles to the appropriate roles, groups, or users in your application.

-   To assign a role to another role, see [Add a role to an existing role](https://www.servicenow.com/docs/access?context=t_AddARoleToAnExistingRole&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   To assign a role to a group, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   To assign a role to a user, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Tables installed

|Table name \[name\]|Description|
|-------------------|-----------|
|Journey Accelerator Plan Header Field \[sn\_ja\_plan\_header\_field\]|Tracks the fields that are available for configuration in the plan header.|
|Journey Accelerator Model Task \[sn\_ja\_model\_task\]|Contains Journey Accelerator task records used to copy a task.|
|Journey Accelerator Plan \[sn\_ja\_plan\]|Contains Journey Accelerator plans and manages associations with related tables.|
|Journey Accelerator Plan Configuration \[sn\_ja\_plan\_config\]|Contains details about Journey Accelerator plan configurations.|
|Journey Accelerator Plan Header Configuration \[sn\_ja\_plan\_header\_config\]|Tracks fields used for plan header configuration.|
|Journey Accelerator Plan Type \[sn\_ja\_plan\_type\]|Tracks the different Journey Accelerator plan types.|
|Journey Accelerator Stage \[sn\_ja\_stage\]|Contains Journey Accelerator stage details and relationships to other Journey Accelerator tables.|
|Journey Accelerator Stage Configuration \[sn\_ja\_stage\_config\]xx|Contains details about a stage's configuration.|
|Journey Accelerator Stage Name \[sn\_ja\_stage\_name\]|Tracks the names of the different Journey Accelerator stages.|
|Journey Accelerator Task \[sn\_ja\_task\]|Contains Journey Accelerator task details and relationships to other Journey Accelerator tables.|
|Journey Accelerator Task Template \[sn\_ja\_task\_template\]|Contains details about Journey Accelerator task templates.|
|Journey Accelerator Task Template for Stage Config \[sn\_ja\_m2m\_stage\_task\_temp\]|Used to maintain the relationship of task templates to Journey Accelerator task templates.|

For more information on table administration and how to manage data, see [Table administration](https://www.servicenow.com/docs/access?context=c_TableAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Parent Topic:**[Journey Accelerator reference](ja-reference.md)

