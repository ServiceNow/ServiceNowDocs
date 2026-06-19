---
title: DEX Self-service issue configuration form
description: The DEX Self-service issue configuration form presents elaborate data on the form's fields and their corresponding descriptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-self-service/dex-self-service-issue-config-form.html
release: australia
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# DEX Self-service issue configuration form

The DEX Self-service issue configuration form presents elaborate data on the form's fields and their corresponding descriptions.

<table id="table_vs3_yqb_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

The name of the issue configuration. It is used to identify the issue in the system.

</td></tr><tr><td>

Action Applicability

</td><td>

Determines how the issue configuration is used.-   Diagnose: Used for diagnostic device health checks.
-   Device actions: Used for device actions.

**Note:** If you select **Device actions**, the **Evaluation criteria** and **Evaluation metrics** fields are not available.

-   Both: Used for both diagnostic checks and device actions.

</td></tr><tr><td>

Category

</td><td>

The device health category that classifies the issue.

</td></tr><tr><td>

Subcategory

</td><td>

The subcategory that further classifies the issue within the selected category.

</td></tr><tr><td>

Type

</td><td>

Indicates whether the issue relates to a device or an application.

</td></tr><tr><td>

Device OS

</td><td>

The operating system the issue applies to.-   Windows
-   macOS
-   Both Windows and macOS

</td></tr><tr><td>

User applicability

</td><td>

Determines the users who can view and use the issue configuration.-   End user: The action is visible to employees in Employee Center, Desktop Assistant, and Now Assist.
-   Service desk agent: The action is visible to agents in the agent workspace only.
-   Both end users and service desk agents.

</td></tr><tr><td>

Enabled in DEX Now Assist topic

</td><td>

Determines whether the issue is available in Virtual Agent interactions.

</td></tr><tr><td>

Enabled in EC Self-service

</td><td>

Determines whether the issue is available in the Employee Center self-service portal.

</td></tr><tr><td>

Evaluation metric

</td><td>

The metrics used to evaluate the issue. Multiple metrics can be selected. DEX Self-service checks all selected metrics and determines whether the device health status is Good, Average, or Poor. For more information, see [Customize metric definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-experience-score/dexscr-customize-dex-score-metric-defs.md).

</td></tr><tr><td>

Evaluation criteria

</td><td>

The metric configuration ID and threshold value used to evaluate the issue condition.

</td></tr><tr><td>

Issue Description

</td><td>

A description of the issue that appears in the end-user experience.

</td></tr><tr><td>

Resolution

</td><td>

The resolution code that defines how the issue is resolved. Resolutions are configured in Proactive Engagement. For more information, see [Configuring Proactive Engagement resolutions with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/proactive-engagement/configuring-metric-rule.md).

</td></tr></tbody>
</table>