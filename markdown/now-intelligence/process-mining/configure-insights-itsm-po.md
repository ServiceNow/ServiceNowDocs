---
title: Configure insights in the Process Mining dashboard
description: Configure rule definitions for incidents, problems, change requests, or request items to discover insights in the Summary and insights page.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content pack for ITSM, Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Configure insights in the Process Mining dashboard

Configure rule definitions for incidents, problems, change requests, or request items to discover insights in the Summary and insights page.

## Before you begin

**Important:** This feature is available with the ServiceNow Store Process Mining ITSM content pack v1.2. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Role required: sn\_process\_optimization\_power\_user

## About this task

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Configurations**.

2.  [Configure the desired finding definitions](../concept/view-business-findings.md#).

    The insights filters listed in the table below are available by default.

<table id="table_jc3_pzy_2qb"><thead><tr><th>

Work item

</th><th>

Insights filters

</th></tr></thead><tbody><tr><td>

Incident

</td><td>

-   Multihop issue
-   Solution rejection issue
-   Misuse of On Hold state
-   SLA missed issues


</td></tr><tr><td>

Problem

</td><td>

-   Problem was canceled
-   Problem risk was accepted
-   Resolved problem was re-analyzed
-   Problem fix not completed
-   Problem reopened


</td></tr><tr><td>

Change requests

</td><td>

-   Model is changed in the process
-   Pre-approved change requests
-   Failed change requests


</td></tr><tr><td>

Requested items

</td><td>

-   RITM state is closed incomplete or closed skipped
-   Multihop: RITM going through two or more reassignment


</td></tr></tbody>
</table>    When the finding rules are updated, you can view that in the Insights section in the dashboard.

3.  On the Summary and insights page, for the selected insight:

    -   To perform process analysis, select **Process Analysis**. You can view the Process Mining map with the applied filters.
    -   To perform cluster analysis, select **Cluster Analysis**. Select **View cluster** to view the results. For more information, see [View a cluster analysis](../concept/cluster-analysis.md).

**Parent Topic:**[Content pack for ITSM](../concept/itsm-proc-opti-content-pack.md)

