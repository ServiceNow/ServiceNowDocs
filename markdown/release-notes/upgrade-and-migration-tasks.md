---
title: Pre- and post-upgrade tasks for various products
description: In preparation for your upgrade, review the upgrade and migration tasks for various applications and features. Plan to complete these tasks, when applicable, before or after the upgrade is complete.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 119
breadcrumb: [Prepare your upgrade, Yokohama release notes]
---

# Pre- and post-upgrade tasks for various products

In preparation for your upgrade, review the upgrade and migration tasks for various applications and features. Plan to complete these tasks, when applicable, before or after the upgrade is complete.

## Prepare your instance for a smoother upgrade

![Pre-upgrade tasks, upgrade, post-upgrade tasks](../image/upgrade-migration-tasks.png)

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

## Upgrade and migration tasks

**Important:** For any changes in the upgrade procedure for self-hosted customers, see [KB0563844](https://hi.service-now.com/kb_view.do?sysparm_article=KB0563844) for details.

<table class="custom-rows"><thead><tr><th class="filter">

Product

</th><th>

Release notes

</th><th class="filter">

Family

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

Not applicable.

</td><td>

Australia

</td></tr><tr><td>

Application Manager

</td><td>

Application Manager is active by default on instances on the Australia release. Upgrade your instance to Australia patch 4 or later to use the latest features. For information about upgrading your ServiceNow AI Platform instance, see [Prepare your upgrade](https://servicenow.com/docs/access?context=rn-prepare-landing-page&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   If you are currently using Application Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Application Vulnerability Response and for upgrades to supported third-party integration applications.
-   For information about the new features of Vulnerability Response, see the [Vulnerability Response release notes](https://servicenow.com/docs/access?context=secops-vuln-resp-rn&family=australia&ft:locale=en-US).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Australia

</td></tr><tr><td>

Asset Audit Response

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Care Team Operations for Biomed

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

 If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td><td>

Australia

</td></tr><tr><td>

Care Team Operations for Environmental Services

</td><td>

If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td><td>

Australia

</td></tr><tr><td>

Care Team Operations for Facilities

</td><td>

If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td><td>

Australia

</td></tr><tr><td>

Care Team Operations for Healthcare IT

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

 If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td><td>

Australia

</td></tr><tr><td>

Cloud Cost Management 10.0

</td><td>

The Cloud Cost Management platform support is available beginning with the Xanadu release. For instructions on upgrading Cloud Cost Management to Australia, see [Upgrade Cloud Cost Management](https://servicenow.com/docs/access?context=upgrade-cloud-insights-to-version-3-0&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Configuration Compliance

</td><td>

If you are currently using Configuration Compliance, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Configuration Compliance and for upgrades to supported third-party integration applications.

 The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=australia&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

 For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Australia

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

Due to changes in the Configuration Item \[cmdb\_ci\] table, if you're upgrading to Australia, you might experience an increased upgrade time. To learn more about this change and reducing its impact, see the [Increased Australia Upgrade Time due to cmdb\_ci composite index addition \[KB2588894\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2588894) article in the Now Support Knowledge Base.

 If you're upgrading from Xanadu or Yokohama directly to the Australia release, you must run the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job to correctly configure some user roles, such as CMDB Admin and CMDB Editor. For more information about this scheduled job and its use, see the [CMDB Zurich release notes](https://www.servicenow.com/docs/bundle/zurich-release-notes/page/release-notes/now-platform-capabilities/cmdb-rn.html).

 The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

Enhancements to Container Vulnerability Response permit you to see enriched container vulnerability data on data imports from your third-party scanners. After you upgrade, you must perform a full import to view the features on discovered container image, container image finding, and container vulnerable item records that are described in the following New in the Australia release section.

 If you're currently using Container Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Container Vulnerability Response and for upgrades to supported third-party integration applications.

 For more information about the released versions of the Container Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Australia

</td></tr><tr><td>

Core Business Suite

</td><td>

-   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).
-   The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
For more information, see [ServiceNow product tiers](https://servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US).


</td><td>

Australia

</td></tr><tr><td>

Customer Engagement Sequences

</td><td>

If you configured sequences with the Schedule call activity on a release before Zurich, the activity is now labeled **Schedule call - Deprecated** in the activity picker in Workflow Studio. Existing sequences continue to work, but the Call icon ![](../../../reuse/icons/product-icons/phone-fill-24.svg) doesn't appear on the **Callback number** field on the Sequence Steps page during runtime. To enable the click-to-call capability, update the Customer Engagement Sequences application to use the new Schedule call activity.

</td><td>

Australia

</td></tr><tr><td>

Employee Center Pro

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Employee Center

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Flows, Subflows, and Actions

</td><td>

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see [Restore save as you go functionality](https://servicenow.com/docs/access?context=restore-save-as-you-go-functionality&family=australia&ft:locale=en-US).

 The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Generative AI Controller

</td><td>

Generative AI Controller is installed or updated when you install or update a Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) or open a support case.

</td><td>

Australia

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
-   The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Healthcare Operations Core

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

 If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td><td>

Australia

</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

</td><td>

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

 If you have the feature administrator role you can now complete tasks that were initially reserved for users with the broader administrator role.

</td><td>

Australia

</td></tr><tr><td>

Impact

</td><td>

The Impact Store Application configuration requires a sequence of tasks in a unified registration process. See [Configure the Impact Store Application](https://servicenow.com/docs/access?context=configuring-impact-platform&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Instance Data Replication

</td><td>

Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table that are created before the upgrade are automatically truncated.

</td><td>

Australia

</td></tr><tr><td>

Key Management

</td><td>

-   In pre-Zurich releases, the GlideEncrypter API used the three-key Triple Data Encryption Standard \(3DES\) encryption standard, which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Australia release in preparation for a full deprecation of GlideEncrypter/3DES in the future:
    -   New Australia instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Australia instances, you can still GlideEncrypter, which has been updated to use AES256-GCM encryption via the Key Management Framework.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td><td>

Australia

</td></tr><tr><td>

MID Server

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=australia&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 21.0.7.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://servicenow.com/docs/access?context=mid-startup-fails&family=australia&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=australia&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td><td>

Australia

</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

To enable Now Assist to provide detailed descriptions of CIs and classes, you must activate the 'External Content Connectors' plugin, install the ‘ServiceNow Product Documentation’ connector, and then crawl the product documentation. For configuration instructions, see [Configure the CI form contextual help skill](https://servicenow.com/docs/access?context=na-cmdb-skill-form-sense-config&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Now Assist for Creator

</td><td>

Australia early availability \(March\)

-   To upgrade the Build Agent application, upgrade the Now Assist for Creator application \(sn\_now\_creator\), which includes the Build Agent Pro plugin \(sn\_build\_agent\_pro\). To upgrade the Build Agent \(Trial\) app, upgrade the sn\_build\_agent plugin.

</td><td>

Australia

</td></tr><tr><td>

Now Assist for Employee Center Pro

</td><td>

Now Assist for Employee Center Pro only provides employee or requester conversations and might require other Now Assist products to deliver AI agents or other related features.

</td><td>

Australia

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

To use the Knowledge Article Advanced Editor page in the generate a knowledge article skill, you must activate the knowledge content recommendation skill. Follow these steps to activate the skill.

1.  Go to **Admin** &gt; **Now Assist Admin**.
2.  Select **Now Assist Skills**.
3.  Select **Platform**.
4.  Select **Knowledge**.
5.  Make sure the knowledge content recommendation skill is active.

 The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. When you upgrade to [Australia Patch 1](https://servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US), if you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

To access the new AI native experience in the Vulnerability Response or Unified Security Exposure Management \(USEM\) workspaces, you must upgrade to the Australia release.

-   **[ServiceNow product tiers](https://servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


 For existing customers who have not upgraded to Australia, generative AI skills, agents, and workflows are supported in the Vulnerability Response workspaces and are included with the Now Assist for Vulnerability Response application.

</td><td>

Australia

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>



</td><td>

Australia

</td></tr><tr><td>

Now Assist

</td><td>

If you customized actions on the user interface or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

 The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform. These changes include a new read\_only\_option field with granular control levels, including strict\_read\_onlyand client\_script\_modifiable. The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen instance security while preserving flexibility. If you have custom client scripts that modify read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to the [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) article in the Now Support Knowledge Base to identify affected fields and adjust the settings.

 The existing access control lists \(ACLs\) have been updated to replace the admin role with purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API is replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the admin role in the code have been substituted with the granular roles for authorization use cases. For more information, see [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html).

</td><td>

Australia

</td></tr><tr><td>

Operational Resilience

</td><td>

Beginning with Operational Resilience release 22.0.x, the following scheduled jobs are deactivated for new installations by default:

-   **Calculate red flags for CSDM and dependencies**
-   **Update CSDM and other dependencies**

For existing installations, these jobs retain their current active or inactive state.

</td><td>

Australia

</td></tr><tr><td>

Performance Analyzer

</td><td>

Starting with the Zurich release, Performance Analyzer is available on your instance automatically. For access to Performance Analyzer for earlier instances, install Performance Analyzer from the ServiceNow® Store.

</td><td>

Australia

</td></tr><tr><td>

Platform Analytics experience

</td><td>

After upgrading, only admins can create Core UI analytics objects: reports, Performance Analytics widgets, responsive dashboards, and interactive filters. Other users can still view and edit Core UI objects but can create only Platform Analytics objects, such as data visualizations.

 When upgrading, the published status on all Core UI reports changes to **false**, making them unpublished.

 After upgrading, the Analytics Hub isn't available. Links to the Analytics Hub are redirected to KPI Details.

</td><td>

Australia

</td></tr><tr><td>

Playbook

</td><td>

After you upgrade to Australia, update the Workflow Studio application in the ServiceNow Store.

</td><td>

Australia

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

Pricing Management v16.0.0 provides a default pricing plan that includes changes to support pricing strategies introduced in this release. If you have been using a custom pricing plan from an earlier release, after upgrading to Pricing Management v16.0.0, the default pricing plan is in a Retired state. Determine whether you want to publish the default pricing plan for use or customize it.

</td><td>

Australia

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

</td><td>

Australia

</td></tr><tr><td>

RPA Hub

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://servicenow.com/docs/access?context=download-installer-rpa&family=australia&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Australia.

 Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Australia.

 Before upgrading RPA Hub to Australia, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=australia&ft:locale=en-US).

 After you upgrade to Australia, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Australia without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td><td>

Australia

</td></tr><tr><td>

ReleaseOps

</td><td>

If you have customized the ReleaseOps sample playbooks, the runbook task playbook activity will not automatically populate when you upgrade to Australia.

</td><td>

Australia

</td></tr><tr><td>

SQL API

</td><td>

ServiceNow provided customers with a free SOAP‑based ODBC client. If you have an active RaptorDB Professional entitlement, you can migrate to the REST‑based SQL API client by completing the required configuration on both the server and client sides. For more information, see [Configure](https://servicenow.com/docs/access?context=configuring-sql-api&family=australia&ft:locale=en-US).

</td><td>

Australia

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

</td><td>

Australia

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

The dynamic schema application framework was revised in the Zurich release. If you implemented dynamic schema in the Xanadu or Yokohama releases, the application is automatically migrated to a new framework as part of the upgrade to releases starting with the Zurich release. For details on the migration and steps you might need to perform, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

 The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

ServiceNow IDE

</td><td>

ServiceNow IDE version 3.2.3 is active by default on instances on the Australia release. Update to ServiceNow IDE version 4.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Install or update the ServiceNow IDE](https://servicenow.com/docs/access?context=install-servicenow-ide&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

ServiceNow SDK

</td><td>

To upgrade to the latest version of the ServiceNow SDK globally or within an application, see [Upgrade the ServiceNow SDK](https://servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=australia&ft:locale=en-US).

 ServiceNow SDK version 4.4 supports integration with ServiceNow instances beginning with the Washington DC release.

 On Windows systems, after upgrading to ServiceNow SDK version 4.3 or later, existing stored credentials aren’t supported due to the deprecation of Keytar. Users on Windows systems must add their user credentials again using the `now-sdk auth --add` command to authenticate with instances. For more information, see [Authenticate](https://servicenow.com/docs/access?context=authenticate-instance-now-sdk&family=australia&ft:locale=en-US).

**Important:** For minor releases of the ServiceNow SDK, see the [ServiceNow SDK release notes](https://github.com/ServiceNow/sdk/releases) on GitHub.

</td><td>

Australia

</td></tr><tr><td>

ServiceNow Studio

</td><td>

ServiceNow Studio no longer has to be downloaded from the ServiceNow Store. It’s available on the ServiceNow AI Platform by default.

</td><td>

Australia

</td></tr><tr><td>

ServiceNow Vault

</td><td>

ServiceNow Vault is a bundle of the following products:

-   [ServiceNow Vault](https://servicenow.com/docs/access?context=servicenow-vault-landing&family=australia&ft:locale=en-US)
-   [Data Discovery](https://servicenow.com/docs/access?context=data-discovery-landing&family=australia&ft:locale=en-US)
-   [Data Privacy](https://servicenow.com/docs/access?context=data-privacy-landing&family=australia&ft:locale=en-US)
-   [Zero Trust Access](https://servicenow.com/docs/access?context=session-access&family=australia&ft:locale=en-US)
-   [Field Encryption](https://servicenow.com/docs/access?context=field-encryption&family=australia&ft:locale=en-US)
-   [Code Signing](https://servicenow.com/docs/access?context=code-signing-landing&family=australia&ft:locale=en-US)
-   [Log Export Service \(LES\)](https://servicenow.com/docs/access?context=les-intro&family=australia&ft:locale=en-US)

</td><td>

Australia

</td></tr><tr><td>

Source-to-Pay Operations Integrations

</td><td>

**Important:** Due to a performance issue identified with the upgrade fix script, the sourcing fix script has been modified. This script will no longer execute automatically during the upgrade process. Instead, it is now delivered as an on-demand job. Administrators must manually execute this job outside of business hours after the upgrade is complete.

</td><td>

Australia

</td></tr><tr><td>

Subscription Management

</td><td>

Subscription Management version 6.1 is active by default on all instances of the Australia release. Update to Subscription Management version 6.1 or later to use the latest features. For more information about updating Subscription Management, see [Update an app or plugin](https://servicenow.com/docs/access?context=update-application-app-mgr&family=australia&ft:locale=en-US).

</td><td>

Australia

</td></tr><tr><td>

Third-party Risk Management

</td><td>

If you’re a VRM user upgrading to TPRM and upgrading to Australia from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Xanadu to Yokohama, Yokohama to Zurich, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

 After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

 For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=australia&ft:locale=en-US).

 For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

</td><td>

Australia

</td></tr><tr><td>

UI Builder

</td><td>

Saving section for later.

</td><td>

Australia

</td></tr><tr><td>

Vulnerability Response

</td><td>

If you're currently using Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Vulnerability Response and for upgrades to supported third-party integration applications.

 For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Australia release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base

</td><td>

Australia

</td></tr><tr><td>

AI Search

</td><td>

[Washington DC Patch 9](https://servicenow.com/docs/access?context=washingtondc-patch-9&family=washingtondc&ft:locale=en-US):

-   After you upgrade to Washington DC Patch 9 from an earlier release, make knowledge block content searchable by reindexing all your indexed sources that include knowledge articles. For details on reindexing, see [Index or reindex an indexed source](https://servicenow.com/docs/access?context=index-single-source-ais&family=washingtondc&ft:locale=en-US) or [Index or reindex multiple indexed sources](https://servicenow.com/docs/access?context=index-multiple-sources-ais&family=washingtondc&ft:locale=en-US).

 Washington DC:

-   When you upgrade to Washington DC, AI Search automatically updates your existing Genius Result configurations to use the new [AI Search Genius Result Configuration form](https://servicenow.com/docs/access?context=genius-result-cfg-form-ais&family=washingtondc&ft:locale=en-US) fields. This update procedure makes the following changes:
    -   Removes existing **Genius result answer type** field values.
    -   Migrates **Genius result logic** field values to the new **AI Search request processor** and **AI Search response processor** fields as appropriate.
-   After you upgrade your instance to Washington DC, AI Search retains the value that you previously set for the **Boolean search operator to use when a search query includes multiple terms** \(**glide.ais.query.search\_operator**\) system property. To gain the benefits of the new enhanced query mode for multi-term searches, set this system property's value to **AND then OR 2+ key terms**. For details on AI Search system properties, see [AI Search system properties](https://servicenow.com/docs/access?context=system-properties-ais&family=washingtondc&ft:locale=en-US).
-   Starting in Washington DC, the User \[sys\_user\] table defaults to sorting indexed records by their sys\_created\_on dates instead of sorting them by their sys\_updated\_on dates. This change requires reindexing of the User table indexed source for AI Search, which can be time-consuming. When you upgrade to Washington DC from a previous family release, AI Search does not automatically reindex the User table indexed source. If you need to be able to search the latest configuration for user records, you can [manually reindex](https://servicenow.com/docs/access?context=index-single-source-ais&family=washingtondc&ft:locale=en-US) the User table indexed source, which may take some time. Otherwise, AI Search will reindex individual User table records as they're updated until all records have been reindexed.

</td><td>

Washington DC

</td></tr><tr><td>

Automated Test Framework

</td><td>

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

 The tests can produce a pass result only when you run them on a base system without any customizations and with the default demo data that is provided with the application or feature plugin. To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data. For more information, see [Available quick start tests by application or feature](https://servicenow.com/docs/access?context=available-quick-start-tests&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

Business Continuity Management

</td><td>

After upgrading to the Washington DC release, you must note the following important information for the existing business impact analyses, business continuity plans, and events:

-   For business impact analyses, the Source column in the dependency assessment is renamed to Primary source and the **BCM** source is renamed to **Manual** for manually added dependencies following an upgrade. When you select the **Update dependencies** button, the system adds the CMDB dependencies.
-   For business continuity plans, the Source column is renamed to Primary source following an upgrade. When you select the **Update dependencies** button, the system adds the CMDB and BIA dependencies. To maintain compatibility with the previous releases, the BCM administrator can configure the sources and keep only the BIA upstream dependency and BIA downstream dependencies as the sources in the updated configuration.
-   For events and exercises, when you select the **Update dependencies** button, the system adds the CMDB, BIA, and Business Continuity Planning \(BCP\) dependencies after an upgrade. To maintain compatibility with the previous releases, the BCM administrator can configure the sources and keep only the BIA upstream dependency and BIA downstream dependencies as the sources in the updated configuration.

</td><td>

Washington DC

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   The column **product\_instance\_id** has been added to the base Configuration Item \[cmdb\_ci\] table to support the new product instance identifier \(PID\), which enables the lookup and linking of any pre-existing related assets, CIs, and Install Base Items \(IBI\). For more information about the impact of that change during upgrade and how to minimize that impact, see the [Upgrade impact of CMDB\_CI schema changes for Washington release \[KB1534035\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB1534035) knowledge base article.
-   If you enable CMDB 360 for the first time after upgrading to the Washington DC release, to enable the capture of CMDB 360 data for CIs from non-CMDB classes \(classes not derived from the Configuration Item \[cmdb\_ci\] class\) you must set the **glide.identification\_engine.multisource\_non\_cmdb\_ci\_enabled** system property to true.
-   If you have been using the legacy Data Certification application on Core UI, then any associated definitions won’t be available in the new implementation of Data Certification in CMDB Workspace. After upgrading to the Washington DC release and to CMDB Workspace version 6.0, you can convert definitions created in the legacy Data Certification application into draft Data Manager Certification policies in CMDB Workspace. For more information, see [.](https://servicenow.com/docs/access?context=convert-data-cert-definitions&family=washingtondc&ft:locale=en-US)

</td><td>

Washington DC

</td></tr><tr><td>

Core ServiceNow AI Platform

</td><td>

Previously, if a transaction was canceled, certain auditable operations were not being recorded. This behavior of missing audit records is because the platform executes some operations between the record change and is canceled before audit creation. But now, audits are created immediately after the record is changed, reducing the chance of a canceled transaction aborting the operation before the audit is recorded. To facilitate this update, audits are now recorded in the same thread as the transaction. Earlier audits were created in a background thread.

 This change redefines the default value of the `glide.db.audit.lazy` property from true to false. Ideally, this property is not defined in the Properties table, which means that the majority of instances start using the new default value and behavior with the Washington DC release. On some instances, this property may have been inserted with the value set to true, which means that these instances won’t be able to use this change to audit behavior. Delete this property to leverage this update.

</td><td>

Washington DC

</td></tr><tr><td>

Encryption Key Management

</td><td>

If you upgrade your instance to Washington DC but don’t upgrade your MID Server, Secrets Management authentication fails. Avoid authentication failures by upgrading your MID Server to Washington DC. If you can’t upgrade, you must turn off authentication until MID Server is upgraded to Washington DC to avoid authentication failures.

 For details on MID Server upgrades, see [MID Server upgrades](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

After you upgrade to Washington DC, the model\_component field isn't available in the Enterprise asset \[sn\_ent\_asset\] table. Instead, a new model\_component\_id field is available in the Asset \[alm\_asset\] table. The ENT - Migrate to new model component script moves the existing model\_component field data to the model\_component\_id field.

 Note the following upgrade scenarios for the Total Cost of Ownership \(TCO\) of assets:

-   Upgrade works for all Enterprise Asset Management flow tasks
-   You must have task rate cards for each workflow task.
-   The TCO upgrade populates the **Asset** and **Expense category** fields on expense lines corresponding to each task.
-   Expense category is populated based on the expense lines and the source of the expense line.
-   You need to populate the TCO benchmark cost and the TCO benchmark threshold field on all existing models manually or using the bulk import functionality.
-   TCO upgrade populates following fields on asset forms:
    -   **Asset end of useful life**: The created date plus the useful life in months.
    -   **Asset first used date**: The created date.
    -   **Asset TCO**: The aggregated sum of all the expense lines related to the asset. For simple assets, Asset TCO is the aggregated sum of expense lines under it. For complex assets, Asset TCO is the aggregated sum of expense lines of the parent as well as its child assets.

</td><td>

Washington DC

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

During the upgrade to Washington DC, the Financial Services Operations Core plugin reparents the following tables:

**Note:** You may experience a longer time for the upgrade to complete if your upgraded instance has a large number of records.

-   The Service Definition \[sn\_bom\_service\_definition\] table extends from the Service Definition \[sn\_case\_type\_selection\] table instead of the Request Definition \[sn\_ind\_request\_definition.
-   The Financial task \[sn\_bom\_task\] table extends from the Customer Service Task \[sn\_customerservice\_task\] table instead of the Global Task \[task\] table.
-   The Policy Participant \[sn\_bom\_policy\_participant\] table extends from the Sold Product Related Party \[sn\_install\_base\_sold\_product\_related\_party\] table.

Reparenting enables leveraging of the benefits and advancements introduced by ServiceNow® Customer Service Management \(CSM\) while preserving the functionality of existing applications.

</td><td>

Washington DC

</td></tr><tr><td>

Hardware Asset Management 10.0.0

</td><td>

After your upgrade to Washington DC, keep in mind the following upgrade scenarios for the Total Cost of Ownership \(TCO\) of assets:

-   Upgrade works for all Hardware Asset Management flow tasks.
-   You must have task rate cards for each workflow task.
-   TCO upgrade populates an asset and expense category field on the expense line corresponding to each task.
-   Expense category is populated based on the expense lines and the source of the expense line.
-   You must populate the TCO benchmark cost and the TCO benchmark threshold field on all existing models manually or using the bulk import functionality.
-   TCO upgrade populates the following fields on assets:
    -   Asset end of useful life: Created date along with useful life in months.
    -   Asset first used date: Same as the created date.
    -   Asset TCO: Aggregated sum of all the expense lines related to the asset. For simple assets, Asset TCO is the aggregated sum of expense lines under it. For complex assets, Asset TCO is the aggregated sum of expense lines of the parent as well as its child assets.

</td><td>

Washington DC

</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

</td><td>

During the upgrade to Washington DC, the Healthcare sold product \[sn\_hcls\_sold\_product\] parent table changes to Install base item \[sn\_install\_base\_item\] for the following tables:

-   Member Plan \[sn\_hcls\_member\_plan\]
-   Medication \[sn\_hcls\_medication\]
-   Immunization \[sn\_hcls\_immunization\]
-   Enrolled Program \[sn\_hcls\_enrolled\_program\]
-   Enrolled Program Service \[sn\_hcls\_enrolled\_program\_service\]

 In addition, the following tables have had their parent tables removed and are standalone tables:

-   Healthcare Organization\[sn\_hcls\_organization\]
-   Healthcare Location\[sn\_hcls\_location\]
-   Practitioner Location\[sn\_hcls\_practitioner\_facility\]

This reparenting enables customers to use the organizations and location tables for a broader set of use cases.

 Existing data is migrated in the following manner so that existing functionality isn’t impacted:

1.  Reference of location field in sn\_hcls\_immunization updated to use cmn\_location.
2.  All data is moved from Healthcare Sold Product to Install Base Item tables.
3.  Rows in the affected Install Base Item are populated based on the source\_task value from the Healthcare Sold Product.
4.  The state of sn\_hcls\_enrolled\_program and sn\_hcls\_enrolled\_program\_service are copied from hcls\_state.
5.  All data moves to the standalone tables of Healthcare Organization, Healthcare Location, and Practitioner Location.
    1.  The script creates records in the Business Location table for existing records in the Healthcare Organization table to form a 1:1 reference.
    2.  Records that refer to a service organization are updated with a reference to the appropriate business location.
    3.  Any practitioner who has a record in the practitioner location will have a record created in the Service Organization Member table with the appropriate business location.
    4.  Records that contain healthcare location data will contain the parent service organization of that healthcare location.

**Note:** You may experience a longer time for the upgrade to complete if your upgraded instance has a large number of records.

</td><td>

Washington DC

</td></tr><tr><td>

Industrial Process Manager

</td><td>

The Industrial Process Manager application now has a dependency with the Operational Technology Service Management applications, which include Operational Technology Incident Management and Operational Technology Change Management. To install Industrial Process Manager on your instance, one of the following SKUs is required:

-   Operational Technology Visibility SKU
-   Operational Technology Service Management SKU
-   Any custom SKU that entitles Industrial Process Manager

</td><td>

Washington DC

</td></tr><tr><td>

Instance Data Replication

</td><td>

Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses the Hermes Messaging Service. For details, see [Upgrading legacy replication sets to V2 in Instance Data Replication](https://servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&family=washingtondc&ft:locale=en-US).

 Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is comprised of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

</td><td>

Washington DC

</td></tr><tr><td>

MID Server

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=washingtondc&ft:locale=en-US). The minimum JRE version supported is 11.0.9 and the recommended version is 11.0.16.1.

 If you have installed your own JRE, the upgrade process takes the following actions to ensure that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=washingtondc&ft:locale=en-US).

 Only one Windows MID Server service is permitted per executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://servicenow.com/docs/access?context=mid-startup-fails&family=washingtondc&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=washingtondc&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=washingtondc&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td><td>

Washington DC

</td></tr><tr><td>

Now Assist for Creator

</td><td>

To receive Workflow Studio performance improvements, install one of these versions of the Workflow Studio application from the ServiceNow Store. For more information about upgrading Workflow Studio, see [Update to the latest version of Workflow Studio](https://servicenow.com/docs/access?context=update-to-the-latest-version-of-workflow-studio&family=washingtondc&ft:locale=en-US).

 |Is Now Assist for Creator already installed?|Version of Workflow Studio to use for upgrade|
|--------------------------------------------|---------------------------------------------|
|No|Upgrade Workflow Studio to version 25.1.3|
|Yes|Upgrade Workflow Studio to version 25.0.0|

</td><td>

Washington DC

</td></tr><tr><td>

Now Assist

</td><td>

For more information about troubleshooting your Now Assist application and plugin upgrades, see the KB article for [issues and mitigation for Now Assist upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452).

</td><td>

Washington DC

</td></tr><tr><td>

Order Management

</td><td>

New features introduced in this Washington DC release aren’t supported in earlier releases of Order Management for Telecommunications, Media, and Technology.

 Starting with the Washington DC release, the **Monthly Recurring Charges** \(MRC\) and the **Non Recurring Charges** \(NRC\) set for product offerings and product attribute characteristics are stored in the Pricing data model in price lists and price list lines, rather than the Product Offering data model. If you want to upgrade your pricing information to use price lists after upgrading to Washington DC, see the [Price Management Plugin \(com.sn\_csm\_pricing\) uptake for Telecommunications, Media, and Technology customers upgrading to Washington \[KB1585863\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585863) article in the Now Support Knowledge Base.

 After upgrading to the Washington DC release, a fix script runs automatically to deactivate certain telecommunications list records that are no longer needed to resume the capture of an unfinished order. For more information on these records and using the former order capture process if needed, see the [Deprecating Telco List for Order Capture \[KB1586538\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1586538) article in the Now Support Knowledge Base.

 After upgrading to the Washington DC, review the reconfiguration workarounds for working on new change orders or orders with disconnect, suspend, or resume actions while using the product configurator. For details, see the [Order line reconfiguration issues in Washington when using Order Capture UI \[KB1585976\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585976) article in the Now Support Knowledge Base.

</td><td>

Washington DC

</td></tr><tr><td>

Order Management

</td><td>

Features introduced in this Washington DC release aren’t supported in earlier releases of Order Management.

 If you’re upgrading from Order Management for Telecommunications and Media version 6.0 or earlier:

-   Starting with the  Washington DC  release, the  Monthly Recurring Charges  \(MRC\) and the  Non-Recurring Charges  \(NRC\) for product offerings and product attribute characteristics are stored in the Pricing data model in price lists and price list lines rather than in the Product Offering data model. If you want to upgrade your pricing information to use price lists after upgrading to  Washington DC, see the  [Price Management Plugin \(com.sn\_csm\_pricing\) uptake for Telecommunications, Media, and Technology customers upgrading to Washington \[KB1585863\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585863) article in the Now Support Knowledge Base.
-   After upgrading to the  release, a fix script runs automatically to deactivate certain telecommunications list records that are no longer needed to resume the capture of an unfinished order. For more information on these records and using the former order capture process if needed, see the  [Deprecating List for Order Capture \[KB1586538\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1586538) article in the Now Support Knowledge Base.

 After upgrading to the  Washington DC release, review the reconfiguration workarounds when working with new change orders or orders with disconnect, suspend, or resume actions while using the product configurator. For details, see the  [Order line reconfiguration issues in Washington when using Order Capture UI \[KB1585976\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585976) article in the Now Support Knowledge Base.

</td><td>

Washington DC

</td></tr><tr><td>

Performance Analytics

</td><td>

The legacy PA Scores \[pa\_scores\] table is being deprecated. If you still have indicator scores captured in the PA Scores table and the number of such scores is fewer than 43 million, these scores will be migrated automatically to the pa\_scores\_l1 and pa\_scores\_l2 tables upon upgrade. The expected amount of time added to upgrade is approximately two hours. For more information, see [KB1294371](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1294371) or [Migrating Performance Analytics scores](https://servicenow.com/docs/access?context=pa-scores-migration&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

Platform Analytics Experience

</td><td>

Platform Analytics Experience functionality was previously located in the Platform Analytics Workspace. The functionality is now part of the core ServiceNow AI Platform, accessible through the Next Experience Unified Navigation. You can migrate any dashboards, reports, and Performance Analytics widgets that were created in Core UI to this functionality.

</td><td>

Washington DC

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

After you upgrade to Washington DC, update the Playbooks and Workflow Studio applications in the ServiceNow Store.

</td><td>

Washington DC

</td></tr><tr><td>

Portfolio Planning

</td><td>

Starting with v8.0.0, you can access the Strategic Portfolio Management \(SPM\) Pro-licensed features only in Strategic Planning Workspace. If you have been using Portfolio Planning Workspace to access SPM Pro-licensed features, such as Goals, Product Feedback, and Hybrid Portfolio Planning, you must now install Strategic Planning to access these features. For more information on the features that can be accessed only in Strategic Planning Workspace, see [Comparing Portfolio Planning with Strategic Planning](https://servicenow.com/docs/access?context=exploring-portfolio-planning&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

Predictive Intelligence

</td><td>

If you’re upgrading to Washington DC, you won't be able to create new regression solutions. If you have existing solutions, they will still be supported and you will be able to train and modify them, but you won't be able to create new ones.

 The changes to the similarity and clustering solutions apply to all instances that are on Washington DC.

</td><td>

Washington DC

</td></tr><tr><td>

Proactive Service Experience Workflows

</td><td>

Customers who prefer not to receive trouble ticket notifications can disable the business rules related to the incident and case tables. To learn more about how to disable the business rules for trouble ticket notification, see [Deactivate trouble ticket notification](https://servicenow.com/docs/access?context=deactivate-trouble-ticket-notification&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

If you used attribute characteristics in the Standard Price Adjustment matrix in the initial release of the Sales and Order Management applications, and you're upgrading to the May 2024 release of Sales and Order Management applications, you must run a scheduled job that corrects the format of the automatically generated **Code** values. Run the **Schedule job to modify code field on characteristic records that contain special characters** on demand job to replace any character that is not a letter \(a-z, A-Z\), a number \(0-9\), an underscore \(\_\), or a dollar sign \($\) with an underscore \(\_\). This job corrects the **Code** value so that it doesn’t start or end with an underscore, doesn’t begin with a digit, and contains no consecutive underscores.

</td><td>

Washington DC

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in the CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the UX List Categories for Customer and Service Organizations. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

</td><td>

Washington DC

</td></tr><tr><td>

Robotic Process Automation \(RPA\) Hub

</td><td>

Ensure that you upgrade any of the following currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://servicenow.com/docs/access?context=download-installer-rpa&family=washingtondc&ft:locale=en-US).

 The following upgrade steps are applicable only when you’re upgrading from San Diego or Tokyo to Washington DC.

 Based on the number of records in the application file table, you could experience a potential delay while upgrading the RPA Hub applications from Tokyo or before to Washington DC.

 Before upgrading RPA Hub to Washington DC, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=washingtondc&ft:locale=en-US).

 After you upgrade to the Washington DC, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from bot process to bot process configuration. If you upgrade to the Utah version without updating the system property value, the tables don’t extend the Application File table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td><td>

Washington DC

</td></tr><tr><td>

Security Posture Control

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install the supported applications for Security Posture Control](https://servicenow.com/docs/access?context=spc-install&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

Service Operations Workspace for IT Service Management

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

 |SOW-ITSM \(sn\_sow\_itsm\_cont\)|SOW-ITOM \(sn\_sow\_itom\_cont\)|
|--------------------------------|--------------------------------|
|1.1.x|21.0.y|
|1.2.x|21.1.y|
|1.3.x|21.2.y, 21.5.y, and 21.6.y|
|2.0.x|22.0.y|
|2.1.x|22.1.y and 22.y.y|
|3.1.x|23.y.y|
|4.x.x|24.y.y|

 In the table, x is the subversion of the Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\) and y is the subversion of the Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\).

 After the 3.0 upgrade, the Recommendation Framework feature is no longer available. Instead, only the standard version of the Recommended Actions for ITSM feature is available.

</td><td>

Washington DC

</td></tr><tr><td>

Service Portal

</td><td>

After upgrading, you must specify the tables from which guest users can access data for any public widgets that accept the table input parameter. By default in the Washington DC release, public widgets that accept the table input parameter can't access and return data from any tables for guest users. If you added the **glide.service\_portal.widget.table\_allow\_list** or **glide.service\_portal.widget.allow\_list** system properties before upgrading, the values of these properties will be migrated to the Public Table Allow List for widgets after upgrading. For more information, see [Configure widget security](https://servicenow.com/docs/access?context=configure-widget-security&family=washingtondc&ft:locale=en-US).

 Additionally, field-level read ACLs are enforced for filter conditions in Simple List widget instances by default. A new system property, **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list**, enforces these ACLs regardless of whether the **Enforce field-level Read ACLs on Filter query terms** option is selected for Simple List widget instances. To use the **Enforce field-level Read ACLs on Filter query terms** option, change the value of **glide.service\_portal.enable\_acls\_for\_encoded\_query\_in\_list** to false. For more information, see [Simple List widget](https://servicenow.com/docs/access?context=simple-list-widget&family=washingtondc&ft:locale=en-US).

 If a user previously selected a user consent preference for user experience analytics for portals different from the rest of the platform, the preference selected for the platform is also used for portals in the Washington DC release. For example, if users opted out of tracking for portals but opted in to tracking for the rest of the platform in the Vancouver release, user experience analytics for portals are tracked for them in the Washington DC release. Users can update their selection from the user profile page in portals at any time.

</td><td>

Washington DC

</td></tr><tr><td>

Software Asset Management

</td><td>

After upgrading to Washington DC, you must redo all your customizations related to Adobe and Microsoft 365 integrations with your ServiceNow instance because the functionalities of these integrations are moved to the Software Asset Management – SaaS License Management store application.

-   If you’ve customized an impacted file, the upgrade process skips the file and indicates a conflict. You must manually resolve the conflict and ensure that the old existing file is deleted.
-   If you haven't customized an impacted file, the file gets deleted as part of the upgrade, and a file with a new sys\_id is created.

</td><td>

Washington DC

</td></tr><tr><td>

Strategic Planning

</td><td>

Starting with v4.0.2, you can access the Strategic Portfolio Management \(SPM\) Pro-licensed features only in Strategic Planning Workspace. If you have been using Portfolio Planning Workspace to access SPM Pro-licensed features, such as Goals, Product Feedback, and Hybrid Portfolio Planning, you must now install Strategic Planning to access these features. For more information on the features that can be accessed only in Strategic Planning Workspace, see [Exploring Portfolio Planning in Strategic Planning](https://servicenow.com/docs/access?context=alignment-planner-workspace&family=washingtondc&ft:locale=en-US).

 If you’re upgrading to Strategic Planning v4.1.2 and previously had customized the List view or the Hierarchy view of the Goals page using the Personalization side panel, the user interface enhancements done in v4.1.2 may not appear. In this case, you must delete your user preference records. For more information on how to delete user preferences made using the Personalization side panel, see [KB1642037](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1642037).

</td><td>

Washington DC

</td></tr><tr><td>

Supplier Lifecycle Operations

</td><td>

After upgrading from the Vancouver release to the Washington DC release, you will see only the Source-to-Pay Workspace on the **All** navigation tab. You don't have to do anything if you choose to continue to use the Source-to-Pay Workspace.

 However, you will see both the Source-to-Pay Workspace and Supplier Manager Workspace on the **Workspaces** tab. If you want to use the Supplier Manager Workspace instead of the default Source-to-Pay Workspace, ensure that you run the `fixscript_migrate_workspace_to_smw.xml` fix script after upgrading to the Washington DC release. You can download the `fixscript_migrate_workspace_to_smw.xml` file from the ServiceNow Store.

 If you want to revert to using the Source-to-Pay Workspace, run the `fixscript_migrate_workspace_to_s2p.xml` fix script. You can download the `fixscript_migrate_workspace_to_smw.xml` file from the ServiceNow Store. For more information about how to run a fix script, see [Run fix scripts](https://servicenow.com/docs/access?context=t_RunFixScripts&family=washingtondc&ft:locale=en-US).

 After you upgrade to Washington DC, you must review all the post-upgrade tasks and complete them as needed. For more information, see [Post-upgrade tasks for Supplier Lifecycle Management](https://servicenow.com/docs/access?context=post-upgrade-tasks-slo&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

Third-party Risk Management

</td><td>

If you are a VRM user upgrading to TPRM, when upgrading to Vancouver or later from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts do not run in the correct order, it can result in data inconsistencies, broken functionalities, and conflicts.

 For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

User Experience Analytics

</td><td>

-   Users can opt out of basic tracking.
-   A funnel data visualization is available for Usage Insights data sources.

</td><td>

Washington DC

</td></tr><tr><td>

Vulnerability Response integrations

</td><td>

-   For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Washington DC release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.
-   For information about the new features of Vulnerability Response, see [Vulnerability Response release notes](https://servicenow.com/docs/access?context=secops-vuln-resp-rn&family=washingtondc&ft:locale=en-US).

</td><td>

Washington DC

</td></tr><tr><td>

Workflow Studio

</td><td>

To receive Workflow Studio performance improvements, install one of these versions of the Workflow Studio application from the ServiceNow Store.

 |Is Now Assist for Creator already installed?|Version of Workflow Studio to use for upgrade|
|--------------------------------------------|---------------------------------------------|
|No|Upgrade Workflow Studio to version 25.1.3|
|Yes|Upgrade Workflow Studio to version 25.0.0|

</td><td>

Washington DC

</td></tr><tr><td>

AI Search

</td><td>

[Xanadu Patch 3](https://servicenow.com/docs/access?context=xanadu-patch-3&family=xanadu&ft:locale=en-US):

-   After you upgrade to Xanadu Patch 3 from an earlier release, make knowledge block content searchable by reindexing all your indexed sources that include knowledge articles. For details on reindexing, see [Index or reindex an indexed source](https://servicenow.com/docs/access?context=index-single-source-ais&family=xanadu&ft:locale=en-US) or [Index or reindex multiple indexed sources](https://servicenow.com/docs/access?context=index-multiple-sources-ais&family=xanadu&ft:locale=en-US).

 Xanadu:

 After you upgrade to Xanadu from an earlier release, perform the following steps to add the Dashboards, data visualizations, and KPIs navigation tabs to global search results in AI Search for Next Experience:

1.  Update the AI Search for Next Experience ServiceNow Store application to version 4 or later. For update instructions, see [Update an application](https://servicenow.com/docs/access?context=t_InstallUpdates&family=xanadu&ft:locale=en-US).
2.  Commit the update set provided in the [AI Search for Next Experience 4.0 PAR tables update sets \(KB1644544\)](https://support.servicenow.com/kb_view.do?sysparm_article=KB1644544) article in the Now Support Knowledge Base. To learn more about update sets, see [System update sets](https://servicenow.com/docs/access?context=system-update-sets&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

If you are upgrading from a previous release, you must configure the reference field in the Tax Code \[sn\_fin\_tax\_code\] table. The exception engine validates the invoice using the tax code and raises exceptions if necessary.

</td><td>

Xanadu

</td></tr><tr><td>

Analytics, Intelligence, and Reporting

</td><td>

If you are upgrading, you can use the Platform Analytics Migration Center to take advantage of a single set of visualizations and unified filters for all data sources.

</td><td>

Xanadu

</td></tr><tr><td>

App Engine Studio

</td><td>

Due to a new process for assigning groups in App Engine Management Center \(AEMC\), ensure you have the same version of the Application Intake plugin installed on each of your instances.

</td><td>

Xanadu

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   For information about the new features of Vulnerability Response, see [Vulnerability Response release notes](https://servicenow.com/docs/access?context=secops-vuln-resp-rn&family=xanadu&ft:locale=en-US).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Xanadu release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Xanadu

</td></tr><tr><td>

Assessments and Surveys

</td><td>

Update the Automated Test Framework \(ATF\) tests, if you're upgrading to Xanadu from any version prior to Utah. In the Utah release, all the buttons on the assessments or surveys cards have been removed. To run ATF tests successfully, the Click the Take Survey button step must be replaced with the Click the Survey card step for all tests that have this step.

</td><td>

Xanadu

</td></tr><tr><td>

Business Continuity Management

</td><td>

The relationship tables introduced in the plan records are generated by the **Update BCP dependencies snapshot** scheduled job. After upgrading to the Xanadu release, you can view these tables only after the scheduled job has run or by manually selecting the **Update dependencies** button.

</td><td>

Xanadu

</td></tr><tr><td>

Case management for CSM

</td><td>

The customer service manager role \[sn\_customerservice\_manager\] includes the approver user role \[approver\_user\]. The approver user role replaces the approval admin role \[approval\_admin\]. Users with the customer service manager role can approve the approval requests that are assigned to them.

</td><td>

Xanadu

</td></tr><tr><td>

Cloud Cost Management 8.0.0

</td><td>

On upgrading to Cloud Cost Management 8.0 version, the new Tag Category **AI Service** is available for Amazon Web Services \(AWS\), Microsoft Azure, and Google Cloud Platform \(GCP\) service providers. Because Cloud Cost Management executes the Billing Download job only from the current month onwards, the spend on AI services will be included only for the current month. If you want to view the billing details for the months prior to the current month, you must manually execute the Billing Download job. Once the Billing Download job is executed successfully, you can view the spend data of your AI services.

</td><td>

Xanadu

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

-   Before the upgrade to Xanadu, the ‘Updated CIs’ and ‘Updated application services’ trend lines in the Recent CI activity and Recent application services activities tiles on the Management view in CMDB Workspace, might not have accurately reflected on changes in your system. After upgrading to Xanadu and to versions 5.5, 6.2, or 7.2 of CMDB Workspace, those trend lines will reflect on the more accurate detection of updated CIs and updated application services.
-   CMDB Health:

If either the **CMDB Health Dashboard - Relationship Compliance Processor** or **CMDB Health Dashboard - Relationship Score Calculation** dashboard job is active, that job is deactivated during the upgrade to Xanadu. After the upgrade is complete, you can reactivate those jobs to resume health reports for CI relationships. The active state of all other CMDB Health dashboard jobs is retained.

Any failure threshold for a KPI or metric that is greater than 100,000, is set to 100,000 during upgrade. This upper limit is enforced to avoid excessive processing when a large number of CIs are failing the specified metric tests.

-   Bookmarks for the CI dashboard no longer work after an upgrade to Xanadu. A `Page not found` error message appears. To see CMDB Health reports for a CI, open the CI form in CMDB Workspace.
-   The legacy Application Service Dashboard on Core UI isn't supported in the Xanadu release. After upgrading, you can still access that legacy dashboard by using a previously created bookmark. You can also instead access the Application Services dashboard in CMDB Workspace from the Application services tile in the Insights view in CMDB Workspace.
-   The CMDB Integrations Dashboard on Core UI isn't supported in the Xanadu release. After upgrading, you can still access that legacy dashboard by using a previously-created bookmark.
-   All records that exist in the CMDB Health Result \[cmdb\_health\_result\] table before an update to Xanadu Patch 5, are deleted during the upgrade.

To access a legacy dashboard on an upgraded instance, navigate to **All** &gt; **Self-Service** &gt; **Dashboards** and then search for the dashboard.

</td><td>

Xanadu

</td></tr><tr><td>

Data Management

</td><td>

A data management policy record is automatically created for each table that is configured with an archive rule or a table cleaner rule prior to the upgrade.

</td><td>

Xanadu

</td></tr><tr><td>

Data Privacy

</td><td>

Licensing changes enable you to install Data Discovery, Data Discovery APIs, Data Anonymization, and Data Privacy APIs without an entitlement, but you must have an entitlement to run a job.

</td><td>

Xanadu

</td></tr><tr><td>

Decision tables in Workflow Studio

</td><td>

Workflow Studio is automatically installed on your instance. However, Workflow Studio is a ServiceNow Store application, so to get the latest features, you must update your version manually to the most recent version. As of Washington DC Patch 3, updating Workflow Studio automatically updates all its application dependencies such as Workflow Studio, playbook, and Decision Builder. You can no longer see or update the individual application dependencies of Workflow Studio from the ServiceNow Store or the list of plugins.

</td><td>

Xanadu

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

If you are an upgrading customer, you must run the **ReConfigure Bitbucket Server Repositories for PullRequest** job to re-configure your existing Bitbucket Server or Bitbucket Data Center repositories so that pull request records can be imported. You can navigate to **All &gt; System Definition &gt; Scheduled Jobs** to search for this job and run it.

</td><td>

Xanadu

</td></tr><tr><td>

External Content Connectors

</td><td>

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

</td><td>

Xanadu

</td></tr><tr><td>

Field Service Management

</td><td>

Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Xanadu Patch 9 version or higher to ensure compatibility.

</td><td>

Xanadu

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

After upgrading, users who previously had the fd\_read\_operations role will now see only basic execution details such as the run state and duration. This restriction prevents users with this role from seeing sensitive information in execution details. To provide read access to all execution details such as input configuration and runtime values, grant the user the new role fd\_read\_operations\_all.

</td><td>

Xanadu

</td></tr><tr><td>

Goal Framework for SPM

</td><td>

After upgrading to Goal Framework for SPM v2.3.0, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job. This scheduled job migrates the existing values in the **Review frequency** and **Breakdown interval** fields to the **Check-in frequency** field in the target records. For more information on how these values are migrated for targets with different values, see [Target breakdowns migration](https://servicenow.com/docs/access?context=target-breakdowns-migration&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Hardware Asset Management 11.0.0

</td><td>

After upgrading to Xanadu, you can view both the Core UI Performance Analytics dashboards and the Next Experience Platform Analytics dashboards for Hardware Asset Management.

**Note:** While migrating the Core UI Performance Analytics dashboards to the Next Experience Platform Analytics dashboards, auto-migration is disabled by default to avoid duplicate dashboards.

</td><td>

Xanadu

</td></tr><tr><td>

ITOM AIOps

</td><td>

Enhance your application service mapping by installing the App Service Extension app from the ServiceNow® Store.

</td><td>

Xanadu

</td></tr><tr><td>

ITOM Optimization

</td><td>

Enhance your application service mapping by installing the App Service Extension app from the ServiceNow® Store.

</td><td>

Xanadu

</td></tr><tr><td>

ITOM Visibility

</td><td>

For an improved Service Mapping experience, install Service Mapping Plus version 1.13.0 from the ServiceNow® Store.

 Enhance your application service mapping by installing the App Service Extension app from the ServiceNow® Store.

</td><td>

Xanadu

</td></tr><tr><td>

Industrial Process Manager

</td><td>

The Industrial Process Manager application now has a dependency with the Operational Technology Service Management applications, which include Operational Technology Incident Management and Operational Technology Change Management. To install Industrial Process Manager on your instance, one of the following SKUs is required:

-   Operational Technology Visibility SKU
-   Operational Technology Service Management SKU
-   Any custom SKU that entitles Industrial Process Manager

</td><td>

Xanadu

</td></tr><tr><td>

MID Server

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=xanadu&ft:locale=en-US). The minimum JRE version supported is 11.0.9 and the recommended version is 11.0.16.1.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=xanadu&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://servicenow.com/docs/access?context=mid-startup-fails&family=xanadu&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=xanadu&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=xanadu&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td><td>

Xanadu

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

Only users with the procurement\_user role can access the Help manage hardware asset requests agentic workflow including the following AI agents:

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

</td><td>

Xanadu

</td></tr><tr><td>

Now Assist for Security Operations

</td><td>

For more information about required applications for Now Assist for Vulnerability Response, see [Supporting information for Now Assist for Vulnerability Response](https://servicenow.com/docs/access?context=supporting-information-now-assist-vr&family=xanadu&ft:locale=en-US). For more information about required applications for Now Assist for Security Incident Response, see [Supporting information for Now Assist for Security Incident Response](https://servicenow.com/docs/access?context=supporting-information-now-assist-security-incident&family=xanadu&ft:locale=en-US).

 The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates AI Search is not enabled.

</td><td>

Xanadu

</td></tr><tr><td>

Now Assist

</td><td>

If you customized UI actions or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

</td><td>

Xanadu

</td></tr><tr><td>

Order Management

</td><td>

Features introduced in the Xanadu release aren't supported in earlier releases of Order Management.

 If you’re upgrading from Order Management for Telecommunications and Media version 6.0 or earlier:

-   Starting with the  Washington DC release, the  Monthly Recurring Charges  \(MRC\) and the  Non-Recurring Charges  \(NRC\) for product offerings and product attribute characteristics are no longer stored in the product offering data model. Instead, the MRC and NRC are stored in the Pricing data model in price lists and price list lines. If you want to upgrade your pricing information to use price lists after upgrading to  Washington DC, see the  [Price Management Plugin \(com.sn\_csm\_pricing\) uptake for Telecommunications, Media, and Technology customers upgrading to Washington \[KB1585863\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585863) article in the Now Support Knowledge Base.
-   After upgrading to the  Xanadu release, a fix script runs automatically to deactivate certain telecommunications list records that are no longer needed to resume the capture of an unfinished order. For more information on these records and using the former order capture process, see the  [Deprecating Telco List for Order Capture \[KB1586538\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1586538) article in the Now Support Knowledge Base.

 If you’re an upgrade customer who uses the **contract start date** and **contract end date** fields and has records, you can migrate those records to the latest data model by running the **Migrate data from deprecated contract fields to new fields on Order and Order Lines** scheduled job. This scheduled job must be manually executed by navigating to **System Definitions** &gt; **Scheduled Jobs**. For more information on scheduled jobs, see [Scheduled jobs](https://servicenow.com/docs/access?context=c_ScheduledJobs&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Platform Analytics experience

</td><td>

New customers: The Platform Analytics experience is automatically available on the ServiceNow AI Platform. It offers an intuitive interface to help you better understand and utilize your data.

 Upgrading customers: If you are currently using Core UI responsive dashboards, you will continue to have access without any disruption. Consider transitioning to the Platform Analytics experience to take full advantage of the new capabilities.

</td><td>

Xanadu

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

After you upgrade to Xanadu, update the Playbooks and Workflow Studio applications in the ServiceNow Store.

</td><td>

Xanadu

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

If you’re using the extension point **sn\_csm\_pricing.PricingAdjustmentsExtensionPoint** for pricing adjustments, change the default pricing plan \(introduced in the November 2024 release\) after upgrading. The pricing plan steps for the Configuration Component Price Adjustment and Standard Price Adjustment matrices are not applicable. As pricing admin or manager, remove the steps for these matrices from the default pricing plan.

1.  Navigate to **All** &gt; **Pricing** &gt; **Pricing Plans**.
2.  Select the published Default Pricing Plan.
3.  Select **Copy**.
4.  In the pricing plan copy, go to the Pricing Plan steps related list.
5.  Select the rows for the Apply configuration component adjustments step \(Sequence 50\) and the Apply contextual adjustments step \(Sequence 60\) and select **Delete** in the Actions on selected rows menu.
6.  Select **Update**.
7.  Publish the pricing plan copy.

</td><td>

Xanadu

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the UX List Categories for Customer and Service Organizations. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

</td><td>

Xanadu

</td></tr><tr><td>

RPA Hub

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://servicenow.com/docs/access?context=download-installer-rpa&family=xanadu&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Xanadu.

 Based on the number of records in the application file table, you could experience a potential delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Xanadu.

 Before upgrading RPA Hub to Xanadu, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=xanadu&ft:locale=en-US).

 After you upgrade to Xanadu, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Xanadu without updating the system property value, the tables don’t extend the Application File table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support knowledge base.

</td><td>

Xanadu

</td></tr><tr><td>

Security Posture Control

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://servicenow.com/docs/access?context=spc-install&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Service Exchange

</td><td>

-   Service Exchange 2.x.x that is being released with the Xanadu release does not support migration of the Service Exchange \(Legacy\) versions. If you are using a Service Exchange \(Legacy\) version, before you upgrade to the Xanadu release, you must follow instructions in the [Service Exchange for Providers \(Legacy\) - Migration Utility \(KB1499823\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.
-   If you are upgrading from version 1.x.x of Service Exchange, follow the steps listed in [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release - KB1700387\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) to migrate your Service Exchange applications.
-   Due to the introduction of mismatched version support, new entitlements cannot be activated until both the consumers and providers upgrade to the Xanadu release. Older active entitlements will continue to work but new ones cannot be activated.

</td><td>

Xanadu

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

 |Service Operations Workspace for ITSM \(sn\_sow\_itsm\_cont\)|Service Operations Workspace for ITOM \(sn\_sow\_itom\_cont\)|
|-------------------------------------------------------------|-------------------------------------------------------------|
|1.1.x|21.0.y|
|1.2.x|21.1.y|
|1.3.x|21.2.y, 21.5.y, and 21.6.y|
|2.0.x|22.0.y|
|2.1.x|22.1.y and 22.y.y|
|3.1.x|23.y.y|
|4.x.x|24.y.y|
|5.0.x|24.2.y|
|5.1.0|25.2.0|
|6.1.1|26.0.12|

</td><td>

Xanadu

</td></tr><tr><td>

ServiceNow SDK

</td><td>

Upgrade to the latest version of the ServiceNow SDK with the `now-sdk upgrade` command. For more information, see [Upgrade the ServiceNow SDK](https://servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Skills Management

</td><td>

The skills dashboard is automatically migrated to the [Next Experience UI](https://servicenow.com/docs/access?context=next-experience-landing-page&family=xanadu&ft:locale=en-US) in the Xanadu release. When you upgrade, you can automatically access the Skills dashboard in the [Next Experience UI](https://servicenow.com/docs/access?context=next-experience-landing-page&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Software Asset Management

</td><td>

After upgrading to the Microsoft Entra ID spoke 4.3 version, the **Microsoft Azure AD - Download Group Membership** directory job isn't executed for existing Microsoft Entra ID SSO or Directory integrations. This directory job also isn't created for new Microsoft Entra ID SSO or Directory integrations. Instead, the **Microsoft Azure AD - Download Groups** directory job downloads all groups and group memberships configured on Microsoft Entra ID.

</td><td>

Xanadu

</td></tr><tr><td>

Strategic Planning

</td><td>

After upgrading to Strategic Planning v4.3.2, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job. This scheduled job migrates the existing values in the **Review frequency** and **Breakdown interval** fields to the **Check-in frequency** field in the target records. For more information on how these values are migrated for targets with different values, see [Target breakdowns migration](https://servicenow.com/docs/access?context=target-breakdowns-migration-spw&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Subscription Management

</td><td>

Subscription Management version 3.2 is active by default on all instances of the Xanadu release. Update to Subscription Management version 4.0 or later to use the latest features. For more information about updating Subscription Management, see [Update an app or plugin](https://servicenow.com/docs/access?context=update-application-app-mgr&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

If you are an existing user of previous releases, both legacy and new product models will be available in the Network Inventory Workspace menu after upgrading to Xanadu. To rectify this issue, you must migrate your legacy product model data to the new product model tables in your current instance. For more details about the procedure, see [KB1695167](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1695167).

</td><td>

Xanadu

</td></tr><tr><td>

Third-party Risk Management

</td><td>

If you are a VRM user upgrading to TPRM, when upgrading to Vancouver or later from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts do not run in the correct order, it can result in data inconsistencies, broken functionalities, and conflicts.

 For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

Claroty CTD v5.1 is also supported for the Vulnerability Response Integration with Claroty CTD application.

</td><td>

Xanadu

</td></tr><tr><td>

Vulnerability Response integrations

</td><td>

-   For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Xanadu release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.
-   For information about the new features of Vulnerability Response, see [Vulnerability Response release notes](https://servicenow.com/docs/access?context=secops-vuln-resp-rn&family=xanadu&ft:locale=en-US).

</td><td>

Xanadu

</td></tr><tr><td>

Workflow Studio

</td><td>

As of Washington DC patch 3, updating Workflow Studio automatically updates all of its application dependencies such as ServiceNow® Workflow Studio, Playbook, and ServiceNow® Decision Builder. You can no longer see or update the individual application dependencies of Workflow Studio from the ServiceNow® Store or the list of plugins.

</td><td>

Xanadu

</td></tr><tr><td>

AI Control Tower

</td><td>

General availability release, no upgrade.

</td><td>

Yokohama

</td></tr><tr><td>

AI Search

</td><td>

When you upgrade to Yokohama from an earlier release, make knowledge block content searchable by reindexing all your indexed sources that include knowledge articles. For details on reindexing, see [Index or reindex an indexed source](https://servicenow.com/docs/access?context=index-single-source-ais&family=yokohama&ft:locale=en-US) or [Index or reindex multiple indexed sources](https://servicenow.com/docs/access?context=index-multiple-sources-ais&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

If you’re upgrading from a previous release, you must configure the reference field in the Tax Code \[sn\_fin\_tax\_code\] table. The exception engine validates the invoice using the tax code and raises exceptions if necessary.

</td><td>

Yokohama

</td></tr><tr><td>

App Engine Studio

</td><td>

Due to a new process for assigning groups in AEMC, the same version of the Application Intake plugin must be activated on each of your instances.

 For more information, see [App Readiness and Compliance Report](https://servicenow.com/docs/access?context=app-readiness-report&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Application Manager

</td><td>

Application Manager is active by default on instances on the Yokohama release. Upgrade your instance to Yokohama patch 11 or later to use the latest features. For information about upgrading your ServiceNow AI Platform instance, see [Prepare your upgrade](https://servicenow.com/docs/access?context=rn-prepare-landing-page&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   For information about the new features of Vulnerability Response, see [Vulnerability Response release notes](https://servicenow.com/docs/access?context=secops-vuln-resp-rn&family=yokohama&ft:locale=en-US).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Xanadu release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Yokohama

</td></tr><tr><td>

Automated Test Framework

</td><td>

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

 The tests can produce a pass result only when you run them on a base system without any customizations and with the default demo data that is provided with the application or feature plugin. To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data. For more information, see [Available quick start tests by application or feature](https://servicenow.com/docs/access?context=available-quick-start-tests&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

Three new indexes \(parent, type\), \(child, type\), and \(child, parent, type, port\) are added to the CI Relationship \[cmdb\_rel\_ci\] table to improve the performance of Identification and Reconciliation Engine \(IRE\) querying this table. This change is likely to increase upgrade time. For more information about the impact of this change during upgrade and to learn how to minimize that impact, see [Increased Yokohama Upgrade Time due to cmdb\_rel\_ci index additions \[KB1703367\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB1703367).

</td><td>

Yokohama

</td></tr><tr><td>

Data Management

</td><td>

-   After upgrading a self-hosted instance to Yokohama, the sys\_physical\_table\_stats table doesn't display the latest data for table size, with the sample\_period\_start column showing dates prior to the upgrade. To see the correct table size, you can set the com.glide.stats.storage\_disk\_usage.information\_schema system property to true, which allows the statsGatherer job to use the information schema to generate the required database statistics.

-   A data management policy record is automatically created for each table that is configured with an archive rule or a table cleaner rule prior to the upgrade.

</td><td>

Yokohama

</td></tr><tr><td>

Data Privacy

</td><td>

Licensing changes enable you to install Data Discovery, Data Discovery APIs, Data Anonymization, and Data Privacy APIs without an entitlement, but you must have an entitlement to run a job.

</td><td>

Yokohama

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

If you are a new customer or are using a zBoot instance and you want to create type-based workflow change requests in DevOps Change Velocity, you must add the**com.snc.change\_management.change\_model.type\_compatibility** property and set it to True. For more information, see [Add a system property](https://servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=yokohama&ft:locale=en-US).

 If you are an upgrading customer, you must run the **ReConfigure Bitbucket Server Repositories for PullRequest** job to re-configure your existing Bitbucket Server or Bitbucket Data Center repositories so that pull request records can be imported. You can navigate to **All &gt; System Definition &gt; Scheduled Jobs** to search for this job and run it.

</td><td>

Yokohama

</td></tr><tr><td>

Encryption Key Management

</td><td>

-   The GlideEncrypter API uses the three-key Triple Data Encryption Standard \(3DES\) encryption standard which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Yokohama release in preparation for a full deprecation of GlideEncrypter/3DES in the future.
    -   New Yokohama instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Yokohama instances, you can still use 3DES, but you can also disable 3DES usage with a system property.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td><td>

Yokohama

</td></tr><tr><td>

External Content Connectors

</td><td>

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

 When you upgrade to version 4 of the External Content Connectors application from an earlier version, searches may not show all previously crawled content until you've completed both a content crawl and a user mapping crawl for each upgraded connector. The first content crawl run after the upgrade will reindex all searchable content from the source system, and the user mapping crawl will reindex all security principals from the source system. All crawled content should be shown in searches after both of these crawls are complete.

</td><td>

Yokohama

</td></tr><tr><td>

Field Service Management

</td><td>

-   Upgrading to Yokohama may extend the upgrade maintenance time of a customer due to Appointment Booking. The Appointment Booking configuration tables get extended to the Application File \[sys\_metadata\] table as a part of the upgrade. After upgrading to Yokohama, re-parenting occurs automatically and the duration of the re-parenting depends on the number of records in Application File \[sys\_metadata\] table.
-   Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Yokohama Patch 3 version or higher to ensure compatibility.

</td><td>

Yokohama

</td></tr><tr><td>

Financial Services Card Operations

</td><td>

During the upgrade to Yokohama, the Financial Services Card Operations plugin reparents the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] to the Financial Task table \[sn\_bom\_task\] in Financial Services Operations Core.

 Reparenting leverages the benefits and advancements of ServiceNow® Financial Services Operations Core while preserving the functionality of existing applications.

**Note:** If your instance uses the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] and it contains a large amount of data, you may experience increased upgrade times.

</td><td>

Yokohama

</td></tr><tr><td>

Generative AI Controller

</td><td>

Generative AI Controller is installed and updated when you install or update any Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

</td><td>

Yokohama

</td></tr><tr><td>

ITOM Visibility

</td><td>

3DES support is planned for permanent removal from the MID Server for MID Servers with SSH-based Discovery or SSH-based integrations. For more information, see [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950).

 After upgrading to Yokohama, a Fix Script named "Add Explicit Public SNMP Credential" might create a public SNMP credential in Production instances. This could lead to unnecessary records via Discovery. The Fix Script is present in Yokohama instances, including OOB. Before applying the upgrade of Discovery core, Yokohama version, verify the fix script behavior in a sandbox environment. Remove the public SNMP credentials if not required.

</td><td>

Yokohama

</td></tr><tr><td>

Impact

</td><td>

The Impact Store Application configuration requires a sequence of tasks. See [Configuring the Impact Store Application](https://servicenow.com/docs/access?context=configuring-impact-platform&family=yokohama&ft:locale=en-US) for details.

</td><td>

Yokohama

</td></tr><tr><td>

Instance Data Replication

</td><td>

Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see [Upgrading legacy sets](https://servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&family=yokohama&ft:locale=en-US).

 Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is comprised of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

</td><td>

Yokohama

</td></tr><tr><td>

MID Server

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=yokohama&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://servicenow.com/docs/access?context=mid-startup-fails&family=yokohama&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=yokohama&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist Analytics

</td><td>

Now Assist Analytics is installed and updated when you install or update any Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

Only users with the procurement\_user role can access the Help manage hardware asset requests agentic workflow including the following AI agents:

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist for Security Incident Response

</td><td>

For more information about required applications for Now Assist for Security Incident Response, see [Supporting information](https://servicenow.com/docs/access?context=supporting-information-now-assist-security-incident&family=yokohama&ft:locale=en-US).

 **Note:**

Upgrading the Now Assist plugins activate any designated skills that were previously untouched by the customer.

-   If you have the plugins installed but never touched the configuration \(never activated the skill nor adjusted associated roles\) of a skill, any Default On skill will be activated on a per skill basis upon upgrading.
-   If you have previously toggled a skill from active and then back to inactive or have updated any roles for that skill, that skill remains inactive upon upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

 Starting with version 2.0.1, the name of the Now Assist for Security Operations application in ServiceNow® Store and in your ServiceNow AI Platform® instance has changed to Now Assist for Security Incident Response. You must upgrade to version 2.0.1 to access the following features:

-   Generate resolution notes in the Now Assist context menu.
-   Generate correlation insights for a security incident investigation from the Now Assist panel.

 The AI Search application must be enabled so that the recommended actions skill works for security incidents. To verify that AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search is not enabled.

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

For more information about required applications for Now Assist for Vulnerability Response, see [Supporting information](https://servicenow.com/docs/access?context=supporting-information-now-assist-vr&family=yokohama&ft:locale=en-US).

 **Note:**

Upgrading the Now Assist plugins activate any designated skills that were previously untouched by the customer.

-   If you have the plugins installed but never touched the configuration \(never activated the skill nor adjusted associated roles\) of a skill, any Default On skill will be activated on a per skill basis upon upgrading.
-   If you have previously toggled a skill from active and then back to inactive or have updated any roles for that skill, that skill remains inactive upon upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

If you’re upgrading to Now Assist in Contract Management starting with Yokohama Patch 3 from a previous version and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
2.  In the **Name** field, search for `Upsert DI skill config`.
3.  In the script, add the use case ids that you want to migrate to the Now Assist Admin console.
4.  Select **Run Fix Script**.

For more information, see [Post-upgrade steps for Now Assist in Contract Management](https://servicenow.com/docs/access?context=cmpro-na-upgrade-steps&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist

</td><td>

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

</td><td>

Yokohama

</td></tr><tr><td>

Platform Analytics experience

</td><td>

If you had previously migrated your analytics assets to Platform Analytics, assets that were in compatibility mode but are newly supported in Yokohama are migrated automatically.

</td><td>

Yokohama

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

After you upgrade to Yokohama, update the Workflow Studio application in the ServiceNow Store.

</td><td>

Yokohama

</td></tr><tr><td>

Portfolio Planning

</td><td>

After upgrading to Portfolio Planning v8.8.0, the custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Portfolio Planning](https://servicenow.com/docs/access?context=create-portfolio-plan-view-ppw&family=yokohama&ft:locale=en-US) and [Create a free-form roadmap view in Portfolio Planning](https://servicenow.com/docs/access?context=create-free-form-roadmap-view-ppw&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

After upgrading to the May 2025 release of Sales and Order Management applications, you must run a scheduled job that automatically enables the **Allow multiple configurations** option when your catalog admin creates product offerings with an associated product specification. This job is called **Scheduled job with an upgrade script to set 'allow\_multiple\_configurations' to true on an Offering**. When multiple product offering configurations are allowed in configurable opportunities, quotes, or orders, agents can create multiple instances of a child product offering and define custom configurations for each offering instance.

**Note:** The **Allow multiple configurations** option is always enabled \(set to true\) for all product offerings that have an associated product specification. However, if the product specification has a child hierarchy, this option is honored only for orders placed through the TMF APIs. For specifications without a hierarchy, the flag is honored across all ordering channels.

 The May 2025 release provides a default pricing plan that includes a new step, Apply Renewal Adjustment. If you've been using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after upgrading to the May 2025 release. Determine whether you want to publish the default plan or customize the default pricing plan for your needs and then publish the custom plan to be used.

</td><td>

Yokohama

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in the CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the **Customer**, **Accounts**, and **Service Organizations** UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

</td><td>

Yokohama

</td></tr><tr><td>

RPA Hub

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://servicenow.com/docs/access?context=download-installer-rpa&family=yokohama&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Yokohama.

 Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Yokohama.

 Before upgrading RPA Hub to Yokohama, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=yokohama&ft:locale=en-US).

 After you upgrade to Yokohama, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Yokohama without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td><td>

Yokohama

</td></tr><tr><td>

Security Posture Control

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://servicenow.com/docs/access?context=spc-install&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Service Exchange

</td><td>

-   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility.
-   The Service Exchange Global Script Include is automatically installed or updated when you install the Service Exchange application on the following platform versions:
    -   Washington DC Patch 9
    -   Xanadu Patch 4
    -   Yokohama
-   Service Exchange 2.x.x, which was first released with the Xanadu release, does not support migration of Service Exchange \(Legacy\) versions. If you are using a Service Exchange \(Legacy\) version, before you upgrade to the Yokohama release, you must follow instructions in the [Service Exchange for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.
-   If you are upgrading from Service Exchange version 1.x.x, follow the steps in [Upgrade Guide - Service Exchange for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) to migrate your Service Exchange applications.
-   Due to the introduction of mismatched version support, new entitlements cannot be activated until both the consumers and providers upgrade to Service Exchange version 2.x.x. Older active entitlements will continue to work but new ones cannot be activated.
-   If you upgrade to Service Exchange version 2.0.55 with Sales and Order Management plug-in version 1.0.4 before upgrading the platform to the Yokohama release, the new Deny ACLs will not be installed. To ensure the Deny ACLs get installed, after upgrading to Yokohama, you must click Repair to reinstall the Service Exchange application.

</td><td>

Yokohama

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

 For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://servicenow.com/docs/access?context=sow-itsm-itom-version&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

ServiceNow IDE

</td><td>

ServiceNow IDE version 1.1.4 is active by default on instances on the Yokohama release. Update to ServiceNow IDE version 2.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Updating apps](https://servicenow.com/docs/access?context=updating-apps-app-manager&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

ServiceNow SDK

</td><td>

Upgrade to the latest version of the ServiceNow SDK with the `now-sdk upgrade` command. For more information, see [Upgrade the ServiceNow SDK](https://servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=yokohama&ft:locale=en-US).

 ServiceNow SDK version 3.0 supports integrating with ServiceNow instances beginning with the Washington DC release.

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow IDE, SDK, and Fluent articles](https://www.servicenow.com/community/servicenow-ide-sdk-and-fluent/tkb-p/ide-sdk-fluent-articles) in the ServiceNow Community.

</td><td>

Yokohama

</td></tr><tr><td>

ServiceNow Studio

</td><td>

ServiceNow Studio no longer has to be downloaded from the ServiceNow Store. It’s available on the ServiceNow AI Platform by default.

</td><td>

Yokohama

</td></tr><tr><td>

Software Asset Management

</td><td>

Starting from the Yokohama release, all the reconciliation script includes are being moved from the family release to the Software Asset Management store application \(com.sn\_itam\_samp\). When upgrading to Yokohama, if you have made customizations to reconciliation script includes, you must move your customizations to the new script includes. The old script includes will be deprecated.

 When upgrading to Yokohama Patch 1 with the Software Asset Management \(sn\_itam\_samp\) 2.1.0 store application installed, you must delete the entitlements for the existing CrowdStrike integration profiles. Then, create new entitlements for various CrowdStrike products, such as CrowdStrike Falcon Endpoint Protection and CrowdStrike Falcon Discover, based on their license metrics. These metrics include the Reserved Hourly Average Sensor and Sensor Subscription, which are found under the CrowdStrike License Metric Group.

-   If any existing CrowdStrike profiles are in the Draft state, create new integration profiles and delete the existing ones.
-   If any existing CrowdStrike profiles are in the Published state, their state changes to Draft.

</td><td>

Yokohama

</td></tr><tr><td>

Strategic Planning

</td><td>

After upgrading to Strategic Planning v4.7.0, the following changes apply to user preferences:

-   Custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Strategic Planning](https://servicenow.com/docs/access?context=create-portfolio-plan-view-spw&family=yokohama&ft:locale=en-US) and [Create a free-form roadmap view in Strategic Planning](https://servicenow.com/docs/access?context=create-free-form-roadmap-view-spw&family=yokohama&ft:locale=en-US).
-   Customizations made to the Timeline and Kanban views in the **Roadmap** tab, and the Kanban view in the **Prioritization** tab at the portfolio plan level, will be copied to the Default view of the portfolio plan. Similarly, any customizations made to the Timeline and Kanban views in the free-form roadmap will also be copied to the Default view of the free-form roadmap.

</td><td>

Yokohama

</td></tr><tr><td>

Subscription Management

</td><td>

Subscription Management version 4.1 is active by default on all instances of the Yokohama release. Update to Subscription Management version 6.0.2 or later to use the latest features. For more information about updating Subscription Management, see [Update an app or plugin](https://servicenow.com/docs/access?context=update-application-app-mgr&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

The Yokohama release needs the Xanadu platform version to support the Design and Assign playbook feature.

</td><td>

Yokohama

</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

After installing Telecommunications Service Operations Management TSOM, any customized IRE identification rules applied to interface cards, slots, sub-slots and network interfaces may be affected. You must review and validate the rules to ensure proper functionality.

</td><td>

Yokohama

</td></tr><tr><td>

Third-party Risk Management

</td><td>

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

 For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](https://servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=yokohama&ft:locale=en-US).

 For existing TPRM customers, after upgrading to version 20.2.4, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

</td><td>

Yokohama

</td></tr><tr><td>

Usage Insights

</td><td>

-   The Usage Insights module is moved under Platform Analytics.
-   Custom user properties must be reconfigured.
-   Default country and user consent policies are updated to No Consent Required.
-   The Usage Insights UI and navigation structure are reworked.

</td><td>

Yokohama

</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

Claroty CTD v5.1 is also supported for the Vulnerability Response Integration with Claroty CTD application.

</td><td>

Yokohama

</td></tr><tr><td>

Vulnerability Response integrations

</td><td>

-   For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Yokohama release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.
-   For information about the new features of Vulnerability Response, see [Vulnerability Response release notes](https://servicenow.com/docs/access?context=secops-vuln-resp-rn&family=yokohama&ft:locale=en-US).

</td><td>

Yokohama

</td></tr><tr><td>

Workforce Optimization for ITSM

</td><td>

-   **[Enhanced security to access Workforce Optimization for ITSM](https://servicenow.com/docs/access?context=components-installed-workforce-optimization-itsm&family=yokohama&ft:locale=en-US)**

When you upgrade to the Yokohama release, you have the option to turn on enhanced security for the Workforce Optimization for ITSM application. To get the enhanced security, you must contact Now Support to install the ITSM Enhanced Security Features plugin \(com.snc.itsm.enhanced\_security\). After you install the plugin, you need the roles listed here to access the respective features.

<table><thead><tr><th>

Features in Workforce Optimization for ITSM

</th><th>

Role required for each user

</th></tr></thead><tbody><tr><td>

Skill review

</td><td>

-   Skill review manager \(sn\_wfo\_skillreview.manager\)
-   Skill review user \(sn\_wfo\_skillreview.user\)


</td></tr><tr><td>

Work scheduler

</td><td>

-   Work scheduler admin \(sn\_wfo\_work\_sched.admin\)
-   Work scheduler manager \(sn\_wfo\_work\_sched.manager\)


</td></tr></tbody>
</table>


</td><td>

Yokohama

</td></tr><tr><td>

AI Search

</td><td>

After you upgrade to Zurich from an earlier family release, run full document crawls in all your external content connectors to update their semantic vector indexing field mappings.

</td><td>

Zurich

</td></tr><tr><td>

Application Manager

</td><td>

Application Manager is active by default on instances on the Zurich release. Upgrade your instance to Zurich patch 4 or later to use the latest features. For information about upgrading your ServiceNow AI Platform instance, see [Prepare your upgrade](https://servicenow.com/docs/access?context=rn-prepare-landing-page&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   If you are currently using Application Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Application Vulnerability Response and for upgrades to supported third-party integration applications.
-   For information about the new features of Vulnerability Response, see the [Vulnerability Response release notes](https://servicenow.com/docs/access?context=secops-vuln-resp-rn&family=zurich&ft:locale=en-US).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Zurich

</td></tr><tr><td>

Automated Test Framework

</td><td>

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

 The tests can produce a pass result only when you run them on a base system without any customizations and with the default demo data that is provided with the application or feature plugin. To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data. For more information, see [Available quick start tests by application or feature](https://servicenow.com/docs/access?context=available-quick-start-tests&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

CPQ Configurator

</td><td>

If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading, you must set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true to be able to use the configurator in Sales and Order Management workflows.

.

</td><td>

Zurich

</td></tr><tr><td>

Change Management

</td><td>

As part of the update to use Flow instead of Progress Workers for conflict detection, the Conflict Checker Progress UI Formatter record references a new UI macro, change\_conflict\_worker\_progress\_gate. This macro checks the **change.conflict.useprogressworker** system property to determine the conflict detection mechanism and then displays the corresponding UI macro to work with either Progress Workers or the Change Management Worker table. For more information, see [Conflict detection](https://servicenow.com/docs/access?context=c_ConflictDetection&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Cloud Cost Management 9.0

</td><td>

The Cloud Cost Management platform support is available beginning with the Xanadu release. For instructions on upgrading Cloud Cost Management to Zurich, see [Upgrade Cloud Insights](https://servicenow.com/docs/access?context=upgrade-cloud-insights-to-version-3-0&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Cloud Exposure View

</td><td>

The Cloud Exposure View is a workspace in the Cloud Security for Cloud Workspace application that is supported by the Unified Security Exposure Management application. Unified Security Exposure Management \(USEM\) and the Cloud Security for Cloud Workspace applications are required. USEM is available to all customers who are entitled to Vulnerability Response. See [Unified Security Exposure Management release notes](https://servicenow.com/docs/access?context=secops-sem-rn&family=zurich&ft:locale=en-US) for more information.

</td><td>

Zurich

</td></tr><tr><td>

Configuration Compliance

</td><td>

If you are currently using Configuration Compliance, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Configuration Compliance and for upgrades to supported third-party integration applications.

 The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=zurich&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

 For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Zurich

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

Due to the removal of the **Design** value for the operational status attribute in a CI, after an upgrade, you must review all CIs that have the discovery source attribute set to **Manual via IRE**. Review the operational status attribute of those CIs and set it to a supported value in CMDB for your environment. For example, you can set the attribute to **Non-Operational**. For more information about the operational status values, see [Tangible/physical life cycle](https://servicenow.com/docs/access?context=csdm-lifecycle-hardware&family=zurich&ft:locale=en-US).

 On an upgraded Zurich instance, to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks, you must manually run the scheduled job **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles**. This scheduled job modifies the user roles as follows:

-   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
-   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).

</td><td>

Zurich

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

If you are currently using Container Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Container Vulnerability Response and for upgrades to supported third-party integration applications.

 The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=zurich&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

 For more information about the released versions of the Container Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Zurich

</td></tr><tr><td>

Customer self-service for Sales and Order Management

</td><td>

The new order checkout experience and improved cart capabilities are delivered through a new Sales Cart plugin \(sn\_sales\_cart\). As an admin, you must perform the [Post-upgrade order migration](https://servicenow.com/docs/access?context=post-upgrade-task-business-portal&family=zurich&ft:locale=en-US) to continue providing a seamless experience for your customers. Failing to perform the upgrade steps can result in your customers losing products added to their carts.

</td><td>

Zurich

</td></tr><tr><td>

Encryption Key Management

</td><td>

-   In previous releases, the GlideEncrypter API used the three-key Triple Data Encryption Standard \(3DES\) encryption standard, which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Zurich release in preparation for a full deprecation of GlideEncrypter/3DES in the future:
    -   New Zurich instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Zurich instances, you can still GlideEncrypter, which has been updated to use AES256-GCM encryption via the Key Management Framework.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td><td>

Zurich

</td></tr><tr><td>

Encryption

</td><td>

For the GlideEncrypter API, NIST 800-131A Rev 2 has recommended against using the Triple Data Encryption Standard \(3DES\) encryption. The following changes are taking place in the Zurich release with the official removal of 3DES encryption for GlideEncrypter.

-   The GlideEncrypter API defaults to using the Key Management Framework \(KMF\) based algorithm, Advanced Encryption Standard \(AES\), for encryption and decryption operations for upgraded instances only.
-   For instances created with the Zurich release or later, this API isn’t supported.
-   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

 In the Zurich release, Column Level Encryption has received a required upgrade to Key Management Framework Column Level Encryption \(KMF-CLE\) due to the platform-wide deprecation of 3DES. For more information about this upgrade, see KB1700704.

</td><td>

Zurich

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

Starting with Zurich release, a new menu, Asset put away, has been added to the ServiceNow Agent app navigation bar. When upgrading to the Zurich release, a fix script identifies whether the ServiceNow Agent app navigation bar was customized and takes the necessary action.

-   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(![image.asset-putaway-icon-ma]\) is included in the navigation bar
-   If the navigation bar was customized before the upgrade, two navigation bars appear: Customized old IT Asset Management and IT Asset Management. The new icon appears in the IT Asset Management navigation bar.

</td><td>

Zurich

</td></tr><tr><td>

External Content Connectors

</td><td>

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

 When you upgrade to version 4 of the External Content Connectors application from an earlier version, searches may not show all previously crawled content until you've completed both a content crawl and a user mapping crawl for each upgraded connector. The first content crawl run after the upgrade will reindex all searchable content from the source system, and the user mapping crawl will reindex all security principals from the source system. All crawled content should be shown in searches after both of these crawls are complete.

</td><td>

Zurich

</td></tr><tr><td>

Field Service Management

</td><td>

Effective March 1, 2025, the Google Places API, Directions API, and Distance Matrix API have been designated as legacy services. The newer versions of these services are Places API \(New\) and Routes API. Google Maps APIs for Field Service capabilities uses the latest version of the APIs in the Zurich release and Dispatcher Workspace version 8.0. To help avoid issues with the Google Maps APIs, enable Places API \(New\) and Routes API from Google Cloud Platform Console.

</td><td>

Zurich

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see [Restore save as you go functionality](https://servicenow.com/docs/access?context=restore-save-as-you-go-functionality&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Generative AI Controller

</td><td>

Generative AI Controller is installed or updated when you install or update a Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) or open a support case.

</td><td>

Zurich

</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   Starting from the Zurich release, a few workflows have been migrated to Workflow Studio as flows.

**Note:** The migration of workflows to Workflow Studio applies to Asset Management, Procurement, and Contract Management applications.

    -   The following workflows have been migrated to Workflow Studio as flows:
        -   Procurement Process Flow – Hardware
        -   Transfer Order
        -   Transfer Order Line
        -   Source Request
        -   Contract Approval
    -   When upgrading to the Zurich release, a fix script identifies whether the workflows were customized and takes necessary action.
        -   If the workflows weren’t customized before the upgrade, the legacy workflows are deactivated from the instance, and Workflow Studio flows are installed and executed post-upgrade.
        -   If the impacted workflows were customized before the upgrade, the Workflow Studio flows are installed but aren’t executed for any of the impacted flows post-upgrade. You can view and access the impacted workflows in the instance after the upgrade. However, the deprecated workflows are considered custom code and aren’t supported for maintenance.
-   After upgrading to the Zurich release, if an approval history record exists for a contract that is no longer required, reject the record instead of deleting it. If the approval history record is deleted, Workflow Studio doesn’t support updating the contract’s **Substate** field value to display the correct state.
-   Starting with Zurich release, a new menu, Asset put away, has been added to the ServiceNow Agent app navigation bar. When upgrading to the Zurich release, a fix script identifies whether the ServiceNow Agent app navigation bar was customized and takes the necessary action.
    -   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(![image.asset-putaway-icon-ma]\) is included in the navigation bar
    -   If the navigation bar was customized before the upgrade, two navigation bars appear: Customized old IT Asset Management and IT Asset Management. The new icon appears in the IT Asset Management navigation bar.
-   A new role, sn\_itam\_recomm.recommendations\_read, helps ensure that only valid users can execute APIs related to the Important Actions menu in the Asset Workspace. The following roles, which have access to the Asset Workspace, now include the sn\_itam\_recomm.recommendations\_read role:
    -   procurement\_user
    -   inventory\_admin
    -   inventory\_user
    -   model\_manager
    -   contract\_manager
    -   itil
    -   catalog\_manager
    -   catalog\_admin
    -   sam
    -   ham\_user
    -   asset
-   Control sensitive data leakage from range queries accessed by unauthenticated users through the following access control lists \(ACLs\):
    -   Contract \[ast\_contract\] table: Only users with the contract\_manager role can perform the query\_range operation on the Start date, Contract number, PO number, and Vendor columns.
    -   Contract user M2M \[clm\_m2m\_contract\_user\] table: Only users with the contract\_manager and asset roles can perform the query\_range operation on the Contract and User columns.
    -   HAMP Success Activity \[sn\_hamp\_success\_activity\] table: Only users with the ham\_admin and asset roles can perform the query\_range operation on the Description, Short description, and Success goals columns.
-   Only users with the admin role can update the following system properties:
    -   glide.sg.voice\_search.enabled
    -   glide.ui.sn\_hamp\_asset\_reclaim\_task\_activity.fields
    -   glide.ui.sn\_hamp\_loaner\_asset\_order\_activity.fields
    -   glide.ui.sn\_hamp\_ztr\_task\_activity.fields
    -   sn\_hamp.enable\_shipping\_carrier\_validation\_asn
    -   sn\_hamp.model\_lifecycle\_phase\_order
    -   sn\_hamp.update\_assets\_norm\_model\_name

</td><td>

Zurich

</td></tr><tr><td>

Impact

</td><td>

The Impact Store Application configuration requires a sequence of tasks in a unified registration process. See [Configure the Impact Store Application](https://servicenow.com/docs/access?context=configuring-impact-platform&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Instance Data Replication

</td><td>

-   Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see [Upgrading legacy sets](https://servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&family=zurich&ft:locale=en-US).
-   Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

</td><td>

Zurich

</td></tr><tr><td>

MID Server

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://servicenow.com/docs/access?context=r_MIDServerSystemRequirements&family=zurich&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

 If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

 All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US).

 Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://servicenow.com/docs/access?context=mid-startup-fails&family=zurich&ft:locale=en-US) for more information.

 For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&family=zurich&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td><td>

Zurich

</td></tr><tr><td>

Notify

</td><td>

Starting with the Zurich release, Notify uses subflows instead of workflows. For existing users in Zurich, your current workflows are still supported. For new users, your Notify plugin installations use subflows.

 As part of this transition, the following workflow activities are available as flow actions and can be used when creating subflows:

-   Join conference call
-   Call
-   Send SMS
-   Forward call
-   Input
-   Hangup
-   Play
-   Record
-   Reject
-   Say
-   Forward to notify client
-   Queue

 Maintain, build, and modify your own custom subflows in Workflow Studio with subflows for new instances. The following base system workflows have been migrated to subflows:

-   \(Re\)join Conference Call
-   Join Conference Call with muting
-   Join Conference Call with SMS

Your existing workflows continue to function after the upgrade.

**Note:** All workflow-related artifacts have been moved to a new plugin, which is maintained in a support-only mode and isn't available for new installations.

</td><td>

Zurich

</td></tr><tr><td>

Now Assist for CMDB

</td><td>

The installation \(activation\) process has changed for the Now Assist for CMDB v2.1 plugin. See [Configure](https://servicenow.com/docs/access?context=now-assist-cmdb-configuring&family=zurich&ft:locale=en-US) for the new instructions.

</td><td>

Zurich

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

If you have the procurement\_user user role, you can access the help manage hardware asset requests agentic workflow, which includes the following AI agents:

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

</td><td>

Zurich

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

 The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. When you upgrade to the [Zurich Patch 8](https://servicenow.com/docs/access?context=zurich-patch-8&family=zurich&ft:locale=en-US) release, if you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://servicenow.com/docs/access?context=now-assist-itsm-incident-assist&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Now Assist for Security Incident Response \(SIR\)

</td><td>

**Note:** The following Now Assist skills, agents, and agentic workflows for Now Assist for Security Incident Response are activated by default:

Skills

-   Security incident summarization
-   Resolution notes generation
-   Post incident analysis
-   Security incident recommended actions
-   Correlation insights generation
-   Security incident quality assessment
-   Natural language condition evaluator
-   Generate content for shift handover
-   Quality assessment report NACM
-   Security incident resolution plan
-   Security operations metrics analysis

Agentic workflows

-   Wrap up security incident
-   Resolve security incident
-   Generate SIR shift handover report
-   Analyze security operations metrics

Agents

-   EDR AI agent
-   Exchange online integration handling AI agent
-   Observable analysis AI agent
-   Security incident activities handling AI agent
-   Security incident resolution AI agent
-   Security incident retrieval AI agent
-   Security incident shift handover AI agent
-   Security incident wrap up generator AI agent
-   Security metrics analysis AI agent

For more information, see [AI assets on by default](https://servicenow.com/docs/access?context=now-assist-skills-on-by-default&family=zurich&ft:locale=en-US)

**Note:** Upgrading the Now Assist plugins activates any designated skills that were previously untouched by the customer.

-   If you installed the plugins for a skill but never configured it, meaning you never activated it nor adjusted associated roles, any skill on by default is activated on a per skill basis when upgrade.
-   If you previously toggled a skill from active and then back to inactive, or updated any roles for that skill, that skill remains inactive when upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

 When you update the Now Assist for Security Incident Response \(SIR\) application, the dependency applications are automatically updated.

 For more information about required applications for Now Assist for Security Incident Response, see [Supporting information](https://servicenow.com/docs/access?context=supporting-information-now-assist-security-incident&family=zurich&ft:locale=en-US).

 The AI Search application must be enabled so that the recommended actions skill works for security incidents with Now Assist for Security Incident Response. To verify that AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search isn’t enabled.

</td><td>

Zurich

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

The following Now Assist skills for Now Assist for Vulnerability Response are activated by default.

-   Recommend preferred solution for VIT \(VR\)
-   Vulnerable item de-duplication \(VR\)
-   Approval Recommendation \(VR\)\(USEM\)
-   Security Exposure Management \(SEM\) Insights \(VR\)\(USEM\)
-   SPC Setup Connector \(Security Posture Control\)

 When you update the Now Assist for Vulnerability Response application, the dependency applications are automatically updated.

 For more information about required applications for Now Assist for Vulnerability Response, see [Supporting information](https://servicenow.com/docs/access?context=supporting-information-now-assist-vr&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

If you’re upgrading to Now Assist in Contract Management from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
2.  In the **Name** field, search for `Upsert DI skill config`.
3.  In the script, add the use case IDs that you want to migrate to the Now Assist Admin console.
4.  Select **Run Fix Script**.

For more information, see [Post upgrade steps](https://servicenow.com/docs/access?context=cmpro-na-upgrade-steps&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Now Assist

</td><td>

Customers who have not opted into third-party, large language models may be routed to them during skill execution. If the new model is not provisioned or available in your environment, this will result in skill execution failures. Check the models your skills use within Now Assist admin console.

 If you customized UI actions or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

 If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

 The Zurich release introduces enhanced protections for read‑only fields across the ServiceNow® AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back-end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow® ‑owned read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122). This article provides additional technical details on how to identify affected fields and adjust their settings.

 The existing Access Control Lists \(ACLs\) will be updated to replace the 'admin' role with specific, purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API will be replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the 'admin' role in the code will be substituted with the new feature-specific granular roles for authorization use cases. Read [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html) to learn more.

</td><td>

Zurich

</td></tr><tr><td>

On-Call Scheduling

</td><td>

Starting from the Zurich release, On-Call Scheduling uses subflows, not workflows. You must transition from workflows to subflows, because the workflows are considered as legacy workflows. For existing users in Zurich, your current workflows continue to be supported. However, for new users, the On-Call Scheduling plugin installations on Zurich and later instances only use subflows.

 Maintain, build, and modify your own custom on-call scheduling flows in Workflow Studio with subflows for new instances. The following subflows are available for configuration:

</td><td>

Zurich

</td></tr><tr><td>

Operational Resilience

</td><td>

After upgrading to Operational Resilience version 21.0.x, rerun the **Update CSDM and other dependencies** scheduled job to populate the additional metadata that was introduced in this release.

</td><td>

Zurich

</td></tr><tr><td>

Performance Analyzer

</td><td>

Starting with the Zurich release, Performance Analyzer is available on your instance automatically. For access to Performance Analyzer on earlier instances, install Performance Analyzer from the ServiceNow® Store.

</td><td>

Zurich

</td></tr><tr><td>

Platform Analytics experience

</td><td>

On upgrade, any homepages on your instance that have been opened are migrated to Core UI dashboards, which are visible in the dashboard library. For more information, see [Homepage deprecation](https://servicenow.com/docs/access?context=homepage-deprecation-help-tool&family=zurich&ft:locale=en-US).

 Simple lists are all converted to the new List element on upgrade.

</td><td>

Zurich

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

After you upgrade to Zurich, update the Workflow Studio application in the ServiceNow Store.

</td><td>

Zurich

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

Pricing Management v15.0.0 provides a default pricing plan that includes new steps to support pricing strategies introduced in this release. If you're using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after you upgrade. Determine whether you want to publish the default plan or customize the default pricing plan for your needs. The default plan contains new steps for calculating net pricing and roll-up values for configurable products in quotes and orders: Net Price Calculation, Line Rollup, and Header Rollup steps. This pricing functionality existed in previous releases for quotes and orders but wasn’t included in the default pricing plan. To retain this previous functionality for quotes and orders, you must add the Net Price Calculation, Line Rollup, and Header Rollup steps in your custom pricing plan before you publish it for use.

 If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true. When set to true, this property enables the CPQ Configurator.

 If you want to use AI Search for product catalog searches, before upgrading install Now Assist for Sales Force Automation \(SFA\), which includes the plugins needed for AI Search functionality. After upgrading, complete various steps to implement AI Search. These steps include running a scheduled job to set up AI Search and enabling AI Search in the product catalog interface by setting the **enable\_ai\_search\_in\_catalog** system property to true. For details on these configuration steps, see [Configuring AI Search for product catalog search](https://servicenow.com/docs/access?context=configure-ai-search-prod-catalog&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the Customer, Accounts, and Service Organizations UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

</td><td>

Zurich

</td></tr><tr><td>

RPA Hub

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://servicenow.com/docs/access?context=download-installer-rpa&family=zurich&ft:locale=en-US).

 The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Zurich.

 Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Zurich.

 Before upgrading RPA Hub to Zurich, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://servicenow.com/docs/access?context=t_AddAPropertyUsingSysPropsList&family=zurich&ft:locale=en-US).

 After you upgrade to Zurich, the bot process definitions change to the new structure, which is the bot process configuration.

 Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Zurich without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td><td>

Zurich

</td></tr><tr><td>

Retail applications

</td><td>

Starting with this release onwards, the retail base case has been made abstract. \(An abstract case or abstract case type is a base configuration of a case that is intended to be extended by specialized case types rather than used directly.\) After upgrading to the Zurich release and for any version updates beginning with the Yokohama release, if you are using the retail base case table you will no longer be able to create new cases or update existing cases. Use the following case types instead:

-   Store Inquiry
-   Retail Customer Complaint
-   In-store Operations
-   HQ Communications

 You can also extend your own case types. For more information on these changes, see the [Impact analysis and guidance: Retail case table updates \[KB2216547\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3Da312916e978aa650f03d739c1253af88%26sysparm_view%3D%26sysparm_domain%3Dnull%26sysparm_domain_scope%3Dnull) article in the Now Support Knowledge Base.

</td><td>

Zurich

</td></tr><tr><td>

SQL API

</td><td>

ServiceNow provided customers with a free SOAP‑based ODBC client. If you have an active RaptorDB Pro entitlement, you can migrate to the REST‑based SQL API client by completing the required configuration on both the server and client sides. For more information, see [Configure](https://servicenow.com/docs/access?context=configuring-sql-api&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Security Posture Control

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://servicenow.com/docs/access?context=spc-install&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Service Exchange

</td><td>

-   Service Exchange version 2.x.x: Which was first released with the Xanadu release, doesn’t support migration of Service Exchange \(Legacy\) versions.

Service Exchange \(Legacy\) version: Before you upgrade to the Zurich release, follow instructions in the [Service Bridge for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.

-   Service Exchange version 1.x.x: When upgrading, follow the steps in the [Upgrade Guide - Service Bridge for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) article in the Now Support Knowledge Base to migrate your Service Exchange applications.
-   Service Exchange version 2.x.x: Due to the introduction of mismatched version support, new entitlements can’t be activated until both the consumers and providers upgrade to Service Exchange version 2.x.x. Older active entitlements continue to work but new ones can’t be activated.
-   When you upgrade to Service Exchange version 2.0.55 with Sales and Order Management plug-in version 1.0.4, before upgrading the platform to the Zurich release, new Deny ACLs aren't installed. To ensure the Deny ACLs get installed, after upgrading to Zurich, select Repair to reinstall the Service Exchange application.
-   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility.
-   When you install the Service Exchange application, the Service Exchange Global Script Include is automatically installed or updated on the following platform versions:
    -   Washington DC patch 9
    -   Xanadu patch 4
    -   Yokohama
    -   Zurich

</td><td>

Zurich

</td></tr><tr><td>

Service Observability

</td><td>

If you have the snc\_sow\_svcobs.manager role, you must belong to a user groups with a type of `srm`.

</td><td>

Zurich

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

 For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://servicenow.com/docs/access?context=sow-itsm-itom-version&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

The dynamic schema application framework has been revised in the Zurich release. If you implemented dynamic schema in Xanadu or Yokohama, the application is automatically migrated to a new framework as part of the upgrade to the Zurich release. For details on the migration, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

</td><td>

Zurich

</td></tr><tr><td>

ServiceNow IDE

</td><td>

ServiceNow IDE version 2.1.2 is active by default on instances on the Zurich release. Update to ServiceNow IDE version 3.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Install or update the ServiceNow IDE](https://servicenow.com/docs/access?context=install-servicenow-ide&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

ServiceNow SDK

</td><td>

To upgrade to the latest version of the ServiceNow SDK globally or within an application, see [Upgrade the ServiceNow SDK](https://servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=zurich&ft:locale=en-US).

 ServiceNow SDK version 4.0 supports integration with ServiceNow instances beginning with the Washington DC release.

 On Windows systems, after upgrading to ServiceNow SDK version 4.3 or later, existing stored credentials aren’t supported due to the deprecation of Keytar. Users on Windows systems must add their user credentials again using the `now-sdk auth --add` command to authenticate with instances. For more information, see [Authenticate](https://servicenow.com/docs/access?context=authenticate-instance-now-sdk&family=zurich&ft:locale=en-US).

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow SDK repository](https://github.com/ServiceNow/sdk/releases) on GitHub.

</td><td>

Zurich

</td></tr><tr><td>

ServiceNow Studio

</td><td>

ServiceNow Studio no longer has to be downloaded from the ServiceNow Store. It’s available on the ServiceNow AI Platform by default.

</td><td>

Zurich

</td></tr><tr><td>

ServiceNow Vault

</td><td>

To install ServiceNow Vault, the following must be installed:

-   [Data Discovery](https://servicenow.com/docs/access?context=data-discovery-landing&family=zurich&ft:locale=en-US)
-   [Data Privacy](https://servicenow.com/docs/access?context=data-privacy-landing&family=zurich&ft:locale=en-US)
-   [Data anonymization](https://servicenow.com/docs/access?context=dps-data-anonymization&family=zurich&ft:locale=en-US)
-   [Field Encryption](https://servicenow.com/docs/access?context=field-encryption&family=zurich&ft:locale=en-US)
-   [Zero Trust Access](https://servicenow.com/docs/access?context=session-access&family=zurich&ft:locale=en-US)

</td><td>

Zurich

</td></tr><tr><td>

Skills Foundation

</td><td>

You cannot download industry skills data as part of the guided setup.

</td><td>

Zurich

</td></tr><tr><td>

Software Asset Management

</td><td>

Starting from the Zurich release, the following workflows are migrated to Flow Designer as flows:

-   Reclamation workflow
-   Procurement Process Flow - Auto allocation enabled

When upgrading to the Zurich release, a fix script identifies whether the workflows were customized. If you haven't customized the workflows before the upgrade, the fix script deactivates the legacy workflows from the instance and deploys the Flow Designer flows on the instance post-upgrade. If you have customized the impacted workflows in the previous release, the fix script doesn’t deploy the Flow Designer flows on the instance post-upgrade. You can view and access the impacted workflows in the instance after the upgrade. However, the deprecated workflows are considered as custom code and ServiceNow doesn’t support those workflows.

 Starting from the Zurich release, the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is moved from the family release to the Software Asset Workspace store application. After upgrading to Zurich, the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is inactivated and the Software Asset Workspace store application \(sn\_sam\_workspace\) is enabled in the instance.

 When upgrading to the Software Asset Management – SaaS License Management plugin \(sn\_sam\_saas\_int\) version 16.0.6 or later in the Zurich release, verify that the Software Asset Workspace store app \(sn\_sam\_workspace\) is updated to version 9.0.4.

</td><td>

Zurich

</td></tr><tr><td>

Source-to-Pay Operations Integrations

</td><td>

**Important:** Due to a performance issue identified with the upgrade fix script, the sourcing fix script has been modified. This script will no longer execute automatically during the upgrade process. Instead, it is now delivered as an on-demand job. Administrators must manually execute this job outside of business hours after the upgrade is complete.

</td><td>

Zurich

</td></tr><tr><td>

Strategic Planning

</td><td>

After upgrading to Strategic Planning v4.8.0, the existing **Investment type** and **Investment class** fields will appear as **Investment type \(Deprecated\)** and **Investment class \(Deprecated\)** respectively across the Planning page including in the Prioritization and Roadmap views and in the Scenario Planning page. The values from these deprecated fields will be automatically copied to the new **Investment type** and **Investment class** fields.

 If you previously applied filters or personalized your view using the deprecated fields, you must update those configurations to use the new **Investment type** and **Investment class** fields across the workspace—including in the Prioritization and Roadmap views on the Planning page, as well as in the Scenario Planning page.

</td><td>

Zurich

</td></tr><tr><td>

Subscription Management

</td><td>

Subscription Management version 5.0 is active by default on all instances of the Zurich release. Update to Subscription Management version 6.1 or later to use the latest features. For more information about updating Subscription Management, see [Update an app or plugin](https://servicenow.com/docs/access?context=update-application-app-mgr&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Synthetic monitoring

</td><td>

If you want to run monitors using a MID Server as a location, you must restart the MID Server after upgrading.

</td><td>

Zurich

</td></tr><tr><td>

Third-party Risk Management

</td><td>

If you’re a VRM user upgrading to TPRM and upgrading to Vancouver or a later release from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](https://servicenow.com/docs/access?context=grc-tprm-upgrade-info&family=zurich&ft:locale=en-US).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

</td><td>

Zurich

</td></tr><tr><td>

Unified Security Exposure Management

</td><td>

Unified Security Exposure Management is available to all customers who are entitled to Vulnerability Response, however, migrating to USEM is a major upgrade that introduces a unified architecture for improved performance, scalability, and streamlined workflows. Before upgrading, leverage the Migration assistant for Unified Security Exposure Management that is available as an update set. See the [Migration Guidance to Unified Security Exposure Management \[KB2556844\]](https://support.servicenow.com/kb?sys_kb_id=8652717893a8ba94f538fb2d6cba1078&id=kb_article_view) Knowledge Base article for more information. This tool provides a guided experience for plugin installation, data mapping, rule migration, and post-migration validation, reducing risk and manual effort. Ensure that all integrations and workflows are reviewed for compatibility before initiating migration. For more information, see [Migrating to USEM](https://servicenow.com/docs/access?context=migrating-to-usem&family=zurich&ft:locale=en-US) and [Migrate to USEM](https://servicenow.com/docs/access?context=migrate-to-usem&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr><tr><td>

Vulnerability Response

</td><td>

If you are currently using Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Vulnerability Response and for upgrades to supported third-party integration applications.

 The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&family=zurich&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to new version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

 For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td><td>

Zurich

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

If you have existing scheduled extractions and have upgraded to Zurich, run the **Scheduled Extraction V2 Move** fix script to place scheduled extractions in a new table where scheduling is done by the scheduled scripts engine. For detailed steps, see [Run fix scripts](https://servicenow.com/docs/access?context=t_RunFixScripts&family=zurich&ft:locale=en-US).

</td><td>

Zurich

</td></tr></tbody>
</table>