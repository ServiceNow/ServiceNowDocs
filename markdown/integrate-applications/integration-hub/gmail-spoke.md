---
title: Gmail Spoke
description: Set up an outbound integration between the ServiceNow instance and the Google APIs.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Gmail Spoke

Set up an outbound integration between the ServiceNow instance and the Google APIs.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

API version v1.

## Spoke version

Gmail spoke v1.3.3 is the latest version.

## Spoke subflows

The Gmail spoke provides sample subflows in the draft state to demonstrate automating Gmail tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Move a ServiceNow attachment to Gmail|Copies an attachment from ServiceNow to Gmail.|

## Spoke actions

The Gmail spoke provides actions to automate Gmail tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Label Management|Add Label to Email|Add a label to an email.|
|Create New Label|Create a label in your Gmail account.|
|Lookup Label ID By Name|Retrieve details of a specified Label ID.|
|Remove Label From Email|Remove the specified label from an email.|
|Email Management|Add Attachment To ServiceNow Record|Add an attachment from an email in your Gmail account to a ServiceNow record.|
|Get Email Details|Retrieve details of a specified email.|
|Look Up Emails|Retrieve details of specified emails.|
|Reply To Email|Send a reply to an email.|
|Send Email|Send email from your Gmail account to specified recipients.|
|Delete Email|Delete the specified email.|
|Undelete Email|Retrieve the specified email from the Bin.|

## Gmail spoke account requirements

The Gmail spoke requires a custom app that you create in the Google Developers Console.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Gmail spoke](../task/setup-gmail.md#).

## MID Server requirements

These actions use REST calls that can run either on an instance or, optionally, through a MID Server. Use the connection record associated with the Gmail alias to configure where actions run and, if needed, specify MID Server selection attributes. For more information, see MID server.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

