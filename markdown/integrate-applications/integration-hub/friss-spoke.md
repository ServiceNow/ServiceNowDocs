---
title: FRISS Spoke
description: Integrate a ServiceNow instance with your FRISS account to leverage the fraud detection capabilities for claims and to detect fraud early in the claims process.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# FRISS Spoke

Integrate a ServiceNow instance with your FRISS account to leverage the fraud detection capabilities for claims and to detect fraud early in the claims process.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Subscription information

This spoke requires a subscription. Contact your ServiceNow account manager or sales representative for subscription details. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

## Supported versions

This spoke was built for FRISS API version v 2.0 but may be compatible with later versions.

## Key features

FRISS spoke enables a flow designer to do the following:

-   Integrate with the FRISS API for Claims to save the scores returned by FRISS into the relevant claim data object.
-   Detect fraud as you manage your claims cases.
-   Get real-time scores of your claims data at different stages of the claims process.
-   Use the user interface for portfolio monitoring.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:**

-   Some of these plugins may require the appropriate licensing if used outside the spoke implementation.
-   The flow actions input parameter is provided for you to use. For more information on the sample input data structure and data types used in an array and object, see [Complex data](https://servicenow.com/docs/bundle/tokyo-application-development/page/administer/flow-designer/concept/complex-data.html).

## Spoke actions

The FRISS spoke provides actions that trigger FRISS Trust automation in response to events that occur within your ServiceNow instance. These actions are classified under the Claim Fraud Management category. Available actions include:

|Action|Description|
|------|-----------|
|Look up History Stream by Claim ID|Retrieves all the screening results by the Claim ID.|
|Look up Fraud Indicator Score by Screening ID|Retrieves the fraud score, which has been calculated by FRISS, for a claim that has been identified by a screening ID.|
|Look up Screening ID|Sends a request to calculate a FRISS score for a claim and returns unique ID called screening ID.|
|Delete History by Claim ID|Deletes the screening that is associated with a Claim ID.|
|Delete History by Screening ID|Deletes the screening by the identifier of a screening by FRISS.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For more information about setting up the FRISS spoke, see [Set up the FRISS spoke](../task/set-up-the-friss-spoke.md).

