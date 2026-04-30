---
title: Secureworks CTP Spoke
description: Integrate ServiceNow instance with Secureworks Counter Threat Platform \(CTP\). Manage events and tickets in Secureworks Counter Threat Platform from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Secureworks CTP Spoke

Integrate ServiceNow instance with Secureworks Counter Threat Platform \(CTP\). Manage events and tickets in Secureworks Counter Threat Platform from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Secureworks CTP spoke v1.0.3 is the latest version.

## Supported versions

This spoke was built for Secureworks CTP V4, but may be compatible with later versions.

## Spoke requirements

Secureworks portal account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Secureworks CTP spoke provides actions to automate Secureworks CTP tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Event Management|Get Event Details|Retrieves the details of a specific event.|
|Get Recent Events|Retrieves details of a list of recent events.|
|Ticket Management|Assign Ticket To Secureworks SOC|Assigns a ticket to the Secureworks Security Operations Centers \(SOC\) Team.|
|Close Secureworks Ticket|Closes the specified Secureworks ticket.|
|Get Ticket Details|Retrieves the details of the specified Secureworks ticket.|
|Look up Tickets|Retrieves a list of tickets from Secureworks.|
|Post Worklog to Secureworks Ticket|Adds a worklog to the Secureworks ticket.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Secureworks CTP spoke](../task/setup-secureworks-ctp.md#).

