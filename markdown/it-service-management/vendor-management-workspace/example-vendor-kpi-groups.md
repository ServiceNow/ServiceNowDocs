---
title: Example for Vendor Management Workspace setup
description: Learn how you can create KPI groups using Vendor Management Workspace with an example.
locale: en-US
release: xanadu
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Vendor KPI Groups in Vendor Management Workspace, Exploring Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Example for Vendor Management Workspace setup

Learn how you can create KPI groups using Vendor Management Workspace with an example.

## Before you begin

Role required: sn\_vlm.vendor\_admin

## About this task

Let's assume that a vendor manager wants to create a vendor KPI group for all of their software vendors. They want to associate KPIs with the vendor KPI group to measure the performance of all vendors in the vendor KPI group.

## Procedure

1.  Create a KPI group.

    1.  Navigate to **Vendor Management** &gt; **Configuration** &gt; **KPI Groups**
    2.  Click **New**
    3.  Create a vendor KPI group for software vendors.
        1.  In the **Name** field, enter `Software`.
        2.  In the **Description** field, enter a description such as, "This KPI Group is for software vendors."
        3.  In the **Type** menu, select **Vendors**.
        4.  Right-click the form header and click **Save**.
2.  Associate three KPIs with the vendor KPI group to evaluate the software vendors in that group.

    1.  In the KPIs related list, click **New**.
    2.  In the **KPI** field, click the search icon, select each of the indicators listed below and click **Submit** to add the KPIs to the group.
        -   Vendor Satisfaction with the Display Aggregate set to Average.
        -   Vendor Requested Items.
        -   Total Incidents Created with the Display Aggregate set to Sum.
3.  Add a weight value, which represents the relative order of importance, for each KPI that contributes towards the vendor score.

    -   For Vendor Satisfaction, set the weight value to `60`.
    -   For Average Stability Requested Items set the weight value to `40`.
    -   For Total Incidents Created, set the weight value to `0`, which indicates that it does not contribute to the vendor score calculation.
    The combined weight of all indicators added to the KPI group must be equal to 100. If the combined weight is above or below 100, then they are proportionately readjusted to 100.

4.  Associate thresholds to the KPI group.

    Define a range for the threshold values and assign a state for each range. For example, you can assign the lower threshold as `0` and the upper threshold as `60` and define the status as critical. .

    Each range has a color associated with it by default. When the vendor score is calculated for the vendors in the vendor KPI group, the score displays the highlighted color associated with the threshold range in the Vendor Management Workspace

    For example:

    1.  In the KPI Group Thresholds related list, click **New**.
        -   In the **Lower Threshold** field, enter `0`.
        -   In the **Upper Threshold** field, enter `60`.
        -   In the **Status** menu, select **Critical**.
        -   In the **Order** field, enter `200`.
    2.  Click **Submit**.
    Here is another example which shows that if the threshold values overlap between two different ranges, the one with a lower order number will be given preference.

    1.  In the KPI Group Thresholds related list, click **New**.
        -   In the **Lower Threshold** field, enter `50`.
        -   In the **Upper Threshold** field, enter `80`.
        -   In the **Status** menu, select **Moderate**.
        -   In the **Order** field, enter `300`.
    2.  Click **Submit**.
    Because the KPI group threshold value of `60` overlaps between the two sets of thresholds set above, the preference is given to the KPI group threshold that has the Critical status because it has a lower order number. Therefore, if the KPI threshold has a value of `60`, the highlighted color for that value in Vendor Management Workspace displays in the color set for the Critical status.

5.  Add thresholds for the individual KPIs.

    After you set the thresholds, you can view the KPI values in highlighted colors that correspond to each threshold range for the KPI in Vendor Management Workspace.

    1.  In the KPIs related list, click the preview icon next to the KPI for which you want to set the threshold and click **Open Record**.
    2.  In the KPI Thresholds related list, click **New**.
        -   In the **Lower Threshold** field, enter `60`.
        -   In the **Upper Threshold** field, enter `80`.
        -   In the **Status** menu, select **Moderate**.
        -   In the **Order** field, enter `300`.
    3.  Click **Submit**.
    The threshold values for the KPI are highlighted with the color based on the threshold range in Vendor Management Workspace.![Threshold color indicators](../image/thresholds-color.png)

6.  Add vendors to the KPI group.

    1.  In the Vendors related list, click **Edit**.
    2.  Add the vendors you want to add to the KPI group and click **Save**.

