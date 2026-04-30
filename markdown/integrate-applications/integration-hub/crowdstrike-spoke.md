---
title: CrowdStrike Spoke
description: Manage licenses for CrowdStrike Falcon protection suite by fetching details of devices with active Falcon sensors installed and checking license compliance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# CrowdStrike Spoke

Manage licenses for CrowdStrike Falcon protection suite by fetching details of devices with active Falcon sensors installed and checking license compliance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

CrowdStrike spoke v1.1.0 is the latest version.

## Spoke requirements

CrowdStrike account with a Falcon administrator role.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses when used outside the spoke implementation.

## Spoke actions

The CrowdStrike spoke provides actions to automate CrowdStrike tasks when events occur in your ServiceNow instance.

<table id="table_vbc_jvt_pqb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Host Management

</td><td>

Look up Active Hosts

</td><td>

Retrieves all active hosts. Active hosts are the hosts on which the last\_seen date is greater than the date provided in the **Active Since** field.

</td></tr><tr><td>

Look up Host Details

</td><td>

Retrieves details of the hosts for the Device IDs passed in the **Host IDs** field.

</td></tr><tr><td rowspan="2">

Sensor Management

</td><td>

Look up Hourly Sensor Usage

</td><td>

Retrieves a daily breakdown of your Customer Identification \(CID\) average hourly sensor usage by sensor category.**Note:** The usage data is retrieved up to two days prior to the current date.

</td></tr><tr><td>

Look up Weekly Sensor Usage

</td><td>

Retrieves a daily breakdown of your CID average weekly sensor usage by sensor category.**Note:** The usage data is retrieved up to two days prior to the current date.

</td></tr></tbody>
</table>**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

