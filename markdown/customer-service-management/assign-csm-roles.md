---
title: Assign roles to CSM users
description: Roles control access to features, capabilities, and data in the Customer Service Management application.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User management, Set up your environment, Configure, Customer Service Management]
---

# Assign roles to CSM users

Roles control access to features, capabilities, and data in the Customer Service Management application.

## Before you begin

Role required: admin

Before you can assign roles to your users, make sure that these users have already been configured.

-   [Configure users and groups](configure-csm-users-groups.md)
-   [Configure accounts and contacts](configure-csm-accounts-contacts.md)
-   [Configure consumers](configure-csm-consumers.md)

## About this task

You can assign roles to individual users or groups. Apply roles to groups and the members of those groups inherit those roles.

The Customer Service Management application provides two types of roles: internal roles for agents and managers and external roles for customers, customer partners, and consumers.

<table id="table_ql1_rw4_rkb"><thead><tr><th>

Internal Roles

</th><th>

External Roles

</th></tr></thead><tbody><tr><td>

**Business-to-business \(B2B\)** -   sn\_customerservice\_agent
-   sn\_customerservice\_manager

</td><td>

**Business-to-business \(B2B\) Customer** -   sn\_customerservice.customer
-   sn\_customerservice.customer\_admin
-   sn\_customerservice.customer\_case\_manager

</td></tr><tr><td>

**Business-to-consumer \(B2C\)** -   sn\_customerservice.consumer\_agent
-   sn\_customerservice\_manager

</td><td>

**Business-to-business \(B2B\) Partner** -   sn\_customerservice.partner
-   sn\_customerservice.partner\_admin

</td></tr><tr><td>

 

</td><td>

**Business-to-consumer \(B2C\)** sn\_customerservice.consumer

</td></tr></tbody>
</table>## Procedure

-   You can assign roles to users and groups using guided setup.

-   You can also assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
    -   [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

**Related topics**  


[Roles installed with Customer Service Management](../reference/r_RolesInstalledWithCustomerService.md)

