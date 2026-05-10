---
title: Components installed with PPM Collaboration
description: Roles and tables are installed with activation of the PPM Collaboration application.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install PPM Collaboration, Collaborate with your project teams using PPM Collaboration application, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Components installed with PPM Collaboration

Roles and tables are installed with activation of the PPM Collaboration application.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles installed

<table id="table_wn1_y53_mmb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Collaboration user \[SN\_collab\_common.collab\_user\]

</td><td>

Users with this role have read-only access to the Entity Channel table.This role is automatically assigned to project managers and task assignees.

</td></tr><tr><td>

Collaboration owner\[SN\_collab\_common.collab\_owner\]

</td><td>

Users with this role have complete create, read, update, and delete access to the Entity Channel table.This role is automatically assigned to project managers.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity Channel\[sn\_collab\_common\_entity\_channel\]

</td><td>

Stores the list of IDs and names of the Slack channels that are created for the projects.

</td></tr></tbody>
</table>**Parent Topic:**[Using Project Management](../../project-management/concept/using-project-management.md)

**Related topics**  


[Install PPM Collaboration](../task/install-ppm-collab-store-app.md)

[Collaborate with your project teams using PPM Collaboration application](../concept/ppm-collab-overview.md)

