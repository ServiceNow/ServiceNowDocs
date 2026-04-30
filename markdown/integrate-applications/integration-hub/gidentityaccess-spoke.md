---
title: Google Identity and Access Spoke
description: Manage folders, projects, roles, and service accounts in Google Identity and Access Management and Google Resource Manager.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Google Identity and Access Spoke

Manage folders, projects, roles, and service accounts in Google Identity and Access Management and Google Resource Manager.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Identity and Access spoke v1.1.1 is the latest version.

## Supported Versions

This spoke was built for API version v2 only Folder Management category and v1 for other categories, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke requirements

Google Cloud Platform account.

## Spoke flows and subflows

This spoke has no flows and subflows.

## Spoke actions

The Google Identity and Access spoke provides actions to automate Google Identity and Access Management and Google Resource Manager tasks when events occur in ServiceNow. For the spoke actions to be performed, you must ensure that your project or organization in Google Cloud Platform has the mentioned permissions. Available actions include:

|Category|Action|Description|Required Permission|
|--------|------|-----------|-------------------|
|Folder Management|Create Folder|Creates a folder.|resourcemanager.folders.create|
|Delete Folder|Deletes a folder.|resourcemanager.folders.delete|
|Look up Child Folder|Retrieves the information of a child folder.|resourcemanager.folders.get|
|Look up Folders|Retrieves the list of folders.|resourcemanager.folders.list|
|Rename Folder|Renames the specified folder.|resourcemanager.folders.update|
|Restore Folder|Restores the specified folder.|resourcemanager.folders.undelete|
|Organization Management|Look up Organization by Organization ID|Retrieves details of the specified organization.|resourcemanager.organizations.get|
|Project Management|Create Project|Creates a project.|resourcemanager.projects.create|
|Delete Project|Deletes the specified project.|resourcemanager.projects.delete|
|Look up Project by Project ID|Retrieves details of the specified project.|resourcemanager.projects.get|
|Look up Projects|Retrieves the list of projects.|resourcemanager.projects.list|
|Look up Projects Stream|Retrieves the list of projects as a complex object.|resourcemanager.projects.list|
|Rename Project|Renames the specified project.|resourcemanager.projects.update|
|Restore Project|Restores the specified project.|resourcemanager.projects.undelete|
|Role Management|Create Role For Organization|Creates a custom role for an organization.|iam.roles.create|
|Create Role For Project|Creates a custom role for the specified project.|iam.roles.create|
|Delete Role For Organization|Deletes a custom role for the specified organization.|iam.roles.delete|
|Delete Role For Project|Deletes a custom role for the specified project.|iam.roles.delete|
|Look up Role for Organization|Retrieves details of the custom role for the specified organization.|iam.roles.get|
|Look up Role For Project|Retrieves details of the custom role for the specified project.|iam.roles.get|
|Look up Roles in Organization by Organization ID|Retrieves the list of custom roles for the specified organization.|iam.roles.list|
|Look up Roles in Organization Stream|Retrieves the list of custom roles for the specified organization as a complex object.|iam.roles.list|
|Look up Roles in Project by Project ID|Retrieves the list of custom roles for the specified project.|iam.roles.list|
|Look up Roles in Project Stream|Retrieves the list of custom roles in given project ID.|iam.roles.list|
|Restore Role For Organization|Restores the specified custom role for an organization.|iam.roles.undelete|
|Restore Role For Project|Restores the specified custom role for a project.|iam.roles.undelete|
|Service Account Management|Look up Service Account|Retrieves the details of the specified service account.|iam.serviceAccounts.get|
|Look up Service Accounts by Project ID|Retrieves the list of service accounts in a project.|iam.serviceAccounts.list|

For more information about the required permissions, see [IAM permissions reference](https://cloud.google.com/iam/docs/permissions-reference).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Google Identity and Access Spoke](../task/setup-gidentityaccess.md#).

