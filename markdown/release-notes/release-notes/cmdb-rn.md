---
title: Configuration Management Database \(CMDB\) release notes
description: The ServiceNow Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
---

# Configuration Management Database \(CMDB\) release notes

The ServiceNow® Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Zurich release.

## CMDB highlights for the Zurich release

-   Access a centralized location with a comprehensive view of the configuration item \(CI\) details by using the new CI form in CMDB Workspace. You can view and edit the CI attributes, relationships, and data, such as the CMDB Health report for the CI, CMDB 360 data that is associated with the CI, and the CI resources, activities, and related services.
-   Access the Data Certification dashboard in CMDB Workspace to gain insights about the data certification activities and progress, examine policies and tasks, and see the reports about the certification instances, charts of the aging certification tasks, and group and individual workloads.
-   Add or remove CIs directly from a map in Unified Map. You can also add, modify, or delete CI relationships in CMDB.
-   Configure the system to use Identification and Reconciliation Engine \(IRE\) identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** attributes.
-   In zbooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role, and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.

## Important information for upgrading CMDB to Zurich

Due to the removal of the **Design** value for the operational status attribute in a CI, after an upgrade, you must review all CIs that have the discovery source attribute set to **Manual via IRE**. Review the operational status attribute of those CIs and set it to a supported value in CMDB for your environment. For example, you can set the attribute to **Non-Operational**. For more information about the operational status values, see [Life cycle of tangible/physical CIs](https://www.servicenow.com/docs/access?context=csdm-lifecycle-hardware&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

On an upgraded Zurich instance, to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks, you must manually run the scheduled job **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles**. This scheduled job modifies the user roles as follows:

-   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
-   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).

## New in the Zurich release

