---
title: Configure KPIs for ITSM work items in the Process Mining dashboard
description: Add the desired Key Performance Indicators \(KPIs\) to monitor the performance of the ITSM work items in the Process Mining Summary and insights page. Remove the indicators that you no longer want to use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/configure-kpi-itsm-po.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ITSM, Automatic content pack delivery, Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Configure KPIs for ITSM work items in the Process Mining dashboard

Add the desired Key Performance Indicators \(KPIs\) to monitor the performance of the ITSM work items in the Process Mining Summary and insights page. Remove the indicators that you no longer want to use.

## Before you begin

**Important:** This feature is included with the Process Mining ITSM content pack, which is delivered automatically when ITSM is installed on your instance. For more information, see [Automatic delivery of content packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/process-mining-content-pack-delivery.md).

Role required: Administrator

## Procedure

1.  Enable the plugins for the ITSM work item applications for which you want to view the KPIs.

    The Incident Management plugin is enabled by default.

    |To enable this application|Activate this plugin|
    |--------------------------|--------------------|
    |**Problem Management**|Performance Analytics - Content Pack - Problem Management \(com.snc.pa.problem\)|
    |**Change Management**|Performance Analytics - Content Pack - Change Management \(com.snc.pa.change\)|
    |**Request Management**|Performance Analytics - Content Pack - Request Management \(com.snc.pa.request\)|

2.  [Add the desired indicator data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_IndicatorSources.md) to the Summary and insights page.

    The KPIs listed in the following table are available by default.

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
**Parent Topic:**[Content pack for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/itsm-proc-opti-content-pack.md)

