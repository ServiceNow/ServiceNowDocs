---
title: DEX Self-service issue configuration form
description: The DEX Self-service issue configuration form contains the fields that define an issue configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/dex-self-service-issue-config-form.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [DEX Self-service reference, Reference, Digital End-User Experience, IT Operations Management]
---

# DEX Self-service issue configuration form

The DEX Self-service issue configuration form contains the fields that define an issue configuration.

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

Option that determines how the issue configuration is used.-   Diagnose: Used for diagnostic device health checks.
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

Option that indicates whether the issue relates to a device or an application.

</td></tr><tr><td>

Device OS

</td><td>

The operating system the issue applies to.-   Windows
-   macOS
-   Both Windows and macOS

</td></tr><tr><td>

User applicability

</td><td>

Users who can view and use the issue configuration.-   End user: The action is visible to employees in Employee Center, Desktop Assistant, and ServiceNow Otto.
-   Service desk agent: The action is visible to agents in the agent workspace only.
-   Both end users and service desk agents.

</td></tr><tr><td>

Enabled in DEX ServiceNow Otto topic

</td><td>

Option that determines whether the issue is available in Virtual Agent interactions.

</td></tr><tr><td>

Enabled in EC Self-service

</td><td>

Option that determines whether the issue is available in the Employee Center self-service portal.

</td></tr><tr><td>

Evaluation metric

</td><td>

The metrics used to evaluate the issue. You can select multiple metrics. DEX Self-service checks all selected metrics and determines whether the device health status is Good, Average, or Poor. For more information, see [Customize metric definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/dexscr-customize-dex-score-metric-defs.md).

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

The resolution code that defines how the issue is resolved. Resolutions are configured in Proactive Engagement. For more information, see [Configure Proactive Engagement resolutions with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/configuring-metric-rule.md).

</td></tr></tbody>
</table>