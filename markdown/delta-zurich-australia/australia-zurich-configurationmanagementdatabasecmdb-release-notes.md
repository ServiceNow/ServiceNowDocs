---
title: Combined Configuration Management Database \(CMDB\) release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Configuration Management Database \(CMDB\) from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-configurationmanagementdatabasecmdb-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Configuration Management Database \(CMDB\) release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Configuration Management Database \(CMDB\) from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Configuration Management Database \(CMDB\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Configuration Management Database \(CMDB\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Due to the removal of the **Design** value for the operational status attribute in a CI, after an upgrade, you must review all CIs that have the discovery source attribute set to **Manual via IRE**. Review the operational status attribute of those CIs and set it to a supported value in CMDB for your environment. For example, you can set the attribute to **Non-Operational**. For more information about the operational status values, see [Tangible/physical life cycle](https://www.servicenow.com/docs/access?context=csdm-lifecycle-hardware&family=zurich&ft:locale=en-US).

 On an upgraded Zurich instance, to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks, you must manually run the scheduled job **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles**. This scheduled job modifies the user roles as follows:

-   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
-   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).

</td></tr><tr><td>

Australia

</td><td>

Due to changes in the Configuration Item \[cmdb\_ci\] table, if you're upgrading to Australia, you might experience an increased upgrade time. To learn more about this change and reducing its impact, see the [Increased Australia Upgrade Time due to cmdb\_ci composite index addition \[KB2588894\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2588894) article in the Now Support Knowledge Base.

 If you're upgrading from Xanadu or Yokohama directly to the Australia release, you must run the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job to correctly configure some user roles, such as CMDB Admin and CMDB Editor. For more information about this scheduled job and its use, see the [CMDB Zurich release notes](https://www.servicenow.com/docs/access?context=cmdb-rn&family=australia&ft:locale=en-US).

 The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://www.servicenow.com/docs/access?context=read-only-option&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Configuration Management Database \(CMDB\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[CMDB Workspace v8.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=zurich&ft:locale=en-US):**

You can now use the Create CI experience in CMDB Workspace to create a CI with a lookup identifier entry that contains mandatory attributes. When you select a lookup identifier entry on the Required attributes page, those mandatory attributes now appear and you can set their values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&family=zurich&ft:locale=en-US).

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=zurich&ft:locale=en-US):**

    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://www.servicenow.com/docs/access?context=ci-form-cmdb-workspace&family=zurich&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://www.servicenow.com/docs/access?context=data-cert-dashboard-workspace&family=zurich&ft:locale=en-US).
    -   [Manage shared filter settings](https://www.servicenow.com/docs/access?context=unified-map-manage-shared-preset&family=zurich&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&family=zurich&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records as follows:
        -   The table cleanup rule for the CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] table, which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive the certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task\] table.
        -   The archival of related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
