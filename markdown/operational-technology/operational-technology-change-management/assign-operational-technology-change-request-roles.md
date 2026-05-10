---
title: Assign Operational Technology Change Management roles
description: Assign roles to your users so that you can control their access to the features, capabilities, and data in the Operational Technology Change Management application.
locale: en-US
release: australia
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Operational Technology Change Management, Operational Technology]
---

# Assign Operational Technology Change Management roles

Assign roles to your users so that you can control their access to the features, capabilities, and data in the Operational Technology Change Management application.

## Before you begin

Role required: admin or user\_admin

## About this task

Users with the roles that are listed in the following table can use the application.

<table id="table_qlr_hcm_ysb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Change Manager \[sn\_ot\_change\_manager\]

</td><td>

Can manage OT change model records.

</td></tr><tr><td>

Change Admin \[sn\_ot\_change\_admin\]

</td><td>

Can create, view, delete, and edit OT change records. Can configure categories and system properties.

</td></tr><tr><td>

Change Write user \[sn\_ot\_change\_write\]

</td><td>

Can create, view, and edit OT change records.Can also be assigned IT change tasks, and can edit and close the IT change task they're assigned to.

For more information, see [Managing change requests across sites](../concept/visibility-of-changes-across-sites.md).

</td></tr><tr><td>

Change Read user \[sn\_ot\_change\_read\]

</td><td>

Can only view OT change records.

</td></tr></tbody>
</table>## Procedure

1.  Assign roles to users and groups by using the ServiceNow AI Platform user administration feature.

    |Task|User administration feature|
    |----|---------------------------|
    |**Assign a role to a user**|See [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignARoleToAUser.md).|
    |**Assign a role to a group**|See [Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/t_AssignRoleToGroup.md).|


**Parent Topic:**[Configuring Operational Technology Change Management](../concept/configuring-operational-technology-change-request.md)

