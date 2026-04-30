---
title: Roadmunk Spoke
description: The Roadmunk spoke provides actions to view and analyze meaningful usage data for Roadmunk software subscriptions. Analyze usage for your Roadmunk account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Roadmunk Spoke

The Roadmunk spoke provides actions to view and analyze meaningful usage data for Roadmunk software subscriptions. Analyze usage for your Roadmunk account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Roadmunk spoke v1.6.4 is the latest version.

## Supported versions

This spoke was built for the Roadmunk June 2021 release version, but may be compatible with later versions.

## Spoke requirements

Roadmunk account with an Account Admin user role.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Roadmunk spoke provides actions to automate Roadmunk tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Account Management|Look up Account|Retrieves information about a Roadmunk account.|
|Feedback Management|Look up Feedback Stream|Retrieves a list of all feedback.|
|Idea Management|Look up Ideas Stream|Retrieves a list of all ideas.|
|Roadmap Management|Look up Roadmaps Stream|Retrieves a list of all roadmaps.|
|User Management|Look up Users Stream|Retrieves a list of all users within an account.|
|Look up Users Using File|Retrieves a list of users from a file that is attached to a record.|
|Deactivate User|Deactivates a Roadmunk user.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Roadmunk spoke](../task/setup-roadmunk.md#).

