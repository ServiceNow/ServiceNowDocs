---
title: Security Integration Framework release notes
description: Version history for the Security Integration Framework on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-integration-framework.html
release: store
topic_type: reference
last_updated: "2026-04-09"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Security Operations Shared apps for release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Integration Framework release notes

Version history for the Security Integration Framework on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 13.12.3 - April 2026**
    -   New: Administrators can now configure a Configuration Item \(CI\) lookup strategy at the individual integration level, overriding the global system property. A new CI Lookup Strategy field has been added to the integration form with three options: Use System Property \(default, preserves existing behavior using the global sn\_vul.use\_product\_model property\), Force CI Lookup \(always creates configuration items for scanned applications — required for integrations such as Tenable WAS\), and Force Product Model \(always creates a Product Model\). All existing integrations default to Use System Property, ensuring no errors occur as a result of an upgrade.
    -   Fixed:
        -   Resolved an issue where the vulnerability integration related list appeared twice in the admin section of each integration, causing duplicate tabs to display in the integration implementation configuration.
        -   Resolved an issue where users in Global scope could not configure or save credentials for integrations. Configuration attempts would silently fail with no indication of the problem. A scope warning is now displayed, guiding users to switch to the correct application scope before configuring the integration.
-   **Version 13.12.1 - December 2025**

    Fixed: An issue where installing the Mitigation Controls Monitoring application unintentionally removed choice values for the integration\_type field in the sn\_sec\_int\_integration table.

-   **Version 13.11.3 - August 2025**

    Fixed: Resolved an issue where the integration instance form related list was not displaying details specific to the integration / scanner.

-   **Version 13.10.8 - June 2025**

    Fixed: Fixed an ACL vulnerability for privileged operations with proper authentication checks.

-   **Version 6.0.6 - February 2025**
    -   New:
        -   The Service Graph Connector for Netskope is supported.
        -   The SentinelOne Integration for mitigation controls monitoring is supported.
    -   Fixed:
        -   The child policy execution relies on base policy results. You might see performance improvement.
        -   The default set of supported classes to the descendants of: 'Computer', 'Netgear', and 'Unclassed hardware'.
-   **Version 13.10.6 - February 2025**

    Changed: Added an additional\_integration\_types column to the "Third Party Integrations" table to specify the additional integration type information for an integration.

-   **Version 13.11.0 - November 2024**

    No new features or updates included with this version.

-   **Version 13.10.3 - May 2024**

    Minor fixes for this release.

-   **Version 13.9.2 - February 2024**

    Changes to support Invicti and Security Simulation Phishing integration.

-   **Version 13.8.0 - December 2023**

    New: Minor changes to support "First.orgExploit Prediction Scoring System \(EPSS\) Integration".

-   **Version 13.6.1 - November 2023**
    -   Changed:
        -   Removed the one 'Triaging in ServiceNow' option on the integration configuration pages and added the following two options to manage imported data using ServiceNow workflows:
            -   'Manage exceptions in ServiceNow' and 'Manage false positives in ServiceNow'.
            -   By default, these options are set to 'true' but can be changed.
-   **Version 13.5.0 - August 2023**

    Changed: Version 13.5.0 certified for Vancouver, Utah, and Tokyo.

-   **Version 13.4.1 - May 2023**

    New: Added capabilities to create discovered items, vulnerable items, and detections at the parent instance level for an instance.

-   **Version 13.3.0 - November 2022**

    Minor fixes for this release.

-   **Version 13.2.2 - August 2022**

    New: Added changes to support manual ingestion in Vulnerability Response and other new features.

-   **Version 13.1.3 - March 2022**
    -   New:
        -   Shipped new integration records for the following applications and integrations:
            -   The Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute in the Vulnerability Response and Configuration Compliance for Containers application.
            -   Fortify on Demand in Application Vulnerability Response.
            -   HCL BigFix and Microsoft SCCM patch orchestration integrations in Vulnerability Response.
-   **Version 13.0.2 - February 2022**

    No new features or updates are included with this version. This version ensures that features from the last release are compatible with the San Diego family release.

-   **Version 12.2.1 - October 2021**

    Changed: Added the Operational Technology Vulnerability Integration \(OTVUL\) option in the Integration Type \(integration\_type\) column of Third Party Integration table \(sn\_sec\_int\_integration\), in order to support the Operational Technology \(OT\) Vulnerability Integration

-   **Version 12.1.3 - June 2021**

    Fixed: Minor fixes.

-   **Version 12.0.1 - February 2021**

    New: Added a new Vulnerability Response Integration with the National Vulnerability Database \(NVD\) to import data from the NIST National Vulnerability Database.

-   **Version 11.1.3 - December 2020**

    Changed: With Key Management Framework plugin, developers will have an ability to manage keys used for Password2 fields through crypto module definition.

-   **Version 11.1.0 - November 2020**

    This is a dependency app for Vulnerability Response and Security Incident Response applications.

-   **Version 11.0.2 - October 2020**

    This is the Dependency App for Vulnerability Response and Security Incident Response applications.

-   **Version 10.3.0 - June 2020**

    This is the dependency app for Vulnerability Response and Security Incident Response applications.

-   **Version 9.0.3 - November 2019**

    This is the Dependency App for Vulnerability Response and Security Incident Response applications.

-   **Version 8.0.8 - June 2019**

    This is the Dependency App for Vulnerability Response and Security Incident Response applications.


