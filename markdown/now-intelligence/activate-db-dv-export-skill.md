---
title: The dashboard and visualization export skill
description: Give users generative AI capabilities for creating data visualizations from the ServiceNow Otto panel by activating the dashboard and visualization export skill.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/activate-db-dv-export-skill.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Platform Analytics in the ServiceNow Otto panel, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# The dashboard and visualization export skill

Give users generative AI capabilities for creating data visualizations from the ServiceNow Otto panel by activating the dashboard and visualization export skill.

## Before you begin

The dashboard and visualization export skill is included in Generative AI Controller, which is in most ServiceNow Otto applications from the ServiceNow® Store.

**Note:** By default, every authenticated user has access to the dashboard and visualization export skill. You can limit access to specific roles from the AI Admin Hub, either while activating the skill or later. To limit access, you must be in the Dashboard and visualization export scope.

Role required: admin

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills**.

2.  In the product area pane, select **Data and Analytics**.

3.  In AI skills for Analytics, filter on Analytics Skills, then search for the dashboard and visualization export skill.

    \[Omitted image "nowass-db-dv-export-skill.png"\] Alt text: AI Skills tab of AI Admin Hub, showing the dashboard and visualization export skill under Data and Analytics &gt; Analytics.

4.  In the User access - Access Control List section, limit which roles can use this skill.

    1.  Select the edit icon \[Omitted image "edit-icon.png"\].

    2.  If you aren't in the AI Dashboard Insights application scope, cancel the activation and change to this scope, then redo all previous steps.

        \[Omitted image "ai-app-db-dv-export-scope.png"\] Alt text: Changing scope to Dashboard and visualization export.

    3.  Change user access from **Any authenticated user** \(default\) to **Select roles**.

        \[Omitted image "nowass-db-dv-export-acl.png"\] Alt text: Options to edit user access for dashboard and data visualization export. Select roles chosen with four roles added to the list.

    4.  Select one or more roles.

    5.  Select **Apply**.

    You can come back later and change these roles by selecting **Edit configuration** on the dashboard summarization skill tile.

5.  Select **Turn on**.

    To turn off an activated skill, expand the three-dot menu on the skill tile, then select **Deactivate**.


## Result

If the skill was successfully activated, the system notifies you.

**Parent Topic:**[Configuring Now Assist panel skills for Platform Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configuring-now-ass-skills-pa.md)

