---
title: Edit an analysis data source
description: Edit a scheduled analysis of your instance records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-agent-advisor-edit-data-source.html
release: australia
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, AI Agent Advisor]
breadcrumb: [Setting up automation opportunity discovery, Configure, AI Admin Center, Enable AI experiences]
---

# Edit an analysis data source

Edit a scheduled analysis of your instance records.

## Before you begin

You must have access to an ACL-protected table to configure the analysis for it.

For AI Agent Advisor to run a successful analysis, the data source must contain a minimum of 500 records.

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to change the configuration of the data source, filters, schedule, and cost profile that AI Agent Advisor uses to identify the automation opportunities.

You can only edit an active analysis data source. To edit a deactivated analysis data source, you must first reactivate it. For more information, see [Activate a deactivated analysis data source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-advisor-activate-data-source.md).

In the event an error occurs when performing these steps, see the troubleshooting steps described in KB article [KB2931703](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2931703) on Now Support.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** or **Workspaces** &gt; **AI Admin Center**.

    The home page opens.

2.  Select **Admin** \(\[Omitted image "icon-now-assist-center-nav-admin.png"\] Alt text: Admin icon in the side navigation bar.\) in the side navigation bar.

    The AI Admin Hub page opens.

3.  Select **AI Agent Advisor** under **Settings**.

    The AI Agent Advisor setup page opens showing a separate card for each data source configuration.

    \[Omitted image "ai-agent-advisor-data-sources.png"\] Alt text: Separate cards for each data source on the AI Agent Advisor setup page.

4.  Select **More options** \(\[Omitted image "icon-now-assist-center-options.png"\] Alt text: More options icon.\) on the data source analysis you want to edit.

5.  Select **Edit**.

    The AI Agent Advisor setup page opens showing the configuration details.

6.  Review the completed fields and edit as needed.

7.  Select **Save**.

8.  Select **Execute now** to run the analysis.


## Result

AI Agent Advisor runs the analysis according to the configured filters and schedule. After the analysis completes, automation opportunities appear on the AI Admin Center home page and on the Automation opportunities page.

## What to do next

View your automation opportunities on the home page. For more information, see [View your automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-view-automation-opportunities.md).

**Parent Topic:**[Setting up automation opportunity discovery in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-center-automation-discovery-setup.md)

**Related topics**  


[Set up a data source for analysis]()

[Deactivate an analysis data source]()

[Activate a deactivated analysis data source]()

