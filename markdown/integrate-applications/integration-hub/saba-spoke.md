---
title: Saba Spoke
description: The Saba spoke enables you to pull learning courses, course activity and users from a Saba instance into a ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Saba Spoke

The Saba spoke enables you to pull learning courses, course activity and users from a Saba instance into a ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Saba spoke v1.1.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - JSON Parser \[com.glide.hub.action\_step.jsonparser\]
-   IntegrationHub Standard Spokes \[com.glide.hub.action\_step.xmlparser\]

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke flows

The Saba spoke provides a flow to pull tokens on a scheduled basis. Enable the flow to ensure that the spoke actions work properly.

|Flow|Description|
|----|-----------|
|Get Saba Token|Retrieves access token for Saba and generates a new refresh token after every six days.|

## Spoke actions

The Saba spoke provides actions to automate Saba tasks when events occur in the ServiceNow instance. Available actions include:

|Action|Description|
|------|-----------|
|Get Authorization Code|Retrieves the authorization code that is required to get the access token in the Saba system.|
|Get Access Token|Retrieves the access token for Saba based on username, password, authorization code, connection alias, and application registry.|
|Get Refresh Token|Retrieves the refresh token for Saba.|
|Get Saba System Timezone Difference|Compares the time zones of the Saba system and ServiceNow platform and retrieves the difference.|
|Look up Courses Stream|Retrieves the main view to get course data. This is based on filters such as count per page, and start page.|
|Look up User Course Activity Stream|Retrieves user progress on course items.|
|Look up Users Stream|Retrieves data of employees from the the Saba system.|
|Save Assignment|Creates or updates a standard assignment.|

## Spoke module

The Saba spoke adds a Saba application to your ServiceNow instance. The Saba application has the following module:

|Module|Description|
|------|-----------|
|Credentials|Details required to pull tokens from the Saba system.|

## Saba spoke account requirements

The Saba spoke requires registering an OAuth 2.0 application in your Saba account to generate OAuth 2.0 tokens for the Saba spoke. Record the generated Client ID, Client Secret, Application key, Integration user name, and password for later use.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up Saba spoke](../task/set-up-saba.md#).

