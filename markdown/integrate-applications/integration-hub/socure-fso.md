---
title: Socure Spoke
description: Integrate ServiceNow instance with your Socure account to access information about scores, watchlists, and so on.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Socure Spoke

Integrate ServiceNow instance with your Socure account to access information about scores, watchlists, and so on.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Subscription information

This spoke requires a subscription. Contact your ServiceNow account manager or sales representative for subscription details. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

## Spoke version

Socure spoke v1.1.0 is the latest version.

## Supported versions

This spoke was built for Socure V3.0, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Socure Spoke provides actions \(under the ID Modules category\) to automate tasks when events occur in your ServiceNow instance. Available actions include:

|Action|Description|
|------|-----------|
|Look up Address Risk Score|Retrieves the address risk scores and reason codes.|
|Look up Fraud Score|Retrieves the fraud scores and reason codes.|
|Look up Email Risk Score|Retrieves the email risk scores and reason codes.|
|Look up KYC Score|Retrieves the KYC\(Know your Customer\) scores and reason codes.|
|Look up Reason Codes and Descriptions|Retrieves the reason codes and descriptions.|
|Look up Phone Risk Score|Retrieves the phone risk scores and reason codes.|
|Look up Watchlist|Retrieves the global watchlist matches.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Socure spoke](../task/setup-socure.md).

