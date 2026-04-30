---
title: Legacy - Available source control operations
description: The source control integration primarily supports operations from Studio, but can also support some operations directly from the GIT repository.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Available source control operations

The source control integration primarily supports operations from Studio, but can also support some operations directly from the GIT repository.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [Building applications with ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

<table id="table_w5q_nph_t5"><thead><tr><th>

Operation

</th><th>

Description

</th><th>

Available from

</th></tr></thead><tbody><tr><td>

Import from Source Control

</td><td>

Imports an application from the repository to the local instance.

</td><td>

Studio

</td></tr><tr><td>

Link to Source Control

</td><td>

Allows developers to manage application changes from a GIT repository.

</td><td>

Studio

</td></tr><tr><td>

Edit Repository Configuration

</td><td>

Updates the GIT repository user credentials.

</td><td>

Studio

</td></tr><tr><td>

Apply Remote Changes

</td><td>

Updates the local version of the application to match the repository version.

</td><td>

Studio

</td></tr><tr><td>

Commit Changes

</td><td>

Updates the repository version of the application to match the local version.

</td><td>

Studio

</td></tr><tr><td>

Stash Local Changes

</td><td>

Removes and saves local changes for later work.

</td><td>

Studio

</td></tr><tr><td>

Switch Branch

</td><td>

Updates the local version of the application to match the repository branch version.

</td><td>

Studio

</td></tr><tr><td>

Create Branch

</td><td>

Creates a branch in the repository to save a different version of the application.

</td><td>

-   Studio
-   GIT repository

</td></tr><tr><td>

Create Tag

</td><td>

Creates a tag in the repository to link to a particular application version.

</td><td>

-   Studio
-   GIT repository

</td></tr><tr><td>

Manage Stashes

</td><td>

Allows developers to apply or delete stashed changes.

</td><td>

Studio

</td></tr><tr><td>

Create repository

</td><td>

Creates a repository to store application changes

</td><td>

GIT repository

</td></tr><tr><td>

Create credentials

</td><td>

Creates credentials to the repository.

</td><td>

GIT repository

</td></tr><tr><td>

Grant access to repository

</td><td>

Provides read and write access to the repository tied to a specific set of credentials.

</td><td>

GIT repository

</td></tr><tr><td>

Source Control repository sync

</td><td>

Allows admins to apply remote changes from the Source Control repository, to resynchronize with the instance.**Note:** This operation is only available if Delta loading is being used for the repository. See [Legacy - Delta loading](../concept/delta-loading.md).

</td><td>

Repository Configuration form

</td></tr></tbody>
</table>**Parent Topic:**[Legacy - Source Control integration](../concept/c_SourceControlIntegration.md)

