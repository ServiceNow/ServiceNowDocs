---
title: Vulnerability Response release notes
description: The ServiceNow Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Vulnerability Response was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-03"
reading_time_minutes: 5
---

# Vulnerability Response release notes

The ServiceNow® Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Vulnerability Response was enhanced and updated in the Australia release.

## Vulnerability Response highlights for the Australia release

-   The AWS Integration for Security Exposure Management supports integrations with AWS Inspector and AWS Security Hub.
-   The Central Vulnerability Database \(CVDB\) introduces a source-agnostic vulnerability data layer that consolidates data from multiple sources, improving accuracy and traceability.
-   Define the number of background jobs that run concurrently to reduce system resource consumption, with a new Background Job Configuration tile available in the Vulnerability Manager Workspace Admin console under the Others section.

See [Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/vuln-landing-page.md) for more information.

**Important:** Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Vulnerability Response to Australia

If you're currently using Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Vulnerability Response and for upgrades to supported third-party integration applications.

For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base

## New in the Australia release

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/ms-defender-sem.md)**

    The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[AWS Integration for Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/aws-integration-for-security-exposure-management-overview.md)**

    The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Optimized Tenable.io Compliance Results ingestion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/tenableIntegration.md)**

    Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/c_QualysVulnIntegration.md)**

    The Qualys Vulnerability Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Vulnerability Data Management with Central Vulnerability Database \(CVDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/cvd-overview.md)**

    The Central Vulnerability Database \(CVDB\) introduces a unified, source-agnostic vulnerability data layer that consolidates data from multiple sources into a single authoritative record, improving accuracy, consistency, and traceability. Key capabilities include:

    -   Unified vulnerability record: Correlates vulnerability data from multiple sources, supports sources including National Vulnerability Database \(NVD\), scanner intelligence, European Union Vulnerability Database, Japanese Vulnerability Database, and vulnerability intelligence feeds.
    -   Priority-based data reconciliation configuration:
        -   Field-level priority: Ensures each attribute \(e.g., CVSS, remediation, exploit status\) can be configured from the most reliable provider.
        -   Source-level priority: Applies a global ranking when field-level rules are not defined.
        -   Hybrid model: Field-level rules take precedence, with source-level fallback; all source data is preserved for full traceability.
    -   Source attribution and traceability: Maintains detailed source metadata, timestamps, and change history to ensure full auditability and transparency.
    -   Data enrichment: Combines CVSS scores, exploit intelligence, and remediation guidance to provide a richer and more actionable vulnerability context.

## Changed in this release

-   **[Vulnerability Response assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/vr-assignment-rules.md)**

    The sn\_vul.rerun\_task\_rules system property for rerunning assignment rules was changed to sn\_sec\_rem.rerun\_task\_rules. Users must activate this property \(set to 'true'\) to rerun assignment rules.

-   **[Improved vulnerability assessment workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response-workspaces/vr-ws-vuln-assessment.md)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Remediation task rule execution mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-grouping-multiple-findings-remediation-tasks-processing.md)**

    You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Enhanced Compensatory controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-manager-workspace/requesting-approving-risk-reduction.md)**

    When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.


## Activation information

Install Vulnerability Response and supported third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

