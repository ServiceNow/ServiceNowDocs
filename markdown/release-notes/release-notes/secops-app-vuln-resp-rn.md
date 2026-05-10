---
title: Application Vulnerability Response release notes
description: The ServiceNow Application Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Application Vulnerability Response was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 3
---

# Application Vulnerability Response release notes

The ServiceNow® Application Vulnerability Response application brings security and IT together to enable you to remediate your most critical vulnerabilities more quickly and efficiently. Application Vulnerability Response was enhanced and updated in the Australia release.

## Application Vulnerability Response highlights for the Australia release

-   Import application vulnerability response data that includes application, Software Composition Analysis \(SCA\) and secrets data with the Wiz Application Vulnerability Response Integration.
-   If you're currently using Application Vulnerability Response and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management \(USEM\) notes](secops-sem-rn.md) for more information about USEM and the Unified Security Exposure Management migration.
-   Integrate with supported third-party scanners to import vulnerability data and use automated workflows to prioritize, remediate, and manage findings \(application vulnerable items \(AVITs\)\). Each application vulnerability represents a vulnerability entry in the Common Weakness Enumeration \(CWE\) or third-party libraries.
-   Monitor your penetration test requests and findings, as well as your team's overall progress in the Penetration Test Workspace.
-   Reevaluate the risk score, assignments, remediation target date, exceptions, and remediation task for a specific set of application vulnerable items in the Vulnerability Manager Workspace.
-   Compare application vulnerability-related data and determine if application vulnerabilities are found in an application.

See [Application Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/application-vulnerability-response/app-vuln-mgmt.md) for more information.

**Important:** Application Vulnerability Response is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Application Vulnerability Response to Australia

-   If you are currently using Application Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Application Vulnerability Response and for upgrades to supported third-party integration applications.
-   For information about the new features of Vulnerability Response, see the [Vulnerability Response release notes](secops-vuln-resp-rn.md).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

## New in the Australia release

-   **[Wiz Application Vulnerability Response Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/application-vulnerability-response/wiz-exploring-avr-sca-secrets.md)**

    Import application, Software Composition Analysis \(SCA\), findings, Secrets \(passwords, tokens and keys\) data with the following Wiz Vulnerability integrations:

    -   Application List Integration
    -   SCA Findings Integration
    -   Secret Findings Integration
    You can configure these integrations on the Wiz Vulnerability Integration configuration page along with the other Wiz Vulnerability integrations. View imported application list data such as Product Model and Source application ID from Wiz on the Discovered Applications \[sn\_vul\_app\_release\] table records, and SCA and Secrets data on the Application Vulnerable Items \[sn\_vul\_app\_vulnerable\_item\] table records.

-   **[GitHub Application Vulnerability Integration – Generic secrets support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/application-vulnerability-response/configure-github-vulnerability.md)**

    The GitHub Secret Scanning Integration supports imports of generic secrets in addition to standard secrets from your GitHub repositories. An enhanced Manage generic secrets in ServiceNow configuration option lets you control whether generic secrets are ingested. Imported secrets are mapped to Application Vulnerable Items \(AVITs\) with the scan type, Secret, while generic secrets are mapped with the scan type, Generic Secret.

-   **[Improved vulnerability assessment workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response-workspaces/vr-ws-vuln-assessment.md)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Enhanced Compensatory controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-manager-workspace/requesting-approving-risk-reduction.md)**

    When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.


## Activation information

Install Application Vulnerability Response by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

