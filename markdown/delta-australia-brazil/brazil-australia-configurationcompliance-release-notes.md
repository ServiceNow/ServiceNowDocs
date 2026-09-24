---
title: Combined Configuration Compliance release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Configuration Compliance from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-configurationcompliance-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Configuration Compliance release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Configuration Compliance from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Configuration Compliance release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Configuration Compliance to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

If you're currently using Configuration Compliance, and you don't intend to upgrade to Unified Security Exposure Management \(USEM\), install a version previous v30.x of Configuration Compliance and for upgrades to supported third-party integration applications.

Starting with Australia Patch 5, Now Assist for Vulnerability Response is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including the Now Assist for Vulnerability Response product name, which will be replaced with ServiceNow Otto for Unified Security Exposure Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=australia&ft:locale=en-US) is deprecated. If you're currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, backdate any of your existing Wiz primary integrations by three days and run them. See more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

For more information about the released versions of the Vulnerability Response application and the third party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Configuration Compliance.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Activate the Wiz Asset Integration and identify resource types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&family=australia&ft:locale=en-US)**

Enhancements to the Wiz integration include:

    -   Starting with version 32.1 \(USEM\) and version 4.1 \(non-USEM\), the Asset integration is deactivated by default. It is not a mandatory prerequisite for the other Wiz integration imports.

If you choose to activate it, the Asset integration will retrieve assets for all resource types if you don't specify the ones you want on the **Asset Integration Configuration** tab. To avoid importing vulnerability data you don't need, identify only the resources \(assets\) that you want to import with this integration.

    -   Resource Type is no longer a mandatory field for configuring the Vulnerability Response Integration with Wiz. You can now save Wiz configurations for the integrations without specifying a Resource Type, simplifying setup for use cases where specifying a Resource Type isn't appropriate.

 -   **[Compliance test uniqueness key](https://www.servicenow.com/docs/access?context=cc-tenable-compliance-test-uniqueness-key&family=australia&ft:locale=en-US)**

You can now configure which identifier the system uses to uniquely match incoming Tenable conformance test records. Previously, conformance tests were identified by the check\_id field, which caused records to be overwritten when multiple tests shared the same control identifier. You can now select the identifier that best matches how your Tenable data is structured \(**compliance\_control\_id**, **check\_id**, or **compliance\_functional\_id**\), ensuring test records are accurately preserved during ingestion.


 -   **[AWS Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=aws-integration-for-security-exposure-management-overview&family=australia&ft:locale=en-US)**

The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and conformance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenableIntegration&family=australia&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io conformance Results Integration is replaced by the Tenable.io Fixed conformance Results Integration and Tenable.io Open conformance Results Integration. conformance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of conformance data while keeping remediation and conformance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=c_QualysVulnIntegration&family=australia&ft:locale=en-US)**

The Qualys Vulnerability Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and conformance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&family=australia&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&family=australia&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.


 -   **Enhancements to the Vulnerability Response Integration with Wiz**

Enhancements to the Wiz integration that imports cloud configuration findings as Test Results in Configuration Compliance. Configuration issues related to AI assets, such as AI models and agents are routed into AI security exposure management tables \(AI posture findings\).

This enhancement helps with better visibility within AI Control Tower and for any AI-specific remediation workflows to be added in the future. The 'Send AI security findings to AI security exposure management' configuration setting has been added to the Wiz Test Results integration configuration page so that AI security findings are routed into AI security exposure management.

-   **[Qualys parameter to ignore passed test results](https://www.servicenow.com/docs/access?context=Qualys-cc-Integration&family=australia&ft:locale=en-US)**

Starting with v15.2.5 of Configuration Compliance, the ignore\_passed\_result integration instance parameter for the Qualys Integration for Security Operations has been added.

This parameter is set to `false` by default so that passed test results imported by Qualys aren't ignored.

Set the parameter to **true** to ignore passed test results on import.

**Note:** If activated, this parameter does not impact closure of the test results. For example, if you activate the parameter, and a failed test result from a previous import has since passed, it will be closed correctly.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Configuration Compliance features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Configuration Compliance features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Configuration Compliance features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Configuration Compliance.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install Configuration Compliance and third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Configuration Compliance is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Configuration Compliance, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   The AWS Integration for Security Exposure Management supports integrations with AWS Inspector and AWS Security Hub.
-   If you're currently using Configuration Compliance and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management \(USEM\) release notes](https://www.servicenow.com/docs/access?context=secops-sem-rn&family=australia&ft:locale=en-US) for more information about USEM and the Unified Security Exposure Management migration.
-   Import Wiz issues and configuration test results from the Wiz scanners into test results in the Configuration Compliance application with the Vulnerability Response Integration with Wiz.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.
-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.

 See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

