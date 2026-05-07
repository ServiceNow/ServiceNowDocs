---
title: Work with changes in Git
description: Developers using ServiceNow Studio can pull and commit changes in their Git repository.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Source control in ServiceNow Studio, Working with applications, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Work with changes in Git

Developers using ServiceNow Studio can pull and commit changes in their Git repository.

**Note:** If you’re using source control to collaborate with other developers, only changes that have been checked in are available to other developers. For example, if an admin creates a new flow for an app that’s linked to Git, the new flow won’t be available in the app for other ServiceNow Studio users until the admin checks the flow into Git.

-   **[Pull changes from a repository](../task/sns-sc-pull-changes-from-repository.md)**  
App developers using ServiceNow Studio can pull changes from a linked Git repository to apply remote changes to the local instance.
-   **[Commit changes to a repository](../task/sns-sc-commit-changes-to-repository.md)**  
Commit changes made in your application in ServiceNow Studio to a linked Git repository. You can either select a few changes to commit, or commit all changes on the instance at once.
-   **[Stash local changes](../task/sns-sc-stash-local-changes.md)**  
You can stash \(or save\) changes made locally on application files, pull the latest version of files from your repository, and apply those changes to your instance. When complete, your application files match those in the repository. You can then recover and apply your local changes at a later time in ServiceNow Studio.
-   **[Manage stashed changes](../task/sns-sc-manage-stashed-changes.md)**  
App developers can apply or delete stashed changes from ServiceNow Studio.
-   **[Resolve conflicts](../task/sns-sc-resolving-conflicts.md)**  
Resolve conflicts in ServiceNow Studio before applying remote or stashed changes. Conflicts occur when there are multiple change versions of the same application file: one set of changes in the remote or stashed version and another set of changes in the local version.

**Parent Topic:**[Source control in ServiceNow Studio](source-control-in-servicenow-studio.md)

