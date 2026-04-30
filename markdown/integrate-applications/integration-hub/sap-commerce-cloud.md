---
title: SAP Commerce Cloud Spoke
description: The SAP Commerce Cloud spoke is built by Bristlecone, Inc. Retrieve shopping cart content, order details, and order history for a selected customer.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-05"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# SAP Commerce Cloud Spoke

The SAP Commerce Cloud spoke is built by Bristlecone, Inc. Retrieve shopping cart content, order details, and order history for a selected customer.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for SAP Commerce Cloud Version: 2211-jdk21.1 but may be compatible with later versions.

## Spoke requirements

SAP Commerce Cloud subscription.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke version

[SAP Commerce Cloud Spoke](sap-commerce-cloud.md) v 1.1.0 is the latest version.

## Spoke actions

The SAP Commerce Cloud provides actions to automate  tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Order Management|Look Up Order Details|Retrieves order details of the specified order.|
|Look Up Orders|Retrieves the order history for the specified user ID.|
|Shopping Cart|Look Up Shopping Cart|Retrieves the shopping cart content for the specified user ID.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the SAP Commerce Cloud spoke](../task/setup-sap-commerce-cloud.md#).

