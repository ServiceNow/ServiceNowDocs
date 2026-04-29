---
title: Configure insights for SPM demands in the Process Mining dashboard
description: Configure rule definitions for demands to discover insights in the Summary and insights page.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SPM, Activate content packs, Activate, Process Mining, Platform Analytics]
---

# Configure insights for SPM demands in the Process Mining dashboard

Configure rule definitions for demands to discover insights in the Summary and insights page.

## Before you begin

**Important:** This feature is available with the ServiceNow Store Process Mining SPM content pack v1.0. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Role required: sn\_process\_mining\_power\_user

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Configurations**.

2.  [Configure the desired finding definitions](view-business-findings.md#).

    The insights filters available for a demand by default are defined in the following table:

<table><tbody><tr><td rowspan="2">

Finding Definitions

</td><td>

Demands that have been approved without being qualified

</td></tr><tr><td>

Demands that have been moved to the next stage without being approved

</td></tr><tr><td>

Automated Finding Definitions

</td><td>

Rework

</td></tr></tbody>
</table>    When the finding rules are updated, you can view that in the Insights section in the dashboard.

3.  On the Summary and insights page, for the selected insight:

    -   To perform process analysis, select **Process Analysis**. You can view the Process Mining map with the applied filters.
    -   To perform cluster analysis, select **Cluster Analysis**. Select **View cluster** to view the results. For more information, see [View a cluster analysis](cluster-analysis.md).

**Parent Topic:**[Content pack for SPM](integration-with-spm.md)

