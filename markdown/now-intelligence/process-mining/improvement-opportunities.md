---
title: Configure improvement opportunities
description: Create a library of inefficiencies to identify the improvement opportunities for your project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/improvement-opportunities.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [With Process Configuration Builder, Creating process configuration, Using Process Mining, Process Mining, Platform Analytics]
---

# Configure improvement opportunities

Create a library of inefficiencies to identify the improvement opportunities for your project.

## Before you begin

Role required: sn\_process\_optimization\_power\_user or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the side of the page, select the Process configurations icon \(\[Omitted image "icon-process-config.png"\] Alt text: Process configuration builder\).

3.  Open a table from the **Configurations** list.

    The **Process details** page is displayed. Select **Improvement opportunities** from the side panel.

    If you’re proceeding from the **Impact metrics** page, then you come to this page. For more information, see [Configure impact metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/impact-metrics.md).

    The **Improvement opportunities** page displays:

    -   Automated improvement opportunities: The improvement opportunities are displayed based on the default patterns that are already available for selection.
    -   Rule-based improvement opportunities: These improvement opportunities consist of one or more rule chains executed in a sequence. The records that match the logic of these specifications are classified as a match for the improvement opportunities.
    Improvement opportunity definitions highlight potential areas for process optimization based on a set of patterns.

4.  Select from the list of the recommended automated improvement opportunities.

    The recommendations are displayed based on your inputs in the Process details page. To understand how you set the process perspectives, see [Configure process details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/process-details.md).

    \[Omitted image "process-config-imp-opp.png"\] Alt text: Recommended improvement opportunities

5.  Select the improvement opportunities that you want to include in your process configuration, and select **Add Selected**.

    \[Omitted image "improve-opp-pro-config.png"\] Alt text: Improvement opportunities in process configuration

6.  Select **Add new** to create an improvement.

    The improvement opportunity definition page is displayed. For more information, see [Set rule-based improvement opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/rule-based-builder.md) and [Automated improvement opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/automated-findings.md).

    Select the **Get recommendations** button to get recommendations for the automated improvement opportunities based on the configuration you have set in the Process perspectives section of the Process details page.

7.  Select **Finish**.

    The process configuration is complete.


**Parent Topic:**[Create process configuration using Process Configuration Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/process-config-builder.md)

