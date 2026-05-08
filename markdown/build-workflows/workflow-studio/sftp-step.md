---
title: SFTP step
description: Create a reusable action to manage files and directories on an SFTP server and to move files from one SFTP server to another.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Steps, Flows, subflows, and actions reference, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# SFTP step

Create a reusable action to manage files and directories on an SFTP server and to move files from one SFTP server to another.

**Note:**

-   This step requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf). For more information about the ServiceNow® Integration Hub subscription packages, see Integration Hub usage and subscription. After the required plugin is activated, the step is visible under Integrations.
-   The SFTP step runs only on a ServiceNow® MID Server with SSH capabilities. Activate the plugin, Integration Hub in Workflow Data Fabric Professional \(com.glide.hub.integrations.professional\) to use the JDBC capability for the MID Server. For more information, see Request an Integration Hub plugin.
-   The SFTP step requires a credential record that supports either SSH private key credentials or SSH credentials. This step does not support Windows credentials where the **Use MID Server service account** option is selected.

## Roles and availability

The SFTP step is available as an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

## Prerequisite

Activate the Managed File Transfer Extensions for the SFTP Step \(com.glide.hub.action\_step.sftp\_mft\) plugin.

## SFTP commands

-   [Copy File](copy-file-sftp-step.md)
-   [Copy Directory](copy-dir-sftp-step.md)
-   [Create Directory](create-dir-sftp.md)
-   [Get File List](get-file-list-sftp.md)
-   [Remove File](remove-file-sftp.md)
-   [Remove Files](remove-files-sftp.md)
-   [Delete Directory](delete-dir-sftp.md)
-   [Rename File or Directory](rename-file-dir-sftp.md)
-   [Set File Attributes](set-file-attributes-sftp.md)
-   [Copy Attachments To SFTP Server](copy-files-sftp-server.md)
-   [Copy Files To This Instance](copy-files-instace.md)

**Note:** The SFTP commands can be performed on a maximum of 10,000 files at a time.

-   **[Copy File](copy-file-sftp-step.md)**  
Copies a file from the source SFTP server to target SFTP server.
-   **[Copy Directory](copy-dir-sftp-step.md)**  
Copies a directory from the source SFTP server to the target SFTP server.
-   **[Create Directory](create-dir-sftp.md)**  
Creates a new directory on an SFTP server.
-   **[Get File List](get-file-list-sftp.md)**  
Returns a list of files from a given directory and its subfolders on an SFTP server.
-   **[Remove File](remove-file-sftp.md)**  
Removes a file on an SFTP server, including subfolders, when configured.
-   **[Remove Files](remove-files-sftp.md)**  
Remove files on an SFTP server, including subfolders, when configured.
-   **[Delete Directory](delete-dir-sftp.md)**  
Deletes directory on an SFTP server, including subfolders, when configured.
-   **[Rename File or Directory](rename-file-dir-sftp.md)**  
Renames a file or directory on an SFTP server.
-   **[Set File Attributes](set-file-attributes-sftp.md)**  
Sets common file attributes, such as timestamps, size, permissions, and UID/GID, for a file or directory on an SFTP server.
-   **[Copy Attachments To SFTP Server](copy-files-sftp-server.md)**  
Copies the specified attachments from ServiceNow instance to an SFTP server.
-   **[Copy Files To This Instance](copy-files-instace.md)**  
Attaches the specified files in the SFTP server to the specified record in ServiceNow instance.

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

