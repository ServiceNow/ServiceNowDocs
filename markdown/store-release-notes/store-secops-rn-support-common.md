---
title: Security Support Common release notes
description: Version history for the Security Support Common on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-support-common.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Support Common release notes

Version history for the Security Support Common on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 30.4.1 - June 2026**
    -   New:
        -   Added new granular roles and access controls to improve access management and maintain consistent permissions across integrated modules.
        -   Added OWASP mapping support in the security common application, enabling posture rules to reference OWASP items in a structured way.
    -   Fixed:
        -   Reduced unnecessary error alerts by changing unknown encoded URL log messages to informational or warning messages.
        -   Fixed an issue where background job cancellation notes could appear blank in non-English sessions.
        -   Fixed an issue where remediation tasks were not visible when the UI language for non-English sessions.
-   **Version 30.3.3 - April 2026**

    New: Background job configurations now include a priority field that controls the order in which jobs are processed. When multiple jobs share the same priority level, they are processed in the order they were created.

-   **Version 13.25.3 - March 2026**
    -   Fixed:
        -   The Transform Phishing Email to the Security Incident flow remaining in the state, "In Progress" when the \[glide.email.forward\_subject\_prefix\] system property was misconfigured \(null value or trailing commas\).
        -   The "Sightings search source" field was not visible on the \[sn\_sec\_cmn\_sightings\_search\_config\] table creation form when the IBM QRadar Integration for Security Operations application is installed.
        -   A localization issue where the cancellation notes in the \[sn\_sec\_cmn\_background\_job\] Background Job records were not visible in non-English sessions due to missing \[sys\_translated\_text\] records.
        -   The "Field" column in Duplication Action module records appeared empty after installation in different instances due to sys\_id-based dictionary references.
-   **Version 30.2.3 - January 2026**

    Fixed: Minor enhancements.

-   **Version 13.14.0 - August 2024**
    -   Changed:
        -   Migrated Threat lookup workflow to sub-flow
        -   Migrated Enrichment workflow to sub-flow.
-   **Version 13.13.4 - May 2024**
    -   Fixed ACL issues.
    -   OS/Netbios will be updated on Discovered Item on change of payload\(source\_data\).
-   **Version 13.12.5 - March 2024**

    Fixed: On the Run Additional Actions modal, now the Comment field is set as a mandatory field \(to support Microsoft Defender for Endpoint\).

-   **Version 13.12.2 - February 2024**

    Changes to support risk reduction by Compensating Controls feature.

-   **Version 13.11.1 - January 2024**

    Fixed: Attachments on the table sn\_sec\_cmn\_integration\_process are failing because of the Anti-virus scan.

-   **Version 13.11.0 - December 2023**

    No existing features were impacted with this version.

-   **Version 13.9.2 - November 2023**
    -   New:
        -   A configuration which redirects the creation of unclassed assets.
        -   A fix script which determines the default CMDB class mapping.
-   **Version 13.7.2 - August 2023**
    -   Changed: The MS Defender Capabilities Isolate Host and Run Antivirus scandialogue boxes' Typefield is now a drop-down instead of a text.
    -   Fixed: Invalid query in the 'Enrichment data mapping' field, sys\_relationship.
-   **Version 13.6.6 - June 2023**

    Fixed: For Advanced Risk Rule Calculators, the resulting risk score information in the sample scenarios was being populated with incomplete information. This issue has been fixed. The resulting risk score information is now correctly populated.

-   **Version 13.6.5 - May 2023**
    -   Fixed:
        -   Discovered items for cloud resources are created in an unmatched state if there are no CIs found by the lookup rules.
        -   The Dependent field of the Reference Record column in the Threat Lookup Result Table \(sn\_sec\_cmn\_enrichment\_data\_base\) is configured as expected.
        -   'Assignable by' or 'Application Administrator' should not be used with roles when the scoped application has 'Application administration' set to 'false'.
        -   Vancouver Directives - Implemented Table Cleaner rules for ServiceNow AI Platform tables from the Security Incident Response application that are used frequently.
