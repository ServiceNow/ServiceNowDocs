---
title: Exploring Digital End-user Experience Self-service
description: The Digital End-user Experience Self-service \(DEX Self-service\) enables you to monitor your device performance through the Device health check, which is available as a widget in Desktop Assistant and Employee Center, or conversationally through the Now Assist-enabled Virtual Agent.
locale: en-US
release: yokohama
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: concept
last_updated: "2025-04-06"
reading_time_minutes: 6
breadcrumb: [Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Exploring Digital End-user Experience Self-service

The Digital End-user Experience Self-service \(DEX Self-service\) enables you to monitor your device performance through the **Device health check**, which is available as a widget in Desktop Assistant and Employee Center, or conversationally through the Now Assist-enabled Virtual Agent.

## Digital End-user Experience Self-service overview

Using DEX Self-service you can check the device health on demand and address any detected issues by DEX by leveraging recommended resolutions, which can either be remedial actions, self-help instructions, or URLs. Additionally, the widget offers Device Actions that can be triggered even when no issues are detected on the device, allowing you to maintain good performance of the devices and applications.

You can access Device health check from the following sources:

|Source|Feature|
|------|-------|
|Employee Center|[Check your device's health using Employee Center](../task/check-your-device-s-using-employee-center.md)|
|Desktop Assistant|[Check your device's health using Desktop Assistant](../task/check-your-device-s-health-using-desktop-assistant.md)|
|Now Assist for ITSM Virtual Agent|[Check your device’s health using Now Assist for ITSM](../task/check-your-device-s-health-using-now-assist-for-itsm.md)|

DEX Self-service provides the following device health categories and sub-categories in the base system.:

-   Device performance
    -   Computer last restart
    -   Disk space
    -   Battery health
-   Application\(s\) performance
    -   MS Teams application stability
    -   Outlook application stability
    -   Zoom application stability
-   Network stability
    -   Wifi signal strength
    -   VPN connectivity

**Note:** To configure the categories, see [Configure DEX Self-service categories and subcategories](../task/configuring-dex-self-service-categories.md).

DEX Self-service provides the following Issue configurations which are mapped to the relevant sub-categories:

-   Computer restart pending on macOS and Windows device
-   Low disk space on Windows device
-   Low disk space on macOS device
-   MS Teams application crash on Windows device
-   MS Teams application crash on macOS device
-   Outlook application crash on Windows device
-   Outlook application crash on macOS device
-   Poor device battery health on macOS and Windows device
-   Poor WiFi signal on Windows device
-   Poor WiFi signal on macOS device
-   VPN Disconnected in Windows and macOS device
-   Zoom application crash on macOS device
-   Zoom application crash on Windows device

**Note:**

-   By default, DEX Self-service is inactive in the base system. To activate the DEX Self-service, enable the base system content provided in the **Issue Configuration** screen. For more information, see [Enable DEX Self-service for issue configurations](../task/enable-dex-self-service-issues.md).
-   To edit these issue configurations, see [Customize DEX Self-service issue configurations](../task/configuring-dex-self-service-issues.md).
-   For more information on issue configurations, see [Issue config in Digital End-user Experience Self-service](../reference/issue-config-in-dex-ss.md).

The DEX Self-service provides the following device actions in the base system:

-   MAC OS- The device action **Reinstall application** is available for Microsoft Teams, Microsoft Outlook, and Zoom applications.
-   Windows OS- The device action **Clear disk space** is available.

**Note:** To update the device actions, see [Configure DEX Self-service device actions](../task/configuring-dex-self-service-device-actions.md).

## DEX Self-service Employee experience

The Employee experience includes the following:

1.  Access the device health from any of following sources:
    -   Employee Center
    -   Desktop Assistant
    -   Now Assist for ITSM Virtual Agent

        **Note:** To learn how the virtual agent enables you to check your device health, see [.](../task/check-your-device-s-health-using-now-assist-for-itsm.md)

2.  \(Optional\) Select the device to check its health if there are multiple devices.
3.  View the health of the device by category. It could be Good, Average, or Poor To know about how the device health is calculated, see [Device heath check calculation](../reference/Device-health-check-calculation.md) .

    **Note:** Additionally, you can access the Device actions tab irrespective of the device performance. The **Device actions** tab is available if you are accessing Device health check from the Employee Center or Desktop Assistant.

4.  Take action based on the suggested resolution for any issues detected per category. A resolution can be any of the following:
    -   Remedial action button
    -   Self-help instructions
    -   URL
5.  Based on the result of the resolution, the following options are provided:
    -   If the resolution is successful, then a feedback question appears where you can select Yes or No to confirm that process was helpful in resolving the issue. If the user selects No, then the fall back action is provided.
    -   If the resolution fails which means if there is no improvement in device performance or user marked issue as unresolved, then a fallback action is provided.

        **Note:** Fallback options can be configured by the DEX admin as part of the issue configurations.


## DEX Self-service benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Check the health of the device and applications.|[Using Digital End-user Experience Self-service](using-dex-self-service.md)|Employees|
|Use remedial actions – Diagnose the device health and use the suggested resolutions for poor performing subcategories. The resolutions are provided either in the form of remedial action button, URL, or self-help instructions. If the resolution does not improve the performance of the subcategories, fallback options are provided.|[Using Digital End-user Experience Self-service](using-dex-self-service.md)|Employees|
|Use device actions - These actions can be used without having any issue associated with it.  These remedial actions allow the user to maintain good performance of the devices and applications.|[Using Digital End-user Experience Self-service](using-dex-self-service.md)|Employees|
|Configure the categories, issues, and device actions.|[Configuring Digital End-user Experience Self-service](configuring-dex-self-service.md)|DEX Admin|

## What to explore next

To learn more about configuring and using Digital End-user Experience Self-service, see:

-   [Configuring Digital End-user Experience Self-service](configuring-dex-self-service.md)
-   [Enable DEX Self-service for issue configurations](../task/enable-dex-self-service-issues.md)
-   [Using Digital End-user Experience Self-service](using-dex-self-service.md)
-   [Check your device's health using Employee Center](../task/check-your-device-s-using-employee-center.md)
-   [Check your device's health using Desktop Assistant](../task/check-your-device-s-health-using-desktop-assistant.md)
-   [Check your device’s health using Now Assist for ITSM](../task/check-your-device-s-health-using-now-assist-for-itsm.md)

