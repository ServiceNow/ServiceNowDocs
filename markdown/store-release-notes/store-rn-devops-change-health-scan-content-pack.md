---
title: DevOps Change Health Scan Content Pack release notes
description: Version history for the DevOps Change Health Scan Content Pack application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-devops-change-health-scan-content-pack.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - DevOps release notes, ServiceNow Store release notes]
---

# DevOps Change Health Scan Content Pack release notes

Version history for the DevOps Change Health Scan Content Pack application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.3.0 - March 2026**
    -   Changed:
        -   The following new checks have been added in the DevOps Change Health Scan Content Pack app:
            -   Identify any callback processing issues in your instance.
            -   Identify any ACLs incorrectly associated with roles in your instance.
            -   Verify whether all DevOps tables are present in your instance and confirm that all required metadata insys\_ tables\* is available.
            -   Verify whether all DevOps roles in your instance contain the expected roles, including inherited roles.
-   **Version 6.2.0 - December 2025**
    -   Changed:
        -   Health scan enhancements
            -   Identify outdated or prolonged discover and import requests using the DevOps -Stale or Long-Running Discover and Import Requests health check.
            -   Verify whether webhooks have been configured correctly for any tracked repository, pipeline, or plan in GitHub, GitLab, Azure DevOps, and Jenkins using the DevOps webhook configuration analysis health check.
            -   Identify OAuth app configuration issues for GitHub tools in the connected state using the DevOps webhook configuration analysis health check.
            -   Verify if any scheduled job has been configured to run as an invalid or non-admin user.
            -   Navigate to the Findings list from the DevOps Change Workspace home page by selecting View all findings in the Health scan findings widget.
-   **Version 6.1.0 - August 2025**

    Changed: Enhanced user experience for DevOps Health scans in the DevOps Change Workspace.

-   **Version 6.0.0 - May 2025**
    -   Changed:
        -   Additional scans for DevOps Health Scan Content pack
            -   Additional set of proactive checks focused on problems that tend to occur before or after an upgrade along with catching configuration issues like plugin and version incompatibilities or pipelines that chronically fail have been added.
-   **Version 5.1.0 - February 2025**

    The DevOps Change Health Scan Content Pack app offers proactive health checks focused on DevOps Change Velocity. These checks help you identify and fix common configuration or upgrade issues quickly, preventing the need for support tickets. You can choose to run the DevOps Change Velocity Health parent scan, which will execute all the checks available in the DevOps suite of scans, or run each child suite individually which will execute the checks applicable to that child suite. Using the DevOps Change Velocity Health - Scheduled child suite, you can create a schedule to regularly trigger DevOps Health instance suite scans even when you don't have an active session. And using the DevOps Change Velocity Health - On-demand suite, you can run the available DevOps Health scan checks on a specific target to obtain focused scan results.


**Parent Topic:**[ServiceNow Store - DevOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-devops-highlight.md)

