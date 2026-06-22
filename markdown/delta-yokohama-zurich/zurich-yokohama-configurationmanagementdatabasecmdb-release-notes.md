---
title: Combined Configuration Management Database \(CMDB\) release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Configuration Management Database \(CMDB\) from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-configurationmanagementdatabasecmdb-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 23
breadcrumb: [Products combined by family]
---

# Combined Configuration Management Database \(CMDB\) release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Configuration Management Database \(CMDB\) from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Configuration Management Database \(CMDB\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Configuration Management Database \(CMDB\) to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Three new indexes \(parent, type\), \(child, type\), and \(child, parent, type, port\) are added to the CI Relationship \[cmdb\_rel\_ci\] table to improve the performance of Identification and Reconciliation Engine \(IRE\) querying this table. This change is likely to increase upgrade time. For more information about the impact of this change during upgrade and to learn how to minimize that impact, see [Increased Yokohama Upgrade Time due to cmdb\_rel\_ci index additions \[KB1703367\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB1703367).

</td></tr><tr><td>

Zurich

</td><td>

Due to the removal of the **Design** value for the operational status attribute in a CI, after an upgrade, you must review all CIs that have the discovery source attribute set to **Manual via IRE**. Review the operational status attribute of those CIs and set it to a supported value in CMDB for your environment. For example, you can set the attribute to **Non-Operational**. For more information about the operational status values, see [Tangible/physical life cycle](https://servicenow-staging.fluidtopics.net/access?context=csdm-lifecycle-hardware&family=zurich&ft:locale=en-US).

 On an upgraded Zurich instance, to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks, you must manually run the scheduled job **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles**. This scheduled job modifies the user roles as follows:

-   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
-   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Configuration Management Database \(CMDB\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[CMDB Workspace v8.0](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US):**

You can now use the Create CI experience in CMDB Workspace to create a CI with a lookup identifier entry that contains mandatory attributes. When you select a lookup identifier entry on the Required attributes page, those mandatory attributes now appear and you can set their values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=create-ci-manual-cmdb-workspace&family=yokohama&ft:locale=en-US).

-   **[CMDB Workspace v7.6](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US):**
    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://servicenow-staging.fluidtopics.net/access?context=ci-form-cmdb-workspace&family=yokohama&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://servicenow-staging.fluidtopics.net/access?context=data-cert-dashboard-workspace&family=yokohama&ft:locale=en-US).
    -   [Manage a shared preset](https://servicenow-staging.fluidtopics.net/access?context=unified-map-manage-shared-preset&family=yokohama&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace-unified-map&family=yokohama&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records, as follows:
        -   The table cleanup rule for table CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\], which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task table\].
        -   The archival of related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
