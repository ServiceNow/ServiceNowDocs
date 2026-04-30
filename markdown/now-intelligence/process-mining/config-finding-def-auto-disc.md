---
title: Configure automation discovery
description: Automation discovery helps you analyze your records and identity opportunities for automation.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integration with Automation discovery, Integrating Process Mining, Activating Process Mining, Process Mining, Platform Analytics]
---

# Configure automation discovery

Automation discovery helps you analyze your records and identity opportunities for automation.

## Before you begin

You must install the Automation Discovery application \(sn\_auto\_discovery\) before configuring. For more information, see [Install Automation Discovery](../../automation-discovery/task/install-automation-discovery.md).

Role required: administrator

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Configuration**.

2.  Select the Incident table \[incident\].

3.  Use the **KPI Dashboard** field to select a KPI dashboard to associate with this process configuration.

4.  Navigate to the **Automation Discovery** tab.

5.  Select **Enable automation discovery** and **Auto-run with model generation**, and complete the required fields.

    ![auto discovery fully enabled](../image/auto-disc-enabled.png)

    Your project runs automation discovery with model generation automatically when both options are selected.

6.  Select **Update**.

7.  Navigate to **All** &gt; **Process Mining** &gt; **Process Mining Workspace**.

    The Process Mining Workspace page opens.

8.  Open the project, and select **Automation Opportunities**

    Your project's results are broken up into two categories: **Automation Opportunities** and **Not Categorized**.![auto discovery process map](../image/auto-disc-process-map.png)

9.  Select a record for additional information.

    Point to **Open process map** to trigger additional mining.

    If you decide not to select **Enable automation discovery** or **Auto-run with model generation**, your Automation Opportunities don’t display. From the **Analyst Workbench**, select **Generate report** to create a report.

    ![no auto discovery enabled](../image/no-auto-disc-enabled.png)

    Fill out the required fields to create your report.


**Parent Topic:**[Integration with Automation discovery](../concept/auto-disc.md)

