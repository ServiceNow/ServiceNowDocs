---
title: Source control operations in App Engine Studio
description: The source control integration primarily supports operations from App Engine Studio \(AES\), but can also support some operations directly from the Git repository.
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Use AES with a Git source control repository, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Source control operations in App Engine Studio

The source control integration primarily supports operations from App Engine Studio \(AES\), but can also support some operations directly from the Git repository.

<table id="table_w5q_nph_t5"><thead><tr><th>

Operation

</th><th>

Description

</th><th>

Available from

</th></tr></thead><tbody><tr><td>

Import from source control

</td><td>

Imports an application from the repository to the local instance. For more information, see [Import application or application-customization from source control](../task/source-control-import.md).

</td><td>

App Engine Studio

</td></tr><tr><td>

Link to source control

</td><td>

Allows developers to manage application changes from a Git repository. For more information, see [Link an application or application-customization to source control](../task/source-control-link-application.md).

</td><td>

App Engine Studio

</td></tr><tr><td>

Edit Repository Configuration

</td><td>

Updates the Git repository user credentials. For more information, see [Edit a Git repository configuration](../task/source-control-edit-repo.md).

</td><td>

App Engine Studio

</td></tr><tr><td>

Apply Remote Changes

</td><td>

Updates the local version of the application to match the repository version. For more information, see [Pull changes from a repository](../task/source-control-apply-changes.md).

</td><td>

App Engine Studio

</td></tr><tr><td>

Commit Changes

</td><td>

Updates the repository version of the application to match the local version. For more information, see [Commit changes to a repository](../task/source-control-commit-changes.md).

</td><td>

App Engine Studio

</td></tr><tr><td>

Stash Local Changes

</td><td>

Removes and saves local changes for later work. For more information, see [Stash local changes](../task/source-control-stash-changes.md).

</td><td>

App Engine Studio

</td></tr><tr><td>

Switch Branch

</td><td>

Updates the local version of the application to match the repository branch version. For more information, see [Switch branches](../concept/create-versions-branches-git.md#).

</td><td>

App Engine Studio

</td></tr><tr><td>

Create Branch

</td><td>

Creates a branch in the repository to save a different version of the application. For more information, see [Create a branch](../concept/create-versions-branches-git.md#).

</td><td>

-   App Engine Studio
-   Git repository

</td></tr><tr><td>

Create Tag

</td><td>

Creates a tag in the repository to link to a particular application version. For more information, see [Create a tag to link to a particular application version](../concept/create-versions-branches-git.md#).

</td><td>

-   App Engine Studio
-   Git repository

</td></tr><tr><td>

Manage Stashes

</td><td>

Allows developers to apply or delete stashed changes. For more information, see [Manage stashes](../task/source-control-manage-stashes.md).

</td><td>

App Engine Studio

</td></tr><tr><td>

Create repository

</td><td>

Creates a repository to store application changes.

</td><td>

Git repository

</td></tr><tr><td>

Create credentials

</td><td>

Creates credentials to the repository.

</td><td>

Git repository

</td></tr><tr><td>

Grant access to repository

</td><td>

Provides read and write access to the repository tied to a specific set of credentials.

</td><td>

Git repository

</td></tr></tbody>
</table>**Parent Topic:**[Use AES with a Git source control repository](../concept/aes-source-control-use.md)

