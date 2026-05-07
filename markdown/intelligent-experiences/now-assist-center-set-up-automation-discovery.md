---
title: Set up automation discovery for AI Agent Advisor
description: Configure the data sources, filters, and schedule that AI Agent Advisor uses to analyze your instance and identify automation opportunities.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-13"
reading_time_minutes: 2
keywords: [AI Agent Advisor, Now Assist, Now Assist Center, Gen AI, Generative AI]
breadcrumb: [Configure, AI Agent Advisor, Enable AI experiences]
---

# Set up automation discovery for AI Agent Advisor

Configure the data sources, filters, and schedule that AI Agent Advisor uses to analyze your instance and identify automation opportunities.

## Before you begin

For AI Agent Advisor to run a successful analysis, the data source must contain a minimum of 500 records.

Role required: sn\_na\_center.nac\_admin

## About this task

AI Agent Advisor runs a scheduled analysis of your instance records to discover automation opportunities. Follow these steps to specify which records to include, apply filters to focus the analysis, and set the frequency and timing of the analysis.

In the event an error occurs when performing these steps, see the troubleshooting steps described in KB article [KB2931703](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2931703) on Now Support.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Center** or **Workspaces** &gt; **Now Assist Center**.

2.  Select **Change advisor settings** in the AI Agent Advisor section of the home page.

    You can also select **Admin** \(![Admin icon in the side navigation bar.](../image/icon-now-assist-center-nav-admin.png)\) in the side navigation bar and select **AI Agent Advisor** under Settings on the Admin page.

    The AI Agent Advisor Setup tab opens showing a card for each data source. Enable the data sources you want AI Agent Advisor to analyze.

    **Incident** and **Case** data sources are enabled by default.

    ![Automation Opportunities Setup page showing a card for each data source.](../image/now-assist-center-agent-advisor-opportunity-setup.png "Data sources on the Automation Opportunities Setup page")

3.  Select the **Edit** button \(![Edit icon.](../image/icon-now-assist-center-edit.png)\) in the card you want to configure.

    Choose any of the following data sources:

<table id="table_upd_wbh_v3c"><thead><tr><th>

Data source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Incident

</td><td>

Analyzes incident records to identify recurring IT issues and automation patterns.

</td></tr><tr><td>

Case

</td><td>

Analyzes case records to identify common customer service patterns.

</td></tr></tbody>
</table>4.  Apply filters to refine the scope of the analysis.

    1.  Select the time period for the data.

    2.  Use conditions to select certain properties as a filter.

        For more information on how conditions work, see [OR conditions](https://www.servicenow.com/docs/access?context=c_UsingORConditions&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    3.  Select **Apply filter**.

5.  Configure the analysis schedule.

    1.  Select the frequency.

    2.  Select the start time for the analysis to run.

    3.  Select the time zone.

6.  Calculate the estimated time and cost savings from using the automation.

    1.  Enter the hourly labor cost.

    2.  Estimated AI resolution rate.

    3.  Percentage of active work time an AI agent is expected to handle or eliminate per record.

7.  Select **Save**.


## Result

AI Agent Advisor runs the analysis according to the configured filters and schedule. After the analysis completes, automation opportunities appear on the Now Assist Center home page and on the Automation opportunities page.

## What to do next

View your automation opportunities on the home page. For more information, see [View your automation opportunities](now-assist-center-view-automation-opportunities.md).

**Parent Topic:**[Configuring AI Agent Advisor](../concept/configuring-ai-agent-advisor.md)

**Related topics**  


[Confirm installation of AI Agent Advisor](set-up-ai-agent-advisor.md)

