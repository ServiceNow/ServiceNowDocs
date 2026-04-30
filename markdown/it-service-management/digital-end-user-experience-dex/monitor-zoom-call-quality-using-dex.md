---
title: Monitor Zoom call quality using DEX
description: View detailed metrics for the Zoom calls made by users assigned to this device or logged in within the past 15 days.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-10-29"
reading_time_minutes: 2
breadcrumb: [Monitor, Digital End-User Experience, IT Service Management]
---

# Monitor Zoom call quality using DEX

View detailed metrics for the Zoom calls made by users assigned to this device or logged in within the past 15 days.

## Before you begin

Role required: admin

-   Set up DEX for Zoom. For more information, see [Configuring DEX for Zoom](configuring-DEX-for-Zoom.md).
-   Configure advanced monitoring to monitor Zoom calls quality with DEX. For more details, see [Enable application monitoring](../task/enable-app-monitor.md).

## About this task

The detailed Zoom call metrics include call quality, network performance, and call details to help you troubleshoot issues quickly and improve end-user experience visibility.

-   Each time a user disconnects and rejoins a call, the subsequent joining is counted as a new call.
-   Zoom monitoring doesn’t include webinars or breakout rooms.
-   All the metrics are the aggregated data of all the calls.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select the Devices icon \(![Devices icon](../image/icon-devices.png)\).

3.  Select a device.

4.  Select **Zoom call quality** under **Advanced app metrics**.

5.  Select a **User**.

    **Note:**

    -   Only users with a valid email address can be selected.
    -   The users list includes assigned users and logged-in users \(those who logged in within the past 15 days\).
6.  Select start and end dates, then select **Go**.

    **Note:** The date range is limited to a maximum of 48 hours within the past 30 days.

    The zoom calls appear in cards categorized as: **All calls**, **Bad calls**, **Poor calls**, **Fair calls**, and **Good calls**. By selecting one of these cards, you can see the filtered data in Summary and Call quality metrics. You can also use Additional filters listed below the cards.

    **Tip:** Apply **Additional filters** \(Device type, Version, Network type, Location\) to narrow results and quickly find call details.

7.  To view AI-powered Zoom call quality issues investigations and recommendations, see [Investigate Zoom call issues](../task/investigate-and-resolve-zoom-call-issues.md)

8.  Select the **Summary** tab.

    The following call details appear:

    -   **Call quality**
    -   **Call issues**
    -   **Calls over time**
    -   **Jitter**
    -   **Latency**
    -   **Packet loss**

        **Note:**

        -   For the Summary metrics description, see [Metrics monitored by DEX for Zoom](metrics-monitored-by-dex-for-zoom.md).
        -   Clicking anywhere on the **Call quality** or **Call issues** pie chart opens the **Details** page and displays the calls associated with the selected metric. For descriptions of the fields on the Details page, see [Zoom call quality metrics on the Details page](../reference/call-quality-metrics-monitored-by-dex-for-zoom.md).
9.  Select **Call quality metrics** to get call details.

    The following call quality breakdown appears:

    -   **Audio quality**
    -   **Video quality**
    -   **Screenshare quality**
    -   **Version**
    -   **Operating System**
    -   **Location**
    -   **Connection Type**
    -   **Device Type**
    -   **Camera**
    -   **Screenshare**
    **Note:**

    -   For Call quality metrics description, see [Metrics monitored by DEX for Zoom](metrics-monitored-by-dex-for-zoom.md).
    -   Clicking anywhere on the bar graph or pie chart for any call quality metric opens the **Details** page and displays the calls associated with the selected metric. For field descriptions on **Details** page, see [Zoom call quality metrics on the Details page](../reference/call-quality-metrics-monitored-by-dex-for-zoom.md).

