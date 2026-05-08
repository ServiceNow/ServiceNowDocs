---
title: SCCM Usage Metering Spoke
description: Manage the process of fetching software usage data from a Microsoft System Center Configuration Management \(SCCM\) Usage Metering server. Get data about software usage metering and when the software was last used using this spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SCCM Usage Metering Spoke

Manage the process of fetching software usage data from a Microsoft System Center Configuration Management \(SCCM\) Usage Metering server. Get data about software usage metering and when the software was last used using this spoke.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SCCM Usage Metering spoke v1.0.2 is the latest version.

## Supported versions

This spoke was built for Microsoft SCCM version 1602, but may be compatible with later versions.

## Spoke Requirements

-   Microsoft System Center Configuration Management Usage Metering Server version 2012 R2 with software metering enabled. For more information about software metering, see [Software metering in Configuration Manager](https://docs.microsoft.com/en-us/configmgr/apps/deploy-use/monitor-app-usage-with-software-metering)

    **Note:** Ensure that metering rules are configured in SCCM for the required software.

-   Microsoft SQL Server 2014

## Spoke flows and subflows

This spoke has no flows and subflows.

## Spoke actions

The SCCM Usage Metering spoke provides actions to retrieve software usage data from a Microsoft System Center Configuration Management Usage Metering server. Available actions include:

|Action|Description|
|------|-----------|
|Get Software Last Used Data|Retrieves the last usage data of the required software from the Microsoft SCCM server.|
|Get Software Usage Data|Retrieves usage metering of the required software from the Microsoft SCCM server.|

**Note:**

The spoke actions support a maximum payload of 10 MB from the SCCM server for the JDBC step.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

For information about setting up the spoke, see [Set up the SCCM Usage Metering spoke](../task/setup-sccm-usage-metering-spoke.md#).

## MID Server requirements

These actions use REST calls, which can run on an instance or MID Server. Use the connection record that is associated with the Microsoft SCCM Usage Metering alias to configure where actions run as well as to set MID Server selection attributes. For more information, see MID server.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

