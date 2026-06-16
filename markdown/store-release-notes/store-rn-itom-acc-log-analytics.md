---
title: Agent Client Collector Log Analytics release notes
description: Version history for the Agent Client Collector Log Analytics application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-acc-log-analytics.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Agent Client Collector Log Analytics release notes

Version history for the Agent Client Collector Log Analytics application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.10.3 - June 2026**

    Changed: Enhanced to support onboarding of ACC Log Analytics data input in the SOW Integration Launchpad.

-   **Version 3.9.1 - December 2025**

    Fixed: PRB1910656 - Agents do not honor timeout on background checks. Background checks timeout should be 0 to run without timeout.

-   **Version 3.8.10 - August 2025**
    -   Fixed:
        -   PRB1847482 ACC-L: Multiline not working with current Filebeat config.
        -   PRB1839552 Grab windows logs not functioning as expected.
    -   Note: This version certified on Zurich family version.
-   **Version 3.8.9 - March 2025**
    -   Fixed:
        -   PRB1847482 - ACC-L: Multiline not working with current Filebeat config.
        -   PRB1839552 - Grab windows logs not functioning as expected.
-   **Version 3.8.7 - January 2025**
    -   Security improvements
    -   Bug fixes
-   **Version 3.8.6 - November 2024**
    -   Security improvements
    -   Bug fixes
-   **Version 3.8.3 - August 2024**
    -   Changed: Updated supported versions of dependencies to the latest stable version for all underlying technologies
    -   Fixed:
        -   .yml tab-formatting issue
        -   Other minor bug fixes
-   **Version 3.6.4 - May 2024**

    Problem and security fixes.

-   **Version 3.6.2 - February 2024**

    Added support for the Washington DC release.

-   **Version 3.6.1 - January 2024**
    -   New Features:
        -   Changed log path configuration with added support for the environment variables on both Linux and Windows
        -   Introduced a new out-of-the-box policy for Oracle WebLogic, compatible with both Windows and Linux.
-   **Version 3.5.0 - June 2023**

    No significant updates.

-   **Version 3.4.0 - May 2023**

    No significant updates.

-   **Version 3.3.10 - November 2022**
    -   New: A guided setup that assists you with planning the rollout of the Agent Client Collector and performing the basic configuration to go live.
    -   Bug fixes
-   **Version 3.2.2 - October 2022**
    -   New:
        -   Guided Setup available. We encourage you to use our new guided setup which walks you through the ACC-L configuration steps.
        -   Dynamic support for Filebeat parameters using ACC-L.
    -   Fixed:
        -   Multiline configuration issue.
        -   Stream MSSQL ERRORLOG with ACC-L streaming wrong UTF.
        -   Security fixes.
-   **Version 3.2.0 - August 2022**
    -   New: Dynamic support for Filebeat parameters using the ACC-L
    -   Fixed:
        -   Multiline configuration issue
        -   Stream MSSQL ERRORLOG with ACC-L streaming wrong UTF
        -   Security fixes
-   **Version 3.1.0 - December 2021**
    -   New:
        -   Support log collection of applications installed on Windows
        -   Support log extraction for Windows event logs with Winlogbeat
        -   ACC Log Analytics setup: One-click setup of ACC data inputs and ACC extensions from MID Server form
        -   Duplicate preprocessor and mapping scripts for ACC data inputs
    -   Fixed: Navigate to Log Policies from menu or ACC data input
-   **Version 3.0.0 - September 2021**

    The ITOM Agent Client Collector Log Analytics \(ACC-L\) solution seamlessly integrates Health Log Analytics \(HLA\) with Agent Client Collector \(ACC\) and accelerates time to value for ITOM Health customers. Once installed together with Agent Client Colector Monitoring \(ACC-M\), it acts as as the Unified AIOps Agent - a single agent that collects metrics, events and logs.


