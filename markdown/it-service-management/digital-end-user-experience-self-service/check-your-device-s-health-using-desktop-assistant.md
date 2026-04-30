---
title: Check your device's health using Desktop Assistant
description: Use DEX Self-service capability to check your device health.
locale: en-US
release: xanadu
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: task
last_updated: "2025-04-13"
reading_time_minutes: 3
breadcrumb: [Using Digital End-user Experience Self-service, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Check your device's health using Desktop Assistant

Use DEX Self-service capability to check your device health.

## Before you begin

Role required: sn\_dex\_desktop.user

## About this task

The Device health check appears as a widget, which allows you to check the device health on demand and resolve the issues by providing the recommended resolutions for the issues. The resolutions can either be remedial actions, self-help instructions, or URL. You can also use Device actions which can be triggered even when no issues are detected on the device.   These actions enable you to maintain good performance of the devices and applications.

## Procedure

1.  Open **Desktop Assistant** page.

    To know more, see [Open Desktop Assistant](open-desktop-exp.md).

2.  On the  **Desktop Assistant** home page, select the  **Device health check ** card.

    ![Device_health_check_home_page](../image/DA_Home.png)

3.  Select the device for which you want to see the health.

    **Note:** Device health card has now changed to Device health check card.

    The Device health check page appears.

4.  To check the device performance, select the **Diagnose** tab.

    ![Diagnose_tab_in_Device_health_check_home_page](../image/DA_categories.png)

5.  Select the poor performing categories in the **Diagnose** tab.

    The issues and the resolutions to resolve the issues appear.![Issues_and_resolutions_to_improve_the_device_health](../image/DA_issues.png)

6.  View and use the resolution to improve the category.

    **Note:**

    -   The resolution can be remedial action button, a Self-help instruction, or an URL. For more information, see [Resolution for Proactive Engagement](../../proactive-engagement/reference/resolutions.md).
    -   If a remedial action has already been triggered in the last 24 hours either from the **Diagnose** or **Device actions** tab, the remedial action button will be disabled. It will be reactivated after 24hours post action trigger.
    For resolutions of type remedial action, if the resolution is successful \(if there is improvement in evaluation metric\) or for resolution of type URL, self-help instructions, a feedback question appears. You can select **Yes** or **No** to confirm if this process was helpful is resolving the issue.

    In case the answer is **No**, the fallback option to open an IT ticket appears based on configuration. After you open a ticket, the ticket Id is visible for employees to access the details and status of the ticket. For resolutions of type remedial action, If the resolution fails, then automatically the fallback option to open an IT ticket appears based on configuration. After you open a ticket, the ticket Id is visible for employees to access the details and status of the ticket.

7.  To trigger any device actions independent of the device performance, select the **Device actions** tab.![Device_actions_tab_in_Device_health_check_home_page](../image/DA_Device_actions.png)

    **Note:**

    -   These actions can be used without having any issue associated with it.  
    -   If you select a device action related to an application, then you must click **Select item** to select a specific application on which you can run the remedial action button.
    -   If an action is in progress for a specific application, then the status says **1 action is progress**, and the action button allows you to select any other application.
8.  Click the remedial action button to run.

    **Note:**

    -   If the action is successful, then it shows the status as **Completed**.
    -   If the action is not yet started, then it shows the status as **No action history**.
    -   If the action is in progress, then it says **In-progress** and the action button is disabled.
    -   If the action fails, then the status appears as **Failed**.
    -   If the action has already been triggered in the last 24 hours either from the **Diagnose** or **Device actions** tab, the remedial action button will be disabled.

