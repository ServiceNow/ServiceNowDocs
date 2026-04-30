---
title: Calendly Spoke
description: The Calendly spoke provides actions to view and analyze meaningful usage data for Calendly software subscriptions. Analyze usage for a Calendly account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Calendly Spoke

The Calendly spoke provides actions to view and analyze meaningful usage data for Calendly software subscriptions. Analyze usage for a Calendly account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Calendly spoke v1.3.1 is the latest version.

## Spoke requirements

-   Organization owner or admin role in Calendly
-   LastPass Enterprise admin account

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Calendly spoke provides actions to automate Calendly tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
||||
|Event Management|Cancel Event|Cancels the specified event.|
|Look up Event|Retrieves the details of a specified event.|
|Look up Scheduled Events Stream|Retrieves details about all scheduled events within an organization.|
|User Management|Invite User to Organization|Invites the specified user to the organization.|
|Look up Organization|Retrieves the URI of the organization that the authenticated user currently belongs to.|
|Look up Organization Members Stream|Retrieves details about all members within an organization.|
|Look up User|Retrieves the details of the specified user.|
|Remove User from Organization|Deletes a user's organization membership.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Calendly spoke](../task/setup-calendly.md#).

