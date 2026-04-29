---
title: Monitor Microsoft Teams call quality
description: Enable advanced monitoring of Microsoft Teams call quality with DEX for Microsoft 365. Track and analyze call performance for a specific user.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor, Digital End-User Experience, IT Service Management]
---

# Monitor Microsoft Teams call quality

Enable advanced monitoring of Microsoft Teams call quality with DEX for Microsoft 365. Track and analyze call performance for a specific user.

## Before you begin

Role required: admin

-   Configure advanced monitoring for Microsoft Teams. For more details, see [Enable application monitoring](../../digital-end-user-experience/task/enable-app-monitor.md).
-   Set up DEX for Microsoft 365 application. For more information, see [Configuring DEX for Microsoft 365](../concept/configuring-dex-for-microsoft-365.md).

## About this task

View detailed metrics for a user's Microsoft Teams calls, including call quality, network metrics, and session data for a particular user.

**Note:** All data displayed on this page are based on information received from Microsoft.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select the Applications icon \(![The Applications icon.](../../digital-end-user-experience/image/icon-applications.png)\).

3.  Select **Teams**.

4.  Select **Call quality** under **Application metrics**.

5.  Select a **User**.

    **Note:** Only users with a valid email address can be selected.

6.  Select a **Start date/time** and **End date/time**, then select **Go**.

    **Note:** The date range is limited to a maximum of 48 hours within the past 30 days.

7.  Select **Summary**.

    The following details appear:

    -   **Call Quality**: A pie chart shows the percentage of calls with Good quality, Poor quality, or Unclassified.
    -   **Call Types**: A pie chart shows the percentage of call types: audio, video, or other.
    -   **Calls over time**: A line graph shows the number of Good, Poor, or Unclassified quality calls over the selected time period.
    -   **Network Experience**: A line graph shows average packet loss and average jitter over the selected period.
    -   **Metrics**: The following metrics appear in a table.

        |Metric|Description|
        |------|-----------|
        |Average jitter|Measure of the variation in packet delay over a network.|
        |Average packet loss rate|Shows how often data disappears on its way. Lower loss means better sound, video, and performance.|
        |Average round-trip time|Average time it takes for a data packet to travel from the source to the destination and back again. The lower the round-trip time, the faster the network.|
        |Average audio degradation|Average decline in audio quality experienced during a call or voice transmission, usually due to network issues like packet loss, jitter, latency, or codec problems.|
        |Average video frame loss percentage|Average percentage of video frames lost as displayed to the user.|
        |Average bandwidth estimate|Average estimated bandwidth available between two endpoints in bits per second.|

8.  Select **Call quality metrics** to get session details.

    A number of total calls, good calls, and poor calls appears with a timeline chart of calls. The following session details appear:

    -   **Session Quality Breakdown**: A pie chart shows the percentage of Microsoft Teams sessions with Good, Poor, or Unclassified quality.
    -   **Connection Type**: A bar chart shows calls from various connection types.
    -   **Media Type**: A bar chart shows audio and video calls.
    -   **Video codecs used**: A bar chart based on the video codecs used.
    -   **Audio codecs used**: A bar chart based on the audio codecs used.
    -   **Operating system**: A bar chart based on the user's operating system.

