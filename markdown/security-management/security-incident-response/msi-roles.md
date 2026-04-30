---
title: Major Security Incident Management roles
description: Assign roles to ensure that users can perform all necessary actions within the MSIM application.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Explore, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Major Security Incident Management roles

Assign roles to ensure that users can perform all necessary actions within the MSIM application.

<table id="table_fpp_lfc_crb"><thead><tr><th>

Role Type

</th><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MSI Administrator

</td><td>

sn\_msi.workspace\_admin

</td><td>

Can I install and configure Major Incident Management and set up the dependent applications such as File Explorer \(FE\), Microsoft Teams and Chat Channel configuration, Workspace setup, and MSI Administration: Configurations and Notifications setup.How to set up:

 -   File Explorer \(FE\) component:
    -   Configure file repository.
    -   Configure file and folder actions, which are provided on the File Explorer component of the Collaboration tab in the Major Security Incident Management workspace.
    -   Create the root folders and subfolders, and provide access to the subfolders.
-   Chat channel management
    -   Activate and configure Microsoft Teams by validating Microsoft Teams connection.
    -   Create chat teams and chat channels, and add users and assign users to the various user groups.
-   MSI Administration:
    -   Configurations: Configure the security analysts actions, notifications sent when incidents are proposed and promoted, and display tags for the security incidents.
    -   Notifications: Automate email notification process and user notifications when a security incident is either proposed or promoted as a major security incident.

</td></tr><tr><td>

MSI Manager

</td><td>

sn\_msi.workspace\_manager

</td><td>

-   View access to the major security incident management configuration settings page. Restricted from modifying any of the configuration settings.
-   View and edit incident record data in the **Details**, **Collaboration**, and **Task Organizer** tabs of the Major Incident Management workspace.
-   Promote the security incident to a major security incident.
-   Configure file and folders actions available on the File Explorer component on the **Collaboration** tab of the Major Incident Management workspace.
-   Linking and unlinking additional records to Major Security Incidents from the workspace.

</td></tr><tr><td>

MSI Responder

</td><td>

sn\_msi.workspace\_responder

</td><td>

-   Optional role to view, edit, and respond to major security incidents in the **Details** and **Tasks** tabs of the Major Incident Management workspace.
-   Linking and unlinking additional records to Major Security Incidents from the workspace.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Major Security Incident Management](exploring-major-security-incident-management.md)

**Related topics**  


[Major Security Incident Management](../concept/major-security-incident-management.md)

[Get started with MSIM](get-started-with-msim.md)

[Checklist for MSIM setup](../../security-incident-response/reference/msim-checklist.md)

