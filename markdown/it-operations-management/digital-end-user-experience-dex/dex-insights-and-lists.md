---
title: Setting up DEX insights and lists
description: DEX provides visibility and insight into the state and performance of user applications and devices. You can view system compliance, manage files, and set up Windows registry keys.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/dex-insights-and-lists.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [dex insights, insights and lists, system compliance, file management, device performance visibility, Windows registry keys]
breadcrumb: [Configure, Digital End-User Experience, IT Operations Management]
---

# Setting up DEX insights and lists

DEX provides visibility and insight into the state and performance of user applications and devices. You can view system compliance, manage files, and set up Windows registry keys.

DEX collects and displays application and device data in your environment. The insights and lists features give you a structured view of that data, so you can monitor device health, verify configuration compliance, and manage endpoint resources.

The following capabilities are available in the insights and lists area of DEX:

-   **System compliance**: view the compliance status of devices against defined policies and check definitions. Identify devices that do not meet configuration requirements.
-   **File management**: view and manage files on monitored devices. Use file lists to locate, review, and act on files across your device fleet.
-   **Windows registry keys**: set up and monitor Windows registry key values on managed devices. Use registry key lists to verify configuration settings and detect unauthorized changes.

To access insights and lists, the DEX plugin \(sn\_dex\) must be installed and the DEX Desktop Assistant \[sn\_dex\_desktop\] application must be deployed on the devices you want to monitor. Role required: sn\_dex.user or sn\_dex.admin.

To access the insights and lists features, navigate to DEX and select **Insights** in the primary navigation pane. The available lists appear based on your role and the data collected by the Agent Client Collector \(ACC\) on each device.

**Note:** The historical data displayed in insights and lists covers the past 7 days. The latest data reflects the most recent information collected by the ACC.

