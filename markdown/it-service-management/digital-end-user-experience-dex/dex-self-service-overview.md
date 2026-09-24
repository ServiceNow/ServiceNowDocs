---
title: Digital End-user Experience Self-service overview
description: Digital End-user Experience Self-service \(DEX Self-service\) enables you to monitor device health performance and view and resolve detected issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/dex-self-service-overview.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Explore, Digital End-User Experience, IT Service Management]
---

# Digital End-user Experience Self-service overview

Digital End-user Experience Self-service \(DEX Self-service\) enables you to monitor device health performance and view and resolve detected issues.

DEX Self-service provides comprehensive insights into device health by detecting issues and enabling you to use suggested resolutions to improve device and application performance. These resolutions include remedial actions, self-help instructions, or links to help resources. You can initiate device actions even when no issues are detected to maintain optimal device and application performance. If a resolution doesn't improve performance, fallback options guide you to the next steps to be taken.

\[Omitted video\] Description: Overview of DEX Self-service

The video provides an overview of DEX Self-service, including how to access it and how employees can use it to resolve common device and application issues independently. It demonstrates this process with an example of using DEX Self-service from Desktop Assistant.

By default, DEX Self-service is inactive in the base system. To activate it, you must enable the base system issue configurations. For more information, see [Enable issue configurations for DEX Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/enable-dex-self-service-issues.md).

When you install DEX Self-service, several base system components are automatically installed. For more information, see [Components installed with DEX Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/components-installed-with-dex-self-service.md).

## DEX Self-service benefits

-   Device and application health monitoring: Real-time monitoring of device and application health provides insight into performance status.
-   Issue resolution with guided support: Resolutions are suggested for detected issues, with fallback options available if resolutions don't improve performance.
-   Proactive device health maintenance: Device actions can be triggered to maintain optimal device and application performance even if no issues are detected.
-   Flexible configuration: Device health categories, issues, and device actions can be configured by administrators to meet organizational needs.

## DEX Self-service access

You can access Device health check from the following sources:

-   Employee Center. For more information, see [Check device health using Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/check-your-device-s-using-employee-center.md).
-   Desktop Assistant. For more information, see [Check device health using Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/check-your-device-s-health-using-desktop-assistant.md).
-   ServiceNow Otto Virtual Agent. For more information, see [Check device health using ServiceNow Otto for ITSM Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/check-your-device-s-health-using-now-assist-for-itsm.md).

## DEX Self-service workflow for employees

1.  Device health check access from Employee Center, Desktop Assistant, or ServiceNow Otto for ITSM Virtual Agent.
2.  Device selection if there are multiple devices, where employees can select a device to check its health.
3.  Device health review by performance category \(Good, Average, or Poor\). For more information about how device health is calculated, see [Device heath check calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/Device-health-check-calculation.md).
4.  Device actions execution for optimal device performance, even when no issues are detected.

    **Note:** You can access the Device actions tab from Employee Center or Desktop Assistant.

5.  Resolution of device health issues by using issue-specific suggested resolutions, which include remedial actions, self-help instructions, or links to help resources.
6.  Resolution status feedback to determine if the resolution was successful. If a resolution proves unsuccessful or there is no improvement in device performance, a fallback action is provided to guide the next steps. DEX administrators configure fallback options as part of the issue configurations.

## Operating system support

DEX Self-service supports Windows and macOS devices. Issue configurations related to DEX Self-service device health check and device actions are scoped to Windows, macOS, or both. Only configurations matching the device OS are available on that device.

The two operating systems differ in how the Agent Client Collector \(ACC\) agent runs device health checks and device actions.

-   Windows: The ACC agent runs device health check and device actions under the ACC agent service account. For setup details, see [Install ACC for DEX on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/install-acc-for-dex-windows.md).
-   macOS: The ACC agent runs device health checks and device actions under a specific local service account named `_servicenow`. Using an incorrect account name during setup causes device health check and actions to appear to run but not complete successfully. For setup details, see [Install ACC for DEX on macOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/install-acc-for-dex-macos.md) and [Configure ServiceNow sudoers file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/config-sudoers-file.md).

**Related topics**  


[Configuring Digital End-user Experience Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/configuring-dex-self-service.md)

[Enable issue configurations for DEX Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/enable-dex-self-service-issues.md)

[Using Digital End-user Experience Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/using-dex-self-service.md)

[Check device health using Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/check-your-device-s-using-employee-center.md)

[Check device health using Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/check-your-device-s-health-using-desktop-assistant.md)

[Check device health using ServiceNow Otto for ITSM Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/check-your-device-s-health-using-now-assist-for-itsm.md)

