---
title: Configuration Compliance release notes
description: The ServiceNow Configuration Compliance application enables you to prioritize and remediate the most critical configuration-related vulnerabilities in your environment quickly and efficiently. Configuration Compliance was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 5
---

# Configuration Compliance release notes

The ServiceNow® Configuration Compliance application enables you to prioritize and remediate the most critical configuration-related vulnerabilities in your environment quickly and efficiently. Configuration Compliance was enhanced and updated in the Australia release.

## Configuration Compliance highlights for the Australia release

-   The AWS Integration for Security Exposure Management supports integrations with AWS Inspector and AWS Security Hub.
-   If you're currently using Configuration Compliance and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management \(USEM\) notes](secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Import Wiz issues and configuration test results from the Wiz scanners into test results in the Configuration Compliance application with the Vulnerability Response Integration with Wiz.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.
-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.

See [Configuration Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/vr-config-compliance-landing.md) for more information.

**Important:** Configuration Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Configuration Compliance to Australia

If you are currently using Configuration Compliance, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Configuration Compliance and for upgrades to supported third-party integration applications.

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/vr-wiz-exploring-host-cf.md) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

## New in the Australia release

-   **[Tenable compliance test uniqueness key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/cc-tenable-compliance-test-uniqueness-key.md)**

    You can now configure which identifier the system uses to uniquely match incoming Tenable compliance test records. Previously, compliance tests were identified by the check\_id field, which caused records to be overwritten when multiple tests shared the same control identifier. You can now select the identifier that best matches how your Tenable data is structured \(**compliance\_control\_id**, **check\_id**, or **compliance\_functional\_id**\), ensuring test records are accurately preserved during ingestion.

-   **[Qualys parameter to ignore passed test results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/configuration-compliance/Qualys-cc-Integration.md)**

    Starting with v15.2.5 of Configuration Compliance, the ignore\_passed\_result integration instance parameter for the Qualys Integration for Security Operations has been added.

    This parameter is set to `false` by default so that passed test results imported by Qualys are not ignored.

    Set the parameter to **true** to ignore passed test results on import.

    **Note:** If activated, this parameter does not impact closure of the test results. For example, if you activate the parameter, and a failed test result from a previous import has since passed, it will be closed correctly.

-   **[AWS Integration for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/aws-integration-for-security-exposure-management-overview.md)**

    The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Optimized Tenable.io Compliance Results ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/tenableIntegration.md)**

    Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/c_QualysVulnIntegration.md)**

    The Qualys Vulnerability Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/ms-defender-sem.md)**

    The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Remediation task rule execution mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-grouping-multiple-findings-remediation-tasks-processing.md)**

    You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.


## Activation information

Install Configuration Compliance and third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

