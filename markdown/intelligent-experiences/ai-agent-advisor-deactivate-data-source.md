---
title: Deactivate an analysis data source
description: Deactivate a data source analysis that you no longer want to run for automation opportunity discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-agent-advisor-deactivate-data-source.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, AI Agent Advisor]
breadcrumb: [Setting up automation opportunity discovery, Configure, AI Agent Advisor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Deactivate an analysis data source

Deactivate a data source analysis that you no longer want to run for automation opportunity discovery.

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

    An active data source analysis displays an Active status and a **More options** button \(\[Omitted image "icon-now-assist-center-options.png"\] Alt text: More options icon.\).

4.  Select **More options** \(\[Omitted image "icon-now-assist-center-options.png"\] Alt text: More options icon.\) on the data source analysis you want to deactivate.

5.  Select **Deactivate**.


## Result

AI Agent Advisor ceases to run the scheduled analysis of the data source.

**Parent Topic:**[Setting up automation opportunity discovery in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-automation-discovery-setup.md)

**Related topics**  


[Set up a data source for analysis \(Next Experience UI\)]()

[Set up a data source for analysis \(Lux UI\)]()

[Edit an analysis data source]()

[Delete an analysis data source]()

[Activate a deactivated analysis data source]()

