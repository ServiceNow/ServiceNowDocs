---
title: Blue Prism Spoke
description: Manage jobs and processes in Blue Prism environment from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Blue Prism Spoke

Manage jobs and processes in Blue Prism environment from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Blue Prism spoke v1.0.2 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Workflow Studio - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Integration Hub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow Integration Hub Action Step - XML Parser \(com.glide.hub.action\_step.xmlparser\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for Blue Prism Process Dispatch Framework version 2.6, but may be compatible with later versions.

## Spoke Requirements

Blue Prism account.

## Spoke flows and subflows

This spoke has no flows and subflows.

## Spoke actions

The Blue Prism spoke provides actions to automate Blue Prism tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Job Management|Get Job Status|Retrieves the status of the specified job.|
|List Job Outputs|Retrieves the list of outputs of a job associated with the specified session ID.|
|Start Job|Executes a job with the specified inputs on the Blue Prism environment.|
|Process Management|Get Process Parameters|Retrieves the list of parameters for the specified process on the Blue Prism environment.|
|List Processes|Retrieves the list of processes on the Blue Prism environment.|
|Utilities|Generate Collection Inputs|Creates a formatted string of the collection type. This formatted string is used as input for the Start Job action.|

For information about setting up the spoke, see [Set up the Blue Prism spoke](../task/setup-blueprism.md#).

## MID Server requirements

To use these actions, your instance must have a MID Server set up and configured to use SOAP. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md). For more information about the MID Server, see [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

