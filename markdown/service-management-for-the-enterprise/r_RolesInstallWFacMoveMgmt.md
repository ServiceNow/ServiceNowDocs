---
title: Roles installed with Facilities Move Management
description: Roles control access to features and capabilities in Facilities Move Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installed with Facilities Move Management, Activate Facilities Move Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Roles installed with Facilities Move Management

Roles control access to features and capabilities in Facilities Move Management.

Facilities Move Management adds the following roles.

<table id="table_b4f_jcp_yq"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Move Basic\[move\_basic\]

</td><td>

Can read and create service orders and follow up on the orders they created.

</td><td>

-   document\_management\_user
-   move\_read
-   service\_fulfiller
-   task\_activity\_writer
-   skill\_user
-   territory\_user
-   inventory\_user

</td></tr><tr><td>

Move administrator\[move\_admin\]

</td><td>

Has full control over all Service Management data. Also administers Territories and Skills, as needed.

</td><td>

-   territory\_admin
-   skill\_model\_admin
-   move\_approver\_user
-   skill\_admin
-   catalog admin
-   knowledge\_manager
-   move\_agent
-   template\_admin
-   move\_dispatcher

</td></tr><tr><td>

Move dispatcher\[move\_dispatcher\]

</td><td>

Schedules and assigns the tasks to agents. They can be searched \(filtered by\) the group they manage.

</td><td>

-   skill\_model\_user
-   inventory\_user
-   territory\_user
-   move\_basic

</td></tr><tr><td>

Move agent\[move\_agent\]

</td><td>

Can accept or reject a task. It is the one who performs the work on the site.

</td><td>

-   move\_basic

</td></tr><tr><td>

Move initiator\[move\_initiator\]

</td><td>

Similar to sm\_basic \(can read and create service orders and follow up on the orders they created\), but can also grant UI access.

</td><td>

-   move\_basic

</td></tr><tr><td>

Move approver\[move\_approver\_user\]

</td><td>

Approve orders and requests.

</td><td>

-   approver\_user

</td></tr><tr><td>

Move read\[move\_read\]

</td><td>

Can only read and create service orders and follow up on the orders they created.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Installed with Facilities Move Management](r_InstallWFacMoveMgmt.md)

