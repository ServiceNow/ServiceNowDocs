---
title: Dropbox Business Spoke
description: Use Dropbox Business as file storage in place of attachments in ServiceNow. This spoke adds Dropbox storage to your ServiceNow instance and enables users to reference Dropbox files in ServiceNow records.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Dropbox spoke subflows]
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Dropbox Business Spoke

Use Dropbox Business as file storage in place of attachments in ServiceNow. This spoke adds Dropbox storage to your ServiceNow instance and enables users to reference Dropbox files in ServiceNow records.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Dropbox Business spoke v1.0.4 is the latest version.

## Supported versions

API version v2.

## Spoke subflows

The Dropbox Business spoke provides sample subflows in the draft state to demonstrate automating Dropbox tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Flow|Description|
|----|-----------|
|Process File Changes|Subflow to process file changes in Dropbox.|
|Process Team Member Changes|Subflow to process team member changes in Dropbox.|

## Spoke actions

The Dropbox Business spoke provides actions to perform Dropbox tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|File and Folder Management|Copy Dropbox File To Attachment|Copies a Dropbox file and attaches it to a ServiceNow record. If a ServiceNow incident record is supplied as input, the specified record is attached to it.|
|Copy File or Folder|Creates a copy of the specified Dropbox file or folder in Dropbox.|
|Create Folder|Creates a folder at the specified path in Dropbox.|
|Delete File Or Folder|Deletes a file or folder at the specified path in Dropbox.|
|Get File Changes - Webhook|Retrieves the file changes noticed in Dropbox.|
|Look up Folder|Looks up the contents of a Dropbox folder and returns an object containing information about the folder|
|Update Latest Cursor|Updates the latest cursor value for the corresponding team in the Team Details table.|
|Upload Attachment to Dropbox|Copies a ServiceNow attachment to a Dropbox folder. It copies to the specified folder. To change the file name during the copy, use the optional file name.|
|User Management|Add Users To Group|Adds users to a specified group|
|Add Users To Team|Adds users to a specified team.|
|Get Admin Details|Retrieves details of the administrator account used to generate the access token.|
|Get Current Account|Retrieves information about the current account.|
|Get Team Members Info|Retrieves information on specified team members. Returns profile and role details.|
|Look up Groups in Team|Lists all the groups in the team. Output includes group IDs, number of members, group name, and the role of users who manage the group.|
|Look up Users in Group|Lists all the members in the specific group. Returns user profile data and role in the group.|
|Look up Users in Team|List all the members in the team. Returns user profile data, membership type, and role.|
|Remove User From Team|Removes user from a team. Options include user retains files, and access to team shares, keeps email account and unrestricted team shares, and to delete relevant data.|
|Remove Users From Group|Removes one or more users from an existing group.|

## Dropbox Business spoke account requirements

The Dropbox Business spoke requires a custom app that you create in Dropbox Business.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Dropbox Business spoke](../task/setup-dbox-busi.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Dropbox alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see [MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

