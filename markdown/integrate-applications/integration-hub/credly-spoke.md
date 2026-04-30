---
title: Credly spoke
description: Credly integration helps employees prove, manage, and showcase their skills more effectively, addressing common issues related to skill verification, visibility, recognition, and career development.Also reuse this short description in the release notes.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-02"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Credly spoke

Credly integration helps employees prove, manage, and showcase their skills more effectively, addressing common issues related to skill verification, visibility, recognition, and career development.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Credly spoke v 1.0.0 is the latest version.

## Supported versions

This spoke was built for xanadu, and is compatible with later Washington DC and Xanadu versions.

## Key features

Credly enables a flow designer to:

-   Sync employee badges
-   Accept/reject badges

## Spoke requirements

A valid Credly account

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed: Credentials core

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Credly provides sample flows to demonstrate automating the Talent Development Core tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Credly event processing|Fetches employee badges to sync from Credly.|

## Spoke subflows

The Credly spoke provides sample subflows to demonstrate automating Talent Development Core tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Process credly event|Processes the credly event that was triggered.|

## Spoke actions

The Credly provides actions to automate Talent Development Core tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Retrieving information|Process event information|Retrieves the event process information.|
|Gen organization name|Retrieves the employee's organization name.|
|Get event details|Retrieves the event details.|
|Get employee data|Retrieves the employee data.|

## Spoke module

Data accessed through these spoke modules is stored in these tables:

|Table|Description|
|-----|-----------|
|Credly Event Log|Retrieves the list of events that were created.|

## Spoke user roles

The Credly provides these user roles to control access to data:

|User role|Description|
|---------|-----------|
|Admin|Role that is authorized to sync employee badges.|
| | |

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.



