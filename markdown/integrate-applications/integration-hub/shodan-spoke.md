---
title: Shodan Spoke
description: Manage exploits, alerts, hosts, and others, in Shodan account from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Shodan Spoke

Manage exploits, alerts, hosts, and others, in Shodan account from your ServiceNow® instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Shodan spoke v1.1.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Shodan spoke provides actions to automate Shodan tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Exploit Management|Exploit Search|Searches for exploits from vulnerability data sources.|
|Get Exploit Count|Retrieves the number of exploits for a specific query.|
|Network Alert Management|Get Alert Details|Retrieves details of the specific network alert.|
|Look up Alerts|Retrieves the list of network alerts.|
|Search Management|Get Host Details|Retrieves details of all services that are associated with specified host IP.|
|Get Host Count|Retrieves the total number of hosts that match the provided query and requested facet information.|
|Search Shodan|Retrieves details from a Shodan search.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

Two connection and credential alias records are available along with the Shodan spoke.

For information about setting up the spoke, see [Set up the Shodan spoke](../task/setup-shodan-spoke.md#).

