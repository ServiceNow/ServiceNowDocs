---
title: SBOM Response release notes
description: Version history for the Vulnerability Response Data Model for SBOM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-SBOM-response.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# SBOM Response release notes

Version history for the Vulnerability Response Data Model for SBOM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.5.3 - June 2026 \(USEM\)**
    -   The following enhancements and changes support internal security directives:
        -   Enhancements to the SBOM Response plugin to align with ServiceNow Platform Security guidance.
        -   Read-only dictionary fields for SBOM Response tables.
        -   Fix script renamed to a per-plugin name to prevent update set conflicts with other SBOM plugins.
    -   Fixed: Vendor SBOM upload reliability — Resolved an error that occurred when uploading vendor-supplied SBOMs.
-   **Version 6.5.2 - April 2026**

    Fixed: UI action buttons on the BOM entity details page are visible regardless of your selected language preference.

-   **Version 6.4.1 - December 2025**
    -   Fixed:
        -   Fixed an issue where titles in the All BOM Entity widget wrapped vertically instead of truncating properly when the page was resized.
        -   Fixed multiple accessibility issues across the SBOM workspace, including heading structure, content alignment, and layout behaviour at various screen sizes.
-   **Version 6.3.2 - September 2025**

    Fixed: Resolved vulnerability visibility issue by removing redundant active status filter from component vulnerabilities relationship. As a result, vulnerabilities are now visible in the vulnerabilities tab.

-   **Version 6.3.1 - August 2025**
    -   Fixed:
        -   Fixed an issue in the OSVAPIIntegration script where the integration failed with an error. OSV API that lacked the expected results key. The script now safely checks for the existence of results before accessing it, ensuring the integration handles empty or malformed responses gracefully without breaking.
        -   Fixed a display issue in the component widget where the count was incorrectly showing as 0 in the summary view. Upon investigation, it was determined that while the drill-down view displayed the correct component count, the main widget consistently showed zero. This has been resolved, and the component widget now accurately reflects the true component count at all levels of the interface.
-   **Version 6.2.2 - June 2025**

    Fixed an issue in OSV integration where conflicts arose with existing NVD entries due to CVE IDs in the payload, resulting in broken component-vulnerability links. The integration now handles such cases to prevent duplicate or invalid records. Improvements to deps.dev Integration - Optimized the sorting logic for package version lists and replaced the onComplete script with a Business Rule triggered on version updates, improving performance and accuracy in stale/abandoned package detection. OSV Integration Optimization - Removed unnecessary caching to reduce memory usage and prevent potential out-of-memory issues during large data processing. Business Application Population Enhancement - Now populating business\_application on AVIT and app release records only when the associated component has a business application, aligning with customer requirements.

-   **Version 6.1.0 - May 2025**

    Fixed an issue where AVI counts on components were not updating after AVIT creation via SBOM AVI rules.

-   **Version 6.0.1 - February 2025**
    -   New:
        -   Improvements to the Software Bill of Materials Workspace permit you to delete multiple BOM entity records and their related components from the Home \(landing\) page with bulk edit.
        -   Any Application Vulnerable Items \(AVIT\)s that are associated with the BOM entities you delete automatically transition to 'Closed'.
-   **Version 5.0.5 - December 2024**

    Minor fixes for this release.

-   **Version 5.0.3 - November 2024**
    -   New:
        -   Improvements to the SBOM Response application to help you determine your over-all license compliance and risk exposure to the open-source and vendor-supplied software components you use in your application development:
            -   View all the licenses that are used in your organization in the License administration module.
            -   Classify existing licenses as: "Permitted", "Restricted", "Banned", or "Unclassified", and create new licenses.
            -   For unassigned or missing licenses, you can manually assign licenses to components used by your applications.
-   **Version 4.0.5 - October 2024**
    -   New:
        -   'Closed' AVITs will not transition to 'Open' if AVITs have the substates: 'Mitigation Control in Place', 'Not Affected', or 'False Positive'.
        -   The sn\_sbom\_resp.reopen\_avits\_if\_detected system property for this feature is activated by default.
        -   Set the value of the sn\_sbom\_resp.reopen\_avits\_if\_detected system property to 'false' if you do not want 'Closed' AVITs to reopen automatically.
-   **Version 4.0.3 - August 2024**

    New: View components that are identified as stale or abandoned as Non-compliant' in the Policy as Code Engine \(PaCE\) interface that is available in the SBOM Workspace.

-   **Version 3.3.0 - June 2024**

    New: Data Model changes to accommodate the Vulnerability Intelligence integration.

-   **Version 3.2.3 - May 2024**
    -   New:
        -   Upload SBOM files for the CycloneDX and SPDX standards.
        -   XML and JSON formats are supported for CycloneDX for versions up to and including v1.4.
        -   JSON format is supported for SPDX for versions up to and including v2.3.
        -   Performance enhancements in the SBOM Workspace for the BOM Entities and Components pages. You might experience faster load times for the Home and Components modules in the SBOM Workspace.
-   **Version 3.1.3 - February 2024**
    -   New:
        -   Updated Overview tab for the application vulnerable item \(AVIT\) record enables you to view the following data:
            -   Details.
            -   Associated vulnerability.
            -   SBOM component.
            -   Discovered application.
        -   Added the Fixed versions related list on the AVIT record.
    -   Changed:
        -   Enhancements to integration processing for OSV.dev and Deps.dev.
        -   Condition builder on the AVIT creation rules form that enables you to add rule conditions for applications, vulnerabilities, business application, and components.
    -   Removed: Deactivated remediation task rules for SBOM AVITs. You can activate this feature for SBOM AVITs with a system property.
-   **Version 3.0.3 - November 2023**
    -   New:
        -   Supports the Deps.dev and OSV.dev integrations that are included with the SBOM Response application that you can run on-demand.
            -   OSV.dev provides vulnerability intelligence information for a given version of a package or library.
            -   Deps.dev provides a version list for a given package or library and package intelligence for Stale and Abondoned components.
        -   Supports the third-party Snyk Vulnerability Insights integration that can provide you with information for how to fix components with vulnerabilities. This integration is not included with SBOM Response but is available in the ServiceNow Store.
        -   Uploaded data extracted from these vulnerability intelligence integrations is dispalyed on the SBOM Response workspace dashboard and in the list and form views of the components.
            -   View components that are 'Stale' and 'Abandoned'.
            -   View the current and latest versions of the BOM Components.
            -   View Common Vulnerabilities and Exposures \(CVE\) and Common Weakness Enumeration \(CWE\) data for components broken down by severity.
-   **Version 2.0.6 - September 2023**
    -   New:
        -   The data model is updated so it supports the Vulnerability Intelligence use case.
        -   Discovered application and SBOM component are two new fields displayed on the AVI form.
        -   Mark as false positive and Request exception are supported on AVIs in the SBOM Workspace.
    -   Changed:
        -   Fewer fields are supported in the condition builder for AVI creation rules in the SBOM Workspace.
-   **Version 2.0.5 - August 2023**

    Initial release: SBOM Response provides you with visibility into the risks with using open-source components in your organization. You can respond to identified risks with the workflow and automation capabilities of the NOW Platform.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

