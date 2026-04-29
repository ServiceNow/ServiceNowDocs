---
title: Task Plan Templates roles
description: Roles included with the Task Plan Templates application enable users to view, create, and edit task plan templates, template items, and template item conditions. Users can use these defined templates to automatically create tasks, child cases, and child case tasks for different types of cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Task Plan Templates roles

Roles included with the Task Plan Templates application enable users to view, create, and edit task plan templates, template items, and template item conditions. Users can use these defined templates to automatically create tasks, child cases, and child case tasks for different types of cases.

The following granular roles are included with the Task Plan Templates plugin \(com.sn\_task\_plan\_templates\).

<table id="table_ljy_zcn_kfc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_task\_plan.admin​

</td><td>

Can create, view, update and delete records in the following table:​

 ​

 -   Task Plan Category \[sn\_task\_plan\_category\]​

-   Task Plan Template Configuration \[sn\_task\_plan\_config\]​

-   Task Plan Configuration Category \[sn\_task\_plan\_config\_category\]​

-   Task Plan Template \[sn\_task\_plan\_template\]​

-   Task Plan Template Access \[sn\_task\_plan\_template\_access\]​

-   Task Plan Template Category \[sn\_task\_plan\_template\_category\]​

-   Task Plan Template Execution \[sn\_task\_plan\_template\_execution\]​

-   Template Item \[sn\_task\_plan\_template\_item\]​

-   Template Item Condition \[sn\_task\_plan\_template\_item\_condition\]​

-   Template Item Configuration \[sn\_task\_plan\_template\_item\_config\]​


</td><td>

-   sn\_task\_plan.creator​

-   sn\_task\_plan.delete​

-   sn\_task\_plan.report\_viewer​

-   sn\_task\_plan.navigation\_menu​


</td></tr><tr><td>

sn\_task\_plan.viewer

</td><td>

Can view information in the following tables:-   Task Plan Template \[sn\_task\_plan\_template\]
-   Template Item \[sn\_task\_plan\_template\_item\]
-   Template Item Condition \[sn\_task\_plan\_template\_item\_condition\]

</td><td>

 

</td></tr><tr><td>

sn\_task\_plan.writer

</td><td>

Can view and update information in the following tables:-   Task Plan Template \[sn\_task\_plan\_template\]
-   Template Item \[sn\_task\_plan\_template\_item\]
-   Template Item Condition \[sn\_task\_plan\_template\_item\_condition\]

</td><td>

sn\_task\_plan.viewer

</td></tr><tr><td>

sn\_task\_plan.creator

</td><td>

Can create records in the following tables:-   Task Plan Template \[sn\_task\_plan\_template\]
-   Template Item \[sn\_task\_plan\_template\_item\]
-   Template Item Condition \[sn\_task\_plan\_template\_item\_condition\]

</td><td>

sn\_task\_plan.writer

</td></tr><tr><td>

sn\_task\_plan.delete

</td><td>

Can delete records from the following tables:-   Task Plan Template \[sn\_task\_plan\_template\]
-   Template Item \[sn\_task\_plan\_template\_item\]
-   Template Item Condition \[sn\_task\_plan\_template\_item\_condition\]

</td><td>

sn\_task\_plan.viewer

</td></tr><tr><td>

sn\_task\_plan.report\_viewer

</td><td>

Can view the task plan template reports.

</td><td>

 

</td></tr><tr><td>

sn\_task\_plan.navigation\_menu

</td><td>

Can view the Task Plan Templates lists.

</td><td>

sn\_task\_plan.viewer

</td></tr></tbody>
</table>