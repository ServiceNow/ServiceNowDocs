---
title: Combined Configuration Management Database \(CMDB\) release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Configuration Management Database \(CMDB\) from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-configurationmanagementdatabasecmdb-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Configuration Management Database \(CMDB\) release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Configuration Management Database \(CMDB\) from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Configuration Management Database \(CMDB\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Configuration Management Database \(CMDB\) to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

Due to changes in the Configuration Item \[cmdb\_ci\] table, if you're upgrading to Australia, you might experience an increased upgrade time. To learn more about this change and reducing its impact, see the [Increased Australia Upgrade Time due to cmdb\_ci composite index addition \[KB2588894\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2588894) article in the Now Support Knowledge Base.

If you're upgrading from Xanadu or Yokohama directly to the Australia release, you must run the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job to correctly configure some user roles, such as CMDB Admin and CMDB Editor. For more information about this scheduled job and its use, see the [CMDB Zurich release notes](https://www.servicenow.com/docs/access?context=cmdb-rn&family=australia&ft:locale=en-US).

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

Dynamic IRE is now enabled by default on zBooted instances, while on upgraded instances that are using Static IRE, you can switch into using Dynamic IRE. Key benefits from the new Dynamic IRE engine include CI identification using an improved dynamic process and automatic updates of IRE identification rules during ingestion of data payloads.

For more information, see [Dynamic IRE](https://www.servicenow.com/docs/access?context=dynamic-ire&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Configuration Management Database \(CMDB\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[CMDB success advisor summary on the Governance view](https://www.servicenow.com/docs/access?context=sg-workspace-governance-view&family=australia&ft:locale=en-US)**

Review a ServiceNow Otto for CMDB-generated summary of the top data quality issues for Data Foundations, Hardware Asset Management \(HAM\), and Software Asset Management \(SAM\), directly on the Governance view in Service Graph Workspace. Select **View remediations** or **View insights** on a card to open the corresponding dashboard in CMDB success advisor.


 -   **[CMDB success advisor](https://www.servicenow.com/docs/access?context=cmdb-sa-landing-page&family=australia&ft:locale=en-US)**

Use CMDB success advisor to achieve Data Foundations, HAM, and SAM target outcomes. The store app monitors and improves CMDB data quality through dedicated dashboards for principal CI classes, hardware assets, and software installs. Dashboards provide targeted recommendations and remediation actions to address data gaps and are accessible directly from the Service Graph Workspace.


 -   **[CMDB Workspace v9.0 \(including Service Graph Workspace\)](https://www.servicenow.com/docs/access?context=sg-workspace&family=australia&ft:locale=en-US)**
    -   Use Service Graph Workspace which is included in the CMDB Workspace store app, to view data, such as company, location, user, and CMDB data, using panels and dashboards. The Service Graph Workspace is specifically organized to help CMDB administrators, data owners, and analysts work with the CMDB. You can search the CMDB in Service Graph Workspace without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation.
    -   Configure de-duplication remediation processes for related tables to turn off automated workflows, such as ignoring errors and skipping business rules, that might block referenced duplicate CIs from updating to the main CI. Skipping automated workflows for related tables enables de-duplication tasks, which would otherwise fail, to complete successfully. For more information, see [Effects on related tables \(such as Change\)](https://www.servicenow.com/docs/access?context=de-duplication-tasks&family=australia&ft:locale=en-US) and [Turn off workflows of related tables during remediation](https://www.servicenow.com/docs/access?context=dedup-ci-disable-workflow&family=australia&ft:locale=en-US).
-   **[Simplify resolving de-duplication tasks by using a ServiceNow Otto for CMDB skill](https://www.servicenow.com/docs/access?context=reconcile-dup-task&family=australia&ft:locale=en-US)**

Use the De-duplication task resolution assistant skill in the Duplicate CI Remediator to use preselected remediation options instead of manually making selections. An AI agent preselects the options to resolve the task, such as the choice of the main CI. Then, before initiating the remediation, you can review all suggested options with supported reasoning.

To use the De-duplication task resolution assistant skill, you must install the ServiceNow Otto for CMDB version v3.0.


 -   **[Dynamic IRE](https://www.servicenow.com/docs/access?context=dynamic-ire&family=australia&ft:locale=en-US)**

Use Dynamic IRE to accurately identify CIs across multiple data sources, and by so, minimize duplicate CIs. Dynamic IRE is applicable only to the Hardware \[cmdb\_ci\_hardware\] class and its descending class, using a dynamic identification process which eliminates the need to manually create and maintain identification rules.

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&family=australia&ft:locale=en-US)**

Run quick start tests after upgrades and deployments of new applications or integrations to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Configuration Management Database \(CMDB\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Cleaner category grouping for Data Foundations advisor](https://www.servicenow.com/docs/access?context=cmdb-sa-df-dashboard&family=australia&ft:locale=en-US)**

The CI class categories filter and the Set principal classes dialog box hide Data Model Navigator child categories that are already nested under a parent category, so the top-level list doesn't repeat categories.


 -   **[Elevated user roles are no longer required for CMDB tasks](https://www.servicenow.com/docs/access?context=manage-cmdb&family=australia&ft:locale=en-US)**

Access to CMDB tables is no longer restricted to users with elevated privileges. Instead, for improved security, users with access privileges that are trimmed to CMDB features can complete any administrative or end-user CMDB task:

    -   CMDB tables that required the admin or itil\_admin roles are now also accessible to the sn\_cmdb\_admin user role.
    -   CMDB tables that required the itil role are now also accessible to the sn\_cmdb\_editor user role.
-   **[Automatically generate de-duplication tasks for lookup and related tables](https://www.servicenow.com/docs/access?context=id-detect-dup-ci&family=australia&ft:locale=en-US)**

Configure IRE to automatically generate de-duplication tasks for specific lookup or related tables during the identification process. You can then process those de-duplication tasks to remediate any duplications.

-   **[Remediate duplicate related items in lookup tables](https://www.servicenow.com/docs/access?context=id-detect-dup-ci&family=australia&ft:locale=en-US)**

Configure IRE to create de-duplication tasks for duplicate related items in a lookup table, detected during a lookup-based identification. Sort which duplicates do or don't require remediation by configuring the system property **glide.identification\_engine.lookup\_match.create\_duplicate\_task\_ci.enabled**. For more information, see [Detecting duplicate CIs](https://www.servicenow.com/docs/access?context=id-detect-dup-ci&family=australia&ft:locale=en-US).

-   **[Domain separation for key CMDB tables](https://www.servicenow.com/docs/access?context=c_DomainSeparationSetup&family=australia&ft:locale=en-US)**

The following tables now support domain separation on instances which are configured with domain separation:

    -   Key Value \[cmdb\_key\_value\]
    -   Printer Instance \[cmdb\_print\_queue\_instance\]
    -   Software Instance \[cmdb\_software\_instance\]
    -   Client Access \[samp\_client\_access\]
    -   Oracle Options \[samp\_oracle\_options\]
Domain separation can help protect sensitive information by supporting domain-specific data segregation.

For more information about domain separation and how to activate it, see [Setup and administration](https://www.servicenow.com/docs/access?context=c_DomainSeparationSetup&family=australia&ft:locale=en-US).

-   **[Execution modes](https://www.servicenow.com/docs/access?context=query-builder-engine-execution-mode&family=australia&ft:locale=en-US)**

The CMDB Query Builder expanded its support for various types of query structures that can run in V2 engine mode. Also, the performance of running queries in V2 mode is improved. Query structures that aren't supported include related list conditions, NOT operators combined with filters, certain Service Mapping relationships, and OR operators unless explicitly enabled by the **glide.cmdb.query.or\_execution\_mode** system property.


</td></tr><tr><td>

Brazil

</td><td>

-   **CMDB Workspace merged with Service Graph Workspace features**

Service Graph Workspace is deprecated as of this release. CMDB Workspace will have Service Graph Workspace features.

-   **[ServiceNow Otto replaces Now Assist name](https://www.servicenow.com/docs/access?context=reconcile-dup-task&family=brazil&ft:locale=en-US)**

Now Assist and Moveworks experiences is renamed to ServiceNow Otto \(Duplicate CI Remediator\).

-   **[Reset certification tasks](https://www.servicenow.com/docs/access?context=data-certific-reset-task-wrkspc&family=brazil&ft:locale=en-US)**

Reset a certification task to restart the certification process for the task. Reset sets all certification results for the task to a 'Review not completed' state and removes any comments that were added.

-   **[Review certification tasks](https://www.servicenow.com/docs/access?context=data-certific-review-tasks&family=brazil&ft:locale=en-US)**

When opening a task that isn’t closed, the Review not completed tab is selected by default for a quick access to task review. An Important information panel is now available throughout the task review process, that provides key details for the task such as special instructions and the ‘Allow field updates’ setting. You can attach files, such as supporting documents for various findings, to a task, and also, a percent complete number shows on the task page. The percent complete number is calculated as various certification activities are complete and reflects on the task review progress in real time.

-   **app\_service\_owner role contains the app\_service\_user role**

Use the app\_service\_owner role to grant create, read, update, and delete access to Service Instance records without granting the broader itil role. The app\_service\_owner role also includes the app\_service\_user role.

-   **Dynamic IRE Adoption**

Dynamic IRE is now enabled by default on zBooted instances, while on upgraded instances that are using Static IRE you can switch into using Dynamic IRE. Key benefits from the new Dynamic IRE engine include CI identification using an improved dynamic process and automatic updates of IRE identification rules during ingestion of data payloads.

-   **Inaccesible Records Indicator**

You can now review details about the outcome of a policy execution in the policy record in the CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] table. Review the Wok Notes and the Activities fields and use details such as the number of CIs that weren't processed because they exist in other tasks, and access issues preventing processing of CIs to mitigate issues, for example, by updating the policy configurations or by updating user permissions.

-   **[Unified Map performance improvements for Safari](https://www.servicenow.com/docs/access?context=unified-map-config-browsers&family=brazil&ft:locale=en-US)**

Unified Map now detects when it's running in Safari and disables edge animations by default to avoid a severe performance issue. This behavior applies to any workspace using the Unified Map template and its shared components, so pages built on that template are protected from the same issue without additional configuration.


 -   **PA Indicator Optimization**

Indicator conditions enable you to associate an indicator source with a single scheduled data collection job.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Configuration Management Database \(CMDB\) features or functionality were removed.

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

Between your current release family and Brazil, some Configuration Management Database \(CMDB\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

The Multisource Report Builder has been removed. Use CMDB 360 in CMDB Workspace or in Service Graph Workspace to generate reports for multisource data. For more information, see [CMDB 360](https://www.servicenow.com/docs/access?context=multisource-cmdb&family=australia&ft:locale=en-US).

</td></tr><tr><td>

Brazil

</td><td>

-   **Itil role removed from app\_service\_admin**

The sn\_cmdb\_editor and app\_service\_user roles replace the itil role within the app\_service\_admin role. While you can still view Service Instance records and use Unified Map, viewing related items for a CI, such as linked incidents or changes, still requires the itil role.

-   **sn\_getwell\_cis\_processed\_via\_ire database view removal**

sn\_getwell\_cis\_processed view\_ire is deprecated.

-   **CMDB Baseline, Dependency Views, and CMDB Relationship editor**

Starting with the Brazil release, CMDB Baseline is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Unified Map provides the latest experience for this functionality.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Configuration Management Database \(CMDB\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Configuration Management Database \(CMDB\) is a ServiceNow AI Platform feature that is active by default.

The Australia release includes an installation of CMDB Workspace. However, you can download the latest version of CMDB Workspace store app \(which includes Service Graph Workspace\) so that you can use its latest features in your Australia instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Configuration Management Database \(CMDB\) is a ServiceNow AI Platform feature that is active by default.

The Brazil release includes an installation of CMDB Workspace. However, you can download the latest version of CMDB Workspace store app so that you can use its latest features in your Brazil instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Configuration Management Database \(CMDB\) we have noted them here.

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

If any specific browser requirements were introduced or changed for Configuration Management Database \(CMDB\) we have noted them here.

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

Review details on accessibility information for Configuration Management Database \(CMDB\), such as specific requirements or compliance levels.

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

If there are specific localization considerations for Configuration Management Database \(CMDB\) we have noted them here.

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

If there are specific highlight considerations for Configuration Management Database \(CMDB\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Use CMDB success advisor to achieve Data Foundations, Hardware Asset Management \(HAM\), and Software Asset Management \(SAM\) target outcomes.
-   Users with CMDB related roles can perform all CMDB functions as access to CMDB tables is no longer restricted to users with elevated privileges.
-   Switch into using the Service Graph Workspace instead of CMDB Workspace. The Service Graph Workspace provides access to data such as company, location, user and CMDB. The new workspace is specifically organized to help CMDB administrators, data owners, and analysts work efficiently with the CMDB.
-   Simplify duplicate CI remediation by using the ServiceNow Otto for CMDB remediation option in the Duplicate CI Remediator, and using the automatically-filled remediation options.
-   Use Dynamic Identification and Reconciliation Engine \(IRE\) that eliminates the need for manually-created identification rules and reduces incorrect detection of duplicate CIs in the CMDB.
-   Protect sensitive information with domain separation that supports key CMDB tables such as the Key Value \[cmdb\_key\_value\] table.

 See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Lets you build and store logical representations of assets, services, and the relationships between them that comprise the infrastructure of your organization.
-   Serves as a centralized location for full visibility into your IT environment.
-   Monitors your network and help improve stability and performance.
-   Enables and enhances the effectiveness of other ServiceNow applications, such as problem and change management, to support needed business goals.

 See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