-   **[CMDB Workspace v8.0](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US):**

    You can now use the Create CI experience in CMDB Workspace to create a CI with a lookup identifier entry that contains mandatory attributes. When you select a lookup identifier entry on the Required attributes page, those mandatory attributes now appear and you can set their values for proper IRE processing. For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US):**

    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://www.servicenow.com/docs/access?context=ci-form-cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://www.servicenow.com/docs/access?context=data-cert-dashboard-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    -   [Create or manage a shared preset](https://www.servicenow.com/docs/access?context=unified-map-manage-shared-preset&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records as follows:
        -   The table cleanup rule for the CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\] table, which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

            Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive the certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task\] table.
        -   The archival of related records in the CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] table is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
    The Zurich release includes an installation of CMDB Workspace. However, you can download a newer version of CMDB Workspace so that you can use its latest features in your Zurich instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**
    -   On the Published policy tile on the Data Manager policies page, the policies list view now shows the scheduled job that is associated with the policy and the user that the policy runs as.

        For more information, see [Create a CMDB Data Manager policy](https://www.servicenow.com/docs/access?context=data-manager-create-policy-wrkspc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   Instead of the system automatically setting the **run as** attribute of the scheduled certification and attestation jobs to be the user that authored the policy, you can now set a specific user that adheres to the policies and regulations in the organization. Configure the default values for the run as user and user accounts available for run as assignees for auditing purposes when it’s important to know who initiated the changes.

        For more information, see [Components related to CMDB Data Manager](https://www.servicenow.com/docs/access?context=components-cmdb-data-manager&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   For certification and attestation policy tasks, choose how to assign tasks in cases where a specified task assignment field is empty for a target CI. Specify a user or a user group to assign such tasks to, or create the tasks without assigning them. An administrator can later review and assign those tasks.

        For more information, see [Create a CMDB Data Manager policy](https://www.servicenow.com/docs/access?context=data-manager-create-policy-wrkspc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   View the closed tasks in the My Work view in CMDB Workspace. Select the Closed card in the Task status tile to review the \(in read-only mode\) details for tasks that are in the Closed Complete, Closed Canceled, Closed Incomplete, or Rejected state.

        For more information, see [My Work view in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace-govern-view&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   New CIs in the Create CI experience no longer have their **Operational status** attribute set. The new **CI Operational state** attribute appears on the Additional attributes page of the Create CI experience. Setting it to any value is optional.

        For more information, see [Create a CI manually in CMDB Workspace](https://www.servicenow.com/docs/access?context=create-ci-manual-cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    -   The itil user role now contains the sn\_cmdb\_user user role and no longer contains the sn\_cmdb\_editor user role. As a result, the following functions that were accessible to itil users now require the sn\_cmdb\_editor user role:
        -   Create and delete the operations that are related to CMDB 360 queries.
        -   Access the CMDB Retirement Definitions module by navigating to **All** &gt; **Configuration** &gt; **CMDB Retirement Definitions**.
        -   Access the Create CI quick link on the Home view of CMDB Workspace.
-   **[Containment in the itil user role](https://www.servicenow.com/docs/access?context=installed-with-cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    In zBooted instances, the itil user role no longer contains the sn\_cmdb\_editor user role and the itil\_admin user role no longer contains the sn\_cmdb\_admin user role. However, the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles now have full \(create, update, delete\) access to the Configuration Item \[cmdb\_ci\] class.

-   **[Constraints when deleting a CMDB Data Manager retirement definition](https://www.servicenow.com/docs/access?context=data-manager-manage-ret-def-wrkspc&version=zurich&pubname=zurich-servicenow-platform&section=data-manager-delete-ret-def-wrkspc&ft:locale=en-US)**

    The same constraints that exist when deleting a retirement definition in CMDB Workspace now apply when directly accessing the CMDB Retirement Custom Definitions \[cmdb\_retirement\_custom\_definitions\] table:

    -   The retirement definition that you want to delete must be in an inactive mode \(**Active** = **false**\).
    -   The retirement definition for the Configuration Item \[cmdb\_ci\] class can't be deleted.
-   **[Prioritize using IRE identification rules for uniquely identifying CIs](https://www.servicenow.com/docs/access?context=ire&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Configure the system to prioritize the use of IRE identification rules to uniquely identify CIs in a payload, instead of using the **source\_name** and **source\_native\_key** fields. For more information about using the **glide.identification\_engine.skip\_sys\_object\_source\_matching** system property to control this behavior, see [Properties](https://www.servicenow.com/docs/access?context=properties-id-reconciliation&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

-   **[Run a query in an enhanced execution mode](https://www.servicenow.com/docs/access?context=config-query-builder-engine-mode&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Set the execution mode for a saved CMDB Query Builder query to run using an enhanced query execution engine, which is designed for improved performance and scalability.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.

-   **[New role required for the Create configuration item agentic workflow](https://www.servicenow.com/docs/access?context=na-cmdb-awf-ci-creator&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The sn\_cmdb\_admin role is now required to use the Create configuration item agentic workflow \(was sn\_cmdb\_editor\).


## Removed in this release

-   Common Service Data Model no longer provides **Design** as a value for the **Operational status** attribute in CIs.

## Deprecations

-   The Data Certification plugin \(com.snc.certification\_v2\) is now deprecated and no longer supported or available for new activation. The latest experience for this functionality is included with CMDB Workspace.


## Activation information

CMDB is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Common Service Data Model \(CSDM\)](https://www.servicenow.com/docs/access?context=csdm-landing-page&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Common Service Data Model \(CSDM\) provides prescriptive guidelines for service modeling within CMDB and is the standard for all ServiceNow products that use CMDB. CSDM provides a framework for mapping data from your IT services and other products to CMDB. Following the CSDM framework helps confirm that the required data for your ServiceNow application maps correctly to the appropriate CMDB tables.

-   **[Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-third-party-integrations&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Use predefined ServiceNow® Service Graph connectors to import data from third-party applications, such as Microsoft SCCM, into your CMDB. In addition, you can use the [IntegrationHub ETL](https://www.servicenow.com/docs/access?context=integrationhub-etl&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) store app to create and manage custom ETL transform maps so that you can integrate third-party data into CMDB without compromising its integrity.

-   **[CMDB Workspace store app](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Use the CMDB Workspace store app to search, explore, and gain insights into CMDB. The CMDB Workspace is a store app that provides a central place for working with CMDB. In CMDB Workspace you can examine the health and recent activity related to CMDB, and access various CMDB dashboards and tools to support the tasks in your organization.

-   **[Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    Use ServiceNow® Now Assist for CMDB to improve the quality of CMDB data, to get help as you search the CMDB, troubleshoot issues with Service Graph Connector import sets, remediate duplicate CIs, manually create CIs, and view the comprehensive summaries for CIs. For release notes, see [Now Assist for CMDB release notes](now-assist-cmdb-rn.md).


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

