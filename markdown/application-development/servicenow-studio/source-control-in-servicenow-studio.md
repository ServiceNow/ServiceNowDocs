---
title: Source control in ServiceNow Studio
description: App developers working in ServiceNow Studio can manage their data repository in numerous ways using source control.
locale: en-US
release: australia
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Source control in ServiceNow Studio

App developers working in ServiceNow Studio can manage their data repository in numerous ways using source control.

After your admin has linked an app to source control, all application developers on a non-production instance can perform these actions:

-   Import applications from a Git repository.
-   Pull and apply remote changes from a Git repository.
-   Commit all local changes on the instance to a Git repository.
-   Create tags to permanently link to a given version of an application.
-   Create branches to maintain multiple versions of an application simultaneously.

For more information, see [Link an app to source control in ServiceNow Studio](../task/link-app-to-source-control.md).

**Note:** If you're using source control to collaborate with other developers, only changes that have been checked in are available to other developers. For example, if an admin creates a new flow for an app that's linked to Git, the new flow won't be available in the app for other users until the admin checks the flow into Git.

-   **[Source control operations in ServiceNow Studio](../reference/source-control-operations-in-sn-studio.md)**  
The source control integration primarily supports operations from ServiceNow Studio, but can also support some operations directly from the Git repository.
-   **[Import an app from source control in ServiceNow Studio](../task/sns-sc-import-app-source-control.md)**  
Importing an application from source control results in a new application being created in your ServiceNow instance based on the remote repository you specify. The account credentials you supply must have read access to the remote repository, and the remote repository you specify must contain a valid ServiceNow application.
-   **[Work with changes in Git](sns-sc-work-with-changes-in-git.md)**  
Developers using ServiceNow Studio can pull and commit changes in their Git repository.
-   **[Create versions and branches in Git](sns-sc-create-versions-branches-git.md#)**  
App developers using ServiceNow Studio can create versions and branches in their Git repositories.
-   **[View commit history](../task/sns-sc-view-commit-history.md)**  
View the commit history of apps linked to a source control repository in ServiceNow Studio
-   **[Move application files in a Git repository](../task/sns-sc-move-app-files-in-git-repo.md)**  
Move application files that are linked to source control to any folder of the repository when working in ServiceNow Studio. Moving application files enables application developers to store supporting content, such as automated tests, in the same repository as the applications they support.

**Parent Topic:**[Working with applications in ServiceNow Studio](working-with-apps-in-servicenow-studio.md)

