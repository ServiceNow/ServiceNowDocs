---
title: Generate vulnerability insights with generative AI
description: Use the Security Exposure Management \(SEM\) Insights generative AI skill to provide contextual summaries and actionable recommendations in the Security Exposure Management \(SEM\) Workspace. Use insights based on exposure data, threat intelligence, remediation status, and asset context to surface dynamic insights for findings views. Help admins, analysts, and vulnerability managers prioritize critical risks and take immediate remediation actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-insights-skill.html
release: australia
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Generate vulnerability insights with generative AI

Use the Security Exposure Management \(SEM\) Insights generative AI skill to provide contextual summaries and actionable recommendations in the Security Exposure Management \(SEM\) Workspace. Use insights based on exposure data, threat intelligence, remediation status, and asset context to surface dynamic insights for findings views. Help admins, analysts, and vulnerability managers prioritize critical risks and take immediate remediation actions.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

The ServiceNow Otto® panel must be activated. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

For more information about configuring this skill, see [Configure a generative AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/activate-skills-now-assist-vulnerability-response.md).

Role required: sn\_vul\_ai.run\_sem\_insights

To generate insights in the SEM workspace, you must have the sn\_vul\_ai.run\_sem\_insights role assigned.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management**.

2.  Open a dashboard to generate insights.

    For example, open the dashboard on the Home page.

3.  Select **Generate Insights**.

    The system creates tailored insights for the selected page.

4.  Review the insights in the **ServiceNow Otto Insights** panel.

    Example insights:

    -   Address 331 Critical findings with no remediation target set.
    -   Investigate 379 Critical findings with no target and no assignment group.
    Select the links on the insight cards to open filtered records and take actions directly from the workspace. For example, you can create remediation tasks or re-evaluate data.


## What to do next

-   Regenerate insights after applying dashboard filters for more tailored results.
-   Provide feedback on insights using the thumbs up or thumbs down icons on each card.
-   Refresh dashboard data with the refresh icon. Refreshing updates data but does not regenerate insights automatically.

**Parent Topic:**[Using Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/using-unified-security-exposure-management.md)

