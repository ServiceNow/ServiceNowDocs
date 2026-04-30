---
title: Monitor hardware asset performance with Asset KPIs report
description: Track the asset availability and related KPI values in the report to see how well a hardware asset is performing.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-06"
reading_time_minutes: 2
breadcrumb: [Manage and monitor hardware asset performance, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Monitor hardware asset performance with Asset KPIs report

Track the asset availability and related KPI values in the report to see how well a hardware asset is performing.

## Before you begin

**Important:** The Asset KPIs report is available with Hardware Asset Management version 13.0.0 and later.

Role required: asset

## About this task

The Asset KPIs report is available for a hardware asset under the following conditions:

-   The asset belongs to a model category of an opted in resource category, and for which the performance tracking is enabled. For details, see [Opt in to model categories to track performance KPIs for hardware assets](opt-in-kpi-tracking-ham.md).
-   The asset has moved to the In use state, and its KPIs have been calculated and are available in the Asset Availability table \[sn\_ent\_asset\_availability\].

    **Note:** The **Calculate asset performance KPIs** scheduled weekly job runs every Saturday to calculate the KPIs for the assets. These KPIs are then reflected in the Asset availability and related KPIs report, which displays the most recent KPI values.


## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset estate**.

2.  Select the **All assets** tab.

3.  Select the asset record for which you want to view the details of the asset key performance indicators \(KPIs\).

4.  On the contextual sidebar, select the Asset availability and related KPIs icon \[![Asset KPI icon](../../enterprise-asset-management/image/asset-kpi-icon.png)\].

    The Asset KPIs report is displayed.

    ![Asset KPIs report](../../enterprise-asset-management/image/asset-kpis-report-sidebar.png)

5.  To view the details of the report, select any section on the report.

    A form view of the availability record for the asset is shown with additional details such as the following:

    -   **Current asset schedule**: The asset schedule linked to the asset currently and used for KPI calculations. If no schedule is linked, the Default asset schedule is used.
    -   **Start**: The date and time when the asset KPI values were first calculated.
    -   **End**: The date and time when the asset KPI values were last calculated.
    -   **Outages During Interval** tab: A list of outages with details like start and end time of the outage and the duration of the outage. For more details on outage record creation and handling, see [Asset performance reports in the Hardware Asset Workspace](../concept/asset-performance-reports-ham.md).

**Parent Topic:**[Manage and monitor hardware asset performance](../concept/manage-and-monitor-hardware-asset-performance.md)

