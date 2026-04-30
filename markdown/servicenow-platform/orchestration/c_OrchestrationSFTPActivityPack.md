---
title: SFTP File Transfer activity pack
description: Use the SFTP File Transfer activities to manage files and directories on an SFTP server and to move files from one SFTP server to another.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# SFTP File Transfer activity pack

Use the SFTP File Transfer activities to manage files and directories on an SFTP server and to move files from one SFTP server to another.

The SFTP activity pack includes scoped activities for common file transfer tasks and a ready-to-use workflow that includes these activities. Use the SFTP workflow to control which files are going to be moved, what conditions the files need to meet, the order in which the files are moved, and which overwrite options are executed.

**Note:** To use the SFTP File Transfer activities and workflow, you must [request activation](../task/t_ActivateAnActivityPack.md) of the Orchestration - SFTP plugin.

-   **[SFTP File Transfer workflow](../reference/r_SFTPWorkflow.md)**  
The SFTP File Transfer activity pack includes a scoped workflow that uses multiple activities to manage files on SFTP servers.
-   **[Copy File activity](../reference/r_CopyFileActivity.md)**  
The Copy File activity copies a file from an SFTP server \(source host\) to another SFTP server \(target host\).
-   **[Create Directory activity](../reference/r_CreateDirectoryActivity.md)**  
The Create Directory activity creates a new directory on an SFTP server.
-   **[Get File List activity](../reference/r_GetFileListActivity.md)**  
The Get File List activity returns a list of files from a given directory and its subdirectories on an SFTP server \(source host\).
-   **[Remove File or Directory activity](../reference/r_RemoveFileOrDirectoryActivity.md)**  
The Remove File or Directory activity removes a file or a directory on an SFTP server, including subdirectories, when configured.
-   **[Rename File or Directory activity](../reference/r_RenameFileOrDirectoryActivity.md)**  
The Rename File or Directory activity renames a file or directory to a new name on an SFTP server.
-   **[Set File Attributes activity](../reference/r_SetFileAttributesActivity.md)**  
The Set File Attributes activity sets common file attributes, such as timestamps, size, permissions, and UID/GID, for a file or directory on an SFTP server.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