The Zurich release includes an installation of CMDB Workspace. However, you can download a newer version of CMDB Workspace so that you can use its latest features in your Zurich instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   **[Dynamic IRE](https://www.servicenow.com/docs/access?context=dynamic-ire&family=zurich&ft:locale=en-US)**

Use Dynamic IRE to accurately identify CIs across multiple data sources, and by so, minimize duplicate CIs. Dynamic IRE is applicable only to the Hardware \[cmdb\_ci\_hardware\] class and its descending class, using a dynamic identification process which eliminates the need to manually create and maintain identification rules.

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&family=zurich&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Australia

</td><td>

-   **[CMDB success advisor](https://www.servicenow.com/docs/access?context=cmdb-sa-landing-page&family=australia&ft:locale=en-US)**

Use CMDB success advisor to achieve Data Foundations and HAM target outcomes. The store app monitors and improves CMDB data quality through dedicated dashboards for principal CI classes and hardware assets, providing targeted recommendations and remediation actions to address data gaps. Access the dashboards directly from the Service Graph Workspace.

-   **[CMDB Workspace v8.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=australia&ft:locale=en-US)**

Create a CI with a lookup identifier entry that contains mandatory attributes in the CMDB Workspace. When you select a lookup identifier entry on the Required attributes page, you can set those mandatory attribute values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&family=australia&ft:locale=en-US).

-   **[CMDB Workspace v9.0 \(including Service Graph Workspace\)](https://www.servicenow.com/docs/access?context=sg-workspace&family=australia&ft:locale=en-US)**
    -   Use Service Graph Workspace which is included in the CMDB Workspace store app, to view data, such as company, location, user, and CMDB data, using panels and dashboards. The Service Graph Workspace is specifically organized to help CMDB administrators, data owners, and analysts work with the CMDB. You can search the CMDB in Service Graph Workspace without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation.
    -   Configure de-duplication remediation processes for related tables to turn off automated workflows, such as ignoring errors and skipping business rules, that might block referenced duplicate CIs from updating to the main CI. Skipping automated workflows for related tables enables de-duplication tasks, which would otherwise fail, to complete successfully. For more information, see [Effects on related tables \(such as Change\)](https://www.servicenow.com/docs/access?context=de-duplication-tasks&family=australia&ft:locale=en-US) and [Turn off workflows of related tables during remediation](https://www.servicenow.com/docs/access?context=dedup-ci-disable-workflow&family=australia&ft:locale=en-US).
-   **[Dynamic IRE](https://www.servicenow.com/docs/access?context=dynamic-ire&family=australia&ft:locale=en-US)**

Use Dynamic IRE to accurately identify CIs across multiple data sources, and by so, minimize duplicate CIs. Dynamic IRE is applicable only to the Hardware \[cmdb\_ci\_hardware\] class and its descending class, using a dynamic identification process which eliminates the need to manually create and maintain identification rules.

-   **[Simplify resolving de-duplication tasks by using a Now Assist for CMDB skill](https://www.servicenow.com/docs/access?context=reconcile-dup-task&family=australia&ft:locale=en-US)**

Use the De-duplication task resolution assistant skill in the Duplicate CI Remediator to use preselected remediation options instead of manually making selections. An AI agent preselects the options to resolve the task, such as the choice of the main CI. Then, before initiating the remediation, you can review all suggested options with supported reasoning.

To use the De-duplication task resolution assistant skill, you must install the Now Assist for CMDB version v3.0.

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&family=australia&ft:locale=en-US)**

Run quick start tests after upgrades and deployments of new applications or integrations to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Configuration Management Database \(CMDB\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=zurich&ft:locale=en-US)**
    -   On the Published policy tile on the Data Manager policies page, the policies list view now shows the scheduled job that is associated with the policy and the user that the policy runs as.

For more information, see [Create a CMDB Data Manager policy](https://www.servicenow.com/docs/access?context=data-manager-create-policy-wrkspc&family=zurich&ft:locale=en-US).

    -   Instead of the system automatically setting the **run as** attribute of the scheduled certification and attestation jobs to be the user that authored the policy, you can now set a specific user that adheres to the policies and regulations in the organization. Configure the default values for the run as user and user accounts available for run as assignees for auditing purposes when it’s important to know who initiated the changes.

For more information, see [Components related to CMDB Data Manager](https://www.servicenow.com/docs/access?context=components-cmdb-data-manager&family=zurich&ft:locale=en-US).

    -   For certification and attestation policy tasks, choose how to assign tasks in cases where a specified task assignment field is empty for a target CI. Specify a user or a user group to assign such tasks to, or create the tasks without assigning them. An administrator can later review and assign those tasks.

For more information, see [Create a CMDB Data Manager policy](https://www.servicenow.com/docs/access?context=data-manager-create-policy-wrkspc&family=zurich&ft:locale=en-US).

    -   View the closed tasks in the My Work view in CMDB Workspace. Select the Closed card in the Task status tile to review the \(in read-only mode\) details for tasks that are in the Closed Complete, Closed Canceled, Closed Incomplete, or Rejected state.

For more information, see [My Work view in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace-govern-view&family=zurich&ft:locale=en-US).

    -   New CIs in the Create CI experience no longer have their **Operational status** attribute set. The new **CI Operational state** attribute appears on the Additional attributes page of the Create CI experience. Setting it to any value is optional.

For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&family=zurich&ft:locale=en-US).

    -   The itil user role now contains the sn\_cmdb\_user user role and no longer contains the sn\_cmdb\_editor user role. As a result, the following functions that were accessible to itil users now require the sn\_cmdb\_editor user role:
        -   Create and delete the operations that are related to CMDB 360 queries.
        -   Access the CMDB Retirement Definitions module by navigating to **All** &gt; **Configuration** &gt; **CMDB Retirement Definitions**.
        -   Access the Create CI quick link on the Home view of CMDB Workspace.
-   **[Containment in the itil user role](https://www.servicenow.com/docs/access?context=installed-with-cmdb-workspace&family=zurich&ft:locale=en-US)**

In zBooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

-   **[Constraints when deleting a CMDB Data Manager retirement definition](https://www.servicenow.com/docs/access?context=data-manager-delete-ret-def-wrkspc&family=zurich&ft:locale=en-US)**

The same constraints that exist when deleting a retirement definition in CMDB Workspace now apply when directly accessing the CMDB Retirement Custom Definitions \[cmdb\_retirement\_custom\_definitions\] table:

    -   The retirement definition that you want to delete must be in an inactive mode \(**Active** = **false**\).
    -   The retirement definition for the Configuration Item \[cmdb\_ci\] class can't be deleted.
-   **[Prioritize using IRE identification rules for uniquely identifying CIs](https://www.servicenow.com/docs/access?context=ire&family=zurich&ft:locale=en-US)**

Configure the system to prioritize the use of IRE identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** fields. For more information about using the **glide.identification\_engine.skip\_sys\_object\_source\_matching** system property to control this behavior, see [Properties](https://www.servicenow.com/docs/access?context=properties-id-reconciliation&family=zurich&ft:locale=en-US).

-   **[Run a query in an enhanced execution mode](https://www.servicenow.com/docs/access?context=config-query-builder-engine-mode&family=zurich&ft:locale=en-US)**

Set the execution mode for a saved CMDB Query Builder query to run using an enhanced query execution engine, which is designed for improved performance and scalability.

-   ****
-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&family=zurich&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).


</td></tr><tr><td>

Australia

</td><td>

-   **[Elevated user roles are no longer required for CMDB tasks](https://www.servicenow.com/docs/access?context=manage-cmdb&family=australia&ft:locale=en-US)**

Access to CMDB tables is no longer restricted to users with elevated privileges. Instead, for improved security, users with access privileges that are trimmed to CMDB features can complete any administrative or end-user CMDB task:

    -   CMDB tables that required the admin or itil\_admin roles are now also accessible to the sn\_cmdb\_admin user role.
    -   CMDB tables that required the itil role are now also accessible to the sn\_cmdb\_editor user role.
For more information, see the [CMDB Granular Role EPIC changes \[KB0561055\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0561055) article in the Now Support Knowledge Base.

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


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Configuration Management Database \(CMDB\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   Common Service Data Model no longer provides **Design** as a value for the **Operational status** attribute in CIs.

</td></tr><tr><td>

Australia

</td><td>

The Multisource Report Builder has been removed. Use CMDB 360 in CMDB Workspace or in Service Graph Workspace to generate reports for multisource data. For more information, see [CMDB 360](https://www.servicenow.com/docs/access?context=multisource-cmdb&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Configuration Management Database \(CMDB\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   The Data Certification plugin \(com.snc.certification\_v2\) is now deprecated and no longer supported or available for new activation. The latest experience for this functionality is included with CMDB Workspace.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Configuration Management Database \(CMDB\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

CMDB is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Configuration Management Database \(CMDB\) is a ServiceNow AI Platform feature that is active by default.

 The Australia release includes an installation of CMDB Workspace. However, you can download the latest version of CMDB Workspace store app \(which includes Service Graph Workspace\) so that you can use its latest features in your Australia instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Configuration Management Database \(CMDB\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

-   Access a centralized location with a comprehensive view of the configuration item \(CI\) details by using the new CI form in CMDB Workspace. You can view and edit the CI attributes, relationships, and data, such as the CMDB Health report for the CI, CMDB 360 data that is associated with the CI, and the CI resources, activities, and related services.
-   Access the Data Certification dashboard in CMDB Workspace to gain insights about the data certification activities and progress, examine policies and tasks, and see the reports about the certification instances, charts of the aging certification tasks, and group and individual workloads.
-   Add or remove CIs directly from a map in Unified Map. You can also add, modify, or delete CI relationships in CMDB.
-   Configure the system to use Identification and Reconciliation Engine \(IRE\) identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** attributes.
-   In zbooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role, and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

 See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Use CMDB success advisor to achieve Data Foundations and Hardware Asset Management \(HAM\) target outcomes.
-   Users with CMDB related roles can perform all CMDB functions as access to CMDB tables is no longer restricted to users with elevated privileges.
-   Switch into using the Service Graph Workspace instead of CMDB Workspace. The Service Graph Workspace provides access to data such as company, location, user and CMDB. The new workspace is specifically organized to help CMDB administrators, data owners, and analysts work efficiently with the CMDB.
-   Simplify duplicate CI remediation by using the Now Assist for CMDB remediation option in the Duplicate CI Remediator, and using the automatically-filled remediation options.
-   Use Dynamic Identification and Reconciliation Engine \(IRE\) that eliminates the need for manually-created identification rules and reduces incorrect detection of duplicate CIs in the CMDB.
-   Protect sensitive information with domain separation that supports key CMDB tables such as the Key Value \[cmdb\_key\_value\] table.

 See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

