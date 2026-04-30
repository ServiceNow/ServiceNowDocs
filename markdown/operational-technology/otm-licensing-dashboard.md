---
title: OTM Licensing dashboard
description: Use the OTM Licensing dashboard to assess resource consumption and status in relation to your acquired subscriptions. The dashboard provides dedicated reports for each OTM application, providing visual representations of daily usage counts and the average utilization of subscription units over a 90-day period. The OTM Licensing dashboard is an integral component of ITOM Licensing application version 4.0, accessible at ServiceNow Store.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [OTM SU Licensing References, Operational Technology Management licensing and subscriptions, Operational Technology]
---

# OTM Licensing dashboard

Use the OTM Licensing dashboard to assess resource consumption and status in relation to your acquired subscriptions. The dashboard provides dedicated reports for each OTM application, providing visual representations of daily usage counts and the average utilization of subscription units over a 90-day period. The OTM Licensing dashboard is an integral component of ITOM Licensing application version 4.0, accessible at ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Required ServiceNow AI Platform roles

admin

## Access the Assessment dashboard

To open the dashboard for OTM, navigate to **All** &gt; **OTM License** &gt; **OTM Licensing Dashboard**.

![OTM Licensing Dashboard with Visibility tab selected](../image/otm-dashboard-visibility-updated.png "OTM Licensing dashboard - Visibility")

![Licensing Dashboard with Foundation tab selected](../image/otm-dashboard-foundation.png "OTM Licensing dashboard - Foundation")

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|admin|Validate the resource usage for different OTM products. Report the cases where the organization exceeded the number of purchased subscription units for specific resources.|

**Note:** ServiceNow applications refer to devices and applications that comprise an application service as configuration items \(CIs\).

## Data visualization

The dashboard includes the following visualization:

<table id="table_lcd_5vt_yrb"><thead><tr><th>

Title

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OTM Visibility Usage and OTM Foundation Usage

</td><td>

ITOM Licensing CI Counts \[itom\_lu\_ci\_counts\] and UsageAnalytics Counts for Tables \[usageanalytics\_count\]

</td><td>

Displays bars that represent counts of CIs of different licensable categories for the last 120 days per ITOM application. The dashboard also displays the line that represents the average consumption of subscription units for the last 90 days.**Note:** CIs managed by SG-OT Excel are counted and listed for license consumption with last\_scan dates more recent than, equal to, and older than 90 days ago.

</td></tr></tbody>
</table>**Parent Topic:**[OTM SU Licensing References](otm-su-licensing-references.md)

