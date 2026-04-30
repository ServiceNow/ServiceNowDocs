---
title: Ethoca spoke
description: Integrate ServiceNow instance with your Ethoca account to manage card dispute resolution and prevent fraud. By using this spoke, you can access detailed merchant information and subscription control, view digital receipts, and manage their disputes.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Ethoca spoke

Integrate ServiceNow instance with your Ethoca account to manage card dispute resolution and prevent fraud. By using this spoke, you can access detailed merchant information and subscription control, view digital receipts, and manage their disputes.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Subscription information

This spoke requires a subscription. Contact your ServiceNow account manager or sales representative for subscription details. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

## Spoke version

Ethoca spoke v1.0.0 is the latest version.

## Supported versions

This spoke was built for Ethoca Consumer Clarity.

## Key features

Ethoca spoke enables a flow designer to build workflows using actions that invoke Ethoca Consumer Clarity API. This includes the ability to:

-   Identify and prevent disputes
-   Efficiently handle important dispute resolution tasks, such as recognizing merchants and improving the cardholder's digital experience

## Spoke requirements

Ethoca configuration details such as, certificate, key alias, consumer key, and keystore password.

## Spoke dependencies

Ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** If used outside the spoke implementation, some of these plugins are licensable features and need appropriate licenses.

## Spoke actions

The Ethoca spoke provides actions to obtain enriched merchant and transaction information. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Consumer Clarity|Look up Consumer Clarity|Enables cardholders to view their credit card transactions with clear merchant information and transaction details.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Ethoca spoke](../task/set-up-ethoca-spoke.md#)

