---
title: Upgrade information for all Australia features and products
description: Cumulative release notes summary on upgrade information for Australia features and products.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 25
breadcrumb: [Release notes summaries for Australia features, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Upgrade information for all Australia features and products

Cumulative release notes summary on upgrade information for Australia features and products.

Before you upgrade to Australia, review the upgrade information for any products you may have. Some products require you to complete specific tasks before you upgrade.

<table id="rn-summary-upgrade-info-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

Not applicable.

</td></tr><tr><td>

Application Manager

</td><td>

Application Manager is active by default on instances on the Australia release. Upgrade your instance to Australia patch 4 or later to use the latest features. For information about upgrading your ServiceNow AI Platform instance, see [Prepare your upgrade](../concept/rn-prepare-landing-page.md).

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   If you are currently using Application Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Application Vulnerability Response and for upgrades to supported third-party integration applications.
-   For information about the new features of Vulnerability Response, see the [Vulnerability Response release notes](../security-operations/secops-vuln-resp-rn.md).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Asset Audit Response

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Care Team Operations for Biomed

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td></tr><tr><td>

Care Team Operations for Environmental Services

</td><td>

If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td></tr><tr><td>

Care Team Operations for Facilities

</td><td>

If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td></tr><tr><td>

Care Team Operations for Healthcare IT

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td></tr><tr><td>

Cloud Cost Management 10.0

</td><td>

The Cloud Cost Management platform support is available beginning with the Xanadu release. For instructions on upgrading Cloud Cost Management to Australia, see [Upgrade Cloud Cost Management](https://www.servicenow.com/docs/access?context=upgrade-cloud-insights-to-version-3-0&version=australia&pubname=australia-it-asset-management&ft:locale=en-US).

</td></tr><tr><td>

Configuration Compliance

</td><td>

If you are currently using Configuration Compliance, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Configuration Compliance and for upgrades to supported third-party integration applications.

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=australia&pubname=australia-security-management&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

Due to changes in the Configuration Item \[cmdb\_ci\] table, if you're upgrading to Australia, you might experience an increased upgrade time. To learn more about this change and reducing its impact, see the [Increased Australia Upgrade Time due to cmdb\_ci composite index addition \[KB2588894\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2588894) article in the Now Support Knowledge Base.

If you're upgrading from Xanadu or Yokohama directly to the Australia release, you must run the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job to correctly configure some user roles, such as CMDB Admin and CMDB Editor. For more information about this scheduled job and its use, see the [CMDB Zurich release notes](https://www.servicenow.com/docs/bundle/zurich-release-notes/page/release-notes/now-platform-capabilities/cmdb-rn.html).

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

Enhancements to Container Vulnerability Response permit you to see enriched container vulnerability data on data imports from your third-party scanners. After you upgrade, you must perform a full import to view the features on discovered container image, container image finding, and container vulnerable item records that are described in the following New in the Australia release section.

If you're currently using Container Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Container Vulnerability Response and for upgrades to supported third-party integration applications.

For more information about the released versions of the Container Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Core Business Suite

</td><td>

-   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


</td></tr><tr><td>

Customer Engagement Sequences

</td><td>

If you configured sequences with the Schedule call activity on a release before Zurich, the activity is now labeled **Schedule call - Deprecated** in the activity picker in Workflow Studio. Existing sequences continue to work, but the Call icon ![](../../reuse/icons/product-icons/phone-fill-24.svg) doesn't appear on the **Callback number** field on the Sequence Steps page during runtime. To enable the click-to-call capability, update the Customer Engagement Sequences application to use the new Schedule call activity.

</td></tr><tr><td>

Employee Center

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Employee Center Pro

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Flows, Subflows, and Actions

</td><td>

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see [Restore save as you go functionality](https://www.servicenow.com/docs/access?context=restore-save-as-you-go-functionality&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Generative AI Controller

</td><td>

Generative AI Controller is installed or updated when you install or update a Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) or open a support case.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   To enhance security and manage admin access precisely, the granular admin roles are now installed. These roles replace broad admin checks by assigning specific privileges based on user tasks, rather than granting full admin access:
    -   sn\_hamp.ham\_system\_admin: Provides access to HAM licensing, HAM Guided Setup, HAM application properties and system properties, and a few tables.
    -   sn\_hamp.ham\_asn\_admin: Provides access to the Advanced Shipment Notification \(ASN\) feature.
    -   asset\_integration\_admin: Provides access to Standard hardware Zero touch request and carrier integration features, and shipment tables.
    -   asset\_system\_admin: Provides access to asset job log, content audit, transfer order, expense management, and model management.
    -   asset\_task\_admin: Provides access to asset tasks.
    -   procurement\_system\_admin: Provides access to procurement module, tables, and tasks.
    -   contract\_system\_admin: Provides access to contract module, tables, and tasks.
    -   asset\_licensing\_admin: Provides access to the ITAM licensing module.
    -   asset\_recommendation\_admin: Provides access to recommendation actions.
-   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Healthcare Operations Core

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td></tr><tr><td>

Impact

</td><td>

The Impact Store Application configuration requires a sequence of tasks in a unified registration process. See [Configure the Impact Store Application](https://www.servicenow.com/docs/access?context=configuring-impact-platform&version=australia&pubname=australia-impact&ft:locale=en-US).

</td></tr><tr><td>

Instance Data Replication

</td><td>

Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table that are created before the upgrade are automatically truncated.

</td></tr><tr><td>

Key Management

</td><td>

-   In pre-Zurich releases, the GlideEncrypter API used the three-key Triple Data Encryption Standard \(3DES\) encryption standard, which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Australia release in preparation for a full deprecation of GlideEncrypter/3DES in the future:
    -   New Australia instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Australia instances, you can still GlideEncrypter, which has been updated to use AES256-GCM encryption via the Key Management Framework.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td></tr><tr><td>

MID Server

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 21.0.7.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information.

For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr><tr><td>

Now Assist

</td><td>

If you customized actions on the user interface or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_onlyand client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html).

</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

To enable Now Assist to provide detailed descriptions of CIs and classes, you must activate the 'External Content Connectors' plugin, install the ‘ServiceNow Product Documentation’ connector, and then crawl the product documentation. For configuration instructions, see [Configure the CI form contextual help skill](https://www.servicenow.com/docs/access?context=na-cmdb-skill-form-sense-config&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Now Assist for Creator

</td><td>

Australia early availability \(March\)

-   To upgrade the Build Agent application, upgrade the Now Assist for Creator application \(sn\_now\_creator\), which includes the Build Agent Pro plugin \(sn\_build\_agent\_pro\). To upgrade the Build Agent \(Trial\) app, upgrade the sn\_build\_agent plugin.

</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

Now Assist for Employee Center Pro only provides employee or requester conversations and might require other Now Assist products to deliver AI agents or other related features.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

To use the Knowledge Article Advanced Editor page in the generate a knowledge article skill, you must activate the knowledge content recommendation skill. Follow these steps to activate the skill.

1.  Go to **Admin** &gt; **Now Assist Admin**.
2.  Select **Now Assist Skills**.
3.  Select **Platform**.
4.  Select **Knowledge**.
5.  Make sure the knowledge content recommendation skill is active.

The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. When you upgrade to [Australia Patch 1](../quality/australia-patch-1.md), if you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

To access the new AI native experience in the Vulnerability Response or Unified Security Exposure Management \(USEM\) workspaces, you must upgrade to the Australia release.

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


For existing customers who have not upgraded to Australia, generative AI skills, agents, and workflows are supported in the Vulnerability Response workspaces and are included with the Now Assist for Vulnerability Response application.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>



</td></tr><tr><td>

Operational Resilience

</td><td>

Beginning with Operational Resilience release 22.0.x, the following scheduled jobs are deactivated for new installations by default:

-   **Calculate red flags for CSDM and dependencies**
-   **Update CSDM and other dependencies**

For existing installations, these jobs retain their current active or inactive state.

</td></tr><tr><td>

Performance Analyzer

</td><td>

Starting with the Zurich release, Performance Analyzer is available on your instance automatically. For access to Performance Analyzer for earlier instances, install Performance Analyzer from the ServiceNow® Store.

</td></tr><tr><td>

Platform Analytics experience

</td><td>

After upgrading, only admins can create Core UI analytics objects: reports, Performance Analytics widgets, responsive dashboards, and interactive filters. Other users can still view and edit Core UI objects but can create only Platform Analytics objects, such as data visualizations.

When upgrading, the published status on all Core UI reports changes to **false**, making them unpublished.

After upgrading, the Analytics Hub isn't available. Links to the Analytics Hub are redirected to KPI Details.

</td></tr><tr><td>

Playbook

</td><td>

After you upgrade to Australia, update the Workflow Studio application in the ServiceNow Store.

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

Pricing Management v16.0.0 provides a default pricing plan that includes changes to support pricing strategies introduced in this release. If you have been using a custom pricing plan from an earlier release, after upgrading to Pricing Management v16.0.0, the default pricing plan is in a Retired state. Determine whether you want to publish the default pricing plan for use or customize it.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

</td></tr><tr><td>

RPA Hub

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Australia.

Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Australia.

Before upgrading RPA Hub to Australia, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

After you upgrade to Australia, the bot process definitions change to the new structure, which is the bot process configuration.

Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Australia without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td></tr><tr><td>

ReleaseOps

</td><td>

If you have customized the ReleaseOps sample playbooks, the runbook task playbook activity will not automatically populate when you upgrade to Australia.

</td></tr><tr><td>

SQL API

</td><td>

ServiceNow provided customers with a free SOAP‑based ODBC client. If you have an active RaptorDB Professional entitlement, you can migrate to the REST‑based SQL API client by completing the required configuration on both the server and client sides. For more information, see [Configuring SQL API](https://www.servicenow.com/docs/access?context=configuring-sql-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Service Exchange \(formerly Service Bridge\)

</td><td>

**Important:** Do not upgrade your ServiceNow® instance to the Australia release if you rely on Service Exchange. A known RPS issue prevents Service Exchange from functioning correctly. Proceed with the upgrade only after Australia Patch 1 becomes available.

-   Service Exchange version 2.x.x, which was first released with the Xanadu release, doesn’t support migration of Service Exchange \(Legacy\) versions.

Service Exchange \(Legacy\) version: Before you upgrade to the Australia release, consult the [Service Exchange for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to find out how to migrate your configuration data.

-   Service Exchange version 1.x.x: When upgrading, consult the [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) article in the Now Support Knowledge Base to find out how to migrate your Service Exchange applications.
-   Service Exchange version 2.x.x: New entitlements that require the latest compatibility version cannot be activated until both consumers and providers upgrade to Service Exchange version 2.x.x. New entitlements configured with a lower compatibility version can be activated. Older active entitlements continue to work but new ones can’t be activated.
-   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility. If the versions diverge, a scan check will report version mismatches and the Health Dashboard will show a version mismatch issue. After upgrading, run and validate the post‑upgrade scan suite to identify and resolve any post‑upgrade issues.
-   If you have upgraded to Service Exchange version 2.0.55 before upgrading the platform to the Australia release and your instance has Sales and Order Management plug-in version 1.0.4 installed, the new Deny ACLs aren't installed. After upgrading to the Australia release, select Repair to reinstall the Service Exchange application to ensure Deny ACLs are installed.
-   When you install the Service Exchange application, the Service Exchange Global script include is automatically installed or updated on the following platform versions:
    -   Yokohama
    -   Zurich
    -   Australia

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

The dynamic schema application framework was revised in the Zurich release. If you implemented dynamic schema in the Xanadu or Yokohama releases, the application is automatically migrated to a new framework as part of the upgrade to releases starting with the Zurich release. For details on the migration and steps you might need to perform, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

ServiceNow IDE

</td><td>

ServiceNow IDE version 3.2.3 is active by default on instances on the Australia release. Update to ServiceNow IDE version 4.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Install or update the ServiceNow IDE](https://www.servicenow.com/docs/access?context=install-servicenow-ide&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr><tr><td>

ServiceNow SDK

</td><td>

To upgrade to the latest version of the ServiceNow SDK globally or within an application, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US).

ServiceNow SDK version 4.4 supports integration with ServiceNow instances beginning with the Washington DC release.

On Windows systems, after upgrading to ServiceNow SDK version 4.3 or later, existing stored credentials aren’t supported due to the deprecation of Keytar. Users on Windows systems must add their user credentials again using the `now-sdk auth --add` command to authenticate with instances. For more information, see [Authenticating to a ServiceNow instance with the ServiceNow SDK](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Important:** For minor releases of the ServiceNow SDK, see the [ServiceNow SDK release notes](https://github.com/ServiceNow/sdk/releases) on GitHub.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

ServiceNow Studio no longer has to be downloaded from the ServiceNow Store. It’s available on the ServiceNow AI Platform by default.

</td></tr><tr><td>

ServiceNow Vault

</td><td>

ServiceNow Vault is a bundle of the following products:

-   [ServiceNow Vault](https://www.servicenow.com/docs/access?context=servicenow-vault-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Data Discovery](https://www.servicenow.com/docs/access?context=data-discovery-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Zero Trust Access \(ZTA\)](https://www.servicenow.com/docs/access?context=session-access&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Field Encryption](https://www.servicenow.com/docs/access?context=field-encryption&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Code Signing](https://www.servicenow.com/docs/access?context=code-signing-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [Log Export Service \(LES\)](https://www.servicenow.com/docs/access?context=les-intro&version=australia&pubname=australia-platform-security&ft:locale=en-US)

</td></tr><tr><td>

Source-to-Pay Operations Integrations

</td><td>

**Important:** Due to a performance issue identified with the upgrade fix script, the sourcing fix script has been modified. This script will no longer execute automatically during the upgrade process. Instead, it is now delivered as an on-demand job. Administrators must manually execute this job outside of business hours after the upgrade is complete.

</td></tr><tr><td>

Subscription Management

</td><td>

Subscription Management version 6.1 is active by default on all instances of the Australia release. Update to Subscription Management version 6.1 or later to use the latest features. For more information about updating Subscription Management, see [Update an application or plugin](https://www.servicenow.com/docs/access?context=update-application-app-mgr&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Third-party Risk Management

</td><td>

If you’re a VRM user upgrading to TPRM and upgrading to Australia from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Xanadu to Yokohama, Yokohama to Zurich, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](../governance-risk-compliance/grc-tprm-upgrade-info.md).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

</td></tr><tr><td>

UI Builder

</td><td>

Saving section for later.

</td></tr><tr><td>

Vulnerability Response

</td><td>

If you're currently using Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Vulnerability Response and for upgrades to supported third-party integration applications.

For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Australia features](../release-notes-summaries.md)

