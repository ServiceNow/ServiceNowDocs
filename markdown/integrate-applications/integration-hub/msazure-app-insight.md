---
title: Microsoft Azure Application Insights Spoke
description: Manage queries, events, and metrics in Microsoft Azure Application Insights account from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Microsoft Azure Application Insights Spoke

Manage queries, events, and metrics in Microsoft Azure Application Insights account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Microsoft Azure Application Insights spoke v2.0.0 is the latest version.

## Supported versions

This spoke was built for Microsoft Azure Application Insights API version v1, but may be compatible with later versions.

## Spoke requirements

-   Register the application in the Microsoft Azure portal and record the access keys and directory IDs. For more information, see [Azure Application Insights Search API](https://dev.applicationinsights.io/documentation/Authorization/AAD-Application-Setup) in [Azure Application Insights REST API documentation](https://dev.applicationinsights.io/documentation/overview).
-   Add your the redirect URL of your ServiceNow instance in your registered application. The redirect URL must be in this format: `https://<instance>.service-now.com/oauth_redirect.do`. For more information, see [Authentication and authorization for Azure Time Series Insights API](https://docs.microsoft.com/en-us/azure/time-series-insights/time-series-insights-authentication-and-authorization) in [Microsoft Docs](https://docs.microsoft.com/en-us/).
-   Create an API key and record the values of API Key and App ID. These values are needed as inputs to the spoke actions. For more information, see [Getting your API key and Application ID](https://dev.applicationinsights.io/documentation/Authorization/API-key-and-App-ID#:~:text=To%20get%20these%20two%20keys,the%20%22Read%20telemetry%22%20box.) in [Azure Application Insights REST API documentation](https://dev.applicationinsights.io/documentation/overview).

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   Flow Designer Action Step - Payload Builder \(com.glide.hub.action\_step.payload\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft Azure Application Insights spoke provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Event Management|Look up Event|Gets the data for a single event.|
|Look up Events by Type|Executes an OData query for events.|
|Look up OData Metadata|Gets the OData EDMX metadata that describes the event data model.|
|Metric Management|Look up Metric Metadata|Gets that metadata that describes the available metrics.|
|Look up Metric|Gets the metric values for a single metric.|
|Look up Metrics|Gets the metric values for multiple metrics.|
|Query Management|Execute Query|Executes an analytics query for data.|
|Look up Query|Executes an analytics query for data.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Azure Application Insights spoke](../task/setup-msazure-app-insight.md#).

