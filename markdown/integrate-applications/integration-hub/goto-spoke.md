---
title: GoTo Spoke
description: The GoTo spoke provides actions to view and analyze meaningful usage data for GoTo software subscriptions. Analyze usage for GoToMeeting, GoToWebinar, and GoToConnect to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# GoTo Spoke

The GoTo spoke provides actions to view and analyze meaningful usage data for GoTo software subscriptions. Analyze usage for GoToMeeting, GoToWebinar, and GoToConnect to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

GoTo spoke v2.0.1 is the latest version.

## Supported versions

This spoke was built for LogMeIn Admin Center v5.29.0, but may be compatible with later versions.

## Spoke requirements

GoTo admin account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The GoTo spoke provides actions to automate GoTo tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Connect Management|Look up Connect Users Stream|Retrieves a list of all users with a GoToConnect license within a GoTo account.|
|Look Up User Activity Summary Stream|Retrieves a summary of all user activities, including information about the set of users and their associated metrics.|
|Look Up User Activity Details Stream|Retrieves the activity records of the specific user.|
|License Management|Look Up Licenses|Retrieves a list of all product licenses within a GoTo account.|
|Remove User License|Removes a user from a specified product license.|
|Meeting Management|Get Historical Meeting Report|Reports the meeting history of all organizers within a GoTo account during a given date range.|
|Get Upcoming Meeting Report|Reports meetings that are scheduled for all organizers within a GoTo account during a given date range.|
|User Management|Delete User|Deletes a user from a GoTo account.|
|Look up Authenticated User|Retrieves details of the authenticated user, including information about the accounts the user holds.|
|Look up Users|Retrieves a list of all users within a GoTo account.|
|Webinar Management|Get Webinars|Retrieves a list of all webinars for a GoTo account.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

For information about setting up the spoke, see [Set up the GoTo spoke](../task/setup-goto.md#).

