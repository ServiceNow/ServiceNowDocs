---
title: Vulnerability Emergency Response release notes
description: Version history for the Vulnerability Emergency Response application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-emergency-response.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Emergency Response release notes

Version history for the Vulnerability Emergency Response application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.0.1 - February 2024**
    -   Changed:
        -   Consideration of secondary Common Vulnerabilities and Exposures \(CVEs\) for scanner ingested vulnerabilities during the assessment.
        -   Major Security Incident Management \(MSIM\) link is displayed on the vulnerable items \(VIT\)/ application vulnerable items \(AVIT\) in the Vulnerability Response \(VR\) workspaces.
        -   Assessment Vulnerabilities on CVEs are shown in the VR workspaces.
        -   The auto-flush rule is shipped to delete all the related data for Vulnerability Assessment if was closed for 6 months. Earlier, it was shipped in the base system as inactive.
    -   Fixed:
        -   Unlinking Vulnerability Assessment from Major Security Incident workspace.
        -   Fixed the Scanned Applications widget to show the count from all CVEs.
        -   Minor updates and usability issues.
-   **Version 2.0.5 - December 2023**

    Fixed: The Vulnerability Assessment Calculators can be deleted only by the user with the sn\_vul\_analyst.read\_risk\_score\_configuration role.

-   **Version 2.0.3 - November 2023**
    -   New:
        -   Vulnerability Crisis Management: A complete workflow to handle vulnerability crisis events with the following capabilities:
            -   Identify vulnerable configuration items \(CIs\) by correlating critical vulnerabilities with software installations inventory from Software Asset Management \(SAM\), Software Bill of Materials Inventory \(SBOM\), scanner-reported vulnerabilities and Configuration Management Database \(CMDB\).
            -   Generate vulnerable items for remediation based on assessment results, streamlining the remediation process.
            -   Initiate a major security incident response, ensuring swift and coordinated action.
            -   Engage and collaborate with teams across the organization, facilitating a unified response to vulnerabilities.
            -   Provide regular status reports to affected teams, partner teams, and leadership, maintaining transparency throughout the crisis.
        -   Exposure Assessment: Updated assessments with the normalized inventory of Software Asset Management \(SAM\).
-   **Version 1.0.2 - October 2023**
    -   Fixed: Previously, the form view of records were not loading in the Vulnerability Manager and IT Remediation Owner Workspaces in the instances with the platform versions, Utah patch 0 - Utah patch 5. This issue has been fixed. The records will now load in form view in all the supported platform versions.
-   **Version 1.0.1 - August 2023 \(Vancouver\)**

    New: The new Vulnerability Analyst workspace contains the Exposure Assessment module. It is used for:

    -   Automatic assessments of CISA KEV
    -   CVE or CPE-based assessment
    -   Software-based \(Vendor, Product,Version, and Edition\) assessment for zero-day vulnerabilities

