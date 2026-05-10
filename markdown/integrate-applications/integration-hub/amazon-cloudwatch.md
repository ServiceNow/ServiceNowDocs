---
title: Amazon CloudWatch Spoke
description: Integrate ServiceNow instance with Amazon CloudWatch. Manage and monitor your Amazon Web Services \(AWS\) resources and applications from your ServiceNow instance. Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Amazon CloudWatch Spoke

Integrate ServiceNow instance with Amazon CloudWatch. Manage and monitor your Amazon Web Services \(AWS\) resources and applications from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Amazon CloudWatch version 2010-08-01, but may be compatible with later versions.

## Spoke version

Amazon CloudWatch spoke v1.0.2 is the latest version.

## Spoke requirements

User with full access to Amazon CloudWatch account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Amazon CloudWatch Spoke provides actions to automate Amazon Web Services \(AWS\) resource and application monitoring tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Alarm Management|Create Composite Alarm|Creates a composite alarm.|
|Delete Composite Alarm|Deletes the specified alarms.|
|Look Up Alarm|Retrieves a list of specified alarms.|
|Set Alarm State|Assigns a temporary state to an alarm for testing.|
|Anomaly Management|Create Anomaly Detector|Creates an anomaly detection model for a CloudWatch metric.|
|Delete Anomaly Detector|Deletes the specified anomaly detection model from an account.|
|Metric Management|Delete Metric Alarm|Deletes the specified alarms.|
|Look up Metric Data|Retrieves different metrics in a single request.|
|Upsert Metrics Alarm|Create a new alarm or updates an alarm and associates the alarm with the specified metric, metric math expression, or an anomaly detection model.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

For information about setting up the spoke, see [Set up the Amazon CloudWatch spoke](../task/setup-amazon-cloudwatch.md#).

