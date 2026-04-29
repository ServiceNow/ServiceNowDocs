---
title: SumTotal Spoke
description: Pull learning courses from SumTotal instance to ServiceNow instance to build an integrated learning content repository.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SumTotal Spoke

Pull learning courses from SumTotal instance to ServiceNow instance to build an integrated learning content repository.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SumTotal spoke v1.0.2 is the latest version.

## Supported versions

This spoke was built for SumTotal version v1, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke actions

|Action|Description|
|------|-----------|
|Look up Activities Stream|Retrieves the main view to get activity or course data.|
|Look up Learning Status Stream|Retrieves the main view to get all user transcript-related data.|
|Look up Users Stream|Retrieves core data of the required employees in SumTotal.|
|Save Assignment|Creates or updates a standard assignment.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the SumTotal spoke](../task/setup-sumtotal.md#).

