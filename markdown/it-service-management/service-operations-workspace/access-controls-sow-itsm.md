---
title: Access controls in Service Operations Workspace for ITSM
description: You can determine which users can access Service Operations Workspace for ITSM after logging in to the ServiceNow instance or access the Service Operations Workspace for ITSM landing page.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Access controls in Service Operations Workspace for ITSM

You can determine which users can access Service Operations Workspace for ITSM after logging in to the ServiceNow instance or access the Service Operations Workspace for ITSM landing page.

For a user, access to Service Operations Workspace for ITSM is based on the following criteria:

-   Is the redirection upon login enabled to the Service Operations Workspace landing page.
-   Does the user have the sn\_sow.sow\_user role to access SOW manually or when redirected upon login.

    **Note:**

    -   The itil role contains the sn\_sow.sow\_user role. But if the user has any custom or granular roles other than itil, then the sn\_sow.sow\_user role should be assigned to the user and the audiences should be updated with custom roles.
    -   Custom roles require updates to ACLs \(access control lists\) that restrict access to certain functionality.
-   First audience that the user belongs to.

![Flow chart for SOW access](../image/sow-access.png)

-   **[Types of landing pages in Service Operations Workspace for ITSM](landing-page-types-sow.md)**  
Landing pages provide an agent with quick visibility into the work assigned, announcements, upcoming tasks, and so on.
-   **[Configure the audience for the SOW landing page](../task/configure-audience-sow-landing-page.md)**  
Define who can access your SOW landing pages. You can targeted experiences for audiences such as agents and managers.
-   **[Configure service desk groups to access the Service Operations Workspace landing page](../task/configure-service-desk-groups-sow.md)**  
Ensure that the right users have access to the Service Operations Workspace landing page.

**Parent Topic:**[Getting started with Service Operations Workspace for ITSM](getting-started-sow.md)

