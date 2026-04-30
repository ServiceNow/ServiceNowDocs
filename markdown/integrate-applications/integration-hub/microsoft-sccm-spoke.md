---
title: Microsoft SCCM Spoke
description: Automate management of user collections, device collections, and application deployments on a Microsoft System Center Configuration Management \(SCCM\) server.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-04-16"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Microsoft SCCM Spoke

Automate management of user collections, device collections, and application deployments on a Microsoft System Center Configuration Management \(SCCM\) server.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft SCCM spoke v1.1.2 is the latest version.

## Spoke flows &amp; subflows

This spoke has no sample flows or subflows.

## Spoke actions

The Microsoft System Center Configuration Management \(SCCM\) spoke spoke provides actions to automate SCCM tasks when events occur in the ServiceNow AI Platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Application Management|Get Applications|Retrieves the application data from the SCCM server.|
|Deployment Management|Get Deployments|Retrieves deployment data from the SCCM server.|
|Device Management|Add to Device Collection|Adds a device to a collection in SCCM.|
|Get Device Collections|Retrieves device collection data from the SCCM server.|
|Is Device In Collection|Checks if a specified device exists in a device collection.|
|Remove From Device Collection|Removes a device from an existing device collection.|
|User Management|Add to User Collection|Adds a user to a collection in SCCM.|
|Get User Collections|Retrieves user collection data from the SCCM Server.|
|Is User In Collection|Checks if a specified user exists in a user collection.|
|Remove From User Collection|Removes a user from a user collection.|

To see inputs and outputs for these activities, see [SCCM activity pack](https://www.servicenow.com/docs/access?context=c_SCCMActivityPack&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the SCCM alias record to authorize actions on a Microsoft System Center Configuration Management \(SCCM\) server.

|Connection alias|Description|Connection URL|
|----------------|-----------|--------------|
|SCCM|Connection to the SCCM server.|The URL of the host machine where the SCCM server is installed.|

For information about setting up the spoke, see [Set up SCCM spoke](../../integrationhub-store-spokes/task/set-up-sccm.md#).

## MID server requirements

To use these actions, your instance must have a MID Server set up and configured to use PowerShell. For more information about running actions on the MID Server, see [Integration steps](integration-steps.md). For information, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../../integrationhub-store-spokes/task/config-adv-mid-settings-for-oauth-on-mid.md).

