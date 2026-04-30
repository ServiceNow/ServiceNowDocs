---
title: Use AES with a Git source control repository
description: App developers working in App Engine Studio \(AES\) can manage their data repository in numerous ways.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Use AES with a Git source control repository

App developers working in App Engine Studio \(AES\) can manage their data repository in numerous ways.

After your [admin has linked an application to Source control](aes-source-control-integration.md), all application developers on a non-production instance can perform these actions:

-   Import applications from a Git repository.
-   Pull and apply remote changes from a Git repository.
-   Commit all local changes on the instance to a Git repository.
-   Create tags to permanently link to a given version of an application.
-   Create branches to maintain multiple versions of an application simultaneously.

**Note:** If you’re using source control to collaborate with other developers, only changes that have been checked in are available to other developers. For example, if an admin creates a new flow for an app that’s linked to Git, the new flow won’t be available in the app for other AES users until the admin checks the flow into Git.

## Options available from App Engine Studio

After an application has been linked to source control, application developers can use App Engine Studio to manage the repository. From App Engine Studio, developers can:

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

The source control integration sanitizes only content within the application path listed in the `sn_source_control.properties` file. Repository content outside the application path is ignored.

## MID Server support

Use an existing MID Server to connect to a source control repository. Accessing an application through a MID Server enables access to repositories behind a firewall.

-   **[Source control operations in App Engine Studio](../reference/source-control-operations.md)**  
The source control integration primarily supports operations from App Engine Studio \(AES\), but can also support some operations directly from the Git repository.
-   **[Import application or application-customization from source control](../task/source-control-import.md)**  
Import an app or app customization from a source control repository into App Engine Studio \(AES\) to continue developing it on this instance.
-   **[Work with changes in Git](work-changes-in-git.md)**  
Developers using App Engine Studio \(AES\) can pull and commit changes in their Git repository.
-   **[Create versions and branches in Git](create-versions-branches-git.md#)**  
App developers using App Engine Studio \(AES\) can create versions and branches in their Git repositories.
-   **[Stash changes](stash-changes.md)**  
Developers can remove and save changes locally to apply them later, and manage stashed changes from App Engine Studio \(AES\).
-   **[Resolve conflicts](../task/source-control-resolve-conflicts.md)**  
App developers can select the app file version to use when applying remote or stashed changes in App Engine Studio \(AES\).
-   **[View commit history](../task/source-control-view-commit-history.md)**  
App developers can view the commit history of apps linked to a source control repository in App Engine Studio \(AES\).
-   **[Move application files in a Git repository](../task/source-control-move-files-git.md)**  
Move application files linked to source control to any folder of the repository when working in App Engine Studio \(AES\). Allow application developers to store supporting content such as automated tests in the same repository as the applications they support.

**Parent Topic:**[Building apps in App Engine Studio](aes-app-creation.md)

