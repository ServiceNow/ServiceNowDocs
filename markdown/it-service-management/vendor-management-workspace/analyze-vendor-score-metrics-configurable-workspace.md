---
title: Analyze Vendor KPI Groups
description: After you set up vendor KPI Groups, you can analyze the metrics related to all of your vendors in one location. You can search all vendor-related information such as incidents, outages, improvement initiatives, and vendors and find associated records.
locale: en-US
release: xanadu
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing vendors using Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Analyze Vendor KPI Groups

After you set up vendor KPI Groups, you can analyze the metrics related to all of your vendors in one location. You can search all vendor-related information such as incidents, outages, improvement initiatives, and vendors and find associated records.

## Before you begin

Role required: sn\_vlm.vendor\_manager

## About this task

In workspace, you can sort the list by vendor types and analyze the performance of each vendor type in a single view. You can then drill down to each vendor and analyze additional data. You can also add attachments for the vendor profile in the **Vendor Details** section and download added attachments.

## Procedure

1.  Navigate to **All** &gt; **Vendor Management** &gt; **Workspace**.

2.  Analyze the vendor score.

    For information on how the vendor score is calculated, refer to [Calculating the vendor score](../reference/vendor-manager-workspace-default-wep.md).

    The color indicator that highlights the vendor score in the header shows you how the vendor is performing based on the set threshold.

    **Note:** The **VMW:Update Vendor Score** scheduled job is set to run daily. If you want to view updated score, you can run this scheduled job at any time.

3.  Click each indicator widget to view the breakdown for that metric.

    You can view:

    -   A single-score widget that displays the indicator metric.
    -   A time-series widget that shows the trend line for the selected KPI group and date range.
        -   When you select the end date as the day before the current date, you can view the actual and the forecast trend for the selected KPI.
        -   You can select a specific day in the time-series to analyze the vendor performance for the selected KPI on that day.
    -   A breakdown of related service offerings for the selected KPI group and date range.
    -   Threshold for each indicator highlighted to provide a visual indication for each service offering

        **Note:** You can analyze the key performance indicator \(KPI\) status such as Critical, Positive, or Warning for each vendor if your system administrator has enabled the display of the indicator status in Vendor Management Workspace. The indicator status to display KPI thresholds defined as critical is enabled by default.

    For the breakdown on the Vendor Satisfaction indicator, you can also view the Assessments Completed widget that displays the results of vendor satisfaction surveys.

4.  Add supporting documents to a vendor profile.

    1.  In the **Vendor Details** section, click the attachments icon .
    2.  Click **Browse** and select the desired file to attach to the profile.
    3.  Optionally, you can click the ellipses icon and download, replace, or remove the attachment.

**Parent Topic:**[Managing vendors using Vendor Management Workspace](../concept/using-vendor-management-workspace.md)

