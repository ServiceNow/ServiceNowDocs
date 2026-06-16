---
title: Agent Client Collector for Visibility Content release notes
description: Version history for the Agent Client Collector for Visibility Content on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-acc-visibility-content.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Agent Client Collector for Visibility Content release notes

Version history for the Agent Client Collector for Visibility Content on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.9.0 - June 2026**
    -   New: Software License Key Discovery Framework: Enables users to discover and manage software license keys from Windows registry locations.
    -   File-based Discovery Enhancements: Discover Files inside ZIP/JAR files through File-based Discovery \(Agent-based\).
-   **Version 1.8.0 - May 2026**
    -   New: SWID Tag Discovery for Windows, Linux and MAC agents
    -   Fixed: Performance improvements for ACC based File Based Discovery
-   **Version 1.7.0 - April 2026**
    -   Backend support to collect SaaS URL data from the endpoint browser via the browser extension.
    -   The administrator can select to monitor only the configured URL or full monitoring \(all URLs\).
-   **Version 1.6.0 - March 2026**
    -   New: ACC-VC now supports discovery of One-Drive editions for Windows along with MS SQL and Adobe.
    -   Changed: Enhance efficiency in File-based Discovery by using separate policies to gather information for SAM and File management.
    -   Fixed: Successfully populate install location for software in the software installation table.FBD to support larger payload through chunking capability.
-   **Version 1.5.0 - December 2025**
    -   New:
        -   Perform SWID Tag discovery via ACC-VC \(Agent based approach\)
        -   Discover Certificates using ACC-VC on all available server ports
    -   Fixed: File based Discovery supports larger payload via chunking capability
-   **Version 1.4.2 - September 2025**
    -   Fixed issues with storage devices, network adapters, and file systems on specific infrastructure.
    -   Fixed issues with scanning symlinks during file-based discovery.
    -   Fixed issues with scan paths with special character file-based discovery.
    -   Fixed issues with discovering IPv6 network adapters.
-   **Version 1.4.0 - August 2025**
    -   New:
        -   Discover Certificates via ACC-VC on configured Ports
        -   File-based discovery is now supported on MacOS
        -   Monitor SaaS usage using a browser extension \(in addition to background scripts\)
    -   Fixed:
        -   File-based discovery improvement allows discovery to restart from last checkpoint on Windows devices
        -   Total Usage Data is now captured through ACC-VC for Windows devices
-   **Version 1.3.1 - June 2025**
    -   Changed:
        -   Activated the "VISC Get application metric" policy by default.
        -   Removed sub-class restriction during application creation. Now, SaaS application creation supports cmdb\_ci\_service\_auto and its subclasses.
    -   Fixed:
        -   Made VISC Get application metric policy active by default.
        -   Sam integration api to return DEX applications as well by default.
-   **Version 1.3.0 - May 2025**
    -   New:
        -   Allows Oracle Java Certification discovery
        -   Now supports the discovery of SQL Server components and their editions
    -   Fixed:
        -   Agent File-Based Discovery was Improved
        -   Fixed minor product bugs
-   **Version 1.1.1 - March 2025**

    Fixed a bug related to the population of the Edition field for Adobe Acrobat software records.

-   **Version 1.1.0 - February 2025**
    -   New: File based discovery support via agent
    -   Fixed:
        -   Performance improvement for "SAM - Update Software Total Usage Metric" job
        -   Fixed a few product bugs
-   **Version 1.0.4 - November 2024**

    Fixed a few product bugs.

-   **Version 1.0.2 - May 2024**

    Fixed a few product issues.

-   **Version 1.0.0 - February 2024**

    Core store application to support Discovery and Digital Experience Management customers.


**Parent Topic:**[ServiceNow Store - IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom.md)

