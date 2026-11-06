---
title: Configure Proactive Engagement resolutions with DEX
description: Configure metric rules with Proactive Engagement resolutions to trigger alerts and resolutions when a monitored device or application deviates from the specified metrics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/configuring-metric-rule.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Set up Proactive Engagement, Configure, Digital End-User Experience, IT Operations Management]
---

# Configure Proactive Engagement resolutions with DEX

Configure metric rules with Proactive Engagement resolutions to trigger alerts and resolutions when a monitored device or application deviates from the specified metrics.

## Before you begin

The Digital End-User Experience application must be installed. For details on the installation of the Digital End-User Experience application, see [Install Digital End-User Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/install-app-device-health.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **SOW** &gt; **DEX Administration** &gt; **Metric rules** &gt; **Create metric rule**.

    \[Omitted image "select\_ci\_pe.png"\] Alt text: Select the CI window

2.  In the CI selection window, select the device or type of application to monitor for issues.

    For more information about CI selection, see [Specify the configuration item for a metric rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/specify-metric-rule-applications.md).

3.  Select **Next**.

4.  Select the metric and criteria to create an alert.

    \[Omitted image "metric\_rule\_add\_criteria.png"\] Alt text: Add criteria

    For more information about alert criteria, see [Define alert criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/define-alert-metric-criteria.md).

5.  Select **Next**.

6.  Update the alert action to define the resolution for the metric rule.

    \[Omitted image "alert-action.png"\] Alt text: Set alert action

    **Note:** Remedial actions that require entering parameters aren't supported and you won't be able to select when the resolution type is Remedial Action.

7.  Select **Next**.

8.  Select the type of resolution and update the resolution details.

    For more information about the different types of resolution, see [Resolutions for Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/resolutions.md).

    \[Omitted image "resolutions\_y.png"\] Alt text: Proactive resolution content window to add the Resolution details.

9.  If the resolution type is a remedial action that has input parameters, enter the advanced settings for each input parameter of the selected remedial action.

    For more information about the Advanced settings, see [Input parameters for remedial actions in Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/advanced-settings.md).

10. Select **Continue to Engagement Settings**.

11. Update the **Engagement settings**.

    \[Omitted image "engagement\_settings\_y.png"\] Alt text: Define the engagement settings

    **Note:**

    -   For information about updating the engagement settings, see [Engagement settings for Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/engagement-settings.md).
    -   Select Desktop Assistant as the notification channel to notify users with self-help instructions. For more information, see [Desktop Assistant notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/da-push-notifications.md).
12. Select **Add Resolution**.

13. To define the name and activate the rule, see [Metric rule triggering Proactive Engagement through alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/metric-rule-triggering-pe-through-alerts.md).

    **Note:** Every time the criteria set in the metric rule are met, the metric rule triggers the resolution and helps you resolve the issue.


