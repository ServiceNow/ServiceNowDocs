---
title: Vulnerability Response Integration with Wiz release notes
description: Version history for the Vulnerability Response Integration with Wiz application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-int-wiz.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Vulnerability Response Integration with Wiz release notes

Version history for the Vulnerability Response Integration with Wiz application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 32.1.3 - June 2026 \(USEM\)**
    -   Changed:
        -   Resource Type is no longer a mandatory field for configuring the Vulnerability Response Integration with Wiz. You can now save Wiz configurations for the integrations without specifying a Resource Type, simplifying setup for use cases where specifying a Resource Type wasn't appropriate.
        -   Access Control Lists \(ACLs\) updated for the Vulnerability Response Integration with Wiz to enhance authorization on data brokers and aggregation surfaces to support internal security directives.
    -   Fixed:
        -   An issue where the application vulnerable item \(AVIT\) short description and resolved-date sync with Wiz AVITs created by the Wiz integration no longer show incomplete short descriptions when the Configuration Item \(CI\) Product Model is unavailable. The Resolved status reported by Wiz now propagates correctly to AVITs and the status update no longer errors out.
        -   An issue where container vulnerable items \(CVITs\) were ingested with a blank Vulnerability field with the Wiz Container Vulnerability Integration and \(CVITs\) were created with empty vulnerability references. Vulnerability references are resolved so CVITs link to the correct vulnerability records.
        -   An issue where the Wiz integration stored host\_tag as raw JSON instead of sn\_sec\_cmn\_host\_tag sys\_ids, causing Resource Tag filters on Discovered Items to return no records. Tags are stored consistently with other integrations and filters work as expected.
        -   Fixed an incorrect description mapping for the Wiz Issues integration where the Description field on sn\_vulc\_result records was being populated with only the Wiz portal URL instead of the detailed control description from the Wiz payload. Descriptions now reflect the source data accurately.
    -   Removed: The sn\_vul.read\_all, sn\_vul\_int\_fw.read\_all, sn\_vulc.read from the sn\_vul\_wiz.read\_integration, and sn\_vul\_wiz.configure\_integration Wiz integration roles tosupport internal security directives.
-   **Version 4.1.1 - June 2026**
    -   Changed:
        -   Resource Type is no longer a mandatory field for configuring the Vulnerability Response Integration with Wiz. You can now save Wiz configurations for the integrations without specifying a Resource Type, simplifying setup for use cases where specifying a Resource Type wasn't appropriate.
        -   Access Control Lists \(ACLs\) updated for the Vulnerability Response Integration with Wiz to enhance authorization on data brokers and aggregation surfaces tosupport internal security directives.
    -   Fixed:
        -   An issue where the application vulnerable item \(AVIT\) short description and resolved-date sync with Wiz AVITs created by the Wiz integration no longer show incomplete short descriptions when the Configuration Item \(CI\) Product Model is unavailable. The Resolved status reported by Wiz now propagates correctly to AVITs and the status update no longer errors out.
        -   An issue where container vulnerable items \(CVITs\) were ingested with a blank Vulnerability field with the Wiz Container Vulnerability Integration and \(CVITs\) were created with empty vulnerability references. Vulnerability references are resolved so CVITs link to the correct vulnerability records.
        -   An issue where the Wiz integration stored host\_tag as raw JSON instead of sn\_sec\_cmn\_host\_tag sys\_ids, causing Resource Tag filters on Discovered Items to return no records. Tags are stored consistently with other integrations and filters work as expected.
        -   Fixed an incorrect description mapping for the Wiz Issues integration where the Description field on sn\_vulc\_result records was being populated with only the Wiz portal URL instead of the detailed control description from the Wiz payload. Descriptions now reflect the source data accurately.
-   **Version 32.0.5 - May 2026 \(USEM\)**

    Fixed: An issue with access control and configuration security has been updated to enforce scope-based restrictions on Wiz configuration records so users can only edit them from within the Wiz application scope \[sn\_vul\_wiz\]. Wiz configuration records remain read-only across other scopes to maintain cross-scope visibility for dependent applications and integrations.

-   **Version 4.0.5 - May 2026**

    Fixed: An issue with access control and configuration security has been updated to enforce scope-based restrictions on Wiz configuration records so users can only edit them from within the Wiz application scope \[sn\_vul\_wiz\]. Wiz configuration records remain read-only across other scopes to maintain cross-scope visibility for dependent applications and integrations.

