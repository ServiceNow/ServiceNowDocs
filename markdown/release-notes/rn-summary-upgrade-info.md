---
title: Upgrade information for all Zurich features and products
description: Cumulative release notes summary on upgrade information for Zurich features and products.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 33
breadcrumb: [Release notes summaries for Zurich features, Release notes for upgrading from Yokohama, Learn about the Zurich release, Zurich release notes]
---

# Upgrade information for all Zurich features and products

Cumulative release notes summary on upgrade information for Zurich features and products.

Before you upgrade to Zurich, review the upgrade information for any products you may have. Some products require you to complete specific tasks before you upgrade.

<table id="rn-summary-upgrade-info-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Search

</td><td>

After you upgrade to Zurich from an earlier family release, run full document crawls in all your external content connectors to update their semantic vector indexing field mappings.

</td></tr><tr><td>

Application Manager

</td><td>

Application Manager is active by default on instances on the Zurich release. Upgrade your instance to Zurich patch 4 or later to use the latest features. For information about upgrading your ServiceNow AI Platform instance, see [Prepare your upgrade](../concept/rn-prepare-landing-page.md).

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   If you are currently using Application Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Application Vulnerability Response and for upgrades to supported third-party integration applications.
-   For information about the new features of Vulnerability Response, see the [Vulnerability Response release notes](../security-operations/secops-vuln-resp-rn.md).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Automated Test Framework

</td><td>

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

