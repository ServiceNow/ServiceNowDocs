---
title: Magnit Spoke
description: The ServiceNow Magnit spoke pulls contingent workers from the Magnit application into a ServiceNow instance and creates onboarding tasks for those contingent workers from a ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Magnit Spoke

The ServiceNow® Magnit spoke pulls contingent workers from the Magnit application into a ServiceNow instance and creates onboarding tasks for those contingent workers from a ServiceNow instance.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Magnit spoke v1.1.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Magnit spoke actions are used to pull data from a Magnit application into a ServiceNow instance. Available actions include:

|Action|Description|
|------|-----------|
|Look Up Correlation ID for Delta Pull|Fetches the correlation ID for a delta pull. This action is handled from the Magnit application end.|
|Look Up Correlation ID for Full Pull|Fetches the correlation ID for a full pull. This action is handled from the Magnit application end.|
|Look up Contingent Workers Stream|**Look Up Correlation ID for Delta Pull** or **Look Up Correlation ID for Full Pull** is passed through the **Look up Contingent Workers Stream** action to pull full data or partial data.|

