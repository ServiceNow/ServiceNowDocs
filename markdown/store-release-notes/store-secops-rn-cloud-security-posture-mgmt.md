---
title: Cloud Security Posture Management release notes
description: Version history for the Cloud Security Posture Management application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-cloud-security-posture-mgmt.html
release: store
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Cloud Security Posture Management release notes

Version history for the Cloud Security Posture Management application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.5.0 - February 2024**

    Removed: The capability to detect internet exposure for AWS assets has been moved out of this plugin.

-   **Version 2.2.1 - August \(Vancouver\)**

    New:

    -   Detect internet-facing assets \(AWS only\).
    -   Detect internet-facing assets with vulnerabilities or security tool coverage gaps such as missing endpoint protection agent \(AWS only\).
-   **Version 2.1.3 - May 2023**
    -   New: Audit results for successful configuration findings are created.
    -   Fixed:
        -   Configuration tests and policies display as expected.
        -   New test results can be ingested into the GRC application.
        -   The attributes for the sections and criticality in imported policies have been fixed so they display as expected.
-   **Version 2.0.3 - February 2023**
    -   New:
        -   Ability to scan cloud environments \(AWS and Azure\) natively.
        -   Out-of-the-box CIS Benchmarks policies for AWS and Azure.
        -   Ability to create custom policies.
        -   Ability to auto-scan child service accounts when datacenters are discovered.

**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

