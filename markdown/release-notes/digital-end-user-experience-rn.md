---
title: Digital End-User Experience release notes
description: The ServiceNow Digital End-User Experience application is a cloud-based tool providing IT with comprehensive visibility and monitoring for user applications, networks, and devices. See the following sections for release notes by version.This release includes updates to Digital End User Experience features and functionality.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/digital-end-user-experience-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-17"
reading_time_minutes: 2
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Digital End-User Experience release notes

The ServiceNow® Digital End-User Experience application is a cloud-based tool providing IT with comprehensive visibility and monitoring for user applications, networks, and devices. See the following sections for release notes by version.

## About Digital End-User Experience

-   Digital End-User Experience \(DEX\) detects and fixes potential technology issues before they affect you. Your IT team deploys DEX to monitor computers and applications.
-   DEX collects usage and performance data from endpoints. It uses metric rules to detect issues, remediate them automatically, and engage you proactively.
-   With the DEX Desktop Assistant, you can troubleshoot local applications, use Virtual Agent, run network tests, and contact IT support. Admins can send alerts to your Desktop Assistant.
-   DEX includes DEX Application and Device Health, DEX Content Playbook, and DEX Desktop Assistant. Application and Device Health provides end-to-end visibility into applications, networks, and devices, regardless of location.

See [Digital End-User Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/dex-landing-cf.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Digital End-User Experience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Browser requirements**

    Enable the DEX browser extension to monitor web applications for various operational or performance-based metrics on your system. For more information, see [Enable DEX browser extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/enable-dex-browser-extension.md).


## Accessibility and localization

-   **Accessibility information**

    Localization is applicable to DEX in all languages supported by the ServiceNow AI Platform.


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-service-management-rn-landing.md)

## Version 5.3.0

This release includes updates to Digital End User Experience features and functionality.

### What's new

-   **[Digital End-User Experience remedial actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/dex-diff-ra.md)**

    You can now use remedial actions to start or stop a Windows service, clear the system cache, and reset the print spooler.

-   ****

    You can now execute remedial actions from Flow designer. Each action runs only when the device is online and the action applies to it.

-   **[Metric rule rate limiting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/metric-rule-rate-limiting.md)**

    Metric rules and event rules are now rate limited per rule on the device. This helps prevent a single noisy rule from flooding the instance with alerts or events.


-   **[Customize DEX alert events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/customize-dex-alert-events.md)**

    A new extension point for metric rule events gives you more control over how events are evaluated before alerts are triggered.


### What's changed

-   **[Devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/dex-workspace-devices-tab.md)**

    The Devices page now includes a link to DEX dashboard, so users with multiple roles can reach the DEX homepage faster.

-   **[Check device health using Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/check-your-device-s-using-employee-center.md)**

    The Diagnose view in Device Health Check now explains why a category shows a **Poor** or **Average** status with no pending actions. It tells users that their IT team is reviewing additional metrics.


