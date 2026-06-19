---
title: Source control in ServiceNow Studio
description: Use source control in ServiceNow Studio to manage app versions, commit changes, and collaborate with other developers through a linked Git repository.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/source-control-in-servicenow-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-05-19"
reading_time_minutes: 2
breadcrumb: [Applications in ServiceNow Studio, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Source control in ServiceNow Studio

Use source control in ServiceNow Studio to manage app versions, commit changes, and collaborate with other developers through a linked Git repository.

After an admin links an app to source control, all application developers on a non-production instance can perform the following actions:

-   Import applications from a Git repository.
-   Pull and apply remote changes from a Git repository.
-   Commit all local changes on the instance to a Git repository.
-   Create tags to permanently link to a specific version of an application.
-   Create branches to maintain multiple versions of an application at the same time.

For more information, see [Link an app to source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/link-app-to-source-control.md).

**Note:** When using source control to collaborate with other developers, only changes that have been checked in are available to other developers. For example, if an admin creates a new flow for an app linked to Git, the flow is not available to other users until the admin checks it into Git.

-   **[Source control operations in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/source-control-operations-in-sn-studio.md)**  
Most source control operations in ServiceNow Studio run from within the platform. Some operations — such as creating branches and tags — can also be performed directly from the Git repository.
-   **[Import an app from source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-import-app-source-control.md)**  
Import an application from a Git repository into ServiceNow Studio to create a local copy of the app on your non-production instance. The repository must contain a valid ServiceNow application, and your credentials must have read access.
-   **[Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md)**  
Pull and commit changes in a Git repository directly from ServiceNow Studio to keep app development in sync across your team.
-   **[Create versions and branches in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-create-versions-branches-git.md)**  
Create tags and branches in a Git repository from ServiceNow Studio to version application releases and manage parallel development streams.
-   **[View commit history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-view-commit-history.md)**  
View the commit history of apps linked to a source control repository in ServiceNow Studio to review what changes were committed, by whom, and when.
-   **[Move application files in a Git repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/sns-sc-move-app-files-in-git-repo.md)**  
Move application files linked to source control to any folder in the repository from ServiceNow Studio to store supporting content, such as automated tests, alongside the applications they support.

**Parent Topic:**[Applications in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/working-with-apps-in-servicenow-studio.md)