-   **Version 13.5.2 - February 2023**
    -   New: Added the column 'Matching type' to the discovered items table to understand whether the discovered item has been matched by IRE or CI lookup rules, or created by IRE or VR.
    -   Changed: Framework updates in Security Support Common can now be used by Configuration Compliance, Application Vulnerability Response, and Container Vulnerability Response.
    -   Fixed: Reapply CI lookup rule is now working on assets with the Cloud asset category.
-   **Version 13.4.4 - November 2022**
    -   New: Added a capability to refresh tags on cloud assets from CMDB on a daily basis.
    -   Changed:
        -   \[Security support common\] Added logic to migrate the Threat lookup trigger to Capability Framework v2.
        -   Added the ability to ignore unclassed hardware and unmatched configuration items during Lookup Rules execution.
    -   Fixed:
        -   Potential memory leak risk from OOTB 'FilterGroupUtil. \_getCisForSubnet' function in VR framework
-   **Version 13.3.3 - August 2022**

    New: Changes for supporting new features in Vulnerability Response. Seeded regions for cloud resources.

-   **Version 13.2.0 - May 2022**

    Changed: Updates like the addition of new attributes, scripts to support cloud assets, etc.

-   **Version 13.1.1 - March 2022**
    -   New:
        -   Added support for making classification rules generic. Previously only available for the Vulnerability Entry \[sn\_vul\_entry\] table, this feature can be enabled on any table in the Vulnerability Response application and within the scope of its dependent applications.
        -   Updated the exception management feature so it works with the Application Vulnerability Response and the Vulnerability Response and Configuration Compliance for Containers applications.
-   **Version 13.0.1 - February 2022**

    No new features or updates are included with this version. This version ensures that features from the last release are compatible with the San Diego family release.

-   **Version 12.5.1 - October 2021**

    New: Data model to support multi-level approval configuration for Vulnerability Response exception management.

-   **Version 12.4.3 - August 2021**
    -   New:
        -   Added a generic flow action URL decoder which support proof point and safelink encoded URLs.
        -   Modified User Reported Phishing functionality to decode URLs before saving them as observables.
-   **Version 12.2.4 - June 2021**
    -   New:
        -   Changes to the common background job framework ensure that jobs are executed in a resource-optimized manner.
        -   With this updated job framework, you can now configure the following settings:
            -   Define job concurrency by limiting the number of jobs that can run at the same time.
            -   Determine the amount of data \(number of items\) you import with specific jobs.
            -   Cancel jobs.
            -   Control the total number of background jobs that are processed in parallel, regardless of the job type.
    -   Fixed:
        -   List support in capability framework version 2. Replaced legacy password2 with KMF field.
-   **Version 12.0.1 - February 2021**

    Minor fixes.

-   **Version 11.1.5 - December 2020**

    Changed: As part of the inclusive language initiative, allow list and deny list are replaced with allow list and deny list respectively.

-   **Version 11.1.2 - November 2020**

    This is a dependency app for Vulnerability Response and Security Incident Response applications.

-   **Version 11.0.1 - October 2020**

    New: This is the Dependency App for Vulnerability Response and Security Incident Response applications.

-   **Version 10.5.0 - September 2020**

    Minor fixes related to User Reported Phishing

-   **Version 10.0.3 - April 2020**

    Fixed: Dispatch actions updated for compatibility with Security Incident Response UI

-   **Version 10.0.0 - March 2020**

    Changed: Updates to support the latest versions of Security Incident Response and Vulnerability Response Applications

-   **Version 9.0.0 - November 2019**
    -   New: Dependency and Util code for Security Incident Response and Vulnerability Response November release
    -   Fixed: PRB fixes post July Q3 release
-   **Version 8.0.10 - June 2019**

    Refer to Vulnerability Response release notes for product changes and updates in the Madrid release.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