The tests can produce a pass result only when you run them on a base system without any customizations and with the default demo data that is provided with the application or feature plugin. To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data. For more information, see [Available quick start tests by application or feature](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

CPQ Configurator

</td><td>

If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading, you must set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true to be able to use the configurator in Sales Customer Relationship Management workflows.

</td></tr><tr><td>

Change Management

</td><td>

As part of the update to use Flow instead of Progress Workers for conflict detection, the Conflict Checker Progress UI Formatter record references a new UI macro, change\_conflict\_worker\_progress\_gate. This macro checks the **change.conflict.useprogressworker** system property to determine the conflict detection mechanism and then displays the corresponding UI macro to work with either Progress Workers or the Change Management Worker table. For more information, see [Conflict detection](https://www.servicenow.com/docs/access?context=c_ConflictDetection&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Cloud Cost Management 9.0

</td><td>

The Cloud Cost Management platform support is available beginning with the Xanadu release. For instructions on upgrading Cloud Cost Management to Zurich, see [Upgrade Cloud Cost Management](https://www.servicenow.com/docs/access?context=upgrade-cloud-insights-to-version-3-0&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

</td></tr><tr><td>

Cloud Exposure View

</td><td>

The Cloud Exposure View is a workspace in the Cloud Security for Cloud Workspace application that is supported by the Unified Security Exposure Management application. Unified Security Exposure Management \(USEM\) and the Cloud Security for Cloud Workspace applications are required. USEM is available to all customers who are entitled to Vulnerability Response. See [Unified Security Exposure Management release notes](../security-operations/secops-sem-rn.md) for more information.

</td></tr><tr><td>

Configuration Compliance

</td><td>

If you are currently using Configuration Compliance, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Configuration Compliance and for upgrades to supported third-party integration applications.

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

Due to the removal of the **Design** value for the operational status attribute in a CI, after an upgrade, you must review all CIs that have the discovery source attribute set to **Manual via IRE**. Review the operational status attribute of those CIs and set it to a supported value in CMDB for your environment. For example, you can set the attribute to **Non-Operational**. For more information about the operational status values, see [Life cycle of tangible/physical CIs](https://www.servicenow.com/docs/access?context=csdm-lifecycle-hardware&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

On an upgraded Zurich instance, to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks, you must manually run the scheduled job **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles**. This scheduled job modifies the user roles as follows:

-   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
-   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).

</td></tr><tr><td>

Container Vulnerability Response

</td><td>

If you are currently using Container Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Container Vulnerability Response and for upgrades to supported third-party integration applications.

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

For more information about the released versions of the Container Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Customer self-service for Sales and Order Management

</td><td>

The new order checkout experience and improved cart capabilities are delivered through a new Sales Cart plugin \(sn\_sales\_cart\). As an admin, you must perform the [Post-upgrade order migration for the Business Portal](https://www.servicenow.com/docs/access?context=post-upgrade-task-business-portal&version=zurich&pubname=zurich-order-management&ft:locale=en-US) to continue providing a seamless experience for your customers. Failing to perform the upgrade steps can result in your customers losing products added to their carts.

</td></tr><tr><td>

Digital End-User Experience

</td><td>

For details on DEX data migration, refer to the [DEX data migration to allocated, last logged in user, last logged in location column of Dex device table \[KB2144029\]](https://support.servicenow.com/kb?sys_kb_id=57fcf86d97ed6650dfd73dae2153af59&id=kb_article_view) and [DEX data migration to CI type column of Alert Metadatas table \[KB2141007\]](https://support.servicenow.com/kb?sys_kb_id=269e049147e5aa503b05ff48436d433c&id=kb_article_view) articles in the Now Support Knowledge Base.

</td></tr><tr><td>

Encryption

</td><td>

For the GlideEncrypter API, NIST 800-131A Rev 2 has recommended against using the Triple Data Encryption Standard \(3DES\) encryption. The following changes are taking place in the Zurich release with the official removal of 3DES encryption for GlideEncrypter.

-   The GlideEncrypter API defaults to using the Key Management Framework \(KMF\) based algorithm, Advanced Encryption Standard \(AES\), for encryption and decryption operations for upgraded instances only.
-   For instances created with the Zurich release or later, this API isn’t supported.
-   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

In the Zurich release, Column Level Encryption has received a required upgrade to Key Management Framework Column Level Encryption \(KMF-CLE\) due to the platform-wide deprecation of 3DES. For more information about this upgrade, see KB1700704.

</td></tr><tr><td>

Encryption Key Management

</td><td>

-   In previous releases, the GlideEncrypter API used the three-key Triple Data Encryption Standard \(3DES\) encryption standard, which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Zurich release in preparation for a full deprecation of GlideEncrypter/3DES in the future:
    -   New Zurich instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Zurich instances, you can still GlideEncrypter, which has been updated to use AES256-GCM encryption via the Key Management Framework.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td></tr><tr><td>

Enterprise Asset Management

</td><td>

Starting with Zurich release, a new menu, Asset put away, has been added to the ServiceNow Agent app navigation bar. When upgrading to the Zurich release, a fix script identifies whether the ServiceNow Agent app navigation bar was customized and takes the necessary action.

-   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(![Asset put away icon](../image/asset-putaway-icon-ma.png)\) is included in the navigation bar
-   If the navigation bar was customized before the upgrade, two navigation bars appear: Customized old IT Asset Management and IT Asset Management. The new icon appears in the IT Asset Management navigation bar.

</td></tr><tr><td>

External Content Connectors

</td><td>

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

When you upgrade to version 4 of the External Content Connectors application from an earlier version, searches may not show all previously crawled content until you've completed both a content crawl and a user mapping crawl for each upgraded connector. The first content crawl run after the upgrade will reindex all searchable content from the source system, and the user mapping crawl will reindex all security principals from the source system. All crawled content should be shown in searches after both of these crawls are complete.

</td></tr><tr><td>

Field Service Management

</td><td>

Effective March 1, 2025, the Google Places API, Directions API, and Distance Matrix API have been designated as legacy services. The newer versions of these services are Places API \(New\) and Routes API. Google Maps APIs for Field Service capabilities uses the latest version of the APIs in the Zurich release and Dispatcher Workspace version 8.0. To help avoid issues with the Google Maps APIs, enable Places API \(New\) and Routes API from Google Cloud Platform Console.

</td></tr><tr><td>

Flows, subflows, and actions in Workflow Studio

</td><td>

An earlier version of the save as you go feature was released and withdrawn from the Washington DC release. If you're upgrading from the Washington DC release, you might have manually turned off the save as you go features by setting a system property. To restore the save as you go features, see [Restore save as you go functionality](https://www.servicenow.com/docs/access?context=restore-save-as-you-go-functionality&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

Generative AI Controller

</td><td>

Generative AI Controller is installed or updated when you install or update a Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) or open a support case.

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
    -   If the navigation bar wasn’t customized before the upgrade, a new Asset put away icon \(![Asset put away icon](../image/asset-putaway-icon-ma.png)\) is included in the navigation bar
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

</td></tr><tr><td>

Impact

</td><td>

The Impact Store Application configuration requires a sequence of tasks in a unified registration process. See [Configure the Impact Store Application](https://www.servicenow.com/docs/access?context=configuring-impact-platform&version=zurich&pubname=zurich-impact&ft:locale=en-US).

</td></tr><tr><td>

Instance Data Replication

</td><td>

-   Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see [Upgrading legacy replication sets to V2 in Instance Data Replication](https://www.servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

</td></tr><tr><td>

MID Server

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

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

</td></tr><tr><td>

Now Assist

</td><td>

Customers who have not opted into third-party, large language models may be routed to them during skill execution. If the new model is not provisioned or available in your environment, this will result in skill execution failures. Check the models your skills use within Now Assist admin console.

If you customized UI actions or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions might not work as expected.

If you run into issues when you're upgrading a Now Assist product, see the [Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates \[KB1637452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) article in the Now Support Knowledge Base. Log in to view the article.

The Zurich release introduces enhanced protections for read‑only fields across the ServiceNow® AI Platform. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back-end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. If you have custom client scripts that modify ServiceNow® ‑owned read‑only fields using `g_form.setValue()` or `g_form.clearValue()`, refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122). This article provides additional technical details on how to identify affected fields and adjust their settings.

The existing Access Control Lists \(ACLs\) will be updated to replace the 'admin' role with specific, purpose-driven granular roles within scripts or security attributes. As part of this update, the `getRoles()` API will be replaced with the `hasRole()` API for authorization purposes. Additionally, all references to the 'admin' role in the code will be substituted with the new feature-specific granular roles for authorization use cases. Read [https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html](https://www.servicenow.com/docs/r/platform-security/granular-admin-roles.html) to learn more.

</td></tr><tr><td>

Now Assist for CMDB

</td><td>

The installation \(activation\) process has changed for the Now Assist for CMDB v2.1 plugin. See [Configuring Now Assist for CMDB](https://www.servicenow.com/docs/access?context=now-assist-cmdb-configuring&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for the new instructions.

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

If you have the procurement\_user user role, you can access the help manage hardware asset requests agentic workflow, which includes the following AI agents:

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. When you upgrade to the [Zurich Patch 8](../quality/zurich-patch-8.md) release, if you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy. For more information, see [Incident assist skill](https://www.servicenow.com/docs/access?context=now-assist-itsm-incident-assist&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

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

For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

**Note:** Upgrading the Now Assist plugins activates any designated skills that were previously untouched by the customer.

-   If you installed the plugins for a skill but never configured it, meaning you never activated it nor adjusted associated roles, any skill on by default is activated on a per skill basis when upgrade.
-   If you previously toggled a skill from active and then back to inactive, or updated any roles for that skill, that skill remains inactive when upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

When you update the Now Assist for Security Incident Response \(SIR\) application, the dependency applications are automatically updated.

For more information about required applications for Now Assist for Security Incident Response, see [Supporting information for Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-security-incident&version=zurich&pubname=zurich-security-management&ft:locale=en-US).

The AI Search application must be enabled so that the recommended actions skill works for security incidents with Now Assist for Security Incident Response. To verify that AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search isn’t enabled.

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

For more information about required applications for Now Assist for Vulnerability Response, see [Supporting information for Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-vr&version=zurich&pubname=zurich-security-management&ft:locale=en-US).

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

If you’re upgrading to Now Assist in Contract Management from Yokohama \(Patch 2 and lower\) or Xanadu \(Patch 8 and lower\), and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
2.  In the **Name** field, search for `Upsert DI skill config`.
3.  In the script, add the use case IDs that you want to migrate to the Now Assist Admin console.
4.  Select **Run Fix Script**.

For more information, see [Post-upgrade steps for Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cmpro-na-upgrade-steps&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

</td></tr><tr><td>

On-Call Scheduling

</td><td>

Starting from the Zurich release, On-Call Scheduling uses subflows, not workflows. You must transition from workflows to subflows, because the workflows are considered as legacy workflows. For existing users in Zurich, your current workflows continue to be supported. However, for new users, the On-Call Scheduling plugin installations on Zurich and later instances only use subflows.

Maintain, build, and modify your own custom on-call scheduling flows in Workflow Studio with subflows for new instances. The following subflows are available for configuration:

</td></tr><tr><td>

Operational Resilience

</td><td>

After upgrading to Operational Resilience version 21.0.x, rerun the **Update CSDM and other dependencies** scheduled job to populate the additional metadata that was introduced in this release.

</td></tr><tr><td>

Performance Analyzer

</td><td>

Starting with the Zurich release, Performance Analyzer is available on your instance automatically. For access to Performance Analyzer on earlier instances, install Performance Analyzer from the ServiceNow® Store.

</td></tr><tr><td>

Platform Analytics experience

</td><td>

On upgrade, any homepages on your instance that have been opened are migrated to Core UI dashboards, which are visible in the dashboard library. For more information, see [Homepage deprecation](https://www.servicenow.com/docs/access?context=homepage-deprecation-help-tool&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

Simple lists are all converted to the new List element on upgrade.

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

After you upgrade to Zurich, update the Workflow Studio application in the ServiceNow Store.

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

Pricing Management v15.0.0 provides a default pricing plan that includes new steps to support pricing strategies introduced in this release. If you're using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after you upgrade. Determine whether you want to publish the default plan or customize the default pricing plan for your needs. The default plan contains new steps for calculating net pricing and roll-up values for configurable products in quotes and orders: Net Price Calculation, Line Rollup, and Header Rollup steps. This pricing functionality existed in previous releases for quotes and orders but wasn’t included in the default pricing plan. To retain this previous functionality for quotes and orders, you must add the Net Price Calculation, Line Rollup, and Header Rollup steps in your custom pricing plan before you publish it for use.

If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true. When set to true, this property enables the CPQ Configurator.

If you want to use AI Search for product catalog searches, before upgrading install Now Assist for Sales Force Automation \(SFA\), which includes the plugins needed for AI Search functionality. After upgrading, complete various steps to implement AI Search. These steps include running a scheduled job to set up AI Search and enabling AI Search in the product catalog interface by setting the **enable\_ai\_search\_in\_catalog** system property to true. For details on these configuration steps, see [Configuring AI Search for product catalog search](https://www.servicenow.com/docs/access?context=configure-ai-search-prod-catalog&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

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

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Zurich.

Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Zurich.

Before upgrading RPA Hub to Zurich, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

After you upgrade to Zurich, the bot process definitions change to the new structure, which is the bot process configuration.

Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Zurich without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Retail applications

</td><td>

Starting with this release onwards, the retail base case has been made abstract. \(An abstract case or abstract case type is a base configuration of a case that is intended to be extended by specialized case types rather than used directly.\) After upgrading to the Zurich release and for any version updates beginning with the Yokohama release, if you are using the retail base case table you will no longer be able to create new cases or update existing cases. Use the following case types instead:

-   Store Inquiry
-   Retail Customer Complaint
-   In-store Operations
-   HQ Communications

You can also extend your own case types. For more information on these changes, see the [Impact analysis and guidance: Retail case table updates \[KB2216547\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb_knowledge.do%3Fsys_id%3Da312916e978aa650f03d739c1253af88%26sysparm_view%3D%26sysparm_domain%3Dnull%26sysparm_domain_scope%3Dnull) article in the Now Support Knowledge Base.

</td></tr><tr><td>

SQL API

</td><td>

ServiceNow provided customers with a free SOAP‑based ODBC client. If you have an active RaptorDB Pro entitlement, you can migrate to the REST‑based SQL API client by completing the required configuration on both the server and client sides. For more information, see [Configuring SQL API](https://www.servicenow.com/docs/access?context=configuring-sql-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Security Posture Control

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://www.servicenow.com/docs/access?context=spc-install&version=zurich&pubname=zurich-security-management&ft:locale=en-US).

</td></tr><tr><td>

Service Exchange

</td><td>

-   Service Exchange version 2.x.x: Which was first released with the Xanadu release, doesn’t support migration of Service Exchange \(Legacy\) versions.

Service Exchange \(Legacy\) version: Before you upgrade to the Zurich release, follow instructions in the [Service Bridge for Providers \(Legacy\) - Migration Utility \[KB1499823\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1499823) article in the Now Support Knowledge Base to migrate your configuration data.

-   Service Exchange version 1.x.x: When upgrading, follow the steps in the [Upgrade Guide - Service Bridge for Providers and Consumers application \(v2.x.x release\) \[KB1700387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700387) article in the Now Support Knowledge Base to migrate your Service Exchange applications.
-   Service Exchange version 2.x.x: Due to the introduction of mismatched version support, new entitlements can’t be activated until both the consumers and providers upgrade to Service Exchange version 2.x.x. Older active entitlements continue to work but new ones can’t be activated.
-   When you upgrade to Service Exchange version 2.0.55 with Sales Customer Relationship Management plug-in version 1.0.4, before upgrading the platform to the Zurich release, new Deny ACLs aren't installed. To ensure the Deny ACLs get installed, after upgrading to Zurich, select Repair to reinstall the Service Exchange application.
-   When using Service Exchange for Providers and Service Exchange for Consumers in a single instance, you must upgrade both applications simultaneously to the same version to maintain compatibility.
-   When you install the Service Exchange application, the Service Exchange Global Script Include is automatically installed or updated on the following platform versions:
    -   Washington DC patch 9
    -   Xanadu patch 4
    -   Yokohama
    -   Zurich

</td></tr><tr><td>

Service Observability

</td><td>

If you have the snc\_sow\_svcobs.manager role, you must belong to a user groups with a type of `srm`.

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://www.servicenow.com/docs/access?context=sow-itsm-itom-version&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

ServiceNow AI Platform core feature

</td><td>

The dynamic schema application framework has been revised in the Zurich release. If you implemented dynamic schema in Xanadu or Yokohama, the application is automatically migrated to a new framework as part of the upgrade to the Zurich release. For details on the migration, see the [Dynamic Schema Zurich Migration Guide \[KB2146133\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2146133) article in the Now Support Knowledge Base.

</td></tr><tr><td>

ServiceNow IDE

</td><td>

ServiceNow IDE version 2.1.2 is active by default on instances on the Zurich release. Update to ServiceNow IDE version 3.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Install or update the ServiceNow IDE](https://www.servicenow.com/docs/access?context=install-servicenow-ide&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr><tr><td>

ServiceNow SDK

</td><td>

To upgrade to the latest version of the ServiceNow SDK globally or within an application, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

ServiceNow SDK version 4.0 supports integration with ServiceNow instances beginning with the Washington DC release.

On Windows systems, after upgrading to ServiceNow SDK version 4.3 or later, existing stored credentials aren’t supported due to the deprecation of Keytar. Users on Windows systems must add their user credentials again using the `now-sdk auth --add` command to authenticate with instances. For more information, see [Authenticating to a ServiceNow instance with the ServiceNow SDK](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow SDK repository](https://github.com/ServiceNow/sdk/releases) on GitHub.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

ServiceNow Studio no longer has to be downloaded from the ServiceNow Store. It’s available on the ServiceNow AI Platform by default.

</td></tr><tr><td>

ServiceNow Vault

</td><td>

To install ServiceNow Vault, the following must be installed:

-   [Data Discovery](https://www.servicenow.com/docs/access?context=data-discovery-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)
-   [Data Privacy](https://www.servicenow.com/docs/access?context=data-privacy-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)
-   [Data anonymization](https://www.servicenow.com/docs/access?context=dps-data-anonymization&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)
-   [Field Encryption](https://www.servicenow.com/docs/access?context=field-encryption&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)
-   [Zero Trust Access \(ZTA\)](https://www.servicenow.com/docs/access?context=session-access&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

</td></tr><tr><td>

Skills Foundation

</td><td>

You cannot download industry skills data as part of the guided setup.

</td></tr><tr><td>

Software Asset Management

</td><td>

Starting from the Zurich release, the following workflows are migrated to Flow Designer as flows:

-   Reclamation workflow
-   Procurement Process Flow - Auto allocation enabled

When upgrading to the Zurich release, a fix script identifies whether the workflows were customized. If you haven't customized the workflows before the upgrade, the fix script deactivates the legacy workflows from the instance and deploys the Flow Designer flows on the instance post-upgrade. If you have customized the impacted workflows in the previous release, the fix script doesn’t deploy the Flow Designer flows on the instance post-upgrade. You can view and access the impacted workflows in the instance after the upgrade. However, the deprecated workflows are considered as custom code and ServiceNow doesn’t support those workflows.

Starting from the Zurich release, the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is moved from the family release to the Software Asset Workspace store application. After upgrading to Zurich, the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is inactivated and the Software Asset Workspace store application \(sn\_sam\_workspace\) is enabled in the instance.

When upgrading to the Software Asset Management – SaaS License Management plugin \(sn\_sam\_saas\_int\) version 16.0.6 or later in the Zurich release, verify that the Software Asset Workspace store app \(sn\_sam\_workspace\) is updated to version 9.0.4.

</td></tr><tr><td>

Source-to-Pay Operations Integrations

</td><td>

**Important:** Due to a performance issue identified with the upgrade fix script, the sourcing fix script has been modified. This script will no longer execute automatically during the upgrade process. Instead, it is now delivered as an on-demand job. Administrators must manually execute this job outside of business hours after the upgrade is complete.

</td></tr><tr><td>

Strategic Planning

</td><td>

After upgrading to Strategic Planning v4.8.0, the existing **Investment type** and **Investment class** fields will appear as **Investment type \(Deprecated\)** and **Investment class \(Deprecated\)** respectively across the Planning page including in the Prioritization and Roadmap views and in the Scenario Planning page. The values from these deprecated fields will be automatically copied to the new **Investment type** and **Investment class** fields.

If you previously applied filters or personalized your view using the deprecated fields, you must update those configurations to use the new **Investment type** and **Investment class** fields across the workspace—including in the Prioritization and Roadmap views on the Planning page, as well as in the Scenario Planning page.

</td></tr><tr><td>

Subscription Management

</td><td>

Subscription Management version 5.0 is active by default on all instances of the Zurich release. Update to Subscription Management version 6.1 or later to use the latest features. For more information about updating Subscription Management, see [Update an application or plugin](https://www.servicenow.com/docs/access?context=update-application-app-mgr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Synthetic monitoring

</td><td>

If you want to run monitors using a MID Server as a location, you must restart the MID Server after upgrading.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

If you’re a VRM user upgrading to TPRM and upgrading to Vancouver or a later release from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. For example, you must upgrade from Utah to Vancouver, Vancouver to Washington DC, and so on. If the scripts don’t run in the correct order, you can get data inconsistencies, broken functionalities, and conflicts.

After upgrading to version 21.0.x, you can enable the Smart Assessment Engine \(SAE\) by setting the Smart Assessment Engine enabled \(**sn\_vdr\_risk\_asmt.sae\_enabled**\) property. After setting this property, Smart Assessment Engine \(SAE\) becomes the default assessment engine and replaces the legacy experience. The transition isn’t reversible.

**Warning:**

Set this property in your non-production instances and conduct thorough testing before changing your production instances. Failure to do so may result in unexpected issues.

For more information on upgrading from VRM to TPRM and the differences between the Smart and Classic Assessment engines, see [Third-party Risk Management upgrade information](../governance-risk-compliance/grc-tprm-upgrade-info.md).

For existing TPRM customers, after upgrading to version 21.0.3, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

</td></tr><tr><td>

Unified Security Exposure Management

</td><td>

Unified Security Exposure Management is available to all customers who are entitled to Vulnerability Response, however, migrating to USEM is a major upgrade that introduces a unified architecture for improved performance, scalability, and streamlined workflows. Before upgrading, leverage the Migration assistant for Unified Security Exposure Management that is available as an update set. See the [Migration Guidance to Unified Security Exposure Management \[KB2556844\]](https://support.servicenow.com/kb?sys_kb_id=8652717893a8ba94f538fb2d6cba1078&id=kb_article_view) Knowledge Base article for more information. This tool provides a guided experience for plugin installation, data mapping, rule migration, and post-migration validation, reducing risk and manual effort. Ensure that all integrations and workflows are reviewed for compatibility before initiating migration. For more information, see [Migrating from Vulnerability Response to Unified Security Exposure Management \(USEM\)](https://www.servicenow.com/docs/access?context=migrating-to-usem&version=zurich&pubname=zurich-security-management&ft:locale=en-US) and [Migrate to Unified Security Exposure Management \(USEM\) from Vulnerability Response](https://www.servicenow.com/docs/access?context=migrate-to-usem&version=zurich&pubname=zurich-security-management&ft:locale=en-US).

</td></tr><tr><td>

Vulnerability Response

</td><td>

If you are currently using Vulnerability Response, and you do not intend to upgrade to Unified Security Exposure Management \(USEM\), install a version below v30.x of Vulnerability Response and for upgrades to supported third-party integration applications.

The Missing Assets \[sn\_vul\_wiz\_missing\_asset\] table used for storing assets imported by the backfill integrations for the [Vulnerability Response Integration with Wiz](https://www.servicenow.com/docs/access?context=vr-wiz-exploring-host-cf&version=zurich&pubname=zurich-security-management&ft:locale=en-US) is deprecated. If you are currently using the Vulnerability Response with Wiz integrations, after updating to new version 1.1, you must backdate any of your existing Wiz primary integrations by three days and run them. Please review more information about the Wiz integration at [SecOps articles on the Security Operations Community](https://www.servicenow.com/community/secops-articles/announcement-wiz-integration-with-servicenow-secops/ta-p/3325055).

For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Zurich release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Zero Copy Connector for ERP

</td><td>

If you have existing scheduled extractions and have upgraded to Zurich, run the **Scheduled Extraction V2 Move** fix script to place scheduled extractions in a new table where scheduling is done by the scheduled scripts engine. For detailed steps, see [Run fix scripts](https://www.servicenow.com/docs/access?context=t_RunFixScripts&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Zurich features](../release-notes-summaries.md)

