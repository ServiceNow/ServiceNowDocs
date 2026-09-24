---
title: Combined Unified Security Exposure Management \(USEM\) release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Unified Security Exposure Management \(USEM\) from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-unifiedsecurityexposuremanagementusem-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Unified Security Exposure Management \(USEM\) release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Unified Security Exposure Management \(USEM\) from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Unified Security Exposure Management \(USEM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Unified Security Exposure Management \(USEM\) to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Unified Security Exposure Management \(USEM\).

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

-   **[SSVC decision values roll up from CVEs to third-party entries](https://www.servicenow.com/docs/access?context=nvd-ssvc-enrichment&family=australia&ft:locale=en-US)**

USEM rolls up the Exploitation, Automatable, and Technical Impact SSVC \(Stakeholder-Specific Vulnerability Categorization\) values from CVE entries to the corresponding third-party entry \(TPE\) records. Changes to these values automatically trigger a risk score recalculation when the TPE risk calculator uses one or more of them.

-   **[Automatic re-evaluation of remediation tasks on Preferred solution change](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&family=australia&ft:locale=en-US)**

Remediation tasks can now automatically re-evaluate findings when their Preferred solution changes, so items are regrouped into the appropriate remediation task without manual intervention. This helps keep remediation tasks accurate and reduces manual cleanup.

-   **[Automatically create vulnerable items and application vulnerable items during assessment](https://www.servicenow.com/docs/access?context=vr-va-ws-cve-exposure-assessment-api&family=australia&ft:locale=en-US)**

Vulnerability assessments now support an Auto-create VITs/AVITs option that automatically creates vulnerable items and application vulnerable items for their affected configuration items and products, removing the need for a separate manual create step. The new CVE Exposure Assessment REST API lets external systems set this option when creating a vulnerability assessment record, or trigger a CVE exposure assessment independently.

-   **[Deploy multiple patches to multiple collections with Microsoft SCCM](https://www.servicenow.com/docs/access?context=mspatch-integration&family=australia&ft:locale=en-US)**

Deploy more than one patch to more than one collection in a single deployment, instead of one patch to one collection at a time. When you select more than one patch for a deployment, the integration automatically creates a Software Update Group in Microsoft SCCM to bundle the patches.

-   **[Deploy multiple patches to multiple computer groups with HCL BigFix](https://www.servicenow.com/docs/access?context=vr-bigfix-integration&family=australia&ft:locale=en-US)**

Deploy more than one patch to more than one computer group in a single deployment, instead of one patch to one computer group at a time.


</td></tr><tr><td>

Brazil

</td><td>

-   **[SSVC decision values roll up from CVEs to third-party entries](https://www.servicenow.com/docs/access?context=nvd-ssvc-enrichment&family=brazil&ft:locale=en-US)**

USEM rolls up the Exploitation, Automatable, and Technical Impact SSVC \(Stakeholder-Specific Vulnerability Categorization\) values from CVE entries to the corresponding third-party entry \(TPE\) records. Changes to these values automatically trigger a risk score recalculation when the TPE risk calculator uses one or more of them.

-   **[Automatic re-evaluation of remediation tasks on Preferred solution change](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&family=brazil&ft:locale=en-US)**

Remediation tasks can now automatically re-evaluate findings when their Preferred solution changes, so items are regrouped into the appropriate remediation task without manual intervention. This helps keep remediation tasks accurate and reduces manual cleanup.

-   **[Deploy multiple patches to multiple collections with Microsoft SCCM](https://www.servicenow.com/docs/access?context=mspatch-integration&family=brazil&ft:locale=en-US)**

Deploy more than one patch to more than one collection in a single deployment, instead of one patch to one collection at a time. When you select more than one patch for a deployment, the integration automatically creates a Software Update Group in Microsoft SCCM to bundle the patches.

-   **[Deploy multiple patches to multiple computer groups with HCL BigFix](https://www.servicenow.com/docs/access?context=vr-bigfix-integration&family=brazil&ft:locale=en-US)**

Deploy more than one patch to more than one computer group in a single deployment, instead of one patch to one computer group at a time.

-   **[Resolve AI exposure tasks in workflow with Employee Center](https://www.servicenow.com/docs/access?context=ai-security-exposure-employee-workflow&family=brazil&ft:locale=en-US)**

AI Security Exposure Management integrates with Employee Center and third-party security tools to enable AI asset owners to remediate AI posture findings \(configuration issues\) directly through lightweight tasks.

-   **AI Service Graph Connector for Prisma AIRS**

This integration imports AI inventory data from Palo Alto Prisma AIRS and populates the CMDB in your ServiceNow AI Platform instance. In addition to inventory data, this integration imports key metrics related to AI model vulnerabilities, validation findings \(automated red teaming results\) that can be viewed in AI control tower.

-   **[Palo Alto Prisma AIRS Integration for AI Security Exposure Management](https://www.servicenow.com/docs/access?context=prisma-airs-integration&family=brazil&ft:locale=en-US)**

Import AI security exposures such as model vulnerabilities, model validation findings \(automated red teaming alerts\), and posture findings \(configuration/policy violations\) into AI Security Exposure Management and automate workflows for remediation.

-   **[Configure the Wiz Test Results Integration to import AI findings](https://www.servicenow.com/docs/access?context=wiz-test-result-tab-filters&family=brazil&ft:locale=en-US)**

Import cloud configuration findings as Test Results into Configuration Compliance. Configuration issues related to AI assets, such as AI models and agents and AI security scans are routed into AI security exposure management tables \(AI posture findings\) if you have AI security exposure management activated.

-   **Attach findings to a penetration testing assessment request**

Admins can now link pentest findings to existing pentest requests during manual upload, enabling consolidation of findings from multiple vendors under a single request.

-   **[Remove older SBOM records](https://www.servicenow.com/docs/access?context=sbom-cleanup&family=brazil&ft:locale=en-US)**

SBOM cleanup lets you create a one-time rule to purge older software bill of materials records that match specified conditions that you create. Cleanup runs are permanent and can't be reversed, and you must review the conditions you set carefully before running one.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Unified Security Exposure Management \(USEM\) features.

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

-   **[Improved vulnerability assessment workflows](https://www.servicenow.com/docs/access?context=vr-ws-vuln-assessment&family=australia&ft:locale=en-US)**
    -   CI filtering for vulnerability assessments: You can now filter which configuration items are included in a vulnerability assessment using a condition builder.
    -   Business Application population on AVITs: AVITs created from SBOM assessment results now include Business Application information, helping you understand application impact and prioritize remediation.
    -   Priority roll‑down from vulnerability assessments: Updates to the priority of a vulnerability assessment now automatically roll down to associated VITs and AVITs, ensuring consistent prioritization based on the highest severity.
-   **[Remediation task rule execution mode](https://www.servicenow.com/docs/access?context=sem-grouping-multiple-findings-remediation-tasks-processing&family=australia&ft:locale=en-US)**

You can now choose how remediation task rules are evaluated during ingestion. The new Match First execution mode evaluates rules sequentially and applies only the first matching rule, assigning each finding to exactly one remediation task. The default Match All mode continues to evaluate all applicable rules.

-   **[Enhanced Compensatory controls](https://www.servicenow.com/docs/access?context=requesting-approving-risk-reduction&family=australia&ft:locale=en-US)**

When new vulnerable items are ingested and associated with a remediation task that already has an approved compensating control, the reduced risk rating is now automatically inherited by those new vulnerable items.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Unified Security Exposure Management \(USEM\) features or functionality were removed.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Unified Security Exposure Management \(USEM\) features or functionality were deprecated.

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

</td></tr><tr><td>

Brazil

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


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install Unified Security Exposure Management \(USEM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=brazil&ft:locale=en-US).

Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


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

</td></tr><tr><td>

Brazil

</td><td>

-   **Additional requirements**

The Security Support Common plugin is activated automatically when any of the plugins for the main Security Operations applications are activated. These applications include Unified Security Exposure Management \(USEM\), Security Incident Response, Threat Intelligence, and Configuration Compliance.


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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

</td><td>

-   Centralize exposure management workflows, improve visibility across exposures, and enforce governance through configurable rules.
-   Reduce the AI attack surface by using AI Security Exposure Management and supported integrations to remediate security exposures in AI assets.
-   Manage user and group role assignments, configure watchdogs with custom conditions, and access advanced settings directly from the Security Exposure Management Workspace.
-   Assign tags to security incidents, response tasks, vulnerable items, observables, IoCs, and security cases to define metadata and access control.
-   Normalize third-party source severity fields into standard ServiceNow severity values.

 See [Unified Security Exposure Management](https://www.servicenow.com/docs/access?context=unified-security-exposure-management-landing-page&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

