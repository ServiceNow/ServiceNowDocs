---
title: Configure Automation Discovery
description: Automation Discovery helps you analyze your records and identity opportunities for automation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/config-finding-def-auto-disc.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration with Automation Discovery, Integrating Process Mining, Activating Process Mining, Process Mining, Platform Analytics]
---

# Configure Automation Discovery

Automation Discovery helps you analyze your records and identity opportunities for automation.

## Before you begin

You must install the Automation Discovery application \(sn\_auto\_discovery\) before configuring. For more information, see [Install Automation Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/install-automation-discovery.md).

Role required: administrator

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Process Configuration**.

2.  Select the Incident table \[incident\].

3.  Use the **KPI Dashboard** field to select a KPI dashboard to associate with this process configuration.

4.  Navigate to the **Automation Discovery** tab.

5.  Select **Enable automation discovery** and **Auto-run with model generation**, and complete the required fields.

    \[Omitted image "auto-disc-enabled.png"\] Alt text: auto discovery fully enabled

    Your project runs automation discovery with model generation automatically when both options are selected.

6.  Select **Update**.

7.  Navigate to **All** &gt; **Process Mining** &gt; **Process Mining Workspace**.

    The Process Mining Workspace page opens.

8.  Open the project, and select **Automation Opportunities**

    Your project's results are broken up into two categories: **Automation Opportunities** and **Not Categorized**.\[Omitted image "auto-disc-process-map.png"\] Alt text: auto discovery process map

9.  Select a record for additional information.

    Point to **Open process map** to trigger additional mining.

    If you decide not to select **Enable automation discovery** or **Auto-run with model generation**, your Automation Opportunities don’t display. From **Analyst workbench**, select **Generate report** to create a report.

    \[Omitted image "no-auto-disc-enabled.png"\] Alt text: no auto discovery enabled

    Fill out the required fields to create your report.


**Parent Topic:**[Integration with Automation Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/auto-disc.md)

