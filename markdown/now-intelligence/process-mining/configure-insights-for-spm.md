---
title: Configure insights for SPM demands in the Process Mining dashboard
description: Configure rule definitions for demands to discover insights in the Summary and insights page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/configure-insights-for-spm.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content pack for SPM, Activate Process Mining content packs, Activating Process Mining, Process Mining, Platform Analytics]
---

# Configure insights for SPM demands in the Process Mining dashboard

Configure rule definitions for demands to discover insights in the Summary and insights page.

## Before you begin

**Important:** This feature is available with the ServiceNow Store Process Mining SPM content pack v1.0. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Role required: sn\_process\_optimization\_power\_user

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Configurations**.

2.  [Configure the desired finding definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/view-business-findings.md).

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
    -   To perform cluster analysis, select **Cluster Analysis**. Select **View cluster** to view the results. For more information, see [View a cluster analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/cluster-analysis.md).

**Parent Topic:**[Content pack for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/integration-with-spm.md)

