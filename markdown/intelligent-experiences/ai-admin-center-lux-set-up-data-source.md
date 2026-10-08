---
title: Set up a data source for analysis \(Lux UI\)
description: Create and activate a scheduled analysis of your instance records to discover automation opportunities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-lux-set-up-data-source.html
release: australia
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 4
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, AI Agent Advisor]
breadcrumb: [Setting up automation opportunity discovery, Configure, AI Agent Advisor, AI Admin Center, Enable AI experiences]
---

# Set up a data source for analysis \(Lux UI\)

Create and activate a scheduled analysis of your instance records to discover automation opportunities.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

You must have access to an ACL-protected table to configure the analysis for it.

For AI Agent Advisor to run a successful analysis, the data source must contain a minimum of 500 records.

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to configure the data source, filters, schedule, and cost profile that AI Agent Advisor uses to identify the automation opportunities and provide savings estimates for them.

In the event an error occurs when performing these steps, see the troubleshooting steps described in KB article [KB2931703](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2931703) on Now Support.

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

    The home page opens.

    The **Automation opportunities** section displays only a **Review configurations** button if no opportunities are identified or if opportunity discovery isn't yet set up.

    \[Omitted image "ai-admin-center-lux-advisor-home-none.png"\] Alt text: Automation opportunities section of the home page with a button to review configurations.

    The **Automation opportunities** section displays the top automation opportunities in separate cards if discovery is set up and opportunities are identified. The section also displays an **Edit advisor settings** link to edit the discovery data sources.

    \[Omitted image "ai-admin-center-lux-home-opportunities.png"\] Alt text: Automation opportunities section of the home page showing the top opportunities in separate cards.

2.  Select **Review configurations** or **Edit advisor settings** to open the Automation opportunities settings page.

    You can also select **Settings** \(\[Omitted image "icon-aiac-lux-nav-settings.png"\] Alt text: Settings icon.\) in the side navigation panel and select **Automation opportunities** under **General** on the Settings page.

    The Automation opportunities settings page opens. If there are any data sources set up, a separate card displays for each data source.

    \[Omitted image "ai-admin-center-lux-advisor-setup-list.png"\] Alt text: Automation opportunities settings page with a card for each data source.

3.  Select **Create new**.

    The AI Agent Advisor setup page opens.

    \[Omitted image "ai-admin-center-lux-advisor-setup.png"\] Alt text: Setup page with fields to configure the data source analysis.

4.  Complete the **General information** section.

    1.  Enter a name for the analysis configuration in the **Add name** field.

    2.  Enter a description in the **Short description** field.

5.  Choose the data source in the **Select table** section.

    1.  If permission is required for AI Agent Advisor to access the table, select **Add role**.

        Then add the required role to the sn\_agent\_miner.app\_admin role and return to the Add new data set page.

        For more information, see [Add a role to an existing role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddARoleToAnExistingRole.md).

    2.  Select a table from the **Table name** menu.

    3.  Select one or more fields from the **Fields** menu.

6.  Select the frequency of the analysis schedule in the **Scheduled to run** section.

    -   Select the 30, 60, or 90 day option.
    -   Toggle the **On-Off** option to `Off` to stop AI Agent Advisor from running the recurring analysis and identifying opportunities.

        If the scheduled run is turned off, new opportunities for the data source won't appear until a new run is scheduled or triggered manually.

7.  Apply filters to refine the scope of the analysis.

    1.  Use conditions to select certain properties as a filter.

        For more information on how conditions work, see [OR conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_UsingORConditions.md).

        **Note:** A filter for the **Created** field is required.

    2.  Select **Add group** to add more conditions.

8.  Create a cost profile to calculate the estimated time and cost savings from using the automation.

    1.  Enter the hourly labor cost.

    2.  Enter the active handling time rate.

        The percentage of a record's total open time that represents actual hands-on effort by a human agent.

9.  Select **Save and activate**.


## Result

AI Agent Advisor runs the analysis according to the configured filters and schedule. After the analysis completes, automation opportunities appear on the AI Admin Center home page and on the Automation opportunities page.

## What to do next

View your automation opportunities. For more information, see [View your automation opportunities \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-view-automation-opportunities.md).

**Parent Topic:**[Setting up automation opportunity discovery in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-automation-discovery-setup.md)

**Related topics**  


[Set up a data source for analysis \(Next Experience UI\)]()

[Edit an analysis data source]()

[Deactivate an analysis data source]()

[Delete an analysis data source]()

[Activate a deactivated analysis data source]()

