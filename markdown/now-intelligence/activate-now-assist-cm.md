---
title: Configure Now Assist skill
description: Dashboard summarization skills are enabled by default when the Dashboard Summary plugin is installed. Configure Now Assist access to these skills under Now Assist skills for Data and Analytics to give users AI-assisted dashboard context.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/activate-now-assist-cm.html
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configure, Dashboard Summary, Now Assist in Platform Analytics, Platform Analytics]
---

# Configure Now Assist skill

Dashboard summarization skills are enabled by default when the Dashboard Summary plugin is installed. Configure Now Assist access to these skills under Now Assist skills for Data and Analytics to give users AI-assisted dashboard context.

## Before you begin

Role required: now\_assist\_admin

## About this task

The Now Assist context menu has two forms and each form uses AI skills differently.

-   **Dashboard Summary**

    The Dashboard Summary is added by default to Platform Analytics experience dashboards. The associated Now Assist dashboard summarization skill is selected by default.

-   **Now Assist context menu dashboard element**

    The Now Assist context menu can be used as a reusable configurable dashboard element with any valid dashboard AI skill. To enable the skills for the dashboard element, see [Configure the Now Assist context menu in Now Assist Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/configure-db-summarization-skill-nacm.md).


**Note:** By default, every authenticated user has access to the Dashboard Summary. To limit access to the Dashboard Summary configure the role sn\_pa\_aia\_insights.summary\_user. To edit access to this role, the admin must be in the AI Dashboard Insights scope.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  In the product area pane, select **Data and Analytics** &gt; **Analytics**.

3.  In Now Assist skills for Analytics, search for the Dashboard Summarization skill.

    \[Omitted image "nowass-cm-summary-skill.png"\] Alt text: Now Assist Skills tab of Now Assist admin console, showing the skill for Now Assist Dashboard Summarization under Analytics.

4.  Select **Activate skill**.

    When the skill is deactivated, all dashboards sow a message that the Dashboard Summary feature requires a skill and advises the user to contact an administrator.

5.  From the Options menu \[Omitted image "csm-ws-dashboards-more-actions-icon.png"\], select Edit Access.

    \[Omitted image "now-ass-db-summary-edit-skill.png"\] Alt text: Tile for the Dashboard Summarization skill showing the Edit access button.

6.  In the **Add user access** section, select the edit icon \[Omitted image "edit-icon.png"\]

7.  Choose **Select Roles** to select the roles that can generate a summary.

    Otherwise, select **Any authenticated user**.\[Omitted image "nowass-db-summ-acl.png"\] Alt text: Options to edit user access for dashboard summarization. Select roles chosen with three roles added to the list.

8.  Select **Apply**.


**Related topics**  


[Use Now Assist context menu for custom skill deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-now-assist-context-menu-for-custom-skill-deployment.md)

