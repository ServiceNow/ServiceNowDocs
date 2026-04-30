---
title: Configure KPIs for ITSM work items in the Process Mining dashboard
description: Add the desired Key Performance Indicators \(KPIs\) to monitor the performance of the ITSM work items in the Process Mining Summary and Insights page. Remove the indicators that you no longer want to use.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Content pack for ITSM, Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Configure KPIs for ITSM work items in the Process Mining dashboard

Add the desired Key Performance Indicators \(KPIs\) to monitor the performance of the ITSM work items in the Process Mining Summary and Insights page. Remove the indicators that you no longer want to use.

## Before you begin

**Important:** This feature is available with the ServiceNow Store Process Mining ITSM content pack v1.2. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Role required: administrator

## Procedure

1.  Enable the plugins for the ITSM work item applications for which you want to view the KPIs.

    The Incident Management plugin is enabled by default.

    |To enable this application|Activate this plugin|
    |--------------------------|--------------------|
    |**Problem Management**|Performance Analytics - Content Pack - Problem Management \(com.snc.pa.problem\)|
    |**Change Management**|Performance Analytics - Content Pack - Change Management \(com.snc.pa.change\)|
    |**Request Management**|Performance Analytics - Content Pack - Request Management \(com.snc.pa.request\)|

2.  [Add the desired indicator data source](../../../use/performance-analytics/concept/c_IndicatorSources.md#) to the Summary and Insights page.

    The KPIs listed in the table below are available by default.

<table id="table_url_glm_2qb"><thead><tr><th>

Work item

</th><th>

Key performance indicator

</th></tr></thead><tbody><tr><td>

Incident

</td><td>

-   Average time to resolve incidents
-   % of incidents resolved on first assignment


</td></tr><tr><td>

Problem

</td><td>

-   Average close time of problems
-   % of problems closed on first assignment


</td></tr><tr><td>

Change request

</td><td>

-   Average close time of changes
-   % of new emergency changes


</td></tr><tr><td>

Requested item

</td><td>

-   Average close time of requested items
-   % of rejected requested items


</td></tr></tbody>
</table>
**Parent Topic:**[Content pack for ITSM](../concept/itsm-proc-opti-content-pack.md)

