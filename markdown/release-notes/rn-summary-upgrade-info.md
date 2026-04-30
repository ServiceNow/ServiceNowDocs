---
title: Upgrade information for all Yokohama features and products
description: Cumulative release notes summary on upgrade information for Yokohama features and products.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-04-08"
reading_time_minutes: 22
breadcrumb: [Release notes summaries for Yokohama features, Release notes for upgrading from Xanadu, Learn about the Yokohama release, Yokohama release notes]
---

# Upgrade information for all Yokohama features and products

Cumulative release notes summary on upgrade information for Yokohama features and products.

Before you upgrade to Yokohama, review the upgrade information for any products you may have. Some products require you to complete specific tasks before you upgrade.

<table id="rn-summary-upgrade-info-table" class="custom-rows"><thead><tr><th class="filter">

Application or feature

</th><th>

Details

</th></tr></thead><tbody><tr><td>

AI Control Tower

</td><td>

General availability release, no upgrade.

</td></tr><tr><td>

AI Search

</td><td>

When you upgrade to Yokohama from an earlier release, make knowledge block content searchable by reindexing all your indexed sources that include knowledge articles. For details on reindexing, see [Perform a full table index or reindex for a single AI Search indexed source](https://www.servicenow.com/docs/access?context=index-single-source-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) or [Perform a full table index or reindex for multiple AI Search indexed sources](https://www.servicenow.com/docs/access?context=index-multiple-sources-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Accounts Payable Operations

</td><td>

If you’re upgrading from a previous release, you must configure the reference field in the Tax Code \[sn\_fin\_tax\_code\] table. The exception engine validates the invoice using the tax code and raises exceptions if necessary.

</td></tr><tr><td>

App Engine Studio

</td><td>

Due to a new process for assigning groups in AEMC, the same version of the Application Intake plugin must be activated on each of your instances.

For more information, see [App Readiness and Compliance Report](https://www.servicenow.com/docs/access?context=app-readiness-report&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td>

Application Manager

</td><td>

Application Manager is active by default on instances on the Yokohama release. Upgrade your instance to Yokohama patch 11 or later to use the latest features. For information about upgrading your ServiceNow AI Platform instance, see [Prepare your upgrade](../concept/rn-prepare-landing-page.md).

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

-   For information about the new features of Vulnerability Response, see [Vulnerability Response release notes](../security-operations/secops-vuln-resp-rn.md).
-   For more information about the released versions of the Application Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Xanadu release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Automated Test Framework

</td><td>

Copy and customize quick start tests provided by the ServiceNow AI Platform® to validate that your instance works after you make any configuration changes. For example, if you apply an upgrade or develop an application.

The tests can produce a pass result only when you run them on a base system without any customizations and with the default demo data that is provided with the application or feature plugin. To apply a quick start test to your instance-specific data, copy the quick start test and add your custom data. For more information, see [Available quick start tests by application or feature](https://www.servicenow.com/docs/access?context=available-quick-start-tests&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

Three new indexes \(parent, type\), \(child, type\), and \(child, parent, type, port\) are added to the CI Relationship \[cmdb\_rel\_ci\] table to improve the performance of Identification and Reconciliation Engine \(IRE\) querying this table. This change is likely to increase upgrade time. For more information about the impact of this change during upgrade and to learn how to minimize that impact, see [Increased Yokohama Upgrade Time due to cmdb\_rel\_ci index additions \[KB1703367\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB1703367).

</td></tr><tr><td>

Data Management

</td><td>

-   After upgrading a self-hosted instance to Yokohama, the sys\_physical\_table\_stats table doesn't display the latest data for table size, with the sample\_period\_start column showing dates prior to the upgrade. To see the correct table size, you can set the com.glide.stats.storage\_disk\_usage.information\_schema system property to true, which allows the statsGatherer job to use the information schema to generate the required database statistics.

-   A data management policy record is automatically created for each table that is configured with an archive rule or a table cleaner rule prior to the upgrade.

</td></tr><tr><td>

Data Privacy

</td><td>

Licensing changes enable you to install Data Discovery, Data Discovery APIs, Data Anonymization, and Data Privacy APIs without an entitlement, but you must have an entitlement to run a job.

</td></tr><tr><td>

DevOps Change Velocity

</td><td>

If you are a new customer or are using a zBoot instance and you want to create type-based workflow change requests in DevOps Change Velocity, you must add the**com.snc.change\_management.change\_model.type\_compatibility** property and set it to True. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

If you are an upgrading customer, you must run the **ReConfigure Bitbucket Server Repositories for PullRequest** job to re-configure your existing Bitbucket Server or Bitbucket Data Center repositories so that pull request records can be imported. You can navigate to **All &gt; System Definition &gt; Scheduled Jobs** to search for this job and run it.

</td></tr><tr><td>

Digital End-User Experience

</td><td>

To upgrade your DEX Desktop Assistant, do the following:

1.  Install the latest version of the Desktop Assistant in your instance.
2.  With admin rights, reinstall the Desktop Assistant on your local machine even if you have the latest version.

</td></tr><tr><td>

Encryption Key Management

</td><td>

-   The GlideEncrypter API uses the three-key Triple Data Encryption Standard \(3DES\) encryption standard which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using after 2023. The following changes are taking place in the Yokohama release in preparation for a full deprecation of GlideEncrypter/3DES in the future.
    -   New Yokohama instances can’t use GlideEncrypter. All base system scripts have been changed to use alternative encryption processes.
    -   if you’re upgrading your Yokohama instances, you can still use 3DES, but you can also disable 3DES usage with a system property.
    -   Learn more about 3DES deprecation in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704481).

</td></tr><tr><td>

External Content Connectors

</td><td>

Beginning with version 2 of the External Content Connectors application, external content connectors implement semantic vector indexing for crawled items. When you upgrade to a version that supports semantic vector indexing, your existing connectors will reindex all previously retrieved items the next time they're visited by a crawl, even if those items' content is unchanged. To force semantic vector indexing of your external content items as soon as possible after upgrading, cancel any running crawls, then restart the canceled crawls manually.

When you upgrade to version 4 of the External Content Connectors application from an earlier version, searches may not show all previously crawled content until you've completed both a content crawl and a user mapping crawl for each upgraded connector. The first content crawl run after the upgrade will reindex all searchable content from the source system, and the user mapping crawl will reindex all security principals from the source system. All crawled content should be shown in searches after both of these crawls are complete.

</td></tr><tr><td>

Field Service Management

</td><td>

-   Upgrading to Yokohama may extend the upgrade maintenance time of a customer due to Appointment Booking. The Appointment Booking configuration tables get extended to the Application File \[sys\_metadata\] table as a part of the upgrade. After upgrading to Yokohama, re-parenting occurs automatically and the duration of the re-parenting depends on the number of records in Application File \[sys\_metadata\] table.
-   Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API. You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. If you need to create a new Google API key after March 1, 2025, you must enable the new APIs from Google Console and upgrade to Yokohama Patch 3 version or higher to ensure compatibility.

</td></tr><tr><td>

Financial Services Card Operations

</td><td>

During the upgrade to Yokohama, the Financial Services Card Operations plugin reparents the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] to the Financial Task table \[sn\_bom\_task\] in Financial Services Operations Core.

Reparenting leverages the benefits and advancements of ServiceNow® Financial Services Operations Core while preserving the functionality of existing applications.

**Note:** If your instance uses the Card Disputes Transaction table \[sn\_bom\_credit\_card\_disputes\_transaction\] and it contains a large amount of data, you may experience increased upgrade times.

</td></tr><tr><td>

Generative AI Controller

</td><td>

Generative AI Controller is installed and updated when you install or update any Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

</td></tr><tr><td>

ITOM Visibility

</td><td>

3DES support is planned for permanent removal from the MID Server for MID Servers with SSH-based Discovery or SSH-based integrations. For more information, see [3DES deprecation in SSH from Xanadu \[KB1644950\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644950).

</td></tr><tr><td>

Impact

</td><td>

The Impact Store Application configuration requires a sequence of tasks. See [Configuring the Impact Store Application](https://www.servicenow.com/docs/access?context=configuring-impact-platform&version=yokohama&pubname=yokohama-impact&ft:locale=en-US) for details.

</td></tr><tr><td>

Instance Data Replication

</td><td>

Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see [Upgrading legacy replication sets to V2 in Instance Data Replication](https://www.servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is comprised of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

</td></tr><tr><td>

MID Server

</td><td>

For the latest MID Server system requirements, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). The minimum JRE version supported is 17.0.10 and the recommended version is 17.0.12.

If you have installed your own JRE, the upgrade process takes the following actions to verify that the MID Server uses a supported JRE:

-   If a MID Server is using an unsupported version of the JRE when it upgrades, the upgrade process displays a warning message with the minimum and recommended JRE version.
-   If a supported JRE is running on the MID Server host, the upgraded MID Server uses that version.

All MID Server host machines require access to the download site at `install.service-now.com` to enable auto-upgrades. For additional details, read how the system manages [MID Server upgrades](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Only one Windows MID Server service is permitted according to the executable path. Upgraded Windows MID Servers that have multiple services pointing to the same installation folder can’t start. See [MID Server fails to start](https://www.servicenow.com/docs/access?context=mid-startup-fails&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

For more information about MID Server upgrades, see the following topics:

-   [MID Server pre-upgrade check](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US): Describes how the AutoUpgrade monitor tests the ability of the MID Server to upgrade on your system before the actual upgrade.
-   [Upgrade the MID Server manually](https://www.servicenow.com/docs/access?context=c_UpgradeAndTestMIDServer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US): Describes how to upgrade your MID Servers manually.

</td></tr><tr><td>

Now Assist

</td><td>

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

</td></tr><tr><td>

Now Assist Analytics

</td><td>

Now Assist Analytics is installed and updated when you install or update any Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

</td></tr><tr><td>

Now Assist for Hardware Asset Management \(HAM\)

</td><td>

Only users with the procurement\_user role can access the Help manage hardware asset requests agentic workflow including the following AI agents:

-   Hardware asset management sourcing AI agent
-   Transfer order creation AI agent
-   Purchase order creation AI agent

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

When you upgrade to the Zurich Patch 4 release, any customizations you may have made to the Now Assist context menu \(NACM\) won’t be preserved. For more information, see the Community article [Upgrade information for the NACM support in Now Assist for ITSM](https://www.servicenow.com/community/itsm-articles/upgrade-scenario-for-resolution-notes-generation-skill-in-itsm/ta-p/3415789).

</td></tr><tr><td>

Now Assist for Security Incident Response

</td><td>

For more information about required applications for Now Assist for Security Incident Response, see [Supporting information for Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-security-incident&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

**Note:**

Upgrading the Now Assist plugins activate any designated skills that were previously untouched by the customer.

-   If you have the plugins installed but never touched the configuration \(never activated the skill nor adjusted associated roles\) of a skill, any Default On skill will be activated on a per skill basis upon upgrading.
-   If you have previously toggled a skill from active and then back to inactive or have updated any roles for that skill, that skill remains inactive upon upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

Starting with version 2.0.1, the name of the Now Assist for Security Operations application in ServiceNow® Store and in your ServiceNow AI Platform® instance has changed to Now Assist for Security Incident Response. You must upgrade to version 2.0.1 to access the following features:

-   Generate resolution notes in the Now Assist context menu.
-   Generate correlation insights for a security incident investigation from the Now Assist panel.

The AI Search application must be enabled so that the recommended actions skill works for security incidents. To verify that AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates that AI Search is not enabled.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

For more information about required applications for Now Assist for Vulnerability Response, see [Supporting information for Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=supporting-information-now-assist-vr&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

**Note:**

Upgrading the Now Assist plugins activate any designated skills that were previously untouched by the customer.

-   If you have the plugins installed but never touched the configuration \(never activated the skill nor adjusted associated roles\) of a skill, any Default On skill will be activated on a per skill basis upon upgrading.
-   If you have previously toggled a skill from active and then back to inactive or have updated any roles for that skill, that skill remains inactive upon upgrading.
-   You maintain full control over deactivating individual skills at any time after activation.

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

If you’re upgrading to Now Assist in Contract Management starting with Yokohama Patch 3 from a previous version and you have customized use cases, run a fix script to migrate the existing data to the Now Assist Admin console.

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.
2.  In the **Name** field, search for `Upsert DI skill config`.
3.  In the script, add the use case ids that you want to migrate to the Now Assist Admin console.
4.  Select **Run Fix Script**.

For more information, see [Post-upgrade steps for Now Assist in Contract Management](https://www.servicenow.com/docs/access?context=cmpro-na-upgrade-steps&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

</td></tr><tr><td>

Platform Analytics experience

</td><td>

If you had previously migrated your analytics assets to Platform Analytics, assets that were in compatibility mode but are newly supported in Yokohama are migrated automatically.

</td></tr><tr><td>

Playbooks in Workflow Studio

</td><td>

After you upgrade to Yokohama, update the Workflow Studio application in the ServiceNow Store.

</td></tr><tr><td>

Portfolio Planning

</td><td>

After upgrading to Portfolio Planning v8.8.0, the custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Portfolio Planning](https://www.servicenow.com/docs/access?context=create-portfolio-plan-view-ppw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) and [Create a free-form roadmap view in Portfolio Planning](https://www.servicenow.com/docs/access?context=create-free-form-roadmap-view-ppw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

</td></tr><tr><td>

Product Catalog Management and Pricing Management

</td><td>

After upgrading to the May 2025 release of Sales Customer Relationship Management applications, you must run a scheduled job that automatically enables the **Allow multiple configurations** option when your catalog admin creates product offerings with an associated product specification. This job is called **Scheduled job with an upgrade script to set 'allow\_multiple\_configurations' to true on an Offering**. When multiple product offering configurations are allowed in configurable opportunities, quotes, or orders, agents can create multiple instances of a child product offering and define custom configurations for each offering instance.

**Note:** The **Allow multiple configurations** option is always enabled \(set to true\) for all product offerings that have an associated product specification. However, if the product specification has a child hierarchy, this option is honored only for orders placed through the TMF APIs. For specifications without a hierarchy, the flag is honored across all ordering channels.

The May 2025 release provides a default pricing plan that includes a new step, Apply Renewal Adjustment. If you've been using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after upgrading to the May 2025 release. Determine whether you want to publish the default plan or customize the default pricing plan for your needs and then publish the custom plan to be used.

</td></tr><tr><td>

Public Sector Digital Services

</td><td>

After the upgrade, certain public sector menus and menu items in the CSM Configurable Workspace revert to their original CSM label names. You can relabel these items for public sector use by updating the labels for the **Customer**, **Accounts**, and **Service Organizations** UX list category records. For more details on relabeling, navigate to **All** &gt; **Constituent Service** &gt; **Administration** &gt; **Guided Setup**, and select **Configurable Workspace for Public Sector Digital Services** &gt; **Customize Workspace Labels Manually**.

</td></tr><tr><td>

RPA Hub

</td><td>

Upgrade any of these currently installed Microsoft Software Installers \(MSIs\) by downloading the RPA applications:

-   RPA Desktop Design Studio
-   Attended Robot
-   Unattended Robot
-   Unattended Robot Login Agent

For more information, see [Download the RPA applications from RPA Hub](https://www.servicenow.com/docs/access?context=download-installer-rpa&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

The following upgrade information is applicable only when you’re upgrading from San Diego or Tokyo to Yokohama.

Based on the number of records in the application file table, you may experience a delay while upgrading the RPA Hub applications from Tokyo or earlier releases to Yokohama.

Before upgrading RPA Hub to Yokohama, you must set the value of the **glide.rollback.blacklist.TableParentChange.change** system property to **false**. If this property doesn't exist in the System Property \[sys\_properties\] table, add the property and set its value to false. For more information on how to add a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

After you upgrade to Yokohama, the bot process definitions change to the new structure, which is the bot process configuration.

Although the bot process configuration doesn't replace the bot process completely, most fields are moved from the bot process to the bot process configuration. If you upgrade to Yokohama without updating the system property value, the tables don’t extend the Application File \[sys\_metadata\] table. To update the table changes manually, see the [Restructuring RPA Hub tables to sys\_metadata in Utah and beyond release \[KB1223629\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1223629) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Security Posture Control

</td><td>

For a complete list of the applications that are required to implement Security Posture Control, see [Install Security Posture Control](https://www.servicenow.com/docs/access?context=spc-install&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US).

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
-   If you upgrade to Service Exchange version 2.0.55 with Sales Customer Relationship Management plug-in version 1.0.4 before upgrading the platform to the Yokohama release, the new Deny ACLs will not be installed. To ensure the Deny ACLs get installed, after upgrading to Yokohama, you must click Repair to reinstall the Service Exchange application.

</td></tr><tr><td>

Service Operations Workspace for ITSM

</td><td>

Ensure that the following applications have compatible upgraded versions:

-   Service Operations Workspace ITSM Applications application \(sn\_sow\_itsm\_cont\)
-   Service Operations Workspace ITOM Applications application \(sn\_sow\_itom\_cont\)

For more information on compatible versions, see [Version compatibility between Service Operations Workspace for ITSM and Service Operations Workspace ITOM](https://www.servicenow.com/docs/access?context=sow-itsm-itom-version&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

ServiceNow IDE

</td><td>

ServiceNow IDE version 1.1.4 is active by default on instances on the Yokohama release. Update to ServiceNow IDE version 2.0 or later to use the latest features. For information about updating ServiceNow IDE, see [Updating applications](https://www.servicenow.com/docs/access?context=updating-apps-app-manager&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

ServiceNow SDK

</td><td>

Upgrade to the latest version of the ServiceNow SDK with the `now-sdk upgrade` command. For more information, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

ServiceNow SDK version 3.0 supports integrating with ServiceNow instances beginning with the Washington DC release.

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow IDE, SDK, and Fluent articles](https://www.servicenow.com/community/servicenow-ide-sdk-and-fluent/tkb-p/ide-sdk-fluent-articles) in the ServiceNow Community.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

ServiceNow Studio no longer has to be downloaded from the ServiceNow Store. It’s available on the ServiceNow AI Platform by default.

</td></tr><tr><td>

Software Asset Management

</td><td>

Starting from the Yokohama release, all the reconciliation script includes are being moved from the family release to the Software Asset Management store application \(com.sn\_itam\_samp\). When upgrading to Yokohama, if you have made customizations to reconciliation script includes, you must move your customizations to the new script includes. The old script includes will be deprecated.

When upgrading to Yokohama Patch 1 with the Software Asset Management \(sn\_itam\_samp\) 2.1.0 store application installed, you must delete the entitlements for the existing CrowdStrike integration profiles. Then, create new entitlements for various CrowdStrike products, such as CrowdStrike Falcon Endpoint Protection and CrowdStrike Falcon Discover, based on their license metrics. These metrics include the Reserved Hourly Average Sensor and Sensor Subscription, which are found under the CrowdStrike License Metric Group.

-   If any existing CrowdStrike profiles are in the Draft state, create new integration profiles and delete the existing ones.
-   If any existing CrowdStrike profiles are in the Published state, their state changes to Draft.

</td></tr><tr><td>

Strategic Planning

</td><td>

After upgrading to Strategic Planning v4.7.0, the following changes apply to user preferences:

-   Custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-portfolio-plan-view-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) and [Create a free-form roadmap view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-free-form-roadmap-view-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).
-   Customizations made to the Timeline and Kanban views in the **Roadmap** tab, and the Kanban view in the **Prioritization** tab at the portfolio plan level, will be copied to the Default view of the portfolio plan. Similarly, any customizations made to the Timeline and Kanban views in the free-form roadmap will also be copied to the Default view of the free-form roadmap.

</td></tr><tr><td>

Subscription Management

</td><td>

Subscription Management version 4.1 is active by default on all instances of the Yokohama release. Update to Subscription Management version 6.0.2 or later to use the latest features. For more information about updating Subscription Management, see [Update an application or plugin](https://www.servicenow.com/docs/access?context=update-application-app-mgr&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Telecommunications Network Inventory

</td><td>

The Yokohama release needs the Xanadu platform version to support the Design and Assign playbook feature.

</td></tr><tr><td>

Telecommunications Service Operations Management \(TSOM\)

</td><td>

After installing Telecommunications Service Operations Management TSOM, any customized IRE identification rules applied to interface cards, slots, sub-slots and network interfaces may be affected. You must review and validate the rules to ensure proper functionality.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

Starting with the Vancouver release, if you’re a VRM user upgrading to TPRM, from an earlier release, you must run each upgrade sequentially to ensure that fix scripts run correctly. This means upgrading from one release to the next rather than skipping to the latest release. Not running scripts in the correct order can result in data inconsistencies, broken functionalities, and conflicts.

For more information on upgrading from VRM to TPRM, see [Third-party Risk Management upgrade information](../governance-risk-compliance/grc-tprm-upgrade-info.md).

For existing TPRM customers, after upgrading to version 20.2.4, data from the Industry column in the Company \[core\_company\] table is automatically migrated to the tprm\_industry column. Migration can take several hours depending on the number of records in the Company \[core\_company\] table. After migration, a system log message confirms that the migration is complete. Review the Company \[core\_company\] table content and update any customizations referencing the Industry field to use tprm\_industry. After verifying the migration and updating customizations, you can drop the Industry column.

</td></tr><tr><td>

Usage Insights

</td><td>

-   The User Experience Analytics module is moved under Platform Analytics.
-   Custom user properties must be reconfigured.
-   Default country and user consent policies are updated to No Consent Required.
-   The User Experience Analytics UI and navigation structure are reworked.

</td></tr><tr><td>

Vulnerability Response Integration with Claroty CTD

</td><td>

Claroty CTD v5.1 is also supported for the Vulnerability Response Integration with Claroty CTD application.

</td></tr><tr><td>

Vulnerability Response integrations

</td><td>

-   For more information about the released versions of the Vulnerability Response application as well as the third-party and ServiceNow applications that are compatible with the Yokohama release, see the [Vulnerability Response Compatibility Matrix and Release Schema Changes \[KB0856498\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0856498) article in the Now Support Knowledge Base.
-   For information about the new features of Vulnerability Response, see [Vulnerability Response release notes](../security-operations/secops-vuln-resp-rn.md).

</td></tr><tr><td>

Workforce Optimization for ITSM

</td><td>

-   **[Enhanced security to access Workforce Optimization for ITSM](https://www.servicenow.com/docs/access?context=components-installed-workforce-optimization-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

When you upgrade to the Yokohama release, you have the option to turn on enhanced security for the Workforce Optimization for ITSM application. To get the enhanced security, you must contact Now Support to install the ITSM Enhanced Security Features plugin \(com.snc.itsm.enhanced\_security\). After you install the plugin, you need the roles listed here to access the respective features.

<table id="table_kz4_cbv_bdc"><thead><tr><th>

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


</td></tr></tbody>
</table>**Parent Topic:**[Release notes summaries for Yokohama features](../release-notes-summaries.md)

