---
title: Threat Intelligence release notes
description: Version history for the Security Operations Threat Intelligence app on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-threat-intel.html
release: store
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Threat Intelligence release notes

Version history for the Security Operations Threat Intelligence app on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 13.4.4 - February 2026**

    Changed: Updated the dependent application to the latest version.

-   **Version 13.4.3 - January 2026**
    -   New:
        -   Added automated ingestion of MITRE DEFEND framework data with improved data quality and consistency, keeping your threat intelligence up-to-date.
        -   Added graphical visualizations showing relationships between DEFEND techniques, entities, and interactions in the Workspace for faster threat analysis
-   **Version 13.4.0 - December 2025**

    Fixed: Security issues related to granular admin roles.

-   **Version 13.3.2 - June 2025**

    Fixed: A security issue related to ACL where users could bypass access control restrictions through the Create New Security Case functionality.

-   **Version 13.3.1 - May 2025**
    -   New:
        -   Extending the existing CVE TID mapping.
            -   Introduced support for the extended CVE-TID mappings via a static CSV file. The CSV file contains predefined CVE-TID mapping records.
            -   Upon upgrade or installation of the plugin, these static mappings will be automatically imported into the system.
-   **Version 13.3.0 - November 2024**

    Changed: Migrated workflows to Flow Designer flows.

-   **Version 13.2.0 - August 2024**

    Fixed: Broken MITRE dashboard links from the Overview tab is now fixed.

-   **Version 13.1.9 - May 2024**

    Changed: Old dashboards are deprecated.

-   **Version 13.1.8 - February 2024**

    New: Introduced Next Experience Dashboard Migration - MITRE \(6 Dashboards - Tokyo based\).

-   **Version 13.1.7 - August 2023**

    Fixed: An ACL Bypass issue is fixed for the add\_custom\_annotation\_popup UI Page.

-   **Version 13.1.6 - May 2023**

    Fixed: Updates to the VirusTotal API key.

-   **Version 13.1.4 - April 2023**

    Changed: Updated to support this application on the Security Incident Response workspace.

-   **Version 13.1.1 - November 2022**
    -   New: Introducing a new module for threat lookup finding calculator, which calculates the findings based on the responses received.
    -   Fixed: Dark theme and accessibility issues.
-   **Version 13.1.0 - June 2022**

    Fixed: Security Bugs

-   **Version 13.0.0 - December 2021**
    -   New: Introduced new features related to MITRE ATT&amp;CK framework which improves the ServiceNow AI Platform SOAR capabilities that enable proactive analysis, response, and reporting on threats across the security infrastructure.
    -   Changed: Updated some of the existing features related to MITRE ATT&amp;CK.
-   **Version 12.0.4 - June 2021**

    Fixed: The hash lookup on observables is now working for the Metadefender integration.

-   **Version 12.0.3 - March 2021**

    Fixed: TAXII end point is updated to MITRE GitHub to optimize the load on MITRE servers. MITRE collections are now pre-populated with the Threat Intelligence Core app.

-   **Version 12.0.0 - December 2020**
    -   New: Introduced the MITRE ATT&amp;CK framework which improves the ServiceNow AI Platform SOAR capabilities that enable proactive analysis, response, and reporting on threats across the security infrastructure.
    -   Changed: As part of inclusive language initiative, allow list and deny list tags are replaced with allow list and deny list respectively.
-   **Version 11.0.2 - October 2020**
    -   Changed:
        -   The integration now supports OAUTH2 authentication. This update requires the user to enter the API Client ID and the API Client Secret to authenticate and complete the configuration.
-   **Version 11.0.1 - September 2020**
    -   New:
        -   Updated Threat Intelligence to support STIX 2.0, STIX 2.1 standards
        -   Modules for STIX 2.0, STIX 2.1 objects and relationships
-   **Version 10.3.3 - June 2020**

    Fixed: ACL fixes related to Security Case Management and Security Annotations.

-   **Version 8.0.9 - July 2019**

    New: Recertified for New York