-   **[SGC Central](https://servicenow-staging.fluidtopics.net/access?context=sgcc-landing&family=yokohama&ft:locale=en-US)**

Use the Service Graph Connector Central view, also known as the SGC Central view, in the CMDB Workspace to discover and install connectors, and then effectively manage the full life cycle of creating, editing, monitoring, and debugging connections.

-   **[Now Assist for Configuration Management Database \(CMDB\)](https://servicenow-staging.fluidtopics.net/access?context=now-assist-landing-cmdb&family=yokohama&ft:locale=en-US)**

Use the new Now Assist for CMDB agentic workflows, AI agents, and skills. The Now Assist CI summarizer AI agent summarizes the key details for CIs, such as the discovery and incident details, directly on the CI forms. The Manage duplicate CIs skill guides you step by step on how to use the deduplication templates to help maintain the health and integrity of CMDB.

-   **[Search the CMDB](https://servicenow-staging.fluidtopics.net/access?context=na-cmdb-awf-search&family=yokohama&ft:locale=en-US)**

The CMDB search agentic workflow enables you to search for CI data by specifying any of several attributes of the CI of interest. The workflow accepts your natural language request, verifies your search goal, and then generates a keyword search, a single-table search with dot walks, or a multi-table search, depending on the information you provide. The workflow can infer CI relationship data to generate an appropriate query.

-   **[Get advice on CMDB governance](https://servicenow-staging.fluidtopics.net/access?context=na-cmdb-awf-governance&family=yokohama&ft:locale=en-US)**

Data governance can be an overwhelming task. The CMDB Governance agentic workflow supports admins and owners by methodically working through the process of improving CMDB data governance. The objective is to ensure that users trust their data for the evolving outcomes they want to achieve.

-   **[Create a CI](https://servicenow-staging.fluidtopics.net/access?context=na-cmdb-awf-ci-creator&family=yokohama&ft:locale=en-US)**

Occasionally, you might need to create a CI manually. To help you, the workflow accepts your natural language request and verifies that it understands which class the new CI should belong to. The workflow then checks IRE policies to determine the required attributes for the CI and request that information. After you provide sufficient data, the workflow uses IRE to ensure that the proposed CI is not a duplicate, and then creates the Cl.

-   **[Administer](https://servicenow-staging.fluidtopics.net/access?context=administer-unified-map&family=yokohama&ft:locale=en-US)**

Configure general Unified Map settings for the workspace on your instance. Only a user with the sn\_cmdb\_admin role can configure these settings.

-   **[Viewing a summary of Unified Map contents in the Overview panel](https://servicenow-staging.fluidtopics.net/access?context=unified-map-show-overview-panel&family=yokohama&ft:locale=en-US)**

Use the new Overview panel to show the summary data for a map that is associated with the home node, including the counts and types of CIs, connections, and discovery sources.

-   **[Edit a map](https://servicenow-staging.fluidtopics.net/access?context=unified-map-editing-map&family=yokohama&ft:locale=en-US)**

While you work in the map editor, you can add CIs to the map and remove CIs from the map. You can also add, modify, and delete CI relationships in the CMDB.

-   **[Quick start tests for CMDB](https://servicenow-staging.fluidtopics.net/access?context=quick-start-tests-cmdb&family=yokohama&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr><tr><td>

Zurich

</td><td>

-   **[CMDB Workspace v8.0](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=zurich&ft:locale=en-US):**

You can now use the Create CI experience in CMDB Workspace to create a CI with a lookup identifier entry that contains mandatory attributes. When you select a lookup identifier entry on the Required attributes page, those mandatory attributes now appear and you can set their values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=create-ci-manual-cmdb-workspace&family=zurich&ft:locale=en-US).

-   **[CMDB Workspace v7.6](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=zurich&ft:locale=en-US):**

    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://servicenow-staging.fluidtopics.net/access?context=ci-form-cmdb-workspace&family=zurich&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://servicenow-staging.fluidtopics.net/access?context=data-cert-dashboard-workspace&family=zurich&ft:locale=en-US).
    -   [Manage shared filter settings](https://servicenow-staging.fluidtopics.net/access?context=unified-map-manage-shared-preset&family=zurich&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace-unified-map&family=zurich&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records as follows:
        -   The table cleanup rule for the CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] table, which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive the certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task\] table.
        -   The archival of related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
The Zurich release includes an installation of CMDB Workspace. However, you can download a newer version of CMDB Workspace so that you can use its latest features in your Zurich instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   **[Quick start tests for CMDB](https://servicenow-staging.fluidtopics.net/access?context=quick-start-tests-cmdb&family=zurich&ft:locale=en-US)**

After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Configuration Management Database \(CMDB\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Access changes for the sn\_cmdb\_editor and sn\_cmdb\_admin user roles](https://servicenow-staging.fluidtopics.net/access?context=installed-with-cmdb-workspace&family=yokohama&ft:locale=en-US)**
    -   Starting with Yokohama Patch 4 \(zbooted or upgraded\), access has been reduced for the sn\_cmdb\_editor \(CMDB Editor\) and the sn\_cmdb\_admin \(CMDB Admin\) user roles which are used in [CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US). The sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Yokohama Patch 6 \(zbooted or upgraded\), you must manually run the scheduled job '**Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the permissions that are necessary for performing some CMDB Workspace tasks.

This scheduled job modifies user roles as follows:

        -   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
        -   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the 'Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles' scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).
-   **[CMDB Workspace v6.3](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US)**
    -   Apply the filters that were previously available only to the coverage charts to all charts in the Discovery sources tile in the CMDB 360 dashboard. For example, you can filter out non-CMDB tables or include records only from principal classes. For more information, see [CMDB 360 experience in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=cmdb360-exp-cmdb-workspace&family=yokohama&ft:locale=en-US).
    -   Use a condition builder or a custom script to narrow down the list of de-duplication tasks that are assigned to a template. For more information, see [Create a de-duplication template](https://servicenow-staging.fluidtopics.net/access?context=workspc-dedup-create-template&family=yokohama&ft:locale=en-US).
    -   Use the new **Allow empty field values** option to allow or disallow certification of empty value fields when creating a certification policy type in CMDB Data Manager. For more information, see [Create a CMDB Data Manager policy in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=data-manager-create-policy-wrkspc&family=yokohama&ft:locale=en-US).
-   **[CMDB Workspace v6.4](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US)**

You can now use dot-walking when setting assignments for the User Field or User Group Field options for CMDB Data Manager policies \(such as Certification\). Also, when converting legacy certification schedules into Data Manager Certification policies, existing dot-walking settings are preserved. For more information, see [Create a CMDB Data Manager policy in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=data-manager-create-policy-wrkspc&family=yokohama&ft:locale=en-US).

-   **[CMDB Workspace v7.4](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US)**

In the CMDB Workspace version 7.4, you can now do the following tasks:

    -   Manually create a CI in CMDB Workspace that complies with its class identification rule and other class requirements, and is tested for uniqueness in CMDB, to help ensure that the CI is valid and maintains the integrity of CMDB. For more information, see [Create a CI manually in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=create-ci-manual-cmdb-workspace&family=yokohama&ft:locale=en-US).
    -   Set the CMDB Health dashboard to use the legacy methods to calculate the completeness, correctness, and compliance KPIs. That legacy calculation method relies on settings of proportional weights of metrics within the aggregated score of KPIs and was used up until the Washington DC release. By default, those weights aren’t used in the calculations of KPI scores.

Also, the CMDB Health dashboard now shows the overall score, which by default, is a simple average of the aggregated scores of the completeness, correctness, and compliance KPIs.

-   **[CMDB Workspace v7.5](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=yokohama&ft:locale=en-US)**

In the CMDB Workspace version 7.5, you can now do the following tasks:

    -   Delete CMDB Data Manager retirement definitions in CMDB Workspace \(other than the cmdb\_ci retirement definition\). For more information, see [Delete a CMDB Data Manager retirement definition](https://servicenow-staging.fluidtopics.net/access?context=data-manager-manage-ret-def-wrkspc&family=yokohama&ft:locale=en-US).
    -   Configure a CMDB Data Manager certification policy to disallow reviewers, to update fields' value while reviewing CIs in a certification task. Administrators can clear the **Allow updates to field values** option to prevent reviewers from updating non-compliant field values into compliance, resulting in rejecting those CIs. For more information, see [Create a CMDB Data Manager policy in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=data-manager-create-policy-wrkspc&family=yokohama&ft:locale=en-US).
    -   Schedule a de-duplication template for daily, weekly, monthly, or periodic runs for continuous remediation of duplicate CIs. For more information, see [Schedule a de-duplication template](https://servicenow-staging.fluidtopics.net/access?context=workspc-dedup-schedule-template&family=yokohama&ft:locale=en-US).
    -   Receive notifications from CMDB Data Manager about certification and attestation tasks, that are incomplete or overdue. For more information, see [Components related to CMDB Data Manager](https://servicenow-staging.fluidtopics.net/access?context=components-cmdb-data-manager&family=yokohama&ft:locale=en-US).
    -   Review and process tasks of your direct reports and of members of any user group that you manage. For more information about accessing these tasks in CMDB Data Manager, see [My Work view in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace-govern-view&family=yokohama&ft:locale=en-US).
    -   Reject a CMDB Data Manager life-cycle task in CMDB Workspace. For more information, see [Review CMDB Data Manager tasks in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=data-manager-review-task-wrkspc&family=yokohama&ft:locale=en-US).
    -   Use the Create CI experience with a preset class when drilling down a class in the CI Summary chart on the Home view of CMDB Workspace. For more information about creating CIs manually while applying IRE processes, see [Create a CI manually in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=create-ci-manual-cmdb-workspace&family=yokohama&ft:locale=en-US).
-   **[Update to the Walk stage reports on the CSDM Data Foundations dashboard](https://servicenow-staging.fluidtopics.net/access?context=csdm-datafdn-dash-walk-tab&family=yokohama&ft:locale=en-US)**

The Technical Service Offerings with Support Group or Change Group report now includes data that meets the **sys\_class \_name = offering** parameter.

-   **[Table label changes](https://servicenow-staging.fluidtopics.net/access?context=cmdb-tables-details&family=yokohama&ft:locale=en-US)**

The following table labels have changed:

    -   The label for the cmdb\_ci\_service\_auto table is now Service Instance instead of Application Service.
    -   The label for the cmdb\_ci\_service\_technical table is now Technology management service instead of Technical service.
-   **[Class descriptions showing in the user interface](https://servicenow-staging.fluidtopics.net/access?context=cmdb-tables-details&family=yokohama&ft:locale=en-US)**

The descriptions for the base system classes are now integrated into CI Class Manager and appear in the **Description** field, on the Basic Info page for a class.

-   **[Reflow for configurable workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=yokohama&ft:locale=en-US)**

The CMDB configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.


</td></tr><tr><td>

Zurich

</td><td>

-   **[CMDB Workspace v7.6](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace&family=zurich&ft:locale=en-US)**
    -   On the Published policy tile on the Data Manager policies page, the policies list view now shows the scheduled job that is associated with the policy and the user that the policy runs as.

For more information, see [Create a CMDB Data Manager policy](https://servicenow-staging.fluidtopics.net/access?context=data-manager-create-policy-wrkspc&family=zurich&ft:locale=en-US).

    -   Instead of the system automatically setting the **run as** attribute of the scheduled certification and attestation jobs to be the user that authored the policy, you can now set a specific user that adheres to the policies and regulations in the organization. Configure the default values for the run as user and user accounts available for run as assignees for auditing purposes when it’s important to know who initiated the changes.

For more information, see [Components related to CMDB Data Manager](https://servicenow-staging.fluidtopics.net/access?context=components-cmdb-data-manager&family=zurich&ft:locale=en-US).

    -   For certification and attestation policy tasks, choose how to assign tasks in cases where a specified task assignment field is empty for a target CI. Specify a user or a user group to assign such tasks to, or create the tasks without assigning them. An administrator can later review and assign those tasks.

For more information, see [Create a CMDB Data Manager policy](https://servicenow-staging.fluidtopics.net/access?context=data-manager-create-policy-wrkspc&family=zurich&ft:locale=en-US).

    -   View the closed tasks in the My Work view in CMDB Workspace. Select the Closed card in the Task status tile to review the \(in read-only mode\) details for tasks that are in the Closed Complete, Closed Canceled, Closed Incomplete, or Rejected state.

For more information, see [My Work view in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=cmdb-workspace-govern-view&family=zurich&ft:locale=en-US).

    -   New CIs in the Create CI experience no longer have their **Operational status** attribute set. The new **CI Operational state** attribute appears on the Additional attributes page of the Create CI experience. Setting it to any value is optional.

For more information, see [Create a CI manually in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=create-ci-manual-cmdb-workspace&family=zurich&ft:locale=en-US).

    -   The itil user role now contains the sn\_cmdb\_user user role and no longer contains the sn\_cmdb\_editor user role. As a result, the following functions that were accessible to itil users now require the sn\_cmdb\_editor user role:
        -   Create and delete the operations that are related to CMDB 360 queries.
        -   Access the CMDB Retirement Definitions module by navigating to **All** &gt; **Configuration** &gt; **CMDB Retirement Definitions**.
        -   Access the Create CI quick link on the Home view of CMDB Workspace.
-   **[Containment in the itil user role](https://servicenow-staging.fluidtopics.net/access?context=installed-with-cmdb-workspace&family=zurich&ft:locale=en-US)**

In zBooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

-   **[Constraints when deleting a CMDB Data Manager retirement definition](https://servicenow-staging.fluidtopics.net/access?context=data-manager-delete-ret-def-wrkspc&family=zurich&ft:locale=en-US)**

The same constraints that exist when deleting a retirement definition in CMDB Workspace now apply when directly accessing the CMDB Retirement Custom Definitions \[cmdb\_retirement\_custom\_definitions\] table:

    -   The retirement definition that you want to delete must be in an inactive mode \(**Active** = **false**\).
    -   The retirement definition for the Configuration Item \[cmdb\_ci\] class can't be deleted.
-   **[Prioritize using IRE identification rules for uniquely identifying CIs](https://servicenow-staging.fluidtopics.net/access?context=ire&family=zurich&ft:locale=en-US)**

Configure the system to prioritize the use of IRE identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** fields. For more information about using the **glide.identification\_engine.skip\_sys\_object\_source\_matching** system property to control this behavior, see [Properties](https://servicenow-staging.fluidtopics.net/access?context=properties-id-reconciliation&family=zurich&ft:locale=en-US).

-   **[Run a query in an enhanced execution mode](https://servicenow-staging.fluidtopics.net/access?context=config-query-builder-engine-mode&family=zurich&ft:locale=en-US)**

Set the execution mode for a saved CMDB Query Builder query to run using an enhanced query execution engine, which is designed for improved performance and scalability.

-   ****
-   **[New role required for the Create configuration item agentic workflow](https://servicenow-staging.fluidtopics.net/access?context=na-cmdb-awf-ci-creator&family=zurich&ft:locale=en-US)**

The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Configuration Management Database \(CMDB\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   Common Service Data Model no longer provides **Design** as a value for the **Operational status** attribute in CIs.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Configuration Management Database \(CMDB\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

CMDB Data manager on Core UI is now deprecated and no longer supported or available for new activation. CMDB Workspace provides the latest experience for this functionality. For more information, see [CMDB Data Manager experience in CMDB Workspace](https://servicenow-staging.fluidtopics.net/access?context=data-mgr-exp-cmdb-workspace&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

-   The Data Certification plugin \(com.snc.certification\_v2\) is now deprecated and no longer supported or available for new activation. The latest experience for this functionality is included with CMDB Workspace.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Configuration Management Database \(CMDB\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

CMDB is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

CMDB is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Configuration Management Database \(CMDB\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

-   **Reflow**

The Configurable Workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to the monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://servicenow-staging.fluidtopics.net/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for the details.


</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

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

Yokohama

</td><td>

-   Access changes to the CMDB Editor and CMDB Admin user roles:
    -   Starting with Yokohama Patch 4, the sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Yokohama Patch 6, you can configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks by manually running a scheduled job.
-   Manually create a configuration item \(CI\) in CMDB Workspace that is verified by the Identification and Reconciliation Engine \(IRE\) and is unique within CMDB. Creating a CI using the IRE identification rules helps to maintain the integrity of CMDB.
-   Use the Now Assist for CMDB CI summarization skill to see a comprehensive summary for a CI, with details such as discovery and related incidents, directly on the configuration item \(CI\) form. Use the manage duplicate CIs skill for step-by-step guidance on how to use de-duplication templates to de-duplicate CIs.
-   The Configuration item summarizer AI agent accepts the sys\_id of a CI and returns a full summary of Configuration Management Database \(CMDB\) data for the CI. The agent isn’t typically used as a standalone agent and any use case can access it.
-   View the various counts, such as the number of CIs and the number of CI types, for the CIs that are connected to the home node in Unified Map.
-   Apply filters that were previously available only to the coverage charts in the CMDB 360 dashboard in CMDB Workspace to all charts in the Discovery sources tile.
-   Use a condition builder or a custom script to restrict the list of de-duplication tasks that are assigned to a de-duplication template when de-duplicating CIs.

 See [Configuration Management](https://servicenow-staging.fluidtopics.net/access?context=manage-cmdb&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Access a centralized location with a comprehensive view of the configuration item \(CI\) details by using the new CI form in CMDB Workspace. You can view and edit the CI attributes, relationships, and data, such as the CMDB Health report for the CI, CMDB 360 data that is associated with the CI, and the CI resources, activities, and related services.
-   Access the Data Certification dashboard in CMDB Workspace to gain insights about the data certification activities and progress, examine policies and tasks, and see the reports about the certification instances, charts of the aging certification tasks, and group and individual workloads.
-   Add or remove CIs directly from a map in Unified Map. You can also add, modify, or delete CI relationships in CMDB.
-   Configure the system to use Identification and Reconciliation Engine \(IRE\) identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** attributes.
-   In zbooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role, and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

 See [Configuration Management](https://servicenow-staging.fluidtopics.net/access?context=manage-cmdb&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

