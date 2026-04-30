---
title: Cisco Webex Meetings Spoke
description: Manage users of the Cisco Webex Meetings application. Get a list of all users, view user activity, and deactivate user accounts.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Cisco Webex Meetings Spoke

Manage users of the Cisco Webex Meetings application. Get a list of all users, view user activity, and deactivate user accounts.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Cisco Webex Meetings spoke v2.3.3 is the latest version.

## Supported versions

Webex Meetings XML API

## Spoke actions

The Cisco Webex Meetings spoke provides actions to automate Webex tasks when events occur in the ServiceNow AI Platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Training Management|Look up Trainings Stream|Retrieves details of all scheduled training sessions.|
|Support Session Management|Look up Support Sessions Stream|Retrieves details of the previously hosted support sessions.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Webex Meetings account requirements

The Cisco Webex Meetings spoke requires creating a custom app in Cisco DevNet to generate OAuth 2.0 tokens. See [Create a Webex OAuth application in Cisco DevNet](../task/setup-webex-meetings-spoke.md#).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the Webex alias record to authorize actions. For information about setting up the spoke, see [Set up Cisco Webex Meetings spoke](../task/setup-webex-meetings-spoke.md#).

