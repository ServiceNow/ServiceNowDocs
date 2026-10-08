---
title: Managing application and record changes
description: All changes made to applications or metadata records display on the Changes tab of the activity bar in ServiceNow Studio. View and manage changes made to applications tracked in update sets or attached to a Git repository.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/managing-application-and-record-changes.html
release: brazil
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-09-21"
reading_time_minutes: 4
breadcrumb: [Use, ServiceNow Studio, Build, AI Workflow Factory, Building applications]
---

# Managing application and record changes

All changes made to applications or metadata records display on the Changes tab of the activity bar in ServiceNow Studio. View and manage changes made to applications tracked in update sets or attached to a Git repository.

## Working with different types of applications

Manage custom apps you create in ServiceNow Studio through update sets or by connecting them to a Git repository. Applications can be converted to ServiceNow Fluent and manage the app through Fluent source control.

For more information, see [Update sets in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.md) and [Convert an application to Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/convert-app-to-fluent.md).

You can customize or extend out-of-the-box/base system ServiceNow applications to function to your specifications. However, because they contain proprietary code, all base system applications must be managed through update sets and XML. Base system apps cannot be converted to Fluent source code or managed through a Git repository.

**Important:** Only admins can work on Fluent apps. Don't convert the app if delegated developers must continue working on the application.

## Update set and Git repository operations

Change operations for apps and metadata records can be performed from the Changes tab. When working with Build Agent, changes from each checkpoint are tracked in an update set. If you want to create a batch update set, select the **Batch** option in the Changes tab, and the platform record for the batch opens in the canvas. For more information about all update set operations, see [Update sets in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.md).

Operations available for apps and records connected to Git differ depending on whether the app has been converted to Fluent. For applications and records converted to Fluent, see [Using Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/fluent-sc-using-fluent-source-control.md). For non-Fluent apps and metadata records, see [Work with changes in Git](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/sns-sc-work-with-changes-in-git.md).

**Note:** Changes tracked in metadata source control display as update sets, not Git source control files. For more information, see [Metadata source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/source-control-in-servicenow-studio.md).

## Working with changes

The Changes tab contains information to help you identify changes.

-   **C**: Out-of-the-box/Store apps
-   **S**: Custom Scoped apps
-   **G**: Global apps
-   \[Omitted image "sn-studio-changes-git.png"\] Alt text:: Changes tracked through a Git repository
-   \[Omitted image "sn-studio-changes-update-set.png"\] Alt text:: Changes tracked through update sets

\[Omitted image "sn-studio-identify-changes.png"\] Alt text: On the Changes tab, view updates to custom, store, and global apps and metadata records tracked in update sets or connected to Git.

Filter the list of changes by selecting **My apps** or **All apps**. All changed apps appear in the Changes tab, whether tracked through update sets or Git source control.

\[Omitted image "sn-studio-changes-filter.png"\] Alt text: View apps that you have changed, or view all apps on the instance that have changed.

Select the more actions icon \[Omitted image "sn-studio-more-options-icon.png"\] Alt text:to access options for showing and hiding file count, metadata category, and parent categories. Select one or all of the options to see more information about each file. Clear all of the options to hide categorizations and just see a list of files.

\[Omitted image "sn-studio-changes-tab-show-all.png"\] Alt text: Select one or more option to show or hide file count, metadata type, and parent categories.

Selecting a changed record tracked under an update set opens it in the canvas with a code or metadata diff viewer. The diff view depends on the type of file that you select.

\[Omitted image "sn-studio-changes-file-diff.png"\] Alt text: Some files open with a code based diff viewer.\[Omitted image "sn-studio-changes-metadata-diff.png"\] Alt text: Other types of files open with a metadata record view of the differences.

Selecting an application connected to Git shows staged changes, untracked changes, and recent commits.

\[Omitted image "sn-studio-changes-git-commit.png"\] Alt text: View changes, commits, and deploy your changes to Git from the Changes panel.

Use the more actions icon on each entry in the Changes tab to access additional options. For applications and records connected to Git, you can add the app to the Explorer and open App details.

**Note:** Selecting **Add app to explorer** can produce different results depending on the following scenarios:

-   If an app is not a Fluent app, then it is converted to Fluent and added to the Explorer.
-   If an app is a Fluent app but is not in the Explorer, it is added to the Explorer.
-   If an app is a Fluent app and is in the Explorer, the Explorer tab is focused and a message indicates that the app is in the workspace.

\[Omitted image "sn-studio-changes-add-actions-git.png"\] Alt text: Add an app linked to Git to the explorer or open app details.

For apps and records tracked through update sets, you can open app details, view all update sets, or create an update set.

\[Omitted image "sn-studio-changes-add-actions.png"\] Alt text: Create or view update sets or open app details.

For more information, see [Update sets in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.md).

**Parent Topic:**[Using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/using-servicenow-studio.md)

