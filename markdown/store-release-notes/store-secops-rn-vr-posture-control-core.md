---
title: Security Posture Control core release notes
description: Version history for the Vulnerability Response Security Posture Control application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-posture-control-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Security Posture Control core release notes

Version history for the Vulnerability Response Security Posture Control application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.1.0 - June 2026**
    -   New:
        -   Configuration Compliance is now a supported dependency for Security Posture Control Core, expanding the policy framework for compliance-driven asset evaluation.
        -   Enhancements to the asset profile framework to improve coverage for service graph connector-sourced data.
    -   Fixed: Stability and performance improvements in policy execution and asset matching.
-   **Version 7.0.2 - April 2026**

    Fixed: Inconsistent behaviors in multi-tenant environments that resulted in support for only a subset of the application's tables that are included the Domain column. Domain separation is now fully supported in Mitigation Controls Monitoring.

-   **Version 7.0.1 - December 2025**
    -   New: "last discovered" from the cmdb\_multisource\_data table is available in the policy condition builder.
    -   Fixed:
        -   Aggregated host name is correctly mapped and populated from multi-source data.
        -   Reported by count is no longer undefined for software assets in the Findings form UI.
-   **Version 6.2.0 - August 2025**
    -   New:
        -   Get insights into your overall security posture and configuration gaps in your security tools using new policies and asset proﬁles that are included with the Security Posture Control application. Activate these asset proﬁles and policies in the Security Posture Control workspace so that you can identify gaps in configuration or coverage of the following tools:
            -   CrowdStrike
            -   Microsoft Intune, Defender, and SCCM
            -   HCL Big Fix
            -   Qualys
            -   Rapid7
    -   Fixed:
        -   The canvas error no longer displays prior to showing results for asset searches.
        -   If you clone a policy, any associations to asset profiles for that policy are also cloned.
        -   Dates for the next scheduled job are displayed correctly when you create policies.
-   **Version 6.1.2 - May 2025**
    -   New:
        -   Asset profiles
            -   Create and define asset profiles to monitor different categories of devices with your SPC policies.
            -   Asset profiles support three Connection types:
                -   With CMDB metadata - Collection of CMDB CI properties such as Host name, OS, OS version, First and Last seen, for example, or connections that have network adaptors or installed software.
                -   With aggregated data - Collection of properties with aggregated values as reported by different sources for a given asset.
                -   From CI class - Collection of CI classes that includes Computer, Server, Virtual Machine Instance, and other classes. You can use this condition and connection type to define asset profiles that are based on specific CMDB property values.
            -   Incorporate your asset profiles into your policies so you can run policies for specific types of assets.
            -   Filter insights in the Configured Insights dashboard so they are based on your asset profiles.
        -   Added support for AWS WAF in the SPC Policies.
    -   Fixed: Added support for the new service graph connector released by Tenable.
    -   Changed: Custom insights are renamed to configurable insights.
-   **Version 6.0.8 - March 2025**
    -   Fixed:
        -   An issue with tool gap queries for ESX virtual machine \(vm\) server policies that caused policies to return inaccurate results.
        -   Duplicate records in the asset cache for cloud vm server mappings that caused incorrect results for policies.
-   **Version 4.6.1 - February 2025**
    -   Fixed:
        -   Veracode Software Bill of Materials \(SBOM\) Integration imports SBOM documents.
        -   Tag values are included in the description when parsing applications from Veracode.
-   **Version 5.1.6 - December 2024**

    Fixed: The not within n days operator now works fine with empty values in policy execution and asset search.

-   **Version 4.0.0 - August 2024**
    -   Changed:
        -   Added support for the "With aggregated data" Connection to ensure that your policy matches assets that have slight variations in reported data.
        -   Enhancements to policy audits ensure that retired assets are not evaluated by activated policies.
        -   Merged the cloud virtual machine asset type with the hardware asset type to simplify experience.
        -   Added support for the "from ci class" connection in the asset search.
        -   The 'View assets' UI action is displayed in policies if there are no findings.
    -   Fixed:
        -   Child policies for base policies with the connections, 'from CI class', 'cloud metadata', and 'has ports exposed to internet' are activated as expected.
        -   Changes in exclusion policies of base policies are reflected on child policies.
-   **Version 3.0.4 - June 2024**
    -   Fixed:
        -   Deleted and inactive policies are not supported as base and exclusion policies.
        -   Inactive child policies are shown as dependencies as expected if a base policy is being deactivated.
        -   Policies with exclusions generate findings as expected.
        -   The 'Software' asset type shows only sources that report software in the policy builder if selected.
        -   Group rules and remediation target rules run as expected for the Security Posture Control policies.
    -   Changed: The label from 'Service Graph Connectors' to 'Asset Sources' to support Discovery as a data source.
-   **Version 3.0.2 - May 2024**
    -   New:
        -   UI actions permit you to save changes, publish changes, and exit edit mode from policies.
        -   If you edit, save, and publish activated policies, versions are tracked and version numbers are displayed on the policy records and their related test results.
        -   If you publish a new version of a policy and deactivate or delete a policy, you have the option to close its existing related test results \(findings\). Test result and remediation task states transition in accordance with the state transition processes of the Configuration Compliance application.
        -   Policy improvements:
            -   Support for the top-level OR condition permits you to monitor diverse types of assets from a single policy.
            -   Software is supported as a top level entity type that can be queried from Security Posture Control. This entity permits you to look for any discrepancies that exist between the installed software reported by your vulnerability scanner products and the software reported by scanners and already accounted for in Software Asset Management \(SAM\) and other ServiceNow products.
-   **Version 2.0.4 - March 2024**

    Fixed: A policy's draft content is not erased when you save its name and metadata details.

-   **Version 2.0.0 - February 2024**
    -   New:
        -   Search for assets and convert your asset search criteria into policies.
        -   Configure your findings or insights for your policies.
        -   Refine the results for your matching assets by creating new policies that are based on existing policies.
        -   Filter assets in your policies by configuration item \(CI\) classes such as cmdb\_server, cmdb\_ci\_computer, and other classes that are supported by service graph connectors.
        -   Query assets based on common CMDB CI metadata such as OS, OS Version, Hostname, Software, and other properties.
        -   Choose from a wide range of supported service graph connectors to import security data and identify high-risk combinations.
-   **Version 1.0.0 - August 2023**

    Initial release: The core framework for Security Posture Control provides foundational features such as the policy builder and the workspace to view and manage findings.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

