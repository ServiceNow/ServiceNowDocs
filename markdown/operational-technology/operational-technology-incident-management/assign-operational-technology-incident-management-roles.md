---
title: Assign roles to your users
description: Assign roles to your users in the Operational Technology Incident Management application so that you can control their access to the features, capabilities, and data.Assign new roles to users who had the OT Incident User \[ot\_incident\_user\] role through a scheduled job in the Operational Technology Incident Management application.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Operational Technology Incident Management, Operational Technology]
---

# Assign roles to your users

Assign roles to your users in the Operational Technology Incident Management application so that you can control their access to the features, capabilities, and data.

## Before you begin

Role required: admin

## About this task

Users with the roles that are listed in the following table can use the Operational Technology Incident Management application.

**Note:** The OT Incident User \[ot\_incident\_user\] role is deprecated. For users who are assigned with this role, you can execute the scheduled job "Assign New OT Incident Roles” to assign them with new Operational Technology Incident Management roles. For more information, see [Assign new roles to your users](assign-operational-technology-incident-management-roles.md#).

<table id="table_q55_vpq_4nb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Incident Admin \[sn\_ot\_incident\_admin\]

</td><td>

Can create, view, delete, and edit OT incident records for any equipment model entities. Users with this role can configure **Priority Lookup Rules** and **OT incident system properties**.

</td></tr><tr><td>

OT Incident Reader\[sn\_ot\_incident\_read\]

</td><td>

Can only view OT incident records.

</td></tr><tr><td>

OT Incident Fulfiller \[sn\_ot\_incident\_write\]

</td><td>

Can create, view, and edit OT incident records.

</td></tr></tbody>
</table>## Procedure

1.  Assign roles to users or groups by using the ServiceNow AI Platform user administration feature.

    |Task|User administration feature|
    |----|---------------------------|
    |**Assign a role to a user**|See [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).|
    |**Assign a role to a group**|See [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).|


**Parent Topic:**[Configuring Operational Technology Incident Management](../concept/configuring-operational-technology-incident-mgt.md)

## Assign new roles to your users

Assign new roles to users who had the OT Incident User \[ot\_incident\_user\] role through a scheduled job in the Operational Technology Incident Management application.

### Before you begin

-   Set the application scope to **Operational Technology Incident Management**.
-   Role required: admin

### About this task

The OT Incident User role \[ot\_incident\_user\] is deprecated. You can assign new roles to users that had the ot\_incident\_user role through a scheduled script execution.

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the search bar, search for the **Assign New OT Incident Roles** scheduled job.

3.  Start a scheduled job by selecting **Execute now**.

4.  To see the activity log for this scheduled job, navigate to **All** &gt; **System Logs** &gt; **System Log** &gt; **All**.


### Result

The scheduled job is executed and users are now assigned with the new Operational Technology Incident Management roles.

