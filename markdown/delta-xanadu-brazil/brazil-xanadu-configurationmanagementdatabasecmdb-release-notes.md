---
title: Combined Configuration Management Database \(CMDB\) release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Configuration Management Database \(CMDB\) from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-configurationmanagementdatabasecmdb-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 30
breadcrumb: [Products combined by family]
---

# Combined Configuration Management Database \(CMDB\) release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Configuration Management Database \(CMDB\) from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Configuration Management Database \(CMDB\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Configuration Management Database \(CMDB\) to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

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

</td></tr><tr><td>

Yokohama

</td><td>

-   **Upgrade information**

Three new indexes \(parent, type\), \(child, type\), and \(child, parent, type, port\) are added to the CI Relationship \[cmdb\_rel\_ci\] table to improve the performance of Identification and Reconciliation Engine \(IRE\) querying this table. This change is likely to increase upgrade time. For more information about the impact of this change during upgrade and to learn how to minimize that impact, see [Increased Yokohama Upgrade Time due to cmdb\_rel\_ci index additions \[KB1703367\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB1703367).


</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

Due to the removal of the **Design** value for the operational status attribute in a CI, after an upgrade, you must review all CIs that have the discovery source attribute set to **Manual via IRE**. Review the operational status attribute of those CIs and set it to a supported value in CMDB for your environment. For example, you can set the attribute to **Non-Operational**. For more information about the operational status values, see [Tangible/physical life cycle](https://www.servicenow.com/docs/access?context=csdm-lifecycle-hardware&family=zurich&ft:locale=en-US).

On an upgraded Zurich instance, to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks, you must manually run the scheduled job **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles**. This scheduled job modifies the user roles as follows:

    -   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
    -   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).

</td></tr><tr><td>

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

Xanadu

</td><td>

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=xanadu&ft:locale=en-US):**
    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://www.servicenow.com/docs/access?context=ci-form-cmdb-workspace&family=xanadu&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://www.servicenow.com/docs/access?context=data-cert-dashboard-workspace&family=xanadu&ft:locale=en-US).
    -   [Manage a shared preset](https://www.servicenow.com/docs/access?context=unified-map-manage-shared-preset&family=xanadu&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&family=xanadu&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records, as follows:
        -   The table cleanup rule for table CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\], which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task table\].
        -   The archival of related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
