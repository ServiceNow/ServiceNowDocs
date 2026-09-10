---
title: Instance Scan release notes
description: The ServiceNow Instance Scan engine is used to interrogate your instance for configurations that indicate health issues and identify opportunities to address ideal configurations. Instance Scan was enhanced and updated in the Australia release.The ServiceNow Instance Scan engine is used to interrogate your instance for configurations that indicate health issues and identify opportunities to address ideal configurations. Instance Scan was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Instance Scan release notes

The ServiceNow® Instance Scan engine is used to interrogate your instance for configurations that indicate health issues and identify opportunities to address ideal configurations. Instance Scan was enhanced and updated in the Australia release.

## About Instance Scan

-   Enable parallel scans to streamline processing and reduce completion times.
-   Experience the new scan\_check\_writer role to write checks in the Instance Scan table.
-   Execute scans on inactive and base system records by enabling certain system properties.

See [Instance Scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/hs-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Instance Scan is a ServiceNow AI Platform feature that is active by default.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-admin-rn-landing.md)

## Australia

The ServiceNow® Instance Scan engine is used to interrogate your instance for configurations that indicate health issues and identify opportunities to address ideal configurations. Instance Scan was enhanced and updated in the Australia release.

### What's new

-   **[Parallel execution of scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/hs-parallel-scan.md)**

    Enable parallel execution of scans instead of sequential processing, eliminating bottlenecks and significantly reducing completion times.

-   **[New role to write checks in Instance Scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/hs-getting-started.md)**

    Experience the new scan\_check\_writer role that has the privilege to write checks on the scan\_check table.

-   **[Instance Scan extension for IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/hs-is-ide.md)**

    You can now access Instance Scan from integrated development environment \(IDE\) on the ServiceNow AI Platform.


### What's changed

-   **[Scan execution of inactive and base system checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/hs-sys-properties.md)**

    You can now execute scans on inactive checks by setting the glide.scan.inactive\_records property to true. Add and enable glide.scan.base\_system\_records property to execute scans on base system checks.


