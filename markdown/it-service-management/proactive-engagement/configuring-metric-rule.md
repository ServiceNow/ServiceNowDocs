---
title: Configuring Proactive Engagement resolutions with DEX
description: Metric rules help the organization by setting the criteria and trigger alerts when the device or the application monitored deviates from the specified metrics.
locale: en-US
release: australia
product: Proactive Engagement
classification: proactive-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Proactive Engagement, Digital End-User Experience, IT Service Management]
---

# Configuring Proactive Engagement resolutions with DEX

Metric rules help the organization by setting the criteria and trigger alerts when the device or the application monitored deviates from the specified metrics.

## Before you begin

Set the resolutions to help you proactively resolve the digital issue using the ServiceNow Digital End-User Experience. For details on the installation of the Digital End-User Experience application, see [Install Digital End-User Experience](../digital-end-user-experience/task/install-app-device-health.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **SOW** &gt; **DEX Administration** &gt; **Metric rules** &gt; **Create metric rule**.

    ![Select the CI window](images/select_ci_pe.png)

2.  Select the device or type of application that you want to monitor and detect issues in the CI selection window.

    For more information on CI selection, see [Specify metric rule CI](../digital-end-user-experience/task/specify-metric-rule-applications.md).

3.  Select **Next**.

4.  Select the metric and criteria to create an alert.

    ![Add criteria](images/metric_rule_add_criteria.png)

    For more information on Alert criteria, see [Define alert criteria](../digital-end-user-experience/task/define-alert-metric-criteria.md).

5.  Select **Next**.

6.  Update the alert action to define the resolution for the metric rule.

    ![Set alert action](images/alert-action.png)

    **Note:** Remedial actions that require entering parameters are not supported and you won't be able to select when the resolution type is Remedial Action.

7.  Select **Next**.

8.  Select the type of resolution and update the resolution details.

    For more information about the different types of resolution, see [Resolution for Proactive Engagement](reference/resolutions.md).

    ![Proactive resolution content window to add the Resolution details.](images/resolutions_y.png)

9.  If you select resolution type as remedial action that has input parameters, enter the **Advanced settings** for each of the input parameters of the selected remedial action.

    For more information about the Advanced settings, see [Input parameters for Remedial action in Proactive Engagement](reference/advanced-settings.md).

10. Select **Continue to Engagement Settings**.

11. Update the **Engagement settings**.

    ![Define the engagement settings](images/engagement_settings_y.png)

    **Note:**

    -   For information on updating the Engagement Settings, see [Engagement Settings for Proactive Engagement](reference/engagement-settings.md)
    -   Choose Desktop Assistant as the notification channel to notify the users with any self-help instructions. For more information, see [Desktop Assistant notifications](../digital-end-user-experience/concept/da-push-notifications.md)
12. Select **Add Resolution**.

13. For defining the name and activation, see [Metric rule triggering Proactive Engagement through alerts](concept/metric-rule-triggering-pe-through-alerts.md)

    **Note:** Every time the criteria set in the metric rule is met, it triggers the resolution and helps you resolve the issue.


**Parent Topic:**[Configuring Proactive Engagement](configuring-proactive-engagement.md)

