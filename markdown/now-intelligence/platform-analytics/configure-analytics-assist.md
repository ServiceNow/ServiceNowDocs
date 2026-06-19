---
title: Activate the data visualization generation skill
description: Give users generative AI capabilities for creating data visualizations from the Now Assist panel by activating the data visualization generation skill.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/platform-analytics/configure-analytics-assist.html
release: zurich
product: Platform Analytics
classification: platform-analytics
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 1
breadcrumb: [Configure, Platform Analytics in the Now Assist panel, Now Assist in Platform Analytics, Platform Analytics]
---

# Activate the data visualization generation skill

Give users generative AI capabilities for creating data visualizations from the Now Assist panel by activating the data visualization generation skill.

## Before you begin

The data visualization generation skill is included in Generative AI Controller, which is in most Now Assist applications from the ServiceNow® Store.

The Query Generation skills "analytics query generation," "analytics insight generation," "analytics hidden insight generation," and "analytics follow-up generation" are required. These skills are active by default. For more information, see [Query Generation skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/platform-analytics/enable-query-generation.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the product area pane, select **Data and Analytics** &gt; **Analytics**.

3.  In Now Assist skills for Analytics, search for the data visualization generation skill.

    \[Omitted image "nowass-data-viz-gen-skill.png"\] Alt text: Now Assist Skills tab of Now Assist Admin console, showing the Data visualization generation skill under Data and Analytics.

4.  In the **Define access** page, you can add roles who can use this skill.

    By default, the now.assist.creator.analytics, now\_assist\_explorer\_user, and now\_assist\_analytics\_generation roles have these rights. Think carefully before making any changes.

    All **Analytics** skills have this option. The data visualization skill and Query Generation skills should have one role in common. Note that each default data visualization generation role contains the sn\_query\_gen.user role, which is the default role for Query Generation skills.

5.  Select **Turn on**.


## Result

If the skill was successfully activated, the system notifies you.

**Parent Topic:**[Configuring Now Assist panel skills for Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/platform-analytics/configuring-now-ass-skills-pa.md)