-   **Version 32.0.3 - April 2026 \(USEM\)**
    -   New:
        -   Import application, Software Composition Analysis \(SCA\), findings, Secrets \(passwords, tokens and keys\) data with the Wiz Application list, Wiz SCA findings, and Wiz Secret findings integrations.
        -   The Universally Unique Identifier \(UUID\) provided by Wiz is now mapped as the detection key for the Wiz Host Vulnerability integration.
        -   Added the source\_id column to the Container Image Finding \(sn\_vul\_container\_image\_findings\) table. The id attribute from the Wiz payload is mapped to this field on findings records, enabling correlation between Wiz and ServiceNow.
        -   The App Vulnerabilities Configuration tab to the Wiz integration configuration page. The tab supports the following configurable parameters: SCA Findings Record Count, App List Record Count, Secret Findings Record Count, and Manage Exceptions in ServiceNow. If you select Manage Exceptions in ServiceNow, imported ignored findings from Wiz are mapped to Open in your instance.
        -   Package table insertion for the Wiz Container Vulnerability Response integration now supports additional detection methods: FILE\_PATH and OS, in addition to the existing LIBRARY and PACKAGE methods.
        -   A new detection\_method column is populated from the Wiz payload and has been added to both the detection and finding tables.
        -   The Validated in Runtime flag is rolled up from Container Image Findings to the Container Vulnerable Item \(CVIT\) level.
    -   Changed:
        -   Finding uniqueness for the Wiz Container Vulnerability integration now includes the "Path" attribute. Existing findings are automatically migrated to the updated key structure, with irrelevant findings closed as invalid.
        -   Repository names for discovered container images are now stored in registry/repository format. All repositories associated with an image are appended to the Repository field on the Discovered Container Image record.
        -   Vulnerabilities, test results, and issues from Wiz are no longer skipped if the Cloud provider, Resource type or Native type fields are empty in the payload.
        -   Severity at the vulnerability entry level is now mapped to the cvssSeverity.
    -   Fixed:
        -   Object ID extraction for AWS virtual machines in the Wiz Host Configuration Compliance integration.
        -   An exception during the Wiz Host Vulnerability Integration job when providerUniqueId was null has been resolved. The integration now uses externalId to set the resource\_id, falling back to providerUniqueId only if externalId is empty.
        -   The Projects field on Discovered Container Image records is no longer empty after running the Wiz Container Vulnerabilities integration. Previously, the field was overwritten instead of appended during processing.
        -   Users with the sn\_vul\_wiz.configure\_integration role can update the Import since date and cancel integration runs for Wiz integrations.
        -   Detections generated by the Wiz Host Vulnerability integration are no longer linked to non-existent VITs, resolving missing detection records for affected customers.
        -   State management logic for CVITs now correctly considers the granularity information while closing and reopening the CVITs.
-   **Version 30.2.3 - January 2026 \(USEM\)**
    -   New:
        -   The Universally Unique Identifier \(UUID\) that identifies detections for the Wiz Host Vulnerability integration will be mapped to a detection key. Note: This change is supported for new customers only. For existing customers, the detection key for the Wiz Host Vulnerability integration is created using the combination ofvulnerability,asset\_id, andproof.
        -   Added thesource\_id column to the Container Image Finding table \(sn\_vul\_container\_image\_findings\) and mapped theid attribute from the Wiz import to this field on findings records.
    -   Changed:
        -   You can configure theFirst parameter for the Wiz Asset Integration to help you resolve 504 errors. You can reduce the page size if you are having memory issues or generating errors. The default value is 500.
        -   The default integration instance parameter for configuring finding keys for the Container Vulnerability Integration includessrc\_ci,vulnerability,package,image\_layer, andimage\_repository.
    -   Fixed: Extra or empty tabs are no longer displayed on the Wiz integration configuration page if the Configuration Compliance application is not installed.
-   **Version 1.2.1 - January 2026**
    -   New:
        -   The Universally Unique Identifier \(UUID\) that identifies detections for the Wiz Host Vulnerability integration will be mapped to a detection key. Note: This change is supported for new customers only. For existing customers, the detection key for the Wiz Host Vulnerability integration is created using the combination of vulnerability, asset\_id, and proof.
        -   Added the source\_id column to the Container Image Finding table \(sn\_vul\_container\_image\_findings\) and mapped the id attribute from the Wiz import to this field on findings records.
    -   Changed:
        -   You can configure the First parameter for the Wiz Asset Integration to help you resolve 504 errors. You can reduce the page size if you are having memory issues or generating errors. The default value is 500.
        -   The default integration instance parameter for configuring finding keys for the Container Vulnerability Integration includes src\_ci, vulnerability, package, image\_layer, and image\_repository.
    -   Fixed: Extra or empty tabs are no longer displayed on the Wiz integration configuration page if the Configuration Compliance application is not installed.
