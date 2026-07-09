---
title: Deactivate indicator support
description: AI Data Explorer supports indicators as data sources by default. If you do not want the application to use indicator data on your instance, you can turn this support off.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/aide-deactivate-indicator-support.html
release: zurich
topic_type: task
last_updated: "2026-06-19"
reading_time_minutes: 1
breadcrumb: [Configure, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Deactivate indicator support

AI Data Explorer supports indicators as data sources by default. If you do not want the application to use indicator data on your instance, you can turn this support off.

## Before you begin

Roles required: now\_assist\_explorer\_admin or higher

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the product area pane, select **Data and Analytics** &gt; **Analytics**.

3.  In Now Assist skills for Analytics, search for the analytics exploration skill.

4.  If the **Activate skill** button is visible for this skill, press it to activate the skill.

5.  If the **Deactivate skill** button is visible for this skill, expand the 3-dot menu \[Omitted image "icon-menu.png"\] Alt text: Menu icon and select **Edit**.

    \[Omitted image "ai-data-expl-edit-skill.png"\] Alt text: Tile for the Analytics exploration skill showing the Edit button.

6.  Under Advanced options, look for Indicators in AI Data Explorer.

7.  Turn off **Enable indicators**.

    \[Omitted image "aide-disable-indicator-support.png"\] Alt text: The Enable Indicators toggle for the analytics exploration skill.

8.  Select **Save and continue**.


## What to do next

**Note:** To deactivate queries on indicator data for all AI applications on an instance, deactivate the Query Generation "analytics query generation for indicators" skill.

**Parent Topic:**[Configure AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configure-now-ass-explorer.md)

