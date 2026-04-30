---
title: Salesforce Marketing Cloud Spoke
description: The Salesforce Marketing Cloud spoke is built by Bristlecone, Inc. This spoke provides actions to retrieve records from your Salesforce Marketing Cloud data extensions and retrieve and update user information.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Salesforce Marketing Cloud Spoke

The Salesforce Marketing Cloud spoke is built by Bristlecone, Inc. This spoke provides actions to retrieve records from your Salesforce Marketing Cloud data extensions and retrieve and update user information.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Salesforce Marketing Cloud spoke v1.5.2 is the latest version.

## Supported versions

This spoke was built for Salesforce Marketing Cloud Corporate Edition.

## Spoke requirements

Admin user with privileges to create new users and roles in Salesforce Marketing Cloud.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Salesforce Marketing Cloud spoke provides actions to automate Salesforce Marketing Cloud tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Data Extension Management|Look up Data Extension Attributes|Retrieves records from data extensions with less than 2500 records.|
|Look up Data Extension Attributes for Bulk Records Stream|Retrieves bulk records from data extensions.|
|User Management|Look up Users Stream|Retrieves user properties for your Salesforce Marketing Cloud users based on the specified user properties and associated filters.|
|Update User by User ID|Updates user properties based on the user ID.|

## Spoke tables

The Salesforce Marketing Cloud spoke adds the following table:

<table id="table_ajt_dvq_n4b"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Configurations

</td><td>

Displays the list of Salesforce Marketing Cloud configurations, such as data extensions.

</td><td>

-   Configuration Type
-   Configuration Value

</td></tr></tbody>
</table>**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Connection and credential alias requirements

The Salesforce Marketing Cloud spoke uses a Connection &amp; Credential alias for the connection setup and the user profile that is attached to the SOAP security policies for the credential setup. If you are connecting to multiple Salesforce Marketing Cloud environments, you must use the same credential information in each environment.

For information about setting up the spoke, see [Set up the Salesforce Marketing Cloud spoke](../task/setup-salesforce-marketing-cloud.md#).

