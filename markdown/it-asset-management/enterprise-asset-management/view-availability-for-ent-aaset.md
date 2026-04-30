---
title: Monitor enterprise asset performance with Asset KPIs report
description: Track the asset availability and related KPI values in the report to see how well an enterprise asset is performing.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-04"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise assets, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Monitor enterprise asset performance with Asset KPIs report

Track the asset availability and related KPI values in the report to see how well an enterprise asset is performing.

## Before you begin

**Important:** The Asset KPIs report is available with Enterprise Asset Management version 9.0 and later.

Role required: sn\_eam.enterprise\_asset\_manager or enterprise\_asset\_technician

## About this task

The Asset KPIs report is available for an enterprise asset under the following conditions:

-   The asset belongs to a model category for which the performance tracking is enabled. For details, see [Opt in to model categories to track performance KPIs for enterprise assets](opt-in-kpi-tracking-eam.md).
-   The asset has moved to the In use state, and its KPIs have been calculated and are available in the Asset Availability \[sn\_ent\_asset\_availability\] table.

    **Note:** The **Calculate asset performance KPIs** scheduled job runs every week on Saturday to calculate the KPIs for the assets. These KPIs are then reflected in the Asset availability and related KPIs report, which displays the most recent KPI values.


## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Enterprise asset estate**.

2.  Select the **All assets** tab.

3.  Select the asset record for which you want to view the details of the asset key performance indicators \(KPIs\).

4.  On the contextual sidebar, select the Asset availability and related KPIs icon \[![Asset KPI icon](../image/asset-kpi-icon.png)\].

    The Asset KPIs report is displayed.

    ![Asset KPIs report](../image/asset-kpis-report-sidebar.png)

5.  To view the details of the report, select any section on the report.

    A form view of the availability record for the asset is shown with additional details such as the following:

    -   **Current asset schedule**: The asset schedule linked to the asset currently and used for KPI calculations. If no schedule is linked, the Default asset schedule is used.
    -   **Start**: The date and time when the asset KPI values were first calculated.
    -   **End**: The date and time when the asset KPI values were last calculated.
    -   **Outages During Interval** tab: A list of outages with details like start and end time of the outage and the duration of the outage. For more details on outage record creation and handling, see [Asset performance reports in the Enterprise Asset Workspace](../concept/asset-performance-reports-eam.md).

**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

