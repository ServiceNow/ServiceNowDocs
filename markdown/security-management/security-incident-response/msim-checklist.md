---
title: Checklist for MSIM setup
description: Before using the ServiceNow Major Security Incident Management \(MSIM\) application, download the application from the ServiceNow Store.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Checklist for MSIM setup

Before using the ServiceNow® Major Security Incident Management \(MSIM\) application, download the application from the ServiceNow® Store.

Track your progress with the setup, installation, and configuration from the following table.

**Note:** The roles assigned for Major Security Incident Management application are listed in the further following sections, for more information, see [Major Security Incident Management roles](../../secops-integration-major-security-incident-management/reference/msi-roles.md).

Use the following checklist to guide you through the end-to-end steps to install and configure Major Security Incident Management application.

<table id="table_k5l_nk1_rpb"><thead><tr><th>

Setup task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Verify that the Major Security Incident Management application is installed and activated from the ServiceNow® Store.

</td><td>

Major Security Incident Management v1.1.1 is available on ServiceNow® Store.

 Follow these instructions: [downloading an application from the ServiceNow Store](download-app-first-time.md).

</td></tr><tr><td>

Verify that the following applications are installed in the given order.

</td><td>

The following applications will be installed by default after you install Major Security Incident Management application in the current application release version:-   File Explorer Core for Security Operations v1.1.1
-   Microsoft SharePoint File Explorer Connector for Security Operations v1.1.1
-   File Explorer Component for Security Operations v1.0.0
-   Microsoft Teams Chat Connector for Security Operations v1.0.0
-   Chat core for Security Operations v1.0.0
-   Major Security Incident Response v1.1.1
-   Collab Chat EVAM card for MSIM workspace v1.0.0 \(This application is set up only for the UI visualizations in the application background for Major Security Incident Management workspace\)
-   Task Organizer UI Component for Major Security Incident Management workspace 1.0.0
-   Security Incident Response v12.8.1

</td></tr><tr><td>

Verify that the user roles are assigned to Major Security Incident as appropriate.

</td><td>

The following roles are involved throughout the incident life-cycle of Major Security Incident remediation process:-   MSI Administrator \[sn\_msi.workspace\_admin\]
-   MSI Manager \[sn\_msi.workspace\_manager\]
-   MSI Responder \[sn\_msi.workspace\_responder\]

For more detailed information on each role, see [Major Security Incident Management roles](../../secops-integration-major-security-incident-management/reference/msi-roles.md).

</td></tr><tr><td>

Verify that you have successfully setup Microsoft SharePoint v1.0.0 configuration.

</td><td>

Microsoft SharePoint manages sites, folders, files, groups, and users in Microsoft SharePoint.

 Add Microsoft SharePoint data to your ServiceNow® instance. To do this, you must have to setup Graph and Rest connections.

 For information, see Microsoft SharePoint spoke v1.1.2 documentation on how to setup REST and Graph connections Configuration.

 Establish Graph and REST connection to connect to your ServiceNow® instance from Microsoft SharePoint.

</td></tr><tr><td>

Verify that you have created a Microsoft SharePoint site to create a document library.

</td><td>

Create a Microsoft SharePoint site, if required or you can use an existing site to create the document library.

</td></tr><tr><td>

Verify that you have created a document library under the Microsoft SharePoint site.

</td><td>

Create a dedicated document library under a new or existing Microsoft SharePoint site.

</td></tr><tr><td>

Verify that required permissions are provided to the users and assigned to the required user groups in the Microsoft SharePoint.

</td><td>

Manage access from Microsoft SharePoint site to different users and user groups.

</td></tr><tr><td>

Verify that you have created and configured Microsoft SharePoint Drive and necessary configuration settings.

</td><td>

To verify the drive configurations, setup Microsoft SharePoint File Explorer Connector, Folder, and File Actions and Folder Templates:

-   [Configure File Explorer Repository Drive](../task/file-explorer-repository-config.md): Create connection from Microsoft SharePoint to ServiceNow® instance.
-   [Configure Folder and File Action Settings](../task/folder-file-action-settings.md): Configure and control the individual Folder and File Actions displayed on the File Explorer Component.
-   [Create Folder Templates](../task/file-explorer-folder-templates.md): Configure to create unique folders for different Major Security Incident types.

</td></tr><tr><td>

Verify that you have successfully established a connection to Microsoft Teams Chat Connector application.

</td><td>

To establish Microsoft Teams Chat Connector application connection with ServiceNow® instance, follow the procedure explained here: [Establish MS Teams Graph connection on ServiceNow AI Platform](../task/msim-micorsoft-team-requirements.md).

</td></tr><tr><td>

Verify that you have configured Microsoft teams with ServiceNow AI Platform® instance and created connections and credentials configurations.

</td><td>

To verify Microsoft Teams configuration with ServiceNow® instance, follow the procedure as explained here:

-   [Establish MS Teams Graph connection on ServiceNow AI Platform](../task/msim-micorsoft-team-requirements.md)
-   [Create a chat channel template](../../secops-integration-major-security-incident-management/task/create-chat-channel-template-for-msim.md)

</td></tr><tr><td>

Verify that the Major Security Incident Administration - Configuration settings are successful.

</td><td>

As an MSI Administrator, you must be able to:

-   Determine whether security analysts can propose and promote the incident and link other security incidents.
-   Enable or disable the notifications when an incident is proposed or promoted. Ability to edit default template messages.
-   Configure security tags that appear on the security analyst interface to differentiate the incidents that have been proposed as a major security incident candidate or promoted to a major security incident.

</td></tr><tr><td>

Verify that the Major Security Incident Administration - Notifications settings are successful.

</td><td>

As an MSI Administrator, trigger email notifications when a security incident is proposed and are sent to all those users and groups who are configured to the notifications list. For more information, see [Set notification preferences for MSIM](../../secops-integration-major-security-incident-management/concept/configuring-msi-administration-settings.md#).

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Major Security Incident Management](../../secops-integration-major-security-incident-management/reference/exploring-major-security-incident-management.md)

**Related topics**  


[Major Security Incident Management](../../secops-integration-major-security-incident-management/concept/major-security-incident-management.md)

[Get started with MSIM](../../secops-integration-major-security-incident-management/reference/get-started-with-msim.md)

[Major Security Incident Management roles](../../secops-integration-major-security-incident-management/reference/msi-roles.md)

