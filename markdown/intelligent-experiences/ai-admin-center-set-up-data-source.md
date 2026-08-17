---
title: Set up a data source for analysis
description: Create and activate a scheduled analysis of your instance records to discover automation opportunities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-admin-center-set-up-data-source.html
release: zurich
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, AI Agent Advisor]
breadcrumb: [Setting up automation opportunity discovery, Configure, AI Admin Center, Enable AI experiences]
---

# Set up a data source for analysis

Create and activate a scheduled analysis of your instance records to discover automation opportunities.

## Before you begin

You must have access to an ACL-protected table to run the analysis for it.

For AI Agent Advisor to configure a successful analysis, the data source must contain a minimum of 500 records.

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to configure the data source, filters, schedule, and cost profile that AI Agent Advisor uses to identify the automation opportunities and provide savings estimates for them.

In the event an error occurs when performing these steps, see the troubleshooting steps described in KB article [KB2931703](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2931703) on Now Support.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** or **Workspaces** &gt; **AI Admin Center**.

    The home page opens.

    The automation opportunities section displays only a **Review configurations** button If no opportunities are identified or if opportunity discovery is not yet set up.

    \[Omitted image "ai-admin-center-home-automation-opportunities-empty.png"\] Alt text: Empty Automation opportunities section of the home page showing a button to review configurations.

    The automation opportunities section displays the top automation opportunities in separate cards if discovery is set up and opportunities are identified. The section also displays a **Change advisor settings** link to edit the discovery data sources.

    \[Omitted image "now-assist-center-home-automation-opportunities-2.png"\] Alt text: Automation opportunities shown in AI Admin Center.

2.  Select **Review configurations** or **Change advisor** settings to open the AI Agent Advisor setup page.

    You can also select **Admin** \(\[Omitted image "icon-now-assist-center-nav-admin.png"\] Alt text: Admin icon in the side navigation bar.\) in the side navigation bar and select **AI Agent Advisor** under **Settings** on the AI Admin Hub page.

    The AI Agent Advisor setup page opens.

    If there are any data sources set up, a separate card displays for each data source.

    \[Omitted image "ai-agent-advisor-data-sources.png"\] Alt text: Separate cards for each data source on the AI Agent Advisor setup page.

3.  Select **Create new**.

    The Add new data set page opens.

    \[Omitted image "ai-agent-advisor-new-data-source.png"\] Alt text: Add new data set page with fields to set up the data source analysis.

4.  Complete the **General information** section.

    1.  Enter a name for the analysis configuration in the **Name** field.

    2.  Enter a description in the **Short description** field.

5.  Choose the data source in the **Select table** section.

    1.  Select **Add role** if permission is required for AI Agent Advisor to access the table; then add the required role to the sn\_agent\_miner.app\_admin role and return to the Add new data set page.

        For more information, see [Add a role to an existing role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/t_AddARoleToAnExistingRole.md).

    2.  Select a table from the **Table name** menu.

    3.  Select one or more fields from the **Fields** menu.

6.  Select the frequency of the analysis schedule in the **Scheduled to run** section.

    -   Select the 30, 60, or 90 day option.
    -   Toggle the **On-Off** option to `Off` to stop AI Agent Advisor from running the recurring analysis and identifying opportunities.

        If the scheduled run is turned off, new opportunities for the data source won’t appear until a new run is scheduled or triggered manually.

7.  Apply filters to refine the scope of the analysis.

    1.  Use conditions to select certain properties as a filter.

        For more information on how conditions work, see [OR conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/c_UsingORConditions.md).

        **Note:** A filter for the **Created** field is required.

    2.  Select **Add condition set** to add conditions.

8.  Create a cost profile to calculate the estimated time and cost savings from using the automation.

    1.  Select **Add new** in the **Savings projections** section.

        The Add new box opens.

    2.  Add general details for the cost profile by entering a name and description.

    3.  Select **Next**.

    4.  Apply filters to the cost profile by using conditions to select certain properties.

    5.  Select **Next**.

    6.  Enter the hourly labor cost.

    7.  Enter the active handling time rate.

        The percentage of a record’s total open time that represents actual hands-on effort by a human agent.

9.  Select **Save and activate**.


## Result

AI Agent Advisor runs the analysis according to the configured filters and schedule. After the analysis completes, automation opportunities appear on the AI Admin Center home page and on the Automation opportunities page.

## What to do next

View your automation opportunities on the home page. For more information, see [View your automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-view-automation-opportunities.md).

**Parent Topic:**[Setting up automation opportunity discovery in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-automation-discovery-setup.md)

**Related topics**  


[Edit an analysis data source]()

[Deactivate an analysis data source]()

[Activate a deactivated analysis data source]()

