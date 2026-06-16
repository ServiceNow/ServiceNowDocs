---
title: Alert Rules Management release notes
description: Version history for the Alert Rules Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-alert-rules.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Alert Rules Management release notes

Version history for the Alert Rules Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 18.15.9 - June 2026**

    No release notes.

-   **Version 18.15.3 - March 2026**
    -   New:
        -   Advanced Respond Automation with Now Assist support
        -   Unified incident creation flow
-   **Version 18.14.2 - December 2025**
    -   New:
        -   Introduction of a new sub-flow - create incident advanced to capture advanced out of the box features
        -   Add delay to create incident advanced sub-flow to allow specific alerts to auto-close and self resolve
-   **Version 18.13.2 - February 2025**

    Fixed: Fixing incident creation logic for reopened alerts.

-   **Version 18.13.0 - August 2024**
    -   Changed: Supported scaling out of the Alert Management rule job, specifically for holding execution after the grouping job is completed.
    -   Fixed:
        -   Resolved issue with incident creation when there is an error in the Alert Correlation job.
        -   Implemented performance fixes.
-   **Version 18.11.4 - August 2023**
    -   Fixed:
        -   Handle executions when job is inactive or disabled
        -   Fix execution trigger when update and create time are the same for primary alerts
-   **Version 18.10.6 - May 2023**
    -   Fixed:
        -   Fixing run remediation action alert when legacy alert action is used
        -   Fixing the logic of auto-close incident if alert is closed
        -   Enforce scope application cross scope access privilege
-   **Version 18.9.4 - January 2023**

    Fixed: Fixing quick response issue not working on previous version

-   **Version 18.8.11 - November 2022**

    New: Support scale out of alert management rules job

-   **Version 18.7.4 - February 2022**
    -   Fixed:
        -   Avoid incidents on secondary alerts
        -   Generalize alert key fields
        -   Execute sub-flow on individual alerts
-   **Version 18.6.2 - September 2021**
    -   Fixed:
        -   Performance improvement - Optimize execution of large alert batches
        -   Fixing execution context to SRO rules only
        -   Fixing rules dependency logic
        -   Introducing configurable property \(max\_application\_for\_ci\) instead of hard-coded value
        -   Minor typo and variable renaming
-   **Version 18.2.6 - July 2021**
    -   New - SRO rules on distributed teams:
        -   Enable SRO rules on alert sources from non-SRO integration \(without integration ID\)
        -   Enable SRO rules on CIs impacting SRO services \(without integration ID\)
        -   Support alerts impacting services of different teams
-   **Version 18.2.1 - May 2021**
    -   Changed:
        -   Performance improvements
        -   Fixes
-   **Version 18.1.0 - March 2021**
    -   New:
        -   Alert rules context - Enable users to set the context for rule execution using key/value pairs
        -   Pre-defined conditions - Use pre-defined, script based conditions to enable user-friendly rules setup on SRO screens
        -   Alert rules dependency - Support start-to-finish dependency of rule execution

**Parent Topic:**[ServiceNow Store - ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)

