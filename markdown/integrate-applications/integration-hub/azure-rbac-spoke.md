---
title: Microsoft Azure RBAC Spoke
description: Integrate ServiceNow instance with Microsoft Azure RBAC to manage roles and retrieve details about role assignments for groups and users.Also reuse this short description in the release notes.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-22"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Microsoft Azure RBAC Spoke

Integrate ServiceNow instance with Microsoft Azure RBAC to manage roles and retrieve details about role assignments for groups and users.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Azure RBAC Spoke v 1.0.2 is the latest version.

## Supported versions

This spoke was built for Microsoft Graph REST API v1.0, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft Azure RBAC Spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|Permissions Required \(from least to most privileged\)|
|--------|------|-----------|------------------------------------------------------|
|Group Management|Look up Groups by Role Stream|Lists all the groups that contains the given role.|Delegated \(work or school account\)|RoleManagement.Read.Directory, RoleManagement.Read.All, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|RoleManagement.Read.Directory, RoleManagement.Read.All, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Role Management|Assign Role to Group|Assigns the required role to a group.|Delegated \(work or school account\)|RoleManagement.ReadWrite.Directory|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|RoleManagement.ReadWrite.Directory|
|Assign Role to User|Assign the required role to a user.|Delegated \(work or school account\)|RoleManagement.ReadWrite.Directory|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|RoleManagement.ReadWrite.Directory|
|Look up Roles|Retrieves details of the required role or retrieves details of all the roles in Entra ID if no inputs are provided.|Delegated \(work or school account\)|RoleManagement.Read.Directory, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|RoleManagement.Read.Directory, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Look up Roles by Group|Lists details of all roles in a group.|Delegated \(work or school account\)|RoleManagement.Read.Directory, RoleManagement.Read.All, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|RoleManagement.Read.Directory, RoleManagement.Read.All, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Look up Roles by User|Lists all roles of the user.|Delegated \(work or school account\)|RoleManagement.Read.Directory, RoleManagement.Read.All, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|RoleManagement.Read.Directory, RoleManagement.Read.All, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Remove Role from a User or Group|Remove the required role for a user or group.|Delegated \(work or school account\)|RoleManagement.ReadWrite.Directory|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|RoleManagement.ReadWrite.Directory|
|User Management|Look up Users by Role Stream|Lists details all the users that have the required role.|Delegated \(work or school account\)|RoleManagement.Read.Directory, RoleManagement.Read.All, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|RoleManagement.Read.Directory, RoleManagement.Read.All, Directory.Read.All, RoleManagement.ReadWrite.Directory, Directory.ReadWrite.All|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

