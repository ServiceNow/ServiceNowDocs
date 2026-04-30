---
title: Investigate Zoom call issues
description: Investigate Zoom call performance with Now Assist to identify root cause of issues, review supporting evidence, and get the resolutions such as remedial actions, self-help instructions, and relevant knowledge articles to resolve the Zoom call issues.
locale: en-US
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-01-30"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Investigate Zoom call issues

Investigate Zoom call performance with Now Assist to identify root cause of issues, review supporting evidence, and get the resolutions such as remedial actions, self-help instructions, and relevant knowledge articles to resolve the Zoom call issues.

## Before you begin

Role required: sn\_dex.user

-   Ensure DEX for Zoom is configured. For more information, see [Configuring DEX for Zoom](../Zoom-calls-monitoring/configuring-DEX-for-Zoom.md).
-   Ensure that advanced monitoring is enabled to capture Zoom call telemetry. For more information, see [Enable application monitoring](enable-app-monitor.md).
-   Enable Now Assist for DEX to access AI-generated Zoom call diagnostics.

**Note:** The Now Assist AI capability for investigating Zoom call quality issues requires a minimum platform version of Zurich patch 7.

## About this task

The Now Assist for Zoom Call Issues analyzes Zoom telemetry, including audio, video, jitter, latency, and packet loss, or other issues along with device and application data to determine the root cause.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select the Devices icon ![](../image/icon-devices.png).

3.  Select a device.

4.  Select **Zoom call quality** under **Advanced app metrics**.

5.  Select a **User**.

    **Note:**

    -   Only users with a valid email address can be selected.
    -   The users list includes assigned users and logged-in users \(those who logged in within the past 15 days\).
6.  Select start and end dates, then select **Go**.

    **Note:** The date range is limited to a maximum of 48 hours within the past 30 days.

    The zoom calls appear in cards categorized as: **All calls**, **Bad calls**, **Poor calls**, **Fair calls**, and **Good calls**. By selecting one of these cards, you can see the filtered data in Summary and Call quality metrics. You can also use Additional filters listed below the cards.

    **Tip:** Apply **Additional filters** \(Device type, Version, Network type, and Location\) to narrow down the results and quickly find call details.

7.  In the **Now Assist for Zoom Call Issues** banner, select **Investigate**.

8.  Review the AI-generated analysis, which includes:

    -   **Primary Root Cause**: Identifies a specific issue impacting Zoom call performance.
    -   **Supporting Evidence**: Displays issue type, affected calls, and telemetry data such as average jitter, latency, packet loss, or audio/video loss.
    -   **Key Correlations Observed**: Indicates whether issues correlate with device, network, or application performance.
9.  Select the **Show recommendations** button.

    **Note:** To view the **Show recommendations** button, you must have the `sn_dex.ai_user` and `itil` roles, and either the `sn_dex.engineer` or `sn_dex.service_desk_user` role.

    .

    Remedial actions, self-help instructions, and related knowledge articles are displayed to help resolve Zoom call issues.

10. To view the detailed metrics for the Zoom calls made by users assigned to this device or logged in within the past 15 days, see [Monitor Zoom call quality using DEX](../Zoom-calls-monitoring/monitor-zoom-call-quality-using-dex.md).


## Result

Use the Zoom calls data and AI-generated insights to resolve performance issues and improve the end-user experience.

