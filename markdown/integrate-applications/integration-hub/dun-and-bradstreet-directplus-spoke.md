---
title: Dun and Bradstreet DirectPlus Spoke
description: Manage comprehensive business data and analytics tasks in your Dun and Bradstreet account from your ServiceNow instance.Also reuse this short description in the release notes.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Dun and Bradstreet DirectPlus Spoke

Manage comprehensive business data and analytics tasks in your Dun and Bradstreet account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Dun and Bradstreet DirectPlus spoke v1.0.0 is the latest version.

## Supported versions

This spoke was built for Dun and Bradstreet DirectPlus v1, but may be compatible with later versions.

## Spoke requirements

Dun and Bradstreet Direct+ account

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Workflow Studio - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Dun and Bradstreet DirectPlus spoke provides sample flows to demonstrate automating the Dun and Bradstreet DirectPlus tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Look up Companies|Retrieves the supplier information and verifies if the supplier is in good business standing before creating a new supplier in the downstream system.|

## Spoke actions

The Dun and Bradstreet DirectPlus spoke provides actions to automate data and analytics tasks tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_a4c_wvp_c2c"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data Block Management

</td><td>

Look up Data Blocks by Duns Number

</td><td>

Retrieves information about the specified data block for the specified D-U-N-S \(Data Universal Numbering System\) number.

</td></tr><tr><td>

Profile Management

</td><td>

Look up Industry Detailed Profile

</td><td>

Retrieves detailed information about the requested industry, including industry indicators, challenges, financials, and industry forecast.

</td></tr><tr><td>

Report Management

</td><td>

Look up Company Report

</td><td>

Retrieves the Dun and Bradstreet\(D&amp;B\)'s Business Information Report and Comprehensive Report that can be used for determining a company's profitability, stability, viability, and payment performance to evaluate the risk for both new or existing business relationships.**Note:** PDF reports are not available for all markets, including Canada. For better global coverage, use the HTML format of the report.

</td></tr><tr><td rowspan="2">

Search Management

</td><td>

Look up Company Typeahead Search

</td><td>

Retrieves the company records based on search term and other additional attributes of the company.**Note:** This action returns the top 25 matched results.

</td></tr><tr><td>

Look up Identity Resolution Cleanse Match

</td><td>

Retrieves the best matches for provided search parameters using Dun &amp; Bradstreet proprietary algorithms.**Note:** For Multi-Process, this action returns only one result. For a nationwide search in US, this action returns a maximum 100 results. In all other scenarios, this action returns the top 25 matched results.

</td></tr></tbody>
</table>## Spoke module

The Dun and Bradstreet DirectPlus spoke adds the Dun and Bradstreet DirectPlus spoke application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Companies|Lists all the available companies records.|

