---
title: Instance Scan release notes
description: The ServiceNow Instance Scan engine is used to interrogate your instance for configurations that indicate health issues and identify opportunities to address ideal configurations. Instance Scan was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Instance Scan release notes

The ServiceNow® Instance Scan engine is used to interrogate your instance for configurations that indicate health issues and identify opportunities to address ideal configurations. Instance Scan was enhanced and updated in the Australia release.

## Instance Scan highlights for the Australia release

-   Enable parallel scans to streamline processing and reduce completion times.
-   Experience the new scan\_check\_writer role to write checks in the Instance Scan table.
-   Execute scans on inactive and base system records by enabling certain system properties.

See [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information.

## New in the Australia release

-   **[Parallel execution of scans](https://www.servicenow.com/docs/access?context=hs-parallel-scan&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    Enable parallel execution of scans instead of sequential processing, eliminating bottlenecks and significantly reducing completion times.

-   **[New role to write checks in Instance Scan](https://www.servicenow.com/docs/access?context=hs-getting-started&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    Experience the new scan\_check\_writer role that has the privilege to write checks on the scan\_check table.

-   **[Instance Scan extension for IDE](https://www.servicenow.com/docs/access?context=hs-is-ide&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    You can now access Instance Scan from integrated development environment \(IDE\) on the ServiceNow AI Platform.


## Changed in this release

-   **[Scan execution of inactive and base system checks](https://www.servicenow.com/docs/access?context=hs-sys-properties&version=australia&pubname=australia-platform-administration&ft:locale=en-US)**

    You can now execute scans on inactive checks by setting the glide.scan.inactive\_records property to true. Add and enable glide.scan.base\_system\_records property to execute scans on base system checks.


## Activation information

Instance Scan is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

