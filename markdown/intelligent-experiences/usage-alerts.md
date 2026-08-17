---
title: Usage alerts
description: Define threshold-based rules at the skill levels to monitor and manage assist consumption and skill execution counts when limits are reached. The solution aims to prevent resource exhaustion, and provide clear, actionable insights through an alerts feed and a rule management interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/usage-alerts.html
release: australia
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [Usage alerts, skill usage alerts, email notification for skill usage]
breadcrumb: [AI Admin Hub Settings, Exploring AI Admin Hub, AI Admin Hub, Enable AI experiences]
---

# Usage alerts

Define threshold-based rules at the skill levels to monitor and manage assist consumption and skill execution counts when limits are reached. The solution aims to prevent resource exhaustion, and provide clear, actionable insights through an alerts feed and a rule management interface.

Set up a rule engine and usage alert system in AI Admin Hub to receive prioritized notifications both in the instance and via email when thresholds are exceeded. This setup allows you to receive early warnings for unexpected or excessive usage. You can also investigate consumption spikes and adjust rules before limits are reached.

**Important:** The minimum version required is Australia patch 4.

\[Omitted image "ai-admin-hub-usage-alerts.png"\] Alt text: Usage Alerts

Key features:

-   Explore the severity filter tabs \(All, Critical, Warning, Info\) for the alerts feed to triage, on usage alerts interface
-   Directly navigate from an alert to the detail page of the affected skill
-   Edit a rule that triggered an alert, directly from the alerts feed
-   Dismiss an alert from the active feed without deleting the associated underlying rule
-   Create and update alert rules through a modal form

**Note:**

Domain separation: Rules can only be edited, enabled, turned off, or deleted within the domain where they were created. To modify or remove a rule, first change the domain of the instance to the original domain of the rule. If you don’t do this, the options to edit or delete the rule will remain turned off.

-   **[Create alert rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-alert-rule.md)**  
Create alert rules to track the usage of generative AI skills in AI Admin Hub and notify you in the instance and via email, when the set thresholds are reached.

**Parent Topic:**[AI Admin Hub Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-now-assist-admin-settings.md)

