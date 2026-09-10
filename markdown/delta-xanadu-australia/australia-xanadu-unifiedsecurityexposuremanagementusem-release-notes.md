---
title: Combined Unified Security Exposure Management \(USEM\) release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Unified Security Exposure Management \(USEM\) from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-unifiedsecurityexposuremanagementusem-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Unified Security Exposure Management \(USEM\) release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Unified Security Exposure Management \(USEM\) from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Unified Security Exposure Management \(USEM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Unified Security Exposure Management \(USEM\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   **Upgrade information**

Starting with Australia Patch 5, Now Assist for Vulnerability Response is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including the Now Assist for Vulnerability Response product name, which will be replaced with ServiceNow Otto for Unified Security Exposure Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

To access the new AI native experience in the Unified Security Exposure Management \(USEM\) workspace, you must upgrade to the Australia release.

    -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

        -   Foundation: AI basics to deliver insights
        -   Advanced: AI to boost productivity across relevant use cases
        -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

Unified Security Exposure Management is available to all customers who are entitled to Vulnerability Response. Migrating to USEM is a major upgrade that introduces a unified architecture for improved performance, scalability, and streamlined workflows. Before upgrading, leverage the Migration assistant for Unified Security Exposure Management that is available as an update set. See the [Migration Guidance to Unified Security Exposure Management \[KB2556844\]](https://support.servicenow.com/kb?sys_kb_id=8652717893a8ba94f538fb2d6cba1078&id=kb_article_view) Knowledge Base article for more information. This tool provides a guided experience for plugin installation, data mapping, rule migration, and post-migration validation, reducing risk and manual effort. Ensure that all integrations and workflows are reviewed for compatibility before initiating migration. For more information, see [Migrating to USEM](https://www.servicenow.com/docs/access?context=migrating-to-usem&family=australia&ft:locale=en-US) and [Migrate to USEM](https://www.servicenow.com/docs/access?context=migrate-to-usem&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Unified Security Exposure Management \(USEM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Qualys Integration – API enhancements](https://www.servicenow.com/docs/access?context=qualys-rest-messages-cc&family=zurich&ft:locale=en-US)**

Qualys Integration has been upgraded to support newer Qualys API versions across Host Detection, Host List, Knowledgebase, PC Controls, PC Policies, and PCRS integrations. The integrations now ingest additional data fields, including vulnerability detection source, authentication privilege status, active status for controls and policies, and cloud metadata, giving you better visibility into your vulnerability and compliance data. Use the new `posture_api_version` integration instance parameter to choose between the default v2.0 APIs or the newer v5.0 streaming APIs for the PCRS Policy Host and PCRS Test Results integrations.


</td></tr><tr><td>

Australia

</td><td>

-   **[NVD integration enriches CVEs with SSVC decision data](https://www.servicenow.com/docs/access?context=nvd-ssvc-enrichment&family=australia&ft:locale=en-US)**

USEM enriches CVE entries with Stakeholder-Specific Vulnerability Categorization \(SSVC\) decision values from the National Vulnerability Database \(NVD\), including Exploitation, Automatable, and Technical Impact. Use these additional risk signals to analyze vulnerabilities and prioritize remediation.

-   **[Enhancements to ServiceNow Otto for Unified Security Exposure Management](https://www.servicenow.com/docs/access?context=now-assist-review-vulnerability-exposure-data&family=australia&ft:locale=en-US)**

USEM was enhanced and updated in the Australia release to support the new AI native experience.

    -   Links to Records: Select the counts and findings in the Security Exposure 360 output to link you directly to the underlying vulnerable item \(VITs\) and records in your instance.
    -   Suggested follow-up questions: Follow-up questions are provided that help you drill down.
-   **[Fix Intelligence for Security Exposure Management](https://www.servicenow.com/docs/access?context=fix-intel-for-usem-landing&family=australia&ft:locale=en-US)**

Fix Intelligence for Security Exposure Management is a new application that enriches your host findings with normalized fix information from Armis Centrix™ for Vulnerability Prioritization and Remediation \(ViPR\). Detections are de-duplicated into Fix records that are linked to the findings and assets each fix resolves, with a rolled-up risk score per fix. Your team can remediate by fix instead of one finding at a time.

Prioritize fixes from the **Fix Intelligence** tab, the **Findings View**, and the **Remediation View**, and group the findings that share a fix into a single remediation task. In this release, fixes are identified for host vulnerabilities from Qualys, Rapid7, Tenable.io, Wiz, and Microsoft Defender Vulnerability Management.

-   **[Enhancements to the Vulnerability Response Integration with Wiz Test Results Integration](https://www.servicenow.com/docs/access?context=wiz-test-result-tab-filters&family=australia&ft:locale=en-US)**

Enhancements to the Wiz integration that imports cloud configuration findings as Test Results in Configuration Compliance. Configuration issues related to AI assets, such as AI models and agents are routed into AI security exposure management tables \(AI posture findings\).

This enhancement helps with better visibility within AI Control Tower and for any AI-specific remediation workflows to be added in the future. The 'Send AI security findings to AI security exposure management' configuration setting has been added to the Wiz Test Results integration configuration page. This setting routes AI security findings into AI security exposure management.

-   **[View impacted findings in exception rule approvals](https://www.servicenow.com/docs/access?context=sem-exception-rules-overview&family=australia&ft:locale=en-US)**

Use the **Impacted findings** metric in the approval form's Overview tab to assess the scope and impact of an exception rule before approval. The metric displays the number of existing findings that match the rule's conditions. The impacted findings count is also included in exception rule approval emails, allowing you to make informed approval decisions without leaving your inbox.

-   **[Streamline Microsoft SCCM data ingestion with JDBC](https://www.servicenow.com/docs/access?context=mspatch-integration&family=australia&ft:locale=en-US)**

Connect to Microsoft SCCM using JDBC \(Java Database Connectivity\) to query the SCCM database directly for collection, device, patch update, and deployment status data. Opening a firewall port for WMI \(Windows Management Instrumentation\) RPCs \(remote procedure calls\) is no longer required for these queries. A WMI connection remains required to deploy patches, because patch deployment continues to use the Microsoft SCCM API over WMI.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Unified Security Exposure Management \(USEM\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   **[ITSM Advanced plugin required for change request options in the Remediation view](https://www.servicenow.com/docs/access?context=sem-ws-CRs&family=australia&ft:locale=en-US)**

Use the **Create Change** and **Add to existing change** options in the Remediation view of the Security Exposure Management Workspace to manage remediation tasks through Change Management. These options now require the ITSM Advanced plugin to be active on your instance. If you have migrated to an ITSM AI Native SKU without ITSM Advanced, upgrade to ITSM Advanced SKU to restore access to these options.

-   **[Create remediation tasks directly from the Security Exposure Management Workspace list view](https://www.servicenow.com/docs/access?context=sem-workspace-list-page&family=australia&ft:locale=en-US)**

Remediation owners can now create remediation tasks directly from list views in the Security Exposure Management Workspace by selecting the Create Remediation Task action from the list toolbar in the Assigned to me and Assigned to my group views for host vulnerable items, application vulnerable items, container vulnerable items, and configuration test results. Previously, this action was available only for managers.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Unified Security Exposure Management \(USEM\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Between your current release family and Australia, some Unified Security Exposure Management \(USEM\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Review information on how to activate Unified Security Exposure Management \(USEM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   **Activation information**

Install Unified Security Exposure Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Unified Security Exposure Management \(USEM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If any specific browser requirements were introduced or changed for Unified Security Exposure Management \(USEM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Review details on accessibility information for Unified Security Exposure Management \(USEM\), such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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
</table>## Localization information

If there are specific localization considerations for Unified Security Exposure Management \(USEM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

If there are specific highlight considerations for Unified Security Exposure Management \(USEM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

-   Unified Security Exposure Management now integrates with Early Warning for Security Exposure Management integration to enrich Common Vulnerabilities and Exposures \(CVE\) data with Early Warning insights. Teams can focus remediation on vulnerabilities under active or imminent exploitation.
-   Vulnerability management teams can use AI Security Exposure Management and supported integrations to reduce the AI attack surface by efficiently remediating security exposures in AI assets.
-   USEM was enhanced and updated in the Australia release to support the new AI native experience.
-   Administrators can manage user and group role assignments, create/update watchdogs with custom conditions, and access a centralized Advanced Settings page directly from the Security Exposure Management Workspace. This eliminates the need to navigate multiple configuration pages.
-   Assign tags to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to define metadata and access control all directly from the Security Exposure Management Workspace.
-   Third-party source severity fields are now normalized into standard ServiceNow severity values all directly in the Security Exposure Management Workspace.
-   Approvers can bulk approve or reject multiple requests in a single action.
-   The AWS Integration for Security Exposure Management supports integrations with AWS Inspector and AWS Security Hub.

 See [Unified Security Exposure Management](https://www.servicenow.com/docs/access?context=unified-security-exposure-management-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

