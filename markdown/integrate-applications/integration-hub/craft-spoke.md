---
title: Craft spoke
description: Manage alerts and retrieve company information from Craft from your ServiceNow instance.Also reuse this short description in the release notes.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Craft spoke

Manage alerts and retrieve company information from Craft from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Craft spoke v1.0.0 is the latest version.

## Supported versions

This spoke was built for Craft version v1, but may be compatible with later versions.

## Spoke requirements

Craft account

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Remote Tables \(com.glide.script.vtable\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Craft spoke provides sample flows to demonstrate automating the Craft tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Create Incident if Company is not Active|Fetches company data using the required fragments aliases. If the company is not active, an incident with a description and a short description is created.|

## Spoke actions

The Craft spoke provides actions to automate Craft tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Alert Management|Look up Alerts Stream|Retrieves the list of alerts from Craft.|
|Company Data Management|Look up Added Companies Stream|Retrieves the list of added companies from Craft.|
|Look up Company Data|Retrieves the company information for the specified details.|
|Look up Company Details by Name.|Retrieves the company information for the specified company name.|

## Spoke module

The Craft spoke adds the Craft Spoke application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Craft Alerts|Lists the alerts that are retrieved from the Import Craft Alerts import.|
|Query Fragments|Lists all the query data about the company such as company name, company ID and so on.|

Data accessed through these spoke modules is displayed in these Remote tables:

**Note:** When you open a remote table, the actions you've set up run in the background to fetch information from Craft. This information displays in the table. When you close the remote table, the information is deleted.

<table id="table_jsm_3xt_gdc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Recently added companies

</td><td>

Retrieves the list of companies that were activated in the last 7 days.

</td></tr><tr><td>

Recent Craft alerts

</td><td>

Runs the remote Recent Craft Alerts remote definition in the background and retrieves the list of all alerts.**Note:** You can customize the alert filter by modifying the script in the Recent Craft Alerts remote definition.

</td></tr></tbody>
</table>## Import set

The Craft spoke adds this Import in the integrations:

|Import|Description|
|------|-----------|
|Import Craft Alerts|Retrieves the alerts from Craft and stores them in the Crafts Alerts table.|

