---
title: Metrics monitored by DEX for Zoom
description: View the zoom metrics that appear in Summary and call quality metrics tabs.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Metrics monitored by DEX for Zoom

View the zoom metrics that appear in Summary and call quality metrics tabs.

## Summary tab metrics

<table id="table_ejc_jxl_lhc"><thead><tr><th>

Metric name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Call quality**

</td><td>

The pie chart displays the proportion of calls categorized as Good, Fair, Bad, Poor, or Unclassified, based on a quality scoring formula using network metrics. Call quality is determined by evaluating both incoming and outgoing media channels \(audio, video, and screen share\). Each channel is assessed independently, and the worst score among them is used as the overall call quality.

 The calculation uses the Mean Opinion Score \(MOS\), which is using the key network metrics, including latency, jitter, and packet loss. MOS provides a numerical score that maps to a quality rating based on standard ranges:

-   **Good \(MOS ≥ 4.0 to ≤ 5.0\)**: Clear audio and video reception.
-   **Fair \(MOS ≥ 3.0 to &lt; 4.0\)**: Mostly clear reception with occasional drops in quality.
-   **Poor \(MOS ≥ 2.0 to &lt; 3.0\)**: Loss of video frames, reduced frame rate, and periodic audio issues.
-   **Bad \(MOS ≥ 1.0 to &lt; 2.0\)**: Consistent loss of audio and video, with low resolution and frame rate.

When you select a category in the pie chart, the **Details** page opens and displays call quality information filtered by the selected category. For example, if you select Bad meetings, the page shows details for Bad meetings only.

**Note:** For field descriptions on the Details page, see [Zoom call quality metrics on the Details page](../reference/call-quality-metrics-monitored-by-dex-for-zoom.md).

</td></tr><tr><td>

**Call issues**

</td><td>

The pie chart shows the distribution of detected issues, labeled as Unstable video, Call reconnection problems, Poor screenshare quality, Unstable audio quality, and High CPU usage.When you select an issue in the pie chart, the **Details** page opens which displays calls affected by that issue. For example, if you select **High CPU Usage**, the page lists meetings where high CPU usage was detected.

**Note:** For field descriptions on the **Details** page, see [Zoom call quality metrics on the Details page](../reference/call-quality-metrics-monitored-by-dex-for-zoom.md).

</td></tr><tr><td>

**Calls over time**

</td><td>

The bar chart displays the number of calls categorized as Good, Fair, Bad, or Poor within the selected date range.

</td></tr><tr><td>

**Jitter**

</td><td>

The line graph represents the variation in network packet delay during calls; higher jitter can impact audio or video quality.

</td></tr><tr><td>

**Latency**

</td><td>

The line graph indicates the time delay between sending and receiving audio or video data in a call. Lower latency means more responsive communication.

</td></tr><tr><td>

**Packet loss**

</td><td>

The line graph shows the percentage of data packets lost during transmission; lower packet loss results in better call quality and reliability.

</td></tr></tbody>
</table>**Note:** If no data is available for any channel, the call is marked as **Unclassified**.

## Call quality metrics

The following call quality breakdown appears:

<table id="table_d15_c1m_lhc"><thead><tr><th>

Metric name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Audio quality**

</td><td>

The pie chart displays the proportion of calls categorized as Good, Fair, Bad, Poor, or Unclassified \(calls without audio on\) based on audio quality metrics. When you select a category in the pie chart, the **Details** page opens and displays calls with the selected video quality. For example, if you select Bad, the page lists the calls with bad audio quality.

</td></tr><tr><td>

**Video quality**

</td><td>

The pie chart displays the proportion of calls categorized as Good, Fair, Bad, Poor, or Unclassified based on video quality metrics. When you select a category in the pie chart, the **Details** page opens and displays calls with the selected video quality. For example, if you select Bad, the page lists calls with Bad video quality.

</td></tr><tr><td>

**Screenshare quality**

</td><td>

The pie chart displays the proportion of calls categorized as Good, Fair, Bad, Poor, or Unclassified based on the screen share quality metrics. When you select a category in the pie chart, the **Details** page opens and displays calls with the selected screen share quality. For example, if you select Fair, the page lists calls with Fair screen share quality.

</td></tr><tr><td>

**Version**

</td><td>

The bar chart displays the number of calls categorized as Good, Fair, Bad, or Poor based on overall call quality for each application version within the selected date range. When you select a bar, the **Details** page opens and displays calls of the chosen quality for that version. For example, if you select Bad under version v12311, the page lists calls with Bad quality on that version.

</td></tr><tr><td>

**Operating System**

</td><td>

The bar chart displays the number of calls categorized as Good, Fair, Bad, or Poor based on overall quality, grouped by operating system, such as Windows, macOS, and Android. It shows how call quality varies across platforms. When you select a bar, the **Details** page opens and displays calls of the chosen quality for that operating system. For example, if you select Bad under Windows, the page lists calls with Bad quality on Windows.

</td></tr><tr><td>

**Location**

</td><td>

The bar chart displays the number of calls categorized as Good, Fair, Bad, or Poor based on overall call quality for each location within the selected date range. When you select a bar, the **Details** page opens and displays calls of the chosen quality for that location. For example, if you select Bad under Location 2, the page lists details for Bad calls from Location 2.

</td></tr><tr><td>

**Connection Type**

</td><td>

The bar chart displays the number of calls categorized as Good, Fair, Bad, or Poor based on overall call quality for each connection type \(Wi-Fi, Ethernet, Unknown\) within the selected date range. When you select a bar, the **Details** page opens and displays calls of the chosen quality for that connection type. For example, if you select Fair under Wi-Fi, the page lists details for Fair calls using Wi-Fi.

</td></tr><tr><td>

**Device Type**

</td><td>

The bar chart displays the number of calls categorized as Good, Fair, Bad, or Poor based on overall call quality for each device type within the selected date range.When you select a bar, the **Details** page opens and displays calls of the chosen quality for that device type. For example, if you select Poor under Device type 3, the page lists details for Poor calls on Device type 3.

</td></tr><tr><td>

**Camera**

</td><td>

The bar chart displays the number of calls categorized as Good, Fair, Bad, or Poor based on overall call quality, grouped by whether the camera was on or off during the call.When you select a bar, the **Details** page opens and displays calls of the chosen quality for that camera state. For example, if you select Bad under Camera on, the page lists details for Bad calls where the camera was on.

</td></tr><tr><td>

**Screenshare**

</td><td>

The bar chart displays the number of calls categorized as Good, Fair, Bad, Poor, or Unclassified based on overall call quality, grouped by whether the screen share was on or off.When you select a bar, the **Details** page opens and displays of the chosen quality for that screen share state. For example, if you select Poor under Screenshare on, the page lists details for Poor calls where screen sharing was active.

</td></tr></tbody>
</table>**Note:** For field descriptions on **Details** page, see [Zoom call quality metrics on the Details page](../reference/call-quality-metrics-monitored-by-dex-for-zoom.md).

**Parent Topic:**[DEX Application and Device Health reference](../reference/dex-console-reference.md)

