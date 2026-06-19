---
title: Add the Now Assist context menu
description: Use the Now Assist context menu to enable Now Assist skills to be displayed directly in the dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/add-nacm.html
release: australia
topic_type: task
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Add elements, Edit a dashboard, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Add the Now Assist context menu

Use the Now Assist context menu to enable Now Assist skills to be displayed directly in the dashboard.

## Before you begin

Role required: Any user with an internal role can add the context menu to an inline dashboard.

## About this task

By default there is a Now Assist context menu added to the dashboard configured with the role sn\_pa\_aia\_insights.summary\_user. This role enables users to generate AI-powered summaries from dashboard data. You can add additional context menu elements and configure these with other AI skills.

-   Results apply only to the tab the context menu element is placed on. Results apply to the entire dashboard when the element is placed above the tabs.
-   Any applied filters on the dashboard are taken into account in the summary output.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select [Create a dashboard with the in-line editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-db-in-ac.md) or open the dashboard you want to add the context menu to.

3.  Expand **Add New Element**.

4.  Select the **Now Assist Context Menu** element.

5.  Place the element where you want it on the dashboard.

6.  Associate a Now Assist Context Menu skill with the element.

    1.  Select the **Dashboard Summary** element that you added.

    2.  In the Configuration panel, select the magnifier icon \[Omitted image "magnifier-zoom.png"\] Alt text: Magnify zoom icon. for the skill configuration.

    3.  Select the skill you want to add.

        **Note:** Not all skills on the resulting list are configured for the **Now Assist Context Menu** element. Only the skills configured on the Par\_dashboard table are appropriate for this element. For more information, see [Configure the Now Assist context menu in Now Assist Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configure-db-summarization-skill-nacm.md).


## Result

The Now Assist context menu appears on the dashboard for use by anyone viewing the dashboard, configured to show information associated with the selected skill.

-   **[Configure the Now Assist context menu in Now Assist Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configure-db-summarization-skill-nacm.md)**  
The Now Assist context menu enables users to apply a variety of AI skills in the context of dashboards.

**Parent Topic:**[Add visual elements to an in-line dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/add-elements-to-a-dashboard.md)

