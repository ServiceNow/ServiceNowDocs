---
title: Dashboard summary skill
description: Dashboard summarization skills are enabled by default when the Dashboard Summary plugin is installed. Configure ServiceNow Otto access to these skills under ServiceNow Otto skills for Data and Analytics to give users AI-assisted dashboard context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/dashboard-summary-skill.html
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
keywords: [AI Admin Hub, Now Assist Admin Console]
breadcrumb: [Configure, Dashboard Summary, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Dashboard summary skill

Dashboard summarization skills are enabled by default when the Dashboard Summary plugin is installed. Configure ServiceNow Otto access to these skills under ServiceNow Otto skills for Data and Analytics to give users AI-assisted dashboard context.

## Before you begin

Role required: now\_assist\_admin

## About this task

The ServiceNow Otto context menu has two forms and each form uses AI skills differently.

-   **Dashboard Summary**

    The Dashboard Summary is added by default to Platform Analytics experience dashboards. The associated ServiceNow Otto dashboard summarization skill is selected by default.

-   **ServiceNow Otto context menu dashboard element**

    The context menu can be used as a reusable configurable dashboard element with any valid dashboard AI skill. To enable the skills for the dashboard element, see [Configure the ServiceNow Otto context menu in Now Assist Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configure-db-summarization-skill-nacm.md).


**Note:** By default, every authenticated user has access to the Dashboard Summary. You can limit access to specific roles from the AI Admin Hub, either while activating the skill or later. To limit access, you must be in the AI Dashboard Insights scope.

## Procedure

1.  If you want to limit the roles that can use this skill, change application scopes to AI Dashboard Insights.

2.  Navigate to **All** &gt; **ServiceNow Otto Admin** &gt; **Skills**.

3.  In the product area pane, select **Data and Analytics** &gt; **Analytics**.

4.  In AI skills for Analytics, filter on Analytics Skills, then search for the dashboard summarization skill.

    \[Omitted image "nowass-db-dv-export-skill.png"\] Alt text: AI Skills tab of AI Admin Hub, showing the dashboard and visualization export skill under Data and Analytics &gt; Analytics.

5.  Select **Turn on**.

6.  In the User access - Access Control List section, limit which roles can use this skill.

    1.  Select the edit icon \[Omitted image "edit-icon.png"\].

    2.  If you aren't in the AI Dashboard Insights application scope, cancel the activation and change to this scope, then redo all previous steps.

        \[Omitted image "ai-app-insights-scope.png"\] Alt text: Changing scope to AI Dashboard Insights.

    3.  Change user access from **Any authenticated user** \(default\) to **Select roles**.

        \[Omitted image "nowass-db-summ-acl.png"\] Alt text: Options to edit user access for dashboard summarization. Select roles chosen with three roles added to the list.

    4.  Select one or more roles.

    5.  Select **Apply**.

    You can come back later and change these roles by selecting **Edit configuration** on the dashboard summarization skill tile.

7.  Select **Turn on**.

    When the skill is turned off, all dashboards show a message that the Dashboard Summary feature requires a skill and advises the user to contact an administrator.


**Related topics**  


[Use ServiceNow Otto context menu for custom skill deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-now-assist-context-menu-for-custom-skill-deployment.md)

