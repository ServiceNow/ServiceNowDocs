---
title: Telecommunications API notification user roles
description: Administrators can assign user roles to grant access to the API notification database tables. The following standard roles for the Topic \[sn\_api\_notif\_mgmt\_topic\] and Topic Subscription \[sn\_api\_notif\_mgmt\_subscription\] tables are included in the ServiceNow system.
locale: en-US
release: xanadu
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Handling the external events using Telecommunications API notification, Telecommunications Service Operations Management]
---

# Telecommunications API notification user roles

Administrators can assign user roles to grant access to the API notification database tables. The following standard roles for the Topic \[sn\_api\_notif\_mgmt\_topic\] and Topic Subscription \[sn\_api\_notif\_mgmt\_subscription\] tables are included in the ServiceNow system.

<table id="table_mg4_jgq_bzb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_api\_notif\_ mgmt.topic\_subscription\_viewer

</td><td>

Role that enables with read access to the Topic and Topic Subscription tables.

</td></tr><tr><td>

sn\_api\_notif\_ mgmt.topic\_creator

</td><td>

Role that enables with create, read, and edit access to the Topic table.

</td></tr><tr><td>

sn\_api\_notif\_mgmt.subscription\_creator

</td><td>

Role that enables with create and read access to the Topic Subscription table.

</td></tr><tr><td>

sn\_api\_notif\_mgmt.subscription\_admin

</td><td>

Role that enables with the following permissions:-   Create and read access to the Topic and Topic Subscription tables.
-   Change the status of registration to deregister a topic subscription.

</td></tr></tbody>
</table>**Parent Topic:**[Handling the external events using Telecommunications API notification](../concept/telecommunications-api-notification.md)

