---
title: Investigate boot time issues
description: Identify the root cause of boot time issues and get resolutions such as remedial actions, self-help instructions, and relevant knowledge articles to resolve the boot time issues.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Investigate boot time issues

Identify the root cause of boot time issues and get resolutions such as remedial actions, self-help instructions, and relevant knowledge articles to resolve the boot time issues.

## Before you begin

Role required: sn\_dex.user

Enable Now Assist for DEX to access AI-generated boot time diagnostics.

**Note:** The Now Assist AI capability for investigating boot time issues requires a minimum platform version of Zurich patch 7.

## About this task

Using Now Assist for Boot Time, analyze comprehensive boot performance metrics to help you investigate and resolve device startup issues efficiently. This AI-powered capability provides automated insights into boot performance and identifies potential problems affecting device boot times.

Boot time represents the time a Windows device takes to start and get fully usable after a power-on or restart. The metric is captured from Windows event logs and recorded during a full or real boot. The boot time data is used to identify devices with slow or degraded boot performance and act to improve the end-user experience.

You can view boot time metrics in two locations: the **Insights** page and the **Device** page.

**Tip:** To view boot time on the **Insights** page, go to **Digital Employee Experience** &gt; **Insights** and select **System Time**. Review the **Boot time** and **Last boot timestamp** columns.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to Service Operations Workspace and select **Devices** from the primary navigation pane.

2.  From the device list, select the device that you want to investigate.

3.  In the **Device health** section, select the **Boot time** tab.

    The **Key metrics** section displays the last data fetch timestamp and comprehensive boot time breakdown.

4.  In the **Now Assist for Boot Time Issues** banner, select **Investigate**.

    **Note:** The Now Assist banner appears only if the device has boot time metrics.

    Now Assist analyzes some or all of the boot time key metrics to generate the AI analysis. The key metrics section displays boot time performance data such as boot time, boot start and end timestamps, and other boot time related data.

5.  Review the AI-generated analysis, which includes:

    -   **Now Assist for Boot time issues**: Provides a root cause of boot time issues.
    -   **Key findings**: Provides a key summary of boot time durations.
    -   **Issue Classification**: Provides the primary issue, secondary issue, or other issue details.
6.  Select the **Show recommendations** button.

    **Note:** To view the **Show recommendations** button, you must have the `sn_dex.ai_user` and `itil` roles, and either the `sn_dex.engineer` or `sn_dex.service_desk_user` role.

    Remedial actions, self-help instructions, and related knowledge articles are displayed to help resolve boot-time issues.


## Result

Use the boot time data and AI-generated insights to resolve performance issues and improve the end-user experience.

