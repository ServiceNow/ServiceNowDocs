---
title: Upgrade information for all Brazil features and products
description: Cumulative release notes summary on upgrade information for Brazil features and products.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/rn-summary-upgrade-info.html
release: brazil
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 9
breadcrumb: [Release notes summaries for Brazil features, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Upgrade information for all Brazil features and products

Cumulative release notes summary on upgrade information for Brazil features and products.

Before you upgrade to Brazil, review the upgrade information for any products you may have. Some products require you to complete specific tasks before you upgrade.

<table id="rn-summary-upgrade-info-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

-   ****

For details on upgrading to the redesigned AI Control Tower experience, see the [AI Control Tower Migration \[KB3144679\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3144679) article in Now Support.


</td></tr><tr><td>

AI Desktop Actions

</td><td>

Upgrade the currently installed AI Desktop Actions Software Installers \(MSIs\) by downloading and installing the newer version of the application. Make sure to close the current execution and close the desktop app before staring the installation for upgrade. For more information, see [Download AI Desktop Actions installer for defined desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

</td></tr><tr><td>

AI Risk and Compliance

</td><td>

-   ****

If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.

**Warning:** If AI Risk and Compliance, EA Workspace, and AI Control Tower Core are upgraded out of sync, business application associations may be lost or unavailable. For more information, see [Enterprise Architecture for AICT plugin installation and upgrade considerations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-ea-common-upgrade-considerations.md) and [Configuring AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/configuring-ai-risk-and-compliance.md).


</td></tr><tr><td>

Accounts Payable Operations

</td><td>

-   ****

If you're an APO user upgrading from a previous release and want to configure the case exclusion rules, copy the out-of-box flow **Create Inquiry Case on Invoice email**, customize it as needed, and activate it.


</td></tr><tr><td>

Change Management

</td><td>

The ITSM Enhanced Security Features plugin \(com.snc.itsm.enhanced\_security\) is now activated automatically when you upgrade to the Brazil release. Previously, the plugin was activated only on new instances. Activating the plugin adds "deny unless authenticated" access control list \(ACL\) rules to several IT Service Management tables.

To revert to the pre-upgrade behavior, contact ServiceNow Support for a list of ACLs to deactivate on specific tables. As a last resort, Support can run a script that deactivates all the new ACLs.

</td></tr><tr><td>

Cloud Cost Management

</td><td>

-   ****
    -   The Cloud Cost Management platform support is available beginning with the Xanadu release. For instructions on upgrading Cloud Cost Management to Brazil, see [Upgrade Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/upgrade-cloud-insights-to-version-3-0.md).
    -   After upgrading to the Brazil release, review and reassess any ACL roles you have customized or deleted to confirm they reflect your expected access settings.
    -   Starting with the Brazil release, the sn\_change\_write role for Insights admin \(insights\_admin\) and Insights owner \(insights\_owner\) has been replaced with the sn\_change\_read role.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   ****

Dynamic IRE is now enabled by default on zBooted instances, while on upgraded instances that are using Static IRE, you can switch into using Dynamic IRE. Key benefits from the new Dynamic IRE engine include CI identification using an improved dynamic process and automatic updates of IRE identification rules during ingestion of data payloads.

For more information, see [Dynamic IRE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/dynamic-ire.md).


</td></tr><tr><td>

Container Vulnerability Response

</td><td>

ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including the Now Assist for Vulnerability Response product name, which will be replaced with ServiceNow Otto for Unified Security Exposure Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

Enhancements to Container Vulnerability Response permit you to see enriched container vulnerability data on data imports from your third-party scanners. After you upgrade, perform a full import to view the features on discovered container image, container image finding, and container vulnerable item records that are described in the following New in the Brazil release section.

If you're currently using Container Vulnerability Response, and you don't intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Container Vulnerability Response and for upgrades to supported third-party integration applications.

For more information about the released versions of the Container Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Brazil release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Core Business Suite

</td><td>

-   ****
    -   The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

        -   Foundation: AI basics to deliver insights
        -   Advanced: AI to boost productivity across relevant use cases
        -   Prime: Act autonomously with all AI assets, and create your own
For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-native-sku-overview.md).

    -   ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

</td></tr><tr><td>

Data Privacy and Discovery

</td><td>

-   ****

Before upgrading to this release, review the product documentation for any breaking changes or upgrade considerations specific to your current version. Test upgrades in a non-production instance first to ensure compatibility with your workflows and customizations.


</td></tr><tr><td>

Domain Separation

</td><td>

-   ****

Before upgrading to this release, review the product documentation for any breaking changes or upgrade considerations specific to your current version. Test upgrades in a non-production instance first to ensure compatibility with your domain policies and customizations. Domain separation policies may require validation or adjustment after upgrade to ensure continued enforcement.


</td></tr><tr><td>

Encryption

</td><td>

-   ****
    -   If you're using scheduled upgrade to upgrade your Edge Encryption proxy from a pre-Brazil release to Brazil, you must meet the following requirements before you attempt the upgrade:
        -   Upgrade the Java version to Java 21 or later.
        -   Ensure you're on Zurich Patch 13 \(ZP13\) or Australia Patch 6 \(AP6\) or later. If you're on an earlier version, scheduled upgrade will not work.
    -   If you're using command-line upgrade, you must upgrade the Java version to Java 21 or later.
    -   Java 17 is required to install Edge Encryption on versions Yokohama through Australia. Prior to upgrading to Brazil, you must upgrade to Java 21. See [Installing Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_InstallEdgeEncryptionProxy.md) for installation details.

</td></tr><tr><td>

Firewall Audits and Reporting

</td><td>

-   ****

Upgrade to the latest version through the ServiceNow Store. Review the release notes for each version before upgrading to understand new features and changes.


</td></tr><tr><td>

Flows, subflows, and actions

</td><td>

-   ****

The Brazil release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/read-only-option.md).


</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   ****
    -   After upgrading to the Brazil release, review and reassess any ACL roles you have customized or deleted to confirm they reflect your expected access settings.
    -   A new system property, **sn\_itam\_restrict\_asset\_read**, controls read access to the Asset \[alm\_asset\] table and its child tables for users with only the snc\_internal role. For more information, see [Asset and CI management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/c_ManagingAssets.md).
    -   A new system property, **sn\_itam\_enable\_manufacturer\_reference\_filter**, controls the Manufacturer field reference filter on model records for the Product Model \[cmdb\_model\] table. When this property is set to **true**, only active manufacturers appear as options. Set this property to **false** to also include inactive manufacturers.

</td></tr><tr><td>

Impact

</td><td>

-   ****

Impact configuration requires a sequence of tasks in a unified registration process. See [Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md).


</td></tr><tr><td>

Incident Management

</td><td>

The ITSM Enhanced Security Features plugin \(com.snc.itsm.enhanced\_security\) is now activated automatically when you upgrade to the Brazil release. Previously, the plugin was activated only on new instances. Activating the plugin adds "deny unless authenticated" access control list \(ACL\) rules to several IT Service Management tables.

To revert to the pre-upgrade behavior, contact ServiceNow Support for a list of ACLs to deactivate on specific tables. As a last resort, Support can run a script that deactivates all the new ACLs.

</td></tr><tr><td>

Kubernetes Visibility Agent \(KVA\)

</td><td>

-   ****

Upgrade to the latest version through the ServiceNow Store. After upgrading the application, update the Kubernetes Visibility Agent \(KVA\) deployment in your clusters to the corresponding version.


</td></tr><tr><td>

Operational Resilience

</td><td>

-   ****

If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.


</td></tr><tr><td>

Platform Analytics experience

</td><td>

-   ****

Core UI dashboards and reports are visible from the Platform Analytics Dashboard and Data visualization libraries.


</td></tr><tr><td>

Playbooks

</td><td>

-   ****

After you upgrade to Brazil, update the Workflow Studio application in the ServiceNow® Store.


</td></tr><tr><td>

Pricing Management

</td><td>

-   ****

If you were using a custom pricing plan before upgrading to the v16.0.1 release, review the new default pricing plan, which is in a Retired state after the upgrade. Decide whether to publish the default plan as is or continue customizing your own plan.


</td></tr><tr><td>

Project Portfolio Management

</td><td>

-   ****

Users who already have Project Portfolio Management can upgrade to PPM Standard. New users must purchase PPM Standard. For more information, see [Activate PPM Standard \(Project Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/t_ActivateProjectPortfolioSuiteWithFinancials.md).


</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in CRM Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

Customers who have not opted into new third-party LLM models may be silently routed to them during skill execution. If the new model is not provisioned or available in the customer's environment, this will result in skill execution failures. Check the models your skills are using in the AI Admin Hub console.

</td></tr><tr><td>

SPM Enterprise-Wide Deployment

</td><td>

-   ****

After upgrading to SPM Enterprise-Wide Deployment v1.0.5, the system administrators loose access to the partitioned-data that they don't have the respective partition role assigned. Set the **sn\_spm\_ewd.allow\_admin\_access\_to\_all\_partitions** system property to `true` if system administrators must continue accessing all the partitioned-data even though they don't have the respective partition role. For details, see [Configure administrator access to all partitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-admin-access-to-all-partitions.md).


</td></tr><tr><td>

Self-service and omnichannel engagement for CSM

</td><td>

-   ****

Introduced dynamic resizing to the Active Call Interaction Control toolbar. Buttons adapt to container width at runtime while keyboard navigation and focus order remain consistent.


</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

-   ****

You can upgrade ServiceNow Otto for Virtual Agent from the ServiceNow Store.


</td></tr><tr><td>

Third-party Risk Management

</td><td>

-   ****

If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.

Enabling the **sn\_vdr\_risk\_asmt.sae\_enabled** property makes the Smart Assessment Engine \(SAE\) the default assessment engine and replaces the legacy experience.

**Warning:** Enabling the **sn\_vdr\_risk\_asmt.sae\_enabled** property is irreversible. Set this property in a non-production instance and test thoroughly before enabling it in production.


</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

-   ****
    -   Changes to the automated correlation rules affect which relationships are created after upgrade. Relationships created under the previous rule logic are preserved and aren't modified.
    -   Creation of potential relationships stops once the potential relationship table reaches its configured volume threshold. Review the threshold configuration after upgrade if your instance ingests high-volume feeds.
    -   The Relate Indicators with Objects Based on Common Observables correlation rule is removed. Relationships it created previously are preserved.

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Brazil features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/release-notes-summaries.md)