-   **Version 1.1.1 - December 2025**
    -   New:
        -   Resource types filters are supported on the Test Results, Issues, Host Vulnerability, and Host Test Results tabs on the Wiz Configuration page.
        -   Additional attributes imported from Wiz which are not stored in the Discovered items \[sn\_sec\_cmn\_src\_ci\] table are stamped in this table with "Asset Attributes".
        -   Fix information that includes 'Fix available', 'Partial fix available', 'No fix available', and 'Fix version' from the \[fix\_available\] and \[fix\_version\] columns is rolled up to CVITs from findings. Note: If there are two or more findings on a CVIT, the fixed version might only apply to one. In that case, 'Partial fix available' is rolled up to the CVIT.
        -   The Wiz vendor severity attribute is mapped to the 'Source severity' column on findings records in the Container Image Findings \[sn\_vul\_container\_image\_findings\] table.
        -   Source severity is mapped to the Priority column on the Test Results \[sn\_vulc\_result\] table.
        -   Test results from the host misconfiguration integration are classified as result type 'host\_misconfiguration'.
        -   Data for resources that have the validated\_at\_runtime flag set to 'Yes' is imported and populated on detections.
        -   The backfill integrations for the Host Vulnerability, Test Results, Host Test Results and Issues integrations for these primary integrations have been removed for this release. Note: After you upgrade to this version \(1.1.1\), you must set the import schedule to backdate by three days and run the Host Vulnerability, Test Results, Host Test Results and Issues integrations to import any assets from the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_assets\] table that might have been missed during upgrade.
    -   Changed:
        -   The \[is\_ignored\] column is deprecated for the Host Test Results and Test Results Integrations. This column was replaced by the \[is\_result\_ignored\] column.
        -   The CMDB internet-facing field on the Discovered item is mapped to Limited Internet Exposure on findings.
        -   Increased Column length for the descriptions in the Container Vulnerability Import and Host Vulnerability Import tables.
        -   The cluster and namespace is evaluated for all the following entity Types: DEPLOYMENT, DAEMON\_SET, STATEFUL\_SET, POD.
    -   Removed:
        -   Since their primary integrations can create discovered items and configuration item records after import, the following backfill integrations have been removed:
            -   Test results backfill integration
            -   Host test result backfill integration
            -   Issues backfill integration
    -   The Wiz Missing Assets \[sn\_vul\_wiz\_missing\_assets\] table that supported the backfill integrations is deprecated.
-   **Version 1.0.16 - October 2025**

    Fixed:

    -   Wiz Container Integration failure due to incorrect DateTime format.
    -   Removed the 'CC Resource type' field from the Test Results configuration tab in the UI.
    -   Enabled cluster and namespace population for 'DaemonSet', 'Pods', and 'StatefulSet' Kubernetes types.
    -   Mapped fixed\_version to fix\_status in the container image findings table for better visibility on remediation feasibility.
    -   Disabled the right-click 'Save As' option on the Wiz configuration page to prevent unintended actions.
    -   Corrected mapping of external\_id from cloud account payload to Cloud Account ID in the Wiz Asset Integration.
    -   Mapped isAccessibleFromInternet to cmdb\_ci\_internet\_facing for internet exposure visibility in the Wiz Asset Integration.
-   **Version 1.0.13 - September 2025**
    -   The following have been addressed:
        -   Added below integrations to address the duplicates Discovered items for the wiz.
            -   Assets integration
            -   Back fill integrations for the CC, Host integrations
        -   Added the configurations for each integration\(except Host TR Integration\) for the capabilities to fetch the Ignored items, to close the same.
        -   Deprecating current column: is\_ignored,Adding a new column is\_result\_ignored of string choice field like result\_type with no default value.
        -   Fixed the Delta pull for the Wiz CC integration.
        -   Fixed Populating non\_infra\_last comp scan date in issues and test results integration from non\_infra\_last\_scan\_date and clear the non\_infra\_last\_scan\_date if the resource\_type is not virtual machine or server less.
        -   Making the first values in configuration page as mandatory to avoid if the customer clears the value in first parameter which is mandatory in rest calls.
        -   Added wiz configuration role to sn\_vul.configure\_integration.
-   **Version 1.0.10 - August 2025**

    The Wiz integrations import vulnerability and compliance data from Wiz scanners into your ServiceNow AI Platform instance to help you get deeper insights into your cloud infrastructure risks. These integrations provide you with a comprehensive assessment of your overall cloud security posture and drive remediation actions directly from the ServiceNow AI Platform.


