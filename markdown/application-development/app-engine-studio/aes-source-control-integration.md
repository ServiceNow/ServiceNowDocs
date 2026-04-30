---
title: AES integration with a Git source control repository
description: Enable application developers to integrate App Engine Studio \(AES\) with a Git source control repository to save and manage multiple versions of an application from a non-production instance.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure App Engine Studio, Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# AES integration with a Git source control repository

Enable application developers to integrate App Engine Studio \(AES\) with a Git source control repository to save and manage multiple versions of an application from a non-production instance.

Linking an application to source control enables all application developers on a non-production instance to:

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

## Options available from App Engine Studio

After linking an application to source control, application developers can use App Engine Studio to manage the repository. From App Engine Studio, developers can:

-   Edit the application repository credentials.
-   Commit all local changes on the instance.
-   Apply remote changes from the repository.
-   Create a branch.
-   Switch branches.
-   Import an application from a remote repository.

Source control integration does not support managing applications on a production instance. Instead, you can manage applications on a production instance using the application repository, an update set, or App Engine Studio. For more information about managing applications on a production instance, see [Application sharing](../../applications/concept/c_SharingApplications.md).

## Options available from a Git repository

The ServiceNow platform offers limited support for modifying linked application files outside of an instance. From Git, developers can:

-   Move application files to a different Git directory structure.
-   Edit application files outside of App Engine Studio.

The system generates a properties text file called `sn_source_control.properties` at the root level of the repository. To move application files to a different Git directory structure, application developers can set the **path** parameter to specify the subfolder path containing their application files. For example, if you moved your application to the `src/app` subfolder, set the **path** to `path=src/app`.

The system generates a `checksum.txt` file in the Git repository to determine if any application files have been changed outside of App Engine Studio. When the checksum value from the file matches the current checksum value, the integration skips the validation and sanitization process. When the checksum values do not match, the integration validates and sanitizes the application files as part of the source control operation. The sanitization process:

-   Creates upgrade log entries for each sanitization action taken.
-   Removes unsupported folders and files from the repository.
-   Aborts all source control operations when a system application file fails XML schema validation. For example, if a database dictionary record fails XML schema validation, the system aborts all operations.
-   Skips the current source control operation when a non-system application file fails XML schema validation.

The Git integration sanitizes only content within the application path listed in the `sn_source_control.properties` file. Repository content outside the application path is ignored.

## MID Server support

Use an existing MID Server to connect to a source control repository. Connecting an application through a MID Server enables access to repositories behind a firewall.

## Source control role permissions

For more information on roles and collaborators, see [Application collaboration](../../applications/concept/application-collaboration.md).

-   **[Link an application or application-customization to source control](../task/source-control-link-application.md)**  
Linking an application or application-customization to source control allows application developers to manage changes in App Engine Studio \(AES\) from a Git repository.
-   **[Edit a Git repository configuration](../task/source-control-edit-repo.md)**  
You can edit a Git repository's integration with App Engine Studio \(AES\) to change the network protocol selection, credentials or other field entries.

**Parent Topic:**[Configure App Engine Studio](configure-aes.md)

