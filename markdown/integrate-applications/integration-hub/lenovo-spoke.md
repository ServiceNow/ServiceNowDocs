---
title: Lenovo Spoke
description: Get the warranty details of your hardware assets from Lenovo.Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Lenovo Spoke

Get the warranty details of your hardware assets from Lenovo.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Lenovo Warranty API v2.5, but may be compatible with later versions.

## Spoke requirements

You should have the Client ID provided by Lenovo. If you don’t have one, contact your organization's Lenovo sales or service representative.

## Spoke dependencies

The Lenovo spoke doesn't have a dependency on any other plugin.

## Spoke actions

The Lenovo spoke provides action to automate downloading asset warranty information when events occur in your ServiceNow instance. Available action is as follows:

|Action|Description|
|------|-----------|
|Download Asset Warranty|Connect to the Lenovo Warranty API to download asset warranty information.|

**Note:** For more information on getting asset warranty details from Lenovo, see [Integration with Lenovo for asset warranty details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/integration-with-lenovo-asset-warranty.md).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

To use the actions in the Lenovo spoke, you must create a connection and credential record to authenticate and connect to Lenovo. For more information, see [Create a connection and credential for Lenovo spoke](../task/configure-connection-cred-lenovo.md)

