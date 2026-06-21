---
title: Combined Configuration Compliance release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Configuration Compliance from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-configurationcompliance-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 18
breadcrumb: [Products combined by family]
---

# Combined Configuration Compliance release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Configuration Compliance from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Configuration Compliance release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Configuration Compliance to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

If you are currently using Configuration Compliance, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Configuration Compliance and for upgrades to supported third-party integration applications.

 The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=zurich&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

 For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Australia

</td><td>

If you are currently using Configuration Compliance, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Configuration Compliance and for upgrades to supported third-party integration applications.

 The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=australia&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

 For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Configuration Compliance.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&family=yokohama&ft:locale=en-US)**

Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&family=yokohama&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&family=yokohama&ft:locale=en-US)**

Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[Create remediation tasks manually in the Vulnerability Manager Workspace](https://www.servicenow.com/docs/access?context=vmws-create-remediation-task&family=yokohama&ft:locale=en-US)**

With the sn\_vulc.admin role, you can create remediation tasks manually by selecting some or all the records in the Configuration Test Results lists in the Vulnerability Manager Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating remediation tasks.

-   **[Create remediation tasks manually in the IT Remediation Workspace](https://www.servicenow.com/docs/access?context=itr-ws-create-remediation-task&family=yokohama&ft:locale=en-US)**

With the sn\_vulc.remediation\_owner role, you can create remediation tasks manually by selecting desired records in the Configuration Test Results lists in the IT Remediation Workspace. These records are grouped into one or more remediation tasks according to the grouping criteria selected while creating remediation tasks.

-   **[View risk score details of a test result in the Work notes section](https://www.servicenow.com/docs/access?context=config-compliance-calculator-rules&family=yokohama&ft:locale=en-US)**

Starting with v15.2.1 of Configuration Compliance, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a test result in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

-   **[Quick Start Tests for Configuration Compliance](https://www.servicenow.com/docs/access?context=available-quick-start-tests&family=yokohama&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that Configuration Compliance works as expected. If you customized Configuration Compliance, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&family=zurich&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&family=zurich&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=qualys-rest-messages-cc&family=zurich&ft:locale=en-US)**

Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&family=zurich&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Enhancements to the Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=zurich&ft:locale=en-US)**

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] is deprecated. After updating to version 1.1, you must backdate your existing primary Wiz integrations by three days and run them.

The backfill integrations are activated by default.

After you backdate and run your integrations, the following backfill integrations are no longer required:

    -   Host Vulnerability Backfill Integration
    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The \[is\_ignored\] column is deprecated for the Host Test Results and Test Results Integrations. This column was replaced by the \[is\_result\_ignored\] column.

Source severity is mapped to the Priority column on the Test Results \[sn\_vulc\_result\] table.

Resource type filters are on the Test Results, Issues, and Host Test Results configuration tabs on the Wiz Configuration page. You can add any of the resource types listed.

**Note:**

If you configure resource types on the Resource Type Configuration tab, and you choose to configure parameters on the integration instance records, your configurations on integration instance take precedence over your settings on the Resource Type Configuration tab. See [Identify Wiz Resource types](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&family=zurich&ft:locale=en-US) for more information.

Additional attributes imported from Wiz that are not stored in the Discovered items \[sn\_sec\_cmn\_src\_ci\] table are stamped with `Asset Attributes` in this table.

Test results from the Host misconfiguration integration are classified as result type 'host\_misconfiguration'.

Data for resources that have the validated\_at\_runtime flag set to 'yes' is imported and populated on detections.

The is\_ignored column is deprecated on the Host Test Results and Test Results Integrations. This column was replaced by the is\_result\_ignored column.

The CMDB internet-facing field on the discovered item is mapped to Limited Internet Exposure on findings.

Column length for the descriptions in the Host Vulnerability import table has been increased.

-   **[Qualys parameter to ignore passed test results](https://www.servicenow.com/docs/access?context=Qualys-cc-Integration&family=zurich&ft:locale=en-US)**

Starting with v15.2.5 of Configuration Compliance, the ignore\_passed\_result integration instance parameter for the Qualys Integration for Security Operations has been added.

This parameter is set to `false` by default so that passed test results imported by Qualys are not ignored.

Set the parameter to **true** to ignore passed test results on import.

**Note:** If activated, this parameter does not impact closure of the test results. For example, if you activate the parameter, and a failed test result from a previous import has since passed, it will be closed correctly.

-   **[Identify Wiz Resource Types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&family=zurich&ft:locale=en-US)**

Identify the Resource Types \(assets\) reported by Wiz in your environment on the Wiz Integration Resource Type configuration page in your ServiceNow AI Platform instance that you want to import.

The Resource Types that you select apply to all the primary Wiz vulnerability and compliance integrations except the Wiz Container Vulnerability Integration.

-   **[Wiz Backfill Integrations](https://www.servicenow.com/docs/access?context=wiz-backfill&family=zurich&ft:locale=en-US)**

Retrieve and process data stored on the Wiz Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table for missing assets that were not processed by the primary compliance integrations with specialized Wiz Backfill Integrations.

    -   Test Results Backfill Integration
    -   Host Test Results Backfill Integration
    -   Issues Backfill Integration
The Wiz Backfill Integrations are activated by default.

-   **[Wiz Host Test Result Vulnerability Integration](https://www.servicenow.com/docs/access?context=wiz-host-test-result-tab-filters&family=zurich&ft:locale=en-US)**

Import test results associated with the resource type, `VIRTUAL MACHINE` with the Wiz Host Test Result Vulnerability Integration. This integration is activated by default.

-   **[The Wiz Configuration Compliance \(Test Results\) and Issues Integrations](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=zurich&ft:locale=en-US)**
    -   Import configuration test results with the Wiz Configuration Compliance Integration \(Wiz Test Results\) to detect non-compliant cloud configurations. Findings are mapped to cloud test results \(CTRs\) in the Configuration Compliance application to help you enforce security policies and standards across your cloud environment.
    -   Import data with the Wiz Issues Integration that can help you identify assets that are involved in toxic combinations of vulnerabilities and misconfigurations. These findings are also mapped to CTRs with `Wiz Issues` labeled as the source to help you track and remediate assets that may pose complex multi-vector risks.

</td></tr><tr><td>

Australia

</td><td>

-   **[Activate the Wiz Asset Integration and identify resource types for import](https://www.servicenow.com/docs/access?context=wiz-assets-resources-tab&family=australia&ft:locale=en-US)**

Enhancements to the Wiz integration include:

    -   Starting with version 32.1 \(USEM\) and version 4.1 \(non-USEM\), the Asset integration is deactivated by default and is not a mandatory prerequisite for the other Wiz integration imports.

If you choose to activate it, the Asset integration will retrieve assets for all resource types if you don't specify the ones you want on the **Asset Integration Configuration** tab. To avoid importing vulnerability data you don't need, identify only the resources \(assets\) that you want to import with this integration.

    -   Resource Type is no longer a mandatory field for configuring the Vulnerability Response Integration with Wiz. You can now save Wiz configurations for the integrations without specifying a Resource Type, simplifying setup for use cases where specifying a Resource Type isn't appropriate.
-   **[Compliance test uniqueness key](https://www.servicenow.com/docs/access?context=cc-tenable-compliance-test-uniqueness-key&family=australia&ft:locale=en-US)**

You can now configure which identifier the system uses to uniquely match incoming Tenable compliance test records. Previously, compliance tests were identified by the check\_id field, which caused records to be overwritten when multiple tests shared the same control identifier. You can now select the identifier that best matches how your Tenable data is structured \(**compliance\_control\_id**, **check\_id**, or **compliance\_functional\_id**\), ensuring test records are accurately preserved during ingestion.

-   **[Qualys parameter to ignore passed test results](https://www.servicenow.com/docs/access?context=Qualys-cc-Integration&family=australia&ft:locale=en-US)**

Starting with v15.2.5 of Configuration Compliance, the ignore\_passed\_result integration instance parameter for the Qualys Integration for Security Operations has been added.

This parameter is set to `false` by default so that passed test results imported by Qualys are not ignored.

Set the parameter to **true** to ignore passed test results on import.

**Note:** If activated, this parameter does not impact closure of the test results. For example, if you activate the parameter, and a failed test result from a previous import has since passed, it will be closed correctly.

-   **[AWS Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=aws-integration-for-security-exposure-management-overview&family=australia&ft:locale=en-US)**

The AWS Integration for Security Exposure Management supports integrations with the following AWS services:

    -   AWS Inspector is an automated vulnerability management service that continuously scans EC2 instances, ECR container images, and Lambda functions for software vulnerabilities \(CVEs\) and unintended network exposure. The Vulnerability Response integration with AWS Inspector imports host and container vulnerability findings from AWS Inspector.
    -   AWS Security Hub is a security service that is used to centralize and update security checks across AWS accounts. It provides a unified view of security alerts and compliance status by integrating with various AWS services. The Vulnerability Response integration with AWS Security Hub imports host, container vulnerabilities, and misconfigurations from AWS Security Hub.
-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenableIntegration&family=australia&ft:locale=en-US)**

Starting with v 6.1.3, the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=c_QualysVulnIntegration&family=australia&ft:locale=en-US)**

The Qualys Vulnerability Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **[Unified Microsoft Defender Integration for Security Exposure Management](https://www.servicenow.com/docs/access?context=ms-defender-sem&family=australia&ft:locale=en-US)**

The Microsoft Defender for Cloud and Microsoft Defender Threat and Vulnerability Management \(MS TVM\) plugins are now consolidated into a single plugin: Microsoft Defender Integration for Security Exposure Management. This consolidation deprecates the standalone Microsoft Defender for Cloud plugin. The unified plugin also introduces container image vulnerability ingestion from Microsoft Defender for Cloud, creating Container Vulnerable Items on your instance. A guided migration path is available to transfer existing data from the deprecated applications to the unified plugin.

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&family=australia&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Configuration Compliance features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&family=zurich&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Optimized Tenable.io Compliance Results ingestion](https://www.servicenow.com/docs/access?context=tenable-io-integrations-list&family=zurich&ft:locale=en-US)**

Starting with v\[VERSION\], the Tenable.io Compliance Results Integration is replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=qualys-rest-messages-cc&family=zurich&ft:locale=en-US)**

Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.

-   **Optimized Tenable.io Compliance Results ingestion**

Starting with v\[VERSION\], the Tenable.io Compliance Results Integration is deprecated and replaced by the Tenable.io Fixed Compliance Results Integration and Tenable.io Open Compliance Results Integration. Compliance results are now imported based on their status, optimizing ingestion performance and scalability for environments with large volumes of compliance data while keeping remediation and compliance tracking aligned with the current state of findings.

-   **[Configure Test Result Granularity](https://www.servicenow.com/docs/access?context=cc-tenable-tr-granularity&family=zurich&ft:locale=en-US)**

Starting with v15.6.1, you can configure the granularity of Tenable Configuration Test Results \(CTRs\) to split results into unique findings. For example, if a database has five instances, the system generates five distinct test results, one per instance, providing improved visibility into individual patching efforts.

-   **[Configure Test Result Granularity](https://www.servicenow.com/docs/access?context=cc-qualys-tr-granularity&family=zurich&ft:locale=en-US)**

Starting with v15.4.3, you can configure the granularity of Qualys Configuration Test Results \(CTR\) in configuration compliance and split CTRs into unique findings. For example, if a database has five instances, the system generates five distinct test results, one per instance, providing improved visibility into individual patching efforts.

-   **[Configure maximum rows in related lists](https://www.servicenow.com/docs/access?context=vr-max-rows-rel-list&family=zurich&ft:locale=en-US)**

To improve readability and performance, you can now limit the number of rows shown in related lists on forms by setting the system property **sn\_vul\_cmn.related\_list.set\_max\_row**.

-   **[Improved state management for remediation tasks and vulnerable items](https://www.servicenow.com/docs/access?context=vr-rt-states&family=zurich&ft:locale=en-US)**

State management logic for roll down of state from remediation tasks \(RTs\) to findings and roll up of state from findings to RTs has been refined across all modules. Updates improve accuracy by handling mixed item states \(a combination of Deferred and Closed\), supporting closure of tasks in sub-states like In-Review, and reopening tasks based on the Assigned To field. The update also improves handling of False Positive state transitions based on scanner results as source of truth. These enhancements reduce manual effort, clarify task ownership, and streamline remediation workflows.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Configuration Compliance features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Configuration Compliance features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

Install Configuration Compliance by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Configuration Compliance and third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Configuration Compliance and third-party integrations by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Configuration Compliance we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.

 See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   If you are currently using Configuration Compliance and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management release notes](https://www.servicenow.com/docs/access?context=secops-sem-rn&family=zurich&ft:locale=en-US) for more information about USEM and the Unified Security Exposure Management migration.
-   Import Wiz issues and configuration test results from the Wiz scanners into test results in the Configuration Compliance application with the Vulnerability Response Integration with Wiz.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.
-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.

 See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   The AWS Integration for Security Exposure Management supports integrations with AWS Inspector and AWS Security Hub.
-   If you're currently using Configuration Compliance and you want to upgrade to Unified Security Exposure Management \(USEM\), see [Unified Security Exposure Management \(USEM\) notes](https://www.servicenow.com/docs/access?context=secops-sem-rn&family=australia&ft:locale=en-US) for more information about USEM and the Unified Security Exposure Management migration.
-   Import Wiz issues and configuration test results from the Wiz scanners into test results in the Configuration Compliance application with the Vulnerability Response Integration with Wiz.
-   With the sn\_vulc.remediation\_owner role, create remediation tasks manually in the IT Remediation Workspace.
-   With the sn\_vulc.admin role, create remediation tasks manually in the Vulnerability Manager Workspace.

 See [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

