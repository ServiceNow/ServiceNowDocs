---
title: SmartRecruiters Spoke
description: The SmartRecruiters spoke provides actions to view and analyze meaningful usage data for SmartRecruiters software subscriptions. Analyze usage for your SmartRecruiters account based on more than 60 activities, including job application creation and job ad creation. Use this data to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SmartRecruiters Spoke

The SmartRecruiters spoke provides actions to view and analyze meaningful usage data for SmartRecruiters software subscriptions. Analyze usage for your SmartRecruiters account based on more than 60 activities, including job application creation and job ad creation. Use this data to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for the SmartRecruiters January 2021 release version, but may be compatible with later versions.

## Spoke requirements

SmartRecruiters admin account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The SmartRecruiters spoke provides actions to automate SmartRecruiters tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Audit Management|Look up Audit Events Stream|Retrieves the list of audit events for all users.|
|User Management|Activate User|Activates the specified user's account.|
|Deactivate User|Deactivates the specified user's account.|
|Look up Users Stream|Retrieves the list of all users within an account.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the SmartRecruiters spoke](../task/setup-smartrecruiters.md#).

