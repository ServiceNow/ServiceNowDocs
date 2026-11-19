---
title: Major Security Incident Management roles
description: Assign roles to ensure that users can perform all necessary actions within the MSIM application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/security-incident-response/msi-roles.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
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

Can install and configure Major Incident Management and set up the dependent applications such as File Explorer \(FE\), Microsoft Teams and Chat Channel configuration, Workspace setup, and MSI Administration: Configurations and Notifications setup.Can also view major security incident records and their Details tab through inherited read permissions. Access to restricted incidents remains subject to configured restrictions. This role alone does not grant general incident editing permissions.

How to set up:

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

</td></tr><tr><td>

Incident promotion

</td><td>

sn\_msi.promoter

</td><td>

Can promote a security incident to a major security incident. **Note:** The promoter and proposer roles control the Propose and Promote UI actions, while the msi\_incident\_\* and msi\_task\_\* roles control table-level access regardless of entry point.

</td></tr><tr><td>

Incident promotion

</td><td>

sn\_msi.proposer

</td><td>

Can propose a security incident to a major security incident.

</td></tr><tr><td>

MSI Incident record

</td><td>

sn\_msi.msi\_incident\_create

</td><td>

Can create a major security incident.

</td></tr><tr><td>

MSI Incident record

</td><td>

sn\_msi.msi\_incident\_read

</td><td>

Can read a major security incident.

</td></tr><tr><td>

MSI Incident record

</td><td>

sn\_msi.msi\_incident\_write

</td><td>

Can edit a major security incident.

</td></tr><tr><td>

MSI Incident record

</td><td>

sn\_msi.msi\_incident\_delete

</td><td>

Can delete a major security incident.

</td></tr><tr><td>

MSI Task record

</td><td>

sn\_msi.msi\_task\_create

</td><td>

Can create a major security incident task.

</td></tr><tr><td>

MSI Task record

</td><td>

sn\_msi.msi\_task\_read

</td><td>

Can read a major security incident task.

</td></tr><tr><td>

MSI Task record

</td><td>

sn\_msi.msi\_task\_write

</td><td>

Can edit a major security incident task.

</td></tr><tr><td>

MSI Task record

</td><td>

sn\_msi.msi\_task\_delete

</td><td>

Can delete a major security incident task.

</td></tr><tr><td>

Status report

</td><td>

sn\_msi.msi\_report\_read

</td><td>

Can read the status report configuration of a major security incident.

</td></tr><tr><td>

Status report

</td><td>

sn\_msi.msi\_report\_write

</td><td>

Can configure the status report configuration of a major security incident.

</td></tr><tr><td>

Restricted access

</td><td>

sn\_msi.restriction\_access\_admin

</td><td>

Can bypass the enforce restriction setting to access restricted major security incidents.

</td></tr><tr><td>

Restricted access

</td><td>

sn\_msi.restriction\_access\_manager

</td><td>

Can modify the Enforce restriction field and the allowed members or allowed groups fields. Does not grant access to restricted major security incidents; this role is for field changes only.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.threatintel\_read

</td><td>

Ability to read the Threat Intelligence tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.taskorganizer\_read

</td><td>

Ability to read the Task Organizer tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.taskorganizer\_edit

</td><td>

Ability to edit the Task Organizer tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.collab\_read

</td><td>

Ability to read the Collaboration tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.collab\_edit

</td><td>

Ability to edit the Collaboration tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.details\_read

</td><td>

Ability to read the Details tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.details\_edit

</td><td>

Ability to edit the Details tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.overview\_read

</td><td>

Ability to read the Overview tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.incidentimpact\_read

</td><td>

Ability to read the Incident Impact tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.timeline\_read

</td><td>

Ability to read the Timeline in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.timeline\_edit

</td><td>

Ability to edit the Timeline in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.linkedsivi\_read

</td><td>

Ability to read the Linked SI/VI tab in the MSIM workspace.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.labels\_collab\_edit

</td><td>

Ability to add or remove labels in the Collaboration activity stream component.

</td></tr><tr><td>

Workspace tab access

</td><td>

sn\_msi.labels\_task\_organiser\_edit

</td><td>

Ability to add or remove labels in the Task Organizer component.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Major Security Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/security-incident-response/exploring-major-security-incident-management.md)

**Related topics**  


[Major Security Incident Management]()

[Get started with MSIM]()

[Checklist for MSIM setup]()

[Environment reference for MSIM setup]()

