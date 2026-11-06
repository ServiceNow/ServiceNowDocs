---
title: Investigate Zoom call issues
description: Investigate Zoom call performance with ServiceNow Otto for Zoom Call Issues to identify root causes and get resolutions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/investigate-and-resolve-zoom-call-issues.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use DEX AI capabilities, Digital End-User Experience, IT Operations Management]
---

# Investigate Zoom call issues

Investigate Zoom call performance with ServiceNow Otto for Zoom Call Issues to identify root causes and get resolutions.

## Before you begin

Role required: sn\_dex.user

-   DEX for Zoom must be configured. For more information, see [Configuring DEX for Zoom](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/configuring-DEX-for-Zoom.md).
-   Advanced monitoring must be enabled to capture Zoom call telemetry. For more information, see [Enable application monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/enable-app-monitor.md).
-   ServiceNow Otto for DEX must be enabled to access AI-generated Zoom call diagnostics.

**Note:** This AI skill requires a minimum platform version of Zurich patch 7.

## About this task

ServiceNow Otto for Zoom Call Issues processes Zoom telemetry data including audio, video, jitter, latency, and packet loss,along with device and application data to identify root causes. It then provides remedial actions, self-help instructions, and relevant knowledge articles to address the identified issues.

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    -   AMER \(Americas\): `itomcnc-prod-gateway-amer.sncapps.service-now.com:443`
    -   EMEA \(Europe\): `itomcnc-prod-gateway-emea.sncapps.service-now.com:443`
    -   APAC \(Asia Pacific\): `itomcnc-prod-gateway-apac.sncapps.service-now.com:443`
2.  In the primary navigation pane, select the Devices icon \[Omitted image "icon-devices.png"\].

3.  Select a device.

4.  Select **Zoom call quality** under **Advanced app metrics**.

5.  Select a **User**.

    **Note:**

    -   Only users with a valid email address can be selected.
    -   The users list includes assigned users and logged-in users \(those who logged in within the past 15 days\).
6.  Select start and end dates, then select **Go**.

    **Note:** The date range is limited to a maximum of 48 hours within the past 30 days.

    The Zoom calls appear in cards categorized as: **All calls**, **Bad calls**, **Poor calls**, **Fair calls**, and **Good calls**. By selecting one of these cards, you can see the filtered data in Summary and Call quality metrics.

    **Tip:** Apply **Additional filters** \(Device type, Version, Network type, and Location\) to narrow down the results and quickly find call details.

7.  In the **ServiceNow Otto for Zoom Call Issues** banner, select **Investigate**.

8.  Review the AI-generated analysis, which includes:

    -   **Primary Root Cause**: Identifies a specific issue impacting Zoom call performance.
    -   **Supporting Evidence**: Displays issue type, affected calls, and telemetry data such as average jitter, latency, packet loss, or audio/video loss.
    -   **Key Correlations Observed**: Indicates whether issues correlate with device, network, or application performance.
9.  Select the **Show recommendations** button.

    **Note:** To view the **Show recommendations** button, you must have the `sn_dex.ai_user` and `itil` roles, and either the `sn_dex.engineer` or `sn_dex.service_desk_user` role.

    .

    Remedial actions, self-help instructions, and related knowledge articles are displayed to help resolve Zoom call issues.

10. To view the detailed metrics for the Zoom calls made by users assigned to this device or logged in within the past 15 days, see [Monitor Zoom call quality using DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/monitor-zoom-call-quality-using-dex.md).


## Result

Use the Zoom calls data and AI-generated insights to resolve performance issues and improve the end-user experience.

