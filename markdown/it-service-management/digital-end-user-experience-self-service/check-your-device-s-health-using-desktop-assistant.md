---
title: Check your device's health using Desktop Assistant
description: Use DEX Self-service capability to check your device health.
locale: en-US
release: yokohama
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: task
last_updated: "2025-04-13"
reading_time_minutes: 2
breadcrumb: [Using Digital End-user Experience Self-service, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Check your device's health using Desktop Assistant

Use DEX Self-service capability to check your device health.

## Before you begin

Role required: sn\_dex\_desktop.user

## About this task

The Desktop Assistant Device health check enables you to check device health and resolve issues by following recommended resolutions. These resolutions include remedial actions, self-help instructions, or links to resources that provide remedial actions. You can use Device Actions to maintain optimal device and application performance even when no issues are detected.  

**Note:**

The Device health check widget on Desktop Assistant is visible only if you have the latest version of Desktop Assistant installed. Contact your system administrator to install the latest version.

## Procedure

1.  Open Desktop Assistant.

    For information, see [Open Desktop Assistant](open-desktop-exp.md).

2.  On the  **Desktop Assistant** home page, select **Device health check **.

    ![Device health check home page](../image/DA_Home.png)

3.  On the Device health check page, select the device from the drop-down list.

4.  In the **Diagnose** tab, review the performance category and required actions for the device, applications, and network.

    ![Diagnose tab on Device health check home page](../image/DA_categories.png)

5.  Select a Poor or Average performance category to view the issues and recommended resolutions.

    The resolutions can be remedial action buttons, self-help instructions, or links to resources that provide resolutions. For more information, see [Resolution for Proactive Engagement](../../proactive-engagement/reference/resolutions.md).

    ![Issues and resolutions to improve device performance](../image/DA_issues.png)

6.  Use the recommended resolutions to improve device, application, or network performance.

    **Note:** If a remedial action was triggered in the last 24 hours either from the **Diagnose** or **Device actions** tab, the remedial action button is inactive. It is reactivated 24 hours after the last action was triggered.

7.  Submit feedback about whether the recommended resolution helped resolve an issue.

    -   **Yes**: Select **Yes** if the resolution resolves your issue.
    -   **No**: Select **No** if the resolution doesn’t resolve your issue.

        If you select **No**, you see the option to open an IT ticket, based on the configuration.

8.  Select the **Open an IT ticket** link if you require assistance in resolving an issue.

    An incident record is created and the incident number is displayed. You can select the incident number link to access the record details and status.

9.  Trigger device actions independent of device performance or associated issues.

    1.  On the Device health check page, select the **Device actions** tab.

    2.  To trigger remedial actions for the device, select **Start now**.

    3.  To trigger remedial actions for applications, select **Select item**, select the application from the drop-down list, and then select **Confirm**.

        A status message shows the progress of the action. You can trigger an action for another application while it is still in progress for one application.

    ![Device actions tab in Device health check home page](../image/DA_Device_actions.png)

    |Status of Action|Displayed status|
    |----------------|----------------|
    |Remedial action is successful.|**Completed**|
    |Remedial action hasn’t yet started.|**No action history**|
    |Remedial action is in progress|**In-progress**|
    |Remedial action fails|**Failed**|


