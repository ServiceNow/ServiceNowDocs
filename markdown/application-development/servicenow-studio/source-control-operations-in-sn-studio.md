---
title: Source control operations in ServiceNow Studio
description: The source control integration primarily supports operations from ServiceNow Studio, but can also support some operations directly from the Git repository.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Source control in ServiceNow Studio, Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Source control operations in ServiceNow Studio

The source control integration primarily supports operations from ServiceNow Studio, but can also support some operations directly from the Git repository.

<table id="table_w5q_nph_t5"><thead><tr><th>

Operation

</th><th>

Description

</th><th>

Available from

</th></tr></thead><tbody><tr><td>

Import from source control

</td><td>

Imports an application from the repository to the local instance. For more information, see [Import an app from source control in ServiceNow Studio](../task/sns-sc-import-app-source-control.md).

</td><td>

ServiceNow Studio

</td></tr><tr><td>

Link to source control

</td><td>

Allows developers to manage application changes from a Git repository. For more information, see [Link an app to source control in ServiceNow Studio](../task/link-app-to-source-control.md).

</td><td>

ServiceNow Studio

</td></tr><tr><td>

Edit repository configuration

</td><td>

Updates the Git repository user credentials. For more information, see [Edit a Git repository configuration in ServiceNow Studio](../task/sns-sc-edit-git-repo-configuration.md).

</td><td>

ServiceNow Studio

</td></tr><tr><td>

Apply remote changes

</td><td>

Updates the local version of the application to match the repository version. For more information, see [Pull changes from a repository](../task/sns-sc-pull-changes-from-repository.md).

</td><td>

ServiceNow Studio

</td></tr><tr><td>

Commit changes

</td><td>

Updates the repository version of the application to match the local version. For more information, see [Commit changes to a repository](../task/sns-sc-commit-changes-to-repository.md).

</td><td>

ServiceNow Studio

</td></tr><tr><td>

Stash local changes

</td><td>

Removes and saves local changes for later work. For more information, see [Stash local changes](../task/sns-sc-stash-local-changes.md).

</td><td>

ServiceNow Studio

</td></tr><tr><td>

Switch branch

</td><td>

Updates the local version of the application to match the repository branch version. For more information, see [Switch repository branches](../concept/sns-sc-create-versions-branches-git.md#).

</td><td>

ServiceNow Studio

</td></tr><tr><td>

Create branch

</td><td>

Creates a branch in the repository to save a different version of the application. For more information, see [Create a repository branch](../concept/sns-sc-create-versions-branches-git.md#).

</td><td>

-   ServiceNow Studio
-   Git repository

</td></tr><tr><td>

Create tag

</td><td>

Creates a tag in the repository to link to a particular application version. For more information, see [Create a tag to link to a particular application version](../concept/sns-sc-create-versions-branches-git.md#).

</td><td>

-   ServiceNow Studio
-   Git repository

</td></tr><tr><td>

Manage stashes

</td><td>

Allows developers to apply or delete stashed changes. For more information, see [Manage stashed changes](../task/sns-sc-manage-stashed-changes.md).

</td><td>

ServiceNow Studio

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
</table>**Parent Topic:**[Source control in ServiceNow Studio](../concept/source-control-in-servicenow-studio.md)

