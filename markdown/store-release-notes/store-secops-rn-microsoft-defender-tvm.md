---
title: Vulnerability Response Integration with Microsoft Threat and Vulnerability Management release notes
description: Version history for the Security Operations Vulnerability Response Integration with Microsoft Threat and Vulnerability Management on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-microsoft-defender-tvm.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with Microsoft Threat and Vulnerability Management release notes

Version history for the Security Operations Vulnerability Response Integration with Microsoft Threat and Vulnerability Management on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 31.3.0 - June 2026 \(USEM\)**
    -   Changed:
        -   Migrated query access control list \(ACL\) definitions to the standard product codebase in Vulnerability Intelligence, improving long-term maintainability and ensuring consistent access control enforcement.
        -   Enforced read-only field security restrictions across multiple tables to meet platform security directive requirements and comply with updated security standards.
    -   New: Added support for certificate-based authentication in the Microsoft Threat and Vulnerability Management \(TVM\) integration.
-   **Version 31.0.2 - April 2026 \(USEM\)**
    -   New: Uptake of Common Vulnerability Data \(CVD\) APIs in the Microsoft Defender TVM integration for CVE creation and enrichment, with source-specific field priority support.
    -   Changed: Authentication endpoint for the Microsoft Defender integration is now configurable, replacing the previously hardcoded non-regulated Azure endpoint. This enables regulated market customers, including GCC \(Government Community Cloud\), to authenticate using the correct endpoint for their environment.
    -   Fixed: Microsoft Defender integration authentication failing for GCC customers due to the REST message being hardcoded to the non-regulated Azure endpoint \(login.microsoftonline.com\), resulting in "Confidential client is not supported in cross cloud request" errors.
-   **Version 3.0.2 - April 2026**
    -   New: Microsoft Defender for Cloud container image vulnerability ingestion. In addition to cloud misconfigurations, the integration now supports ingesting container image vulnerabilities from Microsoft Defender for Cloud.All Microsoft security integrations \(Defender for Endpoint TVM and Defender for Cloud\) are now consolidated into a single unified plugin, simplifying installation, configuration, and maintenance.
    -   Changed: The Microsoft Defender for Cloud application \(app-vul-asc\) has been merged into the Microsoft Defender TVM plugin \(sn\_vul\_msft\_tvm\), providing a single entry point for all Microsoft Defender integrations.
    -   Fixed: Resolved application errors in the system log caused by missing dictionary configuration files for the Microsoft Defender for Cloud application after plugin consolidation.
-   **Version 31.0.3 - April 2026 \(USEM\)**
    -   New: Uptake of Common Vulnerability Data \(CVD\) APIs in the Microsoft Defender TVM integration for CVE creation and enrichment, with source-specific field priority support.
    -   Changed: Authentication endpoint for the Microsoft Defender Integration is now configurable, replacing the previously hardcoded non-regulated Azure endpoint. This enables regulated market customers, including GCC \(Government Community Cloud\), to authenticate using the correct endpoint for their environment.
    -   Fixed: Microsoft Defender integration authentication failing for GCC customers due to the REST message being hardcoded to the non-regulated Azure endpoint \(login.microsoftonline.com\), resulting in "Confidential client is not supported in cross cloud request" errors.
-   **Version 3.0.3 - April 2026**
    -   New:
        -   Microsoft Defender for Cloud container image vulnerability imports. In addition to cloud misconfigurations, the integration now supports importing container image vulnerabilities from Microsoft Defender for Cloud.
        -   All Microsoft security integrations \(Defender for Endpoint TVM and Defender for Cloud\) are now consolidated into a single unified plugin, simplifying installation, configuration, and maintenance.
    -   Changed: The Microsoft Defender for Cloud application \(app-vul-asc\) has been merged into the Microsoft Defender TVM plugin \(sn\_vul\_msft\_tvm\), providing a single entry point for all Microsoft Defender integrations.
    -   Fixed: Resolved application errors in the system log caused by missing dictionary configuration files for the Microsoft Defender for Cloud application after plugin consolidation.
-   **Version 2.8.1 - December 2025**

    Fixed: The Vulnerability Response integration with Microsoft TVM now processes cloud resources ingested from Microsoft TVM. The system uses CI lookup rules to match these resources against existing CIs in the CMDB.If no match is found, a new CI is created in the cmdb\_ci\_cmp\_resourcetable for cloud resources.

-   **Version 2.6.6 - September 2025**

    Fixed: Resolved an issue where integration payloads without IP address information were displaying "undefined" in the corresponding detection records instead of showing an empty value.

-   **Version 2.6.5 - August 2025**

    Changed: Introduced a feature to Split Vulnerable Items with multiple remediation recommendations into separate VIs, each with a unique recommendation.

-   **Version 2.6.3 - May 2025**

    Fixed: Minor fixes for this release.

-   **Version 2.6.2 - February 2025**

    Changed: Verify that CVSS scores are populated on the CVE records from TVM.

-   **Version 2.5.1 - November 2024**
    -   New: Vulnerability Managers can now configure the split of detections from Microsoft Threat and Vulnerability Management scanner using CVE ID, enabling them to specify the delimiter for each CVE ID to parse the proof. This enhancement results in the creation of multiple vulnerable items for each proof. By default, the configuration to enable split detection by proof is disabled.
    -   Changed: To improve the coverage of preferred solutions on vulnerable items, remediation data from Microsoft TVM is leveraged to create solutions.
-   **Version 2.4.1 - August 2024**

    Changed: In this release, a new integration instance parameter called "skip\_preferred\_solution" has been introduced. The population of preferred solution on VIT will now be determined based on the skip\_preferred\_solution integration instance parameter.

-   **Version 2.4.0 - June 2024**

    New: The execution of the Microsoft Threat and Vulnerability Management Vulnerabilities Integration also accounts for the number of detections excluded with the application of exclusion rules.

-   **Version 2.3.14 - June 2024**
    -   Removed
        -   The Microsoft TVM Integration Run Status classic experience dashboard has been deprecated.
-   **Version 2.3.10 - May 2024**

    Fixed: MS TVM vulnerability integration is fixed to populate exploit data correctly in vulnerability data imported from MS TVM.

-   **Version 2.3.5 - February 2024**

    Fixed: sn\_vul\_msft\_tvm\_machines\_import.xmlVM Metadata information will not be truncated after this release. Schema size is increased in import set table i.e "sn\_vul\_msft\_tvm\_machines\_import" to handle the same.

-   **Version 2.3.4 - November 2023**
    -   New: A new system property 'sn\_vul\_msft\_tvm.ignore\_mac\_address' is added to ignore certain MAC addresses during CI lookup.
    -   Fixed:
        -   When the Microsoft TVM Vulnerability \(CVE\) Integration is run, the fieldsPublic exploit andExploit in kit in the vulnerability are populated with the correct values.
        -   When an exploit is created by Microsoft TVM integration, theIs exploit verified field is populated with the correct value.
-   **Version 2.3.2 - August 2023 \(Vancouver\)**

    Changed: Integration run status report has been updated to the Next Generation Experience.

-   **Version 2.2.3 - June 2023**

    Fixed: The IP address lookup rule was not returning CIs, even if there was a match available in the Configuration Items table. The issue with the IP address lookup rule has been fixed.

-   **Version 2.2.1 - March 2022**

    Fixed: Empty tags were resulting in machine data being skipped.

-   **Version 2.1.2 - October 2021**

    Updated version number for dependency applications.

-   **Version 2.0.3 - June 2021**

    New: Integration with the Microsoft Defender Threat and Vulnerability Management.


