---
title: Navex EthicsPoint Spoke
description: The Navex EthicsPoint spoke enables you to pull employee relation cases from a Navex EthicsPoint instance into a ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Navex EthicsPoint Spoke

The Navex EthicsPoint spoke enables you to pull employee relation cases from a Navex EthicsPoint instance into a ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Navex EthicsPoint spoke v1.0.3 is the latest version.

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

## Spoke actions

The Navex EthicsPoint spoke provides actions to automate tasks when events occur in the ServiceNow instance.

|Category|Action|Description|
|--------|------|-----------|
|Attachment Management|Look up Case File - Attachment File|Retrieves the case file attachment.|
|Look up Case Text File|Retrieves the case text file.|
|Case Management|Add Child Note|Adds a child note to the specified case.|
|Add Participant|Adds a participant to the specified case.|
|Look up Full Case|Retrieves the full case for the specified case ID.|
|Look up Participant|Retrieves the participant for the specified ID.|
|Look up Query Case Stream|Retrieves the query case stream for the case.|
|Update Case|Updates the case for the specified case ID.|
|Update Participant|Updates the participant for the specified case.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up Navex EthicsPoint spoke spoke](../task/setup-navex-spoke.md#).

