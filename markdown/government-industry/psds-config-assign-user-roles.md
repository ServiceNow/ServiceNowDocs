---
title: Assign roles to Public Sector Digital Services users
description: Roles control access to features, capabilities, and data in the Public Sector Digital Services application.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-01-13"
reading_time_minutes: 1
breadcrumb: [User management, Set up your environment, Configure, Public Sector Digital Services \(PSDS\)]
---

# Assign roles to Public Sector Digital Services users

Roles control access to features, capabilities, and data in the Public Sector Digital Services application.

## Before you begin

Role required: admin

## About this task

You can assign roles to individual users or groups. Apply roles to groups and the members of those groups inherit those roles.

The Public Sector Digital Services application provides two types of roles: internal roles assigned to internal users such as for government service agents and managers, contributors, managers, and admins, and external roles for constituents, applicants, and business owners, contacts, channels, and partners. These roles are automatically installed with activation of the Public Sector Digital Services Core application.

<table id="table_ql1_rw4_rkb"><thead><tr><th>

Internal Roles

</th><th>

External Roles

</th></tr></thead><tbody><tr><td>

**Gov-to-business \(G2B\)** -   sn\_gsm.business\_agent
-   sn\_gsm.government\_service\_manager

</td><td>

**Gov-to-business \(G2B\) Customer** -   sn\_gsm.business\_contact
-   sn\_gsm.business\_contact\_admin
-   sn\_gsm.business\_case\_manager

**Gov-to-business \(G2B\) Partner** -   sn\_gsm.business\_partner
-   sn\_gsm.business\_partner\_admin
-   sn\_gsm.business\_contact

</td></tr><tr><td>

**Gov-to-constituent \(G2C\)** -   sn\_gsm.constituent\_agent
-   sn\_gsm.government\_service\_manager

</td><td>

**Gov-to-constituent \(G2C\)** -   sn\_gsm.constituent
-   sn\_gsm.constituent\_contributor

</td></tr><tr><td colspan="2">

**Gov-to-Gov \(G2G\)**-   sn\_gsm.agency\_agent
-   sn\_gsm.agency\_constituent\_agent
-   sn\_gsm.agency\_manager
-   sn\_gsm.government\_service\_manager
-   sn\_gsm.agency\_contributor

</td></tr></tbody>
</table>## Procedure

-   You can assign roles to users and groups using guided setup.

-   You can also assign roles to users and groups using the ServiceNow AI Platform user administration feature.

    -   [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)
    -   [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

**Related topics**  


[Roles installed with Public Sector Digital Services](../reference/roles-installed-with-public-sector-digital-services.md)

