---
title: Activate a deactivated analysis data source
description: Reactivate a previously deactivated data source analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-agent-advisor-activate-data-source.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, AI Agent Advisor]
breadcrumb: [Setting up automation opportunity discovery, Configure, AI Agent Advisor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Activate a deactivated analysis data source

Reactivate a previously deactivated data source analysis.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

You must have access to an ACL-protected table to configure the analysis for it.

Role required: sn\_na\_center.nac\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **AI Admin Center \(Legacy\)**for the legacy AI Admin Center workspace.

    Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center** for the Lux UI experience.

    The home page opens.

2.  Select **Admin** \(\[Omitted image "icon-now-assist-center-nav-admin.png"\] Alt text: Admin icon in the side navigation bar.\) in the side navigation barin the legacy AI Admin Center workspace.

    Select **Settings** \(\[Omitted image "icon-aiac-lux-nav-settings.png"\] Alt text: Settings icon.\) in the side navigation panel in the Lux UI experience.

3.  Select **Automation opportunities** under **General** or**AI Agent Advisor** under **Settings**.

    The AI Agent Advisor setup page opens showing a separate card for each data source configuration.

    A deactivated data source analysis displays an Inactive status and an **Activate** button.

4.  Select **Activate** on the data source analysis you want to reactivate.

    The AI Agent Advisor setup page opens showing the configuration details.

5.  Review the completed fields and edit as needed.

6.  Select **Save and activate**.

7.  Select **Execute now** to run the analysis.


## Result

AI Agent Advisor runs the analysis according to the configured filters and schedule. After the analysis completes, automation opportunities appear on the AI Admin Center home page and on the Automation opportunities page.

## What to do next

View your automation opportunities on the home page. For more information, see [View your automation opportunities \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-view-automation-opportunities.md).

**Parent Topic:**[Setting up automation opportunity discovery in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-automation-discovery-setup.md)

**Related topics**  


[Set up a data source for analysis \(Next Experience UI\)]()

[Set up a data source for analysis \(Lux UI\)]()

[Edit an analysis data source]()

[Deactivate an analysis data source]()

[Delete an analysis data source]()

