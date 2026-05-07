---
title: Legacy - Source Control integration
description: Enable application developers to integrate with a Git Source Control repository. Save and manage multiple versions of an application from a non-production instance.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Source Control integration

Enable application developers to integrate with a Git Source Control repository. Save and manage multiple versions of an application from a non-production instance.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

Linking an application to Source Control enables all application developers on a non-production instance to:

-   Import applications from a Git repository.
-   Pull and apply remote changes from a Git repository.
-   Commit all local changes on the instance to a Git repository.
-   Create tags to permanently link to a given version of an application.
-   Create branches to maintain multiple versions of an application simultaneously.

## Integration requirements

To link an application to source control:

-   The user must have the admin role.
-   The non-production instance must have network access to the Git repository.
-   Each application must be within its own Git repository.
-   The repository user credentials must grant read and write access.

**Note:** All application developers on the instance share a single set of credentials per repository.

## Options available from ServiceNow Studio

After linking an application to Source Control, application developers can use ServiceNow Studio to manage the repository. From Studio, developers can:

-   Edit the application repository credentials.
-   Commit all local changes on the instance.
-   Apply remote changes from the repository.
-   Create a branch.
-   Switch branches.
-   Import an application from a remote repository.

It is not recommended to use Source Control to manage applications on a production instance, deploying to production may lead to unintended consequences, see [Legacy - Production deployment tips](tips-production-deployment.md). Instead, you can manage applications on a production instance using the application repository, an update set, or the ServiceNow Store. For more information about managing applications on a production instance, see [Application sharing](c_SharingApplications.md).

## Options available from a Git repository

The ServiceNow platform offers limited support for modifying linked application files outside of an instance. From Git, developers can:

-   Move application files to a different Git directory structure.
-   Edit application files outside of ServiceNow Studio.

The system generates a properties text file called `sn_source_control.properties` at the root level of the repository. To move application files to a different Git directory structure, application developers can set the **path** parameter to specify the subfolder path containing their application files. For example, if you moved your application to the `src/app` subfolder, set the **path** to `path=src/app`.

The system generates a `checksum.txt` file in the Git repository to determine if any application files have been changed outside of Studio. When the checksum value from the file matches the current checksum value, the integration skips the validation and sanitization process. When the checksum values do not match, the integration validates and sanitizes the application files as part of the Source Control operation. The sanitization process:

-   Creates upgrade log entries for each sanitization action taken.
-   Removes unsupported folders and files from the repository.
-   Aborts all Source Control operations when a system application file fails XML schema validation. For example, if a database dictionary record fails XML schema validation, the system aborts all operations.
-   Skips the current Source Control operation when a non-system application file fails XML schema validation.

The Source Control integration sanitizes only content within the application path listed in the `sn_source_control.properties` file. Repository content outside the application path is ignored.

## MID Server support

Use an existing MID Server to connect to a Source Control repository. [Linking](../task/t_LinkAnApplicationToSourceControl.md) or [importing](../task/t_ImportAppFromSourceControl.md) an application through a MID Server enables access to repositories behind a firewall.

## Configure MID server for source control integration

Configure a MID server for Source Control Integration to enable communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

-   Add "bundle" extension to `glide.attachment.extensions` properties.
-   If the MID Servers must go through a proxy to access the remote git repository, do as follows:
    -   Add the following line to `agent\conf\wrapper-override.conf` file:
    -   `wrapper.java.additionial.3=-Dhttps.proxyHost=<proxyHost>`
    -   `wrapper.java.additionial.4=-Dhttps.proxyPort=<proxyPort>`
    -   Restart the MID
    -   Add a new entry in "MID Security Policy":
    -   Name: &lt;proxy host name&gt;
    -   Check "Active" only

## Denoise source control commits

Skip unloading into XML files of noisy update fields for any metadata record in source control.

-   **[Legacy - Production deployment tips](tips-production-deployment.md)**  
When you develop customizations to applications on the ServiceNow® platform, you deploy them via the application repository to a production instance. This topic examines and provides cautions for the tradeoffs between installing an application from the application repository versus Git repository with source control.
-   **[Legacy - Available source control operations](../reference/r_AvailableSourceControlOperations.md)**  
The source control integration primarily supports operations from Studio, but can also support some operations directly from the GIT repository.
-   **[Legacy - Import application or application-customization from source control](../task/t_ImportAppFromSourceControl.md)**  
Import an application or application-customization from a source control repository to continue developing it on this instance.
-   **[Legacy - Link an application or application-customization to source control](../task/t_LinkAnApplicationToSourceControl.md)**  
Linking an application or application-customization to source control allows application developers to manage changes from a Git repository.
-   **[Legacy - Migrate completed update set history to Source Control](migrate-update-set-history.md)**  
When linking to Source Control, this feature allows application developers the choice of migrating the information in completed update sets to Source Control history.
-   **[Legacy - Edit a Git repository configuration](../task/edit-git-repo.md)**  
You can edit a Git repository to change the network protocol selection, credentials or other field entries.
-   **[Legacy - Apply remote changes](../task/t_ApplyRemoteChanges.md)**  
Application developers can pull changes from a linked GIT repository to apply remote changes to the local instance.
-   **[Legacy - Commit changes](../task/t_CommitChanges.md)**  
Application developers can commit their changes on the instance to the linked Git repository. You can either select a few changes to commit, or commit all changes on the instance at once.
-   **[Legacy - Stash local changes](../task/t_StashLocalChanges.md)**  
Application developers can remove and save changes locally to apply them later.
-   **[Legacy - Switch branch](../task/t_SwitchBranch.md)**  
Application developers can switch to a different repository branch to work on another version of the application.
-   **[Legacy - Create branch](../task/t_CreateBranch.md)**  
Application developers can create a branch to work on a new version of an existing application.
-   **[Legacy - Set default branch](../task/set-default-branch.md)**  
Set a default branch when you want to use a branch other than main for new changes or for your main development repository.
-   **[Legacy - Manage stashes](../task/t_ManageStashes.md)**  
Application developers can apply or delete stashed changes from Studio.
-   **[Legacy - Resolve conflicts](../task/t_ResolveConflicts.md)**  
Application developers can choose which application file version to use when applying remote or stashed changes.
-   **[Legacy - View commit history](../task/view-commit-history.md)**  
Application developers can view the commit history of applications linked to a source control repository.
-   **[Legacy - Move application files in a GIT repository](../task/move-application-files-git.md)**  
Move application files linked to source control to any folder of the repository. Allow application developers to store supporting content such as automated tests in the same repository as the applications they support.
-   **[Legacy - Collision avoidance](../task/collision-avoidance.md)**  
Avoid modifying an application file across different update sets to ensure seamless experience during the commit process.
-   **[Legacy - Delta loading](delta-loading.md)**  
"Delta loading" is an optimized way to load an application from a Git repository.
-   **[Legacy - De-noise your source control commits](denoise-source-control-commits.md)**  
As a source control developer, you can merge the Git branches, without getting noise from the fields that are auto-updated by the system.

**Parent Topic:**[Legacy - ServiceNow Studio](c_ServiceNowStudio.md)

