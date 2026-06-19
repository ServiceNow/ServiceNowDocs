---
title: Generate vulnerability insights with generative AI
description: Use the Security Exposure Management \(SEM\) Insights generative AI skill to provide contextual summaries and actionable recommendations in the Security Exposure Management \(SEM\) Workspace. Use insights based on exposure data, threat intelligence, remediation status, and asset context to surface dynamic insights for Findings views. Help admins, analysts, and vulnerability managers prioritize critical risks and take immediate remediation actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/sem-insights-skill.html
release: australia
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Generate vulnerability insights with generative AI

Use the Security Exposure Management \(SEM\) Insights generative AI skill to provide contextual summaries and actionable recommendations in the Security Exposure Management \(SEM\) Workspace. Use insights based on exposure data, threat intelligence, remediation status, and asset context to surface dynamic insights for Findings views. Help admins, analysts, and vulnerability managers prioritize critical risks and take immediate remediation actions.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see .

The Now Assist panel must be activated. For more information, see .

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see .

For more information about configuring this skill, see [Configure a generative AI skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/activate-skills-now-assist-vulnerability-response.md).

Role required: sn\_vul\_ai.run\_sem\_insights

To generate insights in the SEM workspace, you must have the sn\_vul\_ai.run\_sem\_insights role assigned.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Security Exposure Management**.

2.  Open the dashboard for which you would want to generate insights.

3.  Select **Generate Insights** to create tailored insights for the selected page.

4.  Review the generated insights displayed in the **Now Assist Insights** panel.

    Example:

    -   273 Critical vulnerabilities have no remediation target set – Create remediation task
    -   379 findings are unassigned – Immediate triage needed
5.  Drill down into any insight by selecting the linked numbers to open filtered records and take action directly from the workspace.


## What to do next

-   **Regenerate insights** after applying dashboard filters for more tailored results.
-   **Provide feedback** on insights using the thumbs up/down icons on each card to rate the usefulness of insights.
-   **Refresh** dashboard data with the refresh icon. Refresh updates data but does not regenerate insights automatically.

**Parent Topic:**[Using Unified Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/using-unified-security-exposure-management.md)