-   **[CMDB Health Dashboard](https://www.servicenow.com/docs/access?context=c_MonitorCMDBHealth&family=xanadu&ft:locale=en-US)**

The CMDB Health Dashboard is now built using UI Builder components and is fully integrated into the CMDB Workspace. When you select either of its views, it opens in CMDB Workspace. The CMDB Health Dashboard has a modernized look and feel of the Next Experience user interface

CI health is now reported on CI forms within the CI Health tile in CMDB Workspace.

-   **[CSDM and the CMDB Data Foundations Dashboards](https://www.servicenow.com/docs/access?context=csdm-cmdb-foundations-dashboards&family=xanadu&ft:locale=en-US)**

Starting with version 4.0, the CSDM and the CMDB Data Foundations Dashboards store app is built using UI Builder components. You can also now access the CSDM Data Foundations Dashboard from Management tools in the Management view in CMDB Workspace.

-   **[CMDB Integrations Dashboard in the Next Experience user interface](https://www.servicenow.com/docs/access?context=cmdb-integ-dashboard&family=xanadu&ft:locale=en-US)**

The CMDB Integrations Dashboard has a modernized look and feel with the Next Experience user interface. Starting with Xanadu release, the CMDB Integrations Dashboard is automatically migrated to the Next Experience user interface. For more information on the Next Experience user interface, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&family=xanadu&ft:locale=en-US).

-   **[\[Placeholder link text to key now-assist-landing-cmdb\]](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&family=xanadu&ft:locale=en-US)**

The ServiceNow® Now Assist for CMDB application brings generative AI to CMDB. The Now Assist for CMDB application provides the following skills:

    -   CI summarization: Shows CI details such as discovery and class, and tallies of records that are related to the CI such as incidents, alerts, and security vulnerabilities, directly on CI forms.
    -   Manage duplicate CIs: Guides you step-by-step through the process of reviewing de-duplication tasks, and then creating and running de-duplication templates to remediate tasks that you choose. As you respond to choices presented by the manage duplicate CIs skill, you receive clear guidance for what should be your next step in the remediation process. This skill also provides root cause analysis to help you prevent future generation of duplicate CIs.
-   **[\[Placeholder link text to key bundle-platcap.now-assist-sgc-landing\]](https://www.servicenow.com/docs/access?context=now-assist-sgc-landing&family=xanadu&ft:locale=en-US)**

The ServiceNow® Now Assist for Service Graph Connectors \(SGC\) application brings in generative AI capabilities to resolve issues within Service Graph Connectors. The Now Assist for SGC application provides the Service Graph Connector diagnosis skill. This skill enables you to troubleshoot issues in a failed import set associated with a Service Graph Connector.

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&family=xanadu&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[CMDB Workspace v8.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US):**

You can now use the Create CI experience in CMDB Workspace to create a CI with a lookup identifier entry that contains mandatory attributes. When you select a lookup identifier entry on the Required attributes page, those mandatory attributes now appear and you can set their values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **[CMDB Workspace v8.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=zurich&ft:locale=en-US):**

You can now use the Create CI experience in CMDB Workspace to create a CI with a lookup identifier entry that contains mandatory attributes. When you select a lookup identifier entry on the Required attributes page, those mandatory attributes now appear and you can set their values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **[CMDB Workspace v9.0 \(including Service Graph Workspace\)](https://www.servicenow.com/docs/access?context=sg-workspace&family=australia&ft:locale=en-US)**
    -   Use Service Graph Workspace which is included in the CMDB Workspace store app, to view data, such as company, location, user, and CMDB data, using panels and dashboards. The Service Graph Workspace is specifically organized to help CMDB administrators, data owners, and analysts work with the CMDB. You can search the CMDB in Service Graph Workspace without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation.
    -   Configure de-duplication remediation processes for related tables to turn off automated workflows, such as ignoring errors and skipping business rules, that might block referenced duplicate CIs from updating to the main CI. Skipping automated workflows for related tables enables de-duplication tasks, which would otherwise fail, to complete successfully. For more information, see [Effects on related tables \(such as Change\)](https://www.servicenow.com/docs/access?context=de-duplication-tasks&family=australia&ft:locale=en-US) and [Turn off workflows of related tables during remediation](https://www.servicenow.com/docs/access?context=dedup-ci-disable-workflow&family=australia&ft:locale=en-US).
-   **[Simplify resolving de-duplication tasks by using a ServiceNow Otto for CMDB skill](https://www.servicenow.com/docs/access?context=reconcile-dup-task&family=australia&ft:locale=en-US)**

Use the De-duplication task resolution assistant skill in the Duplicate CI Remediator to use preselected remediation options instead of manually making selections. An AI agent preselects the options to resolve the task, such as the choice of the main CI. Then, before initiating the remediation, you can review all suggested options with supported reasoning.

To use the De-duplication task resolution assistant skill, you must install the ServiceNow Otto for CMDB version v3.0.


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

Xanadu

</td><td>

-   **[Access changes for the sn\_cmdb\_editor and sn\_cmdb\_admin user roles](https://www.servicenow.com/docs/access?context=installed-with-cmdb-workspace&family=xanadu&ft:locale=en-US)**
    -   Starting with Xanadu Patch 9 \(zbooted or upgraded\), access has been reduced for the sn\_cmdb\_editor \(CMDB Editor\) and the sn\_cmdb\_admin \(CMDB Admin\) user roles which are used in [CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=xanadu&ft:locale=en-US). The sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Xanadu Patch 10 \(zbooted or upgraded\), you must manually run the scheduled job '**Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the permissions that are necessary for performing some CMDB Workspace tasks.

This scheduled job modifies user roles as follows:

        -   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
        -   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the 'Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles' scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).
-   **[CMDB Health](https://www.servicenow.com/docs/access?context=c_CMDBHealth&family=xanadu&ft:locale=en-US)**
    -   Configuring and using CMDB Health is simplified by the removal of some concepts such as overall health scores.
    -   Sections on the CMDB Health Dashboard reporting on compliant CIs are clearly separated from report sections for non-compliant CIs that require your attention.
    -   Failure thresholds for KPIs and metrics enforce an upper limit of 100,000 to avoid excessive processing when a large number of CIs fail the specified metric tests.
    -   The CMDB Health Dashboard still shows non-compliance data that was gathered even if the process is stopped due to excessive failures so you can fix the specific failures already detected.
    -   CI health reporting is integrated into CI forms in CMDB Workspace.
-   **[CMDB Workspace store app](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=xanadu&ft:locale=en-US)**
    -   [CMDB 360](https://www.servicenow.com/docs/access?context=cmdb360-exp-cmdb-workspace&family=xanadu&ft:locale=en-US):
        -   Manage performance by filtering the data included in Coverage charts in the CMDB 360 dashboard in CMDB Workspace by principal class setting or by whether tables are within the CMDB hierarchy.
        -   Manage the scope of data processed by CMDB 360 by setting a maximum threshold for the number of multisource records per class and tracking those classes that exceed that threshold in a table so that those classes are excluded from future CMDB 360 calculations. You can override this exclusion to include selected classes even if they exceed the threshold.
    -   [Data Certification](https://www.servicenow.com/docs/access?context=data-cert-exp-cmdb-workspace&family=xanadu&ft:locale=en-US)

When reviewing Data Certification tasks in CMDB Workspace, use a single click to select all the records associated with a task, to certify or fail the certification in bulk.

    -   [CI timeline in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=xanadu&ft:locale=en-US)

When a CI timeline on the CI details pane in CMDB Workspace fails to load, the error message that appears now includes a link that you can select to go to the CI timeline in the base system.

-   **[CSDM and the CMDB Data Foundations Dashboards](https://www.servicenow.com/docs/access?context=csdm-cmdb-foundations-dashboards&family=xanadu&ft:locale=en-US)**
    -   Limit the performance impact of some of the CMDB and CSDM metrics such as the **CIs Processed via IRE** and **Business Application with Application Service Relationship** by adjusting the settings for triggering the system to automatically deactivate those metrics.
    -   Identify current and non-current metric data by viewing the **Updated** column in the list views of CMDB.
    -   Access the CSDM Data Foundations dashboard from the [Management view in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace-mangmnt-view&family=xanadu&ft:locale=en-US).
-   **[Select a parent class in an IRE identification rule](https://www.servicenow.com/docs/access?context=t_CreateCIIdentificationRule&family=xanadu&ft:locale=en-US)**

Avoid the unnecessary creation of a duplicate CI by setting the **Search On Table** field in an identification rule to one of the parent classes of the current class. When Identification and Reconciliation \(IRE\) identifies a CI in a parent class that matches a CI in the payload, IRE updates that CI with the details from the payload without creating a duplicate CI.

-   **[Improved migration and ongoing sync of CSDM life-cycle data](https://www.servicenow.com/docs/access?context=csdm-life-cycle-standard-values&family=xanadu&ft:locale=en-US)**

The one-time operation aligns CSDM life-cycle values in asset and CI tables. After the initial alignment, business rules can run on regular schedules to ensure that life-cycle values for the asset, CI, and IBI tables remain aligned. Using standard life-cycle values significantly improves data accuracy to help optimize value for many ServiceNow AI Platform applications.

-   **[Application Services dashboard](https://www.servicenow.com/docs/access?context=app-service-dashboard&family=xanadu&ft:locale=en-US)**

Internal queries on the Application Services dashboard that filters for application services now checks not only for all the records in the Application Service \[cmdb\_ci\_service\_auto\] class, but for those records in which the value of **Service classification** is **Application Service**.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[CMDB Workspace v7.5](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US)**

In the CMDB Workspace version 7.5, you can now do the following tasks:

    -   Delete CMDB Data Manager retirement definitions in CMDB Workspace \(other than the cmdb\_ci retirement definition\). For more information, see [Delete a CMDB Data Manager retirement definition](https://www.servicenow.com/docs/access?context=data-manager-manage-ret-def-wrkspc&family=yokohama&ft:locale=en-US).
    -   Configure a CMDB Data Manager certification policy to disallow reviewers, to update fields' value while reviewing CIs in a certification task. Administrators can clear the **Allow updates to field values** option to prevent reviewers from updating non-compliant field values into compliance, resulting in rejecting those CIs. For more information, see [Create a CMDB Data Manager policy in CMDB Workspace](https://www.servicenow.com/docs/access?context=data-manager-create-policy-wrkspc&family=yokohama&ft:locale=en-US).
    -   Schedule a de-duplication template for daily, weekly, monthly, or periodic runs for continuous remediation of duplicate CIs. For more information, see [Schedule a de-duplication template](https://www.servicenow.com/docs/access?context=workspc-dedup-schedule-template&family=yokohama&ft:locale=en-US).
    -   Receive notifications from CMDB Data Manager about certification and attestation tasks, that are incomplete or overdue. For more information, see [Components related to CMDB Data Manager](https://www.servicenow.com/docs/access?context=components-cmdb-data-manager&family=yokohama&ft:locale=en-US).
    -   Review and process tasks of your direct reports and of members of any user group that you manage. For more information about accessing these tasks in CMDB Data Manager, see [My Work view in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace-govern-view&family=yokohama&ft:locale=en-US).
    -   Reject a CMDB Data Manager life-cycle task in CMDB Workspace. For more information, see [Review CMDB Data Manager tasks in CMDB Workspace](https://www.servicenow.com/docs/access?context=data-manager-review-task-wrkspc&family=yokohama&ft:locale=en-US).
    -   Use the Create CI experience with a preset class when drilling down a class in the CI Summary chart on the Home view of CMDB Workspace. For more information about creating CIs manually while applying IRE processes, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&family=zurich&ft:locale=en-US)**

Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


</td></tr><tr><td>

Australia

</td><td>

-   **[Cleaner category grouping for Data Foundations advisor](https://www.servicenow.com/docs/access?context=cmdb-sa-df-dashboard&family=australia&ft:locale=en-US)**

The CI class categories filter and the Set principal classes dialog box hide Data Model Navigator child categories that are already nested under a parent category, so the top-level list doesn't repeat categories.


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

Xanadu

</td><td>

-   CMDB Health:
    -   The CMDB Health Dashboard on Core UI isn't included in new Xanadu instances. On upgraded instances, this dashboard is available but no longer supported.
    -   The CI dashboard isn't included in new Xanadu instances. On upgraded instances, this dashboard is available but no longer supported.
    -   The following widgets have been removed from the CI Health tile in the CMDB Workspace: Incomplete Attributes vs Total Attributes, Non-compliant relationships vs Total Relationships, and Stale relationships vs Total Relationships widgets.
    -   The concept of the overall health score has been removed and no longer appears in any of the CMDB Health dashboards or views.
    -   The concept of weighted averages and scorecards thresholds, which specify the ranges of health states, has been removed.
    -   The bar charts for metrics in the main CMDB Health Dashboard have been removed, as well as the tiles for top 10 incident, alert, and change generators.
    -   The **CMDB Health Dashboard - Top Task Generating CIs Calculation** scheduled job has been removed.
-   CSDM and the CMDB Data Foundations Dashboards:
    -   When drilling down into the CIs Not Processed Via IRE in the Data Management Practices metric group, the **Show Records** button isn't supported.
    -   When drilling down into the Orphan CIs metric, only a list view of orphan CIs appears without any Performance Analytics details.

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

Between your current release family and Brazil, some Configuration Management Database \(CMDB\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Starting with the Xanadu release, the Data Certification plugin \(com.snc.certification\_v2\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. The [CMDB Workspace store app](https://www.servicenow.com/docs/access?context=cmdb-workspace&family=xanadu&ft:locale=en-US) provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0867184]) article in the Now Support knowledge base.
-   ServiceNow hosted Service Graph Connector for ExtraHop is now deprecated and no longer supported or available for new activation. Service Graph Connector for ExtraHop provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Yokohama

</td><td>

CMDB Data manager on Core UI is now deprecated and no longer supported or available for new activation. CMDB Workspace provides the latest experience for this functionality. For more information, see [CMDB Data Manager experience in CMDB Workspace](https://www.servicenow.com/docs/access?context=data-mgr-exp-cmdb-workspace&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

-   Common Service Data Model no longer provides **Design** as a value for the **Operational status** attribute in CIs.

 -   The Data Certification plugin \(com.snc.certification\_v2\) is now deprecated and no longer supported or available for new activation. The latest experience for this functionality is included with CMDB Workspace.


</td></tr><tr><td>

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

Xanadu

</td><td>

CMDB is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Activation information**

CMDB is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

CMDB is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

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
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Configuration Management Database \(CMDB\) we have noted them here.

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

Review details on accessibility information for Configuration Management Database \(CMDB\), such as specific requirements or compliance levels.

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

-   **Accessibility information**
    -   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

    -   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to the monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for the details.


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

If there are specific localization considerations for Configuration Management Database \(CMDB\) we have noted them here.

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

If there are specific highlight considerations for Configuration Management Database \(CMDB\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Access changes to the CMDB Editor and CMDB Admin user roles:
    -   Starting with Xanadu Patch 9, the sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Xanadu Patch 10, you can configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks by manually running a scheduled job.
-   Configuring and using CMDB Health has been streamlined by useful analytic data having been simplified and some concepts such as overall health scores having been removed.
-   New filtering options for the Coverage charts on the CMDB 360 dashboard help you better manage the performance associated with calculating those charts, while limiting analysis to only those classes that you're interested in.
-   Limit the performance impact of CSDM and the CMDB Data Foundations Dashboards by configuring performance settings for some metrics to limit their performance impact, such as triggering the system to automatically deactivate metrics such as **CIs Processed via IRE** and **Business Application with Application Service Relationship**.
-   The CMDB Health Dashboard is now implemented with the Next Experience user interface in the CMDB Workspace.
-   The ServiceNow® Now Assist for CMDB application brings generative AI to CMDB. Now Assist for CMDB is a new application in the Xanadu release. The ServiceNow® Now Assist for Service Graph Connectors \(SGC\) application brings in generative AI capabilities to resolve issues within Service Graph Connector. Now Assist for SGC is a new application in the Xanadu release..

 See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Access changes to the CMDB Editor and CMDB Admin user roles:
    -   Starting with Yokohama Patch 4, the sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Yokohama Patch 6, you can configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks by manually running a scheduled job.
-   Manually create a configuration item \(CI\) in CMDB Workspace that is verified by the Identification and Reconciliation Engine \(IRE\) and is unique within CMDB. Creating a CI using the IRE identification rules helps to maintain the integrity of CMDB.
-   Use the ServiceNow Otto for CMDB CI summarization skill to see a comprehensive summary for a CI, with details such as discovery and related incidents, directly on the configuration item \(CI\) form. Use the manage duplicate CIs skill for step-by-step guidance on how to use de-duplication templates to de-duplicate CIs.
-   The Configuration item summarizer AI agent accepts the sys\_id of a CI and returns a full summary of Configuration Management Database \(CMDB\) data for the CI. The agent isn’t typically used as a standalone agent and any use case can access it.
-   View the various counts, such as the number of CIs and the number of CI types, for the CIs that are connected to the home node in Unified Map.
-   Apply filters that were previously available only to the coverage charts in the CMDB 360 dashboard in CMDB Workspace to all charts in the Discovery sources tile.
-   Use a condition builder or a custom script to restrict the list of de-duplication tasks that are assigned to a de-duplication template when de-duplicating CIs.

 See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

