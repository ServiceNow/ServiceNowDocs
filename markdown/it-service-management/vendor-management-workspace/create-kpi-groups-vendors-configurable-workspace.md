---
title: Create KPI groups to track metrics for your vendors
description: Create key performance indicator \(KPI\) groups and include KPIs that matter most for your vendors. Associate the KPI groups with your vendors, set thresholds to monitor indicator status, and analyze vendor performance.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Create KPI groups to track metrics for your vendors

Create key performance indicator \(KPI\) groups and include KPIs that matter most for your vendors. Associate the KPI groups with your vendors, set thresholds to monitor indicator status, and analyze vendor performance.

## Before you begin

Configure [Performance analytics indicators](https://www.servicenow.com/docs/access?context=c_Indicators&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) that you want to add to each vendor KPI group. For a list of indicators that are available by default refer to [Installed with Vendor Management Workspace](../reference/installed-w-vendor-manager-configurable-workspace.md).

The indicators must have a vendor breakdown on the Company \[core\_company\] table with associated vendors.

You can configure and track up to six KPIs with a percentage value that contribute towards the vendor score. Add 15 more KPIs with any unit value to analyze additional data.

For each indicator, configure:

-   A weight value—A numeric value that indicates the percentage of contribution towards the vendor score. This value represents the importance of that indicator relative to other indicators within that KPI group. Each indicator is weighted against 100% of the combined weight of all indicators added to the KPI group. If the combined weight is over or under 100 %, then the weight of the indicators will be proportionately readjusted to 100.
-   Order of priority—You can also establish the order of priority in which you want these indicators to appear on the vendor profile.
-   Thresholds—Define upper and lower limit values to assess vendor performance for each indicator.

Role required: sn\_vlm.vendor\_admin

## Procedure

1.  Navigate to **All** &gt; **Vendor Management** &gt; **Configuration** &gt; **KPI Groups**.

2.  Create a KPI group.

    **Note:** You can also open an existing KPI group, create a copy of it, and modify it based on your needs.

    1.  Click **New**.
    2.  In the **Name** field, enter a name for the KPI group.
    3.  From the Type menu, select **Vendors**.
    4.  Right-click the form header and click **Save**.
3.  Add KPIs to a KPI group.

    1.  In the KPIs related list, click **New**.

        |Field|Description|
        |-----|-----------|
        |Indicator|Descriptive name for the indicator.|
        |Indicator display name|Business-friendly name for the indicator. This name displays in the Vendor KPI Groups widget in Vendor Management Workspace.|
        |Weight|The percentage of the total score you would like to attribute to this indicator. The combined weight of all indicators added to a KPI group must equal to 100.|
        |Order|The order of priority in which you want this indicator to display in the Vendor Score Metrics widget in Vendor Management Workspace.|
        |Lower Threshold|Lower limit defined for this indicator. You can view the highlighted value seen in Vendor Management Workspace vendor profile.|
        |Upper Threshold|Upper limit defined for this indicator. You can view the highlighted value seen in Vendor Management Workspace.|

    2.  In the **KPI** field, select the KPI to apply for this vendor.

        **Note:** The KPI could also have child KPIs that you could drill down into.

    3.  Click **Submit**.
4.  Set KPI thresholds for a KPI group.

    1.  In the KPI Group Thresholds related list, click **New**.
    2.  In the **Lower Threshold** field, enter the lower threshold limit to be used for the status defined for the KPI group.
    3.  In the **Upper Threshold** field, enter the upper threshold limit to be used for the status defined for the KPI group.
    4.  In the **Order** field, enter a number for the defined threshold limits. This number must be unique for each set of limits.
    5.  In the **Status** field, select the status for the defined threshold as critical, positive, or warning.
    **Note:** The corresponding icon for each status displays in the manager workspace when the **Show Icon** check box is enabled for the status. This is enabled by default for the critical status.

5.  Add vendors to the KPI groups.

    1.  In the Vendors related list, click **Edit**.
    2.  Move the desired vendors from the Collection to the Vendors list.
    3.  Click **Save**.

## What to do next

[Associate](../concept/using-vendor-management-workspace.md) the KPI group to vendors.

