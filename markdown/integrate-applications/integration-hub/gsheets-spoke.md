---
title: Google Sheets Spoke
description: Manage spreadsheets in Google Sheets from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Google Sheets Spoke

Manage spreadsheets in Google Sheets from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Google Sheets spoke v1.0.7 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for Google Sheets v4, but may be compatible with later versions.

## Spoke requirements

Google Cloud Platform account.

## Spoke actions

The Google Sheets spoke provides actions to automate Google Sheets tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Sheet Management|Add Row|Adds a row with the specified values to a sheet.|
|Clear Cells|Clears the values in the sheet for the specified range.|
|Copy Sheet|Copies a sheet from a spreadsheet to another spreadsheet.|
|Create Sheet|Creates a sheet in the specified spreadsheet.|
|Delete Sheet|Deletes a sheet in the spreadsheet.|
|Get Cell Values|Retrieves the values in the sheet for the specified range.|
|Update Cells|Updates a range of cell values in a sheet.|
|Spreadsheet Management|Get Spreadsheet Details|Retrieves details about the specified spreadsheet.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Google Sheet spoke](../task/setup-gsheets.md#).

