---
title: Configure File Explorer Component
description: The File Explorer workspace component organizes and tracks the collection of artifacts \(files\) related to a major security incident. It is designed to support integration with any third-party file hosting provider such as Microsoft SharePoint in the Major Security Incident Management workspace.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Major Security Incident Management, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure File Explorer Component

The File Explorer workspace component organizes and tracks the collection of artifacts \(files\) related to a major security incident. It is designed to support integration with any third-party file hosting provider such as Microsoft SharePoint in the Major Security Incident Management workspace.

-   File Explorer Component: Provides a graphical user interface to display the file system and allows the users to perform file operations.
-   File Explorer Core: Provides an abstraction layer that allows the File Explorer component to display the file system and perform various file operations without knowing anything about the underlying connector that is used to communicate with external repositories.
-   File Explorer Microsoft SharePoint Connector application: Provides the implementation modules required to track and fetch files/folder metadata from a Microsoft SharePoint document library and perform file operations.

The File Explorer Core component provides a base infrastructure required for the different file sharing connector applications to define its connection properties.

You must install and configure the file repository drive and file repository provider by adding the connection properties to pull the files metadata from a file hosting provider location.

For this current version of the File Explorer, these instructions include configuring and subscribing to a retrieving file metadata such as Microsoft SharePoint file and folder updates, file operations, and logging file activity. A designated Microsoft SharePoint document library and related drive configuration will be required to create individual folders that are specific to a major security incident.

File Explorer also allows connector applications such as Microsoft SharePoint. You can use this example to configure its file operation implementations such as **Download** or **Rename** folder and file actions will be enabled in the File Explorer workspace component. These actions are enabled and executed using the integrated flow designer sub flows. For more information, see [Folder and File Action Settings](../task/folder-file-action-settings.md).

File Explorer configuration includes the following setup:

-   [Configure File Explorer Repository Drive](../task/file-explorer-repository-config.md)
-   [Configure Folder and File Action Settings](../task/folder-file-action-settings.md)
-   [Create Folder Templates](../task/file-explorer-folder-templates.md)

-   **[Get Started with File Explorer](../../secops-integration-major-security-incident-management/reference/get-started-with-fe.md)**  
Review the following information before you start working with File Explorer Component.
-   **[Configure File Explorer Repository Drive](../task/file-explorer-repository-config.md)**  
The Microsoft SharePoint connector provides various capabilities to be implemented in Microsoft SharePoint File Explorer features by managing and tracking the file metadata.
-   **[Configure Folder and File Action Settings](../task/folder-file-action-settings.md)**  
 Configure the folder and file actions you would like to be enabled from the File Explorer component on the Major Security Incident Management workspace, using the Folder and File Action Settings setup page. As an MSI Administrator, you can control the individual Folder and File Actions displayed on the File Explorer Component.
-   **[Create Folder Templates](../task/file-explorer-folder-templates.md)**  
Use Folder Templates to automatically create unique folders for different Major Security Incident types. The folder templates within the File Explorer Component are used to create a base folder structure for the security incident in the Microsoft SharePoint.
-   **[File Explorer Activity Stream in Workspace](../../secops-integration-major-security-incident-management/concept/activity-stream-on-the-workspace.md)**  
Use the File Explorer section from the Major Security Incident Management workspace to display the folders and files, the sequence those were created in Microsoft SharePoint document library.
-   **[File Explorer troubleshooting](../../secops-integration-major-security-incident-management/concept/file-explorer-troubleshooting.md#)**  
The troubleshooting section can help you resolve some of the technical issues that you may encounter when setting up File Explorer component.

**Parent Topic:**[Configuring Major Security Incident Management](../../secops-integration-major-security-incident-management/reference/configuring-major-security-incident-management.md)

**Related topics**  


[Configure Microsoft Teams](chat-channel-provider-config.md)

[Configure Slack chat connector for major security incidents](../../secops-integration-major-security-incident-management/concept/configure-slack-chat-connector-msi.md)

