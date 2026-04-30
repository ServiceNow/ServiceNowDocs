---
title: Exploring Digital End-user Experience Self-service
description: Digital End-user Experience Self-service \(DEX Self-service\) enables you to monitor device health performance, view detected issues, and use suggestion resolutions to resolve issues.
locale: en-US
release: zurich
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Employee Self-service, Digital End-User Experience, IT Service Management]
---

# Exploring Digital End-user Experience Self-service

Digital End-user Experience Self-service \(DEX Self-service\) enables you to monitor device health performance, view detected issues, and use suggestion resolutions to resolve issues.

## Digital End-user Experience Self-service overview

With DEX Self-service, you can monitor device health on demand. When issues are detected, you can address them by using the suggested resolutions. These resolutions can be remedial actions, self-help instructions, or links to help resources. Additionally, you can initiate device actions even when no issues are detected to maintain optimal performance of your devices and applications.

By default, DEX Self-service is inactive in the base system. To activate it, you must enable the base system issue configurations. For more information, see [Enable issue configurations for DEX Self-service](../task/enable-dex-self-service-issues.md).

You can access Device health check from the following sources:

|Source|Feature|
|------|-------|
|Employee Center|[Check device health using Employee Center](../task/check-your-device-s-using-employee-center.md)|
|Desktop Assistant|[Check device health using Desktop Assistant](../task/check-your-device-s-health-using-desktop-assistant.md)|
|Now Assist for ITSM Virtual Agent|[Check device health using Now Assist for ITSM Virtual Agent](../task/check-your-device-s-health-using-now-assist-for-itsm.md)|

When you install DEX Self-service, several base system components are automatically installed. For more information, see [Components installed with DEX Self-service](../reference/components-installed-with-dex-self-service.md).

## DEX Self-service workflow for employees

1.  Access Device health check from any of the following sources:
    -   Employee Center. See [Check device health using Employee Center](../task/check-your-device-s-using-employee-center.md).
    -   Desktop Assistant. See [Check device health using Desktop Assistant](../task/check-your-device-s-health-using-desktop-assistant.md).
    -   Now Assist for ITSM Virtual Agent. See [Check device health using Now Assist for ITSM Virtual Agent](../task/check-your-device-s-health-using-now-assist-for-itsm.md).
2.  \(Optional\) If there are multiple devices, select a device to check its health.
3.  View the health of the device by performance category \(Good, Average, or Poor\). For more information about how device health is calculated, see [Device heath check calculation](../reference/Device-health-check-calculation.md).
4.  \(Optional\) Trigger device actions for optimal device performance, even when no issues are detected.

    **Note:** You can access the Device actions tab from the Employee Center or Desktop Assistant.

5.  Resolve device health issues by using issue-specific suggested resolutions. A resolution can be any of the following:
    -   Remedial action
    -   Self-help instruction
    -   Link to help resources
6.  Proceed with one of the following actions based on the resolution status:
    -   If the resolution is successful, select **Yes** or **No** to the feedback question to confirm if the resolution helped address the issue. If you select **No**, a fallback action is provided.
    -   If the resolution fails and there’s no improvement in device performance or if you mark an issue as unresolved, a fallback action is provided.

        **Note:** DEX administrators can configure fallback options as part of the issue configurations.


## DEX Self-service benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Monitor the health of devices and applications.|[Using Digital End-user Experience Self-service](using-dex-self-service.md)|Employees|
|Monitor device health issues and take suggested steps to improve performance. If a resolution doesn’t improve performance, fallback options guide you to the next steps to be taken.|[Using Digital End-user Experience Self-service](using-dex-self-service.md)|Employees|
|Maintain optimal device and application performance by triggering device actions even when no issues are detected.|[Using Digital End-user Experience Self-service](using-dex-self-service.md)|Employees|
|Configure device health categories, issues, and device actions.|[Configuring Digital End-user Experience Self-service](configuring-dex-self-service.md)|DEX Admin|

## What to explore next

To learn more about configuring and using Digital End-user Experience Self-service, see:

-   [Configuring Digital End-user Experience Self-service](configuring-dex-self-service.md)
-   [Enable issue configurations for DEX Self-service](../task/enable-dex-self-service-issues.md)
-   [Using Digital End-user Experience Self-service](using-dex-self-service.md)
-   [Check device health using Employee Center](../task/check-your-device-s-using-employee-center.md)
-   [Check device health using Desktop Assistant](../task/check-your-device-s-health-using-desktop-assistant.md)
-   [Check device health using Now Assist for ITSM Virtual Agent](../task/check-your-device-s-health-using-now-assist-for-itsm.md)

