---
title: Roles installed with Facilities Service Management
description: Roles control access to features and capabilities in Facilities Service Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Installed with Facilities Service Management, Activate Facilities Service Management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Roles installed with Facilities Service Management

Roles control access to features and capabilities in Facilities Service Management.

Facilities Service Management adds the following roles.

**Note:** You must add the Notify viewer \(notify\_view\) role to employees you want to view notify \(conference calls and SMS messages\) content. For more information, see [Roles installed with Notify](https://www.servicenow.com/docs/access?context=r_NotifyRoles&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

<table id="table_b4f_jcp_yq"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

facilities\_read

</td><td>

Can read facilities requests.

</td><td>

none

</td></tr><tr><td>

facilities\_admin

</td><td>

Can create and modify all facilities requests, modify floor plans, and configure buildings, floors, and rooms. Administrators can also create tasks using the Clone Task feature.

</td><td>

-   knowledge\_manager
-   facilities\_staff
-   facilities\_dispatcher
-   catalog\_admin
-   territory\_admin
-   skill\_admin
-   facilities\_approver\_user
-   template\_admin
-   skill\_model\_admin

</td></tr><tr><td>

facilities\_asset\_admin

</td><td>

Can create and modify all facilities assets.

</td><td>

asset

</td></tr><tr><td>

facilities\_approver\_user

</td><td>

Can approve whether a facilities request can move forward.

</td><td>

approver\_user

</td></tr><tr><td>

facilities\_dispatcher

</td><td>

Can schedule and assign tasks to the facilities staff. They can be searched \(filtered by\) the group they manage.

</td><td>

-   skill\_model\_user
-   facilities\_staff
-   territory\_user
-   inventory\_user

</td></tr><tr><td>

facilities\_staff

</td><td>

Provides full access to the Facilities application and all modules. Can create and modify facilities requests and access facilities reports. Facilities staff are typically the users who are assigned to facilities requests and update the request record accordingly.

</td><td>

-   inventory\_user
-   skill\_user
-   document\_management\_user
-   fc\_request\_reader
-   territory\_user
-   service fulfiller
-   fc\_request\_writer
-   facilities\_read

</td></tr><tr><td colspan="3">

The facilities\_staff and facilities\_admin roles automatically inherit the following roles:

</td></tr><tr><td>

fc\_request\_reader

</td><td>

Can read facilities request records.

</td><td>

none

</td></tr><tr><td>

fc\_request\_writer

</td><td>

Can create, read, write, and delete facilities request records.

</td><td>

fc\_request\_reader

</td></tr><tr><td>

fpv\_floorplan\_writer

</td><td>

Can create, read, write, and delete facilities floor plans.

</td><td>

fpv\_floorplan\_reader

</td></tr><tr><td>

fpv\_element\_reader

</td><td>

Can read room records.

</td><td>

none

</td></tr><tr><td>

fpv\_element\_writer

</td><td>

Can create, read, write, and delete room records.

</td><td>

none

</td></tr></tbody>
</table>**Parent Topic:**[Installed with Facilities Service Management](r_InstallWFacServMgmnt.md)

