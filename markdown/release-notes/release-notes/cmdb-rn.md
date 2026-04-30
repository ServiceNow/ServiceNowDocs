---
title: Configuration Management Database \(CMDB\) release notes
description: The ServiceNow CMDB application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 14
---

# Configuration Management Database \(CMDB\) release notes

The ServiceNow® CMDB application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Xanadu release.

## CMDB highlights for the Xanadu release

-   Access changes to the CMDB Editor and CMDB Admin user roles:
    -   Starting with Xanadu Patch 9, the sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Xanadu Patch 10, you can configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks by manually running a scheduled job.
-   Configuring and using CMDB Health has been streamlined by useful analytic data having been simplified and some concepts such as overall health scores having been removed.
-   New filtering options for the Coverage charts on the CMDB 360 dashboard help you better manage the performance associated with calculating those charts, while limiting analysis to only those classes that you're interested in.
-   Limit the performance impact of CSDM and the CMDB Data Foundations Dashboards by configuring performance settings for some metrics to limit their performance impact, such as triggering the system to automatically deactivate metrics such as **CIs Processed via IRE** and **Business Application with Application Service Relationship**.
-   The CMDB Health Dashboard is now implemented with the Next Experience user interface in the CMDB Workspace.
-   The ServiceNow® Now Assist for CMDB application brings generative AI to CMDB. Now Assist for CMDB is a new application in the Xanadu release. The ServiceNow® Now Assist for Service Graph Connectors \(SGC\) application brings in generative AI capabilities to resolve issues within Service Graph Connector. Now Assist for SGC is a new application in the Xanadu release..

See [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more information.

## Important information for upgrading CMDB to Xanadu

-   Before the upgrade to Xanadu, the ‘Updated CIs’ and ‘Updated application services’ trend lines in the Recent CI activity and Recent application services activities tiles on the Management view in CMDB Workspace, might not have accurately reflected on changes in your system. After upgrading to Xanadu and to versions 5.5, 6.2, or 7.2 of CMDB Workspace, those trend lines will reflect on the more accurate detection of updated CIs and updated application services.
-   CMDB Health:

    If either the **CMDB Health Dashboard - Relationship Compliance Processor** or **CMDB Health Dashboard - Relationship Score Calculation** dashboard job is active, that job is deactivated during the upgrade to Xanadu. After the upgrade is complete, you can reactivate those jobs to resume health reports for CI relationships. The active state of all other CMDB Health dashboard jobs is retained.

    Any failure threshold for a KPI or metric that is greater than 100,000, is set to 100,000 during upgrade. This upper limit is enforced to avoid excessive processing when a large number of CIs are failing the specified metric tests.

-   Bookmarks for the CI dashboard no longer work after an upgrade to Xanadu. A `Page not found` error message appears. To see CMDB Health reports for a CI, open the CI form in CMDB Workspace.
-   The legacy Application Service Dashboard on Core UI isn't supported in the Xanadu release. After upgrading, you can still access that legacy dashboard by using a previously created bookmark. You can also instead access the Application Services dashboard in CMDB Workspace from the Application services tile in the Insights view in CMDB Workspace.
-   The CMDB Integrations Dashboard on Core UI isn't supported in the Xanadu release. After upgrading, you can still access that legacy dashboard by using a previously-created bookmark.
-   All records that exist in the CMDB Health Result \[cmdb\_health\_result\] table before an update to Xanadu Patch 5, are deleted during the upgrade.

To access a legacy dashboard on an upgraded instance, navigate to **All** &gt; **Self-Service** &gt; **Dashboards** and then search for the dashboard.

## New in the Xanadu release

-   **[CMDB Workspace v7.6](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US):**
    -   Access a centralized location with a comprehensive view of CI details by using the new CI form in CMDB Workspace. The form shows the attributes \(key attributes are highlighted on a Summary page\), tags, resources, activities, relationships, related services, health state, performance indicators, and CMDB 360 data that is associated with the CI. While viewing, you can also modify many of those CI details. For information about all the details on a CI form, see [Manage CI details in CI Form](https://www.servicenow.com/docs/access?context=ci-form-cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    -   Access the Data Certification dashboard in CMDB Workspace. The Data Certification dashboard provides the insights about the data certification activities and progress, policies and tasks, reports about certification instances, charts that show the aging certification tasks, and group and individual workloads. For more information, see [Data Certification Dashboard](https://www.servicenow.com/docs/access?context=data-cert-dashboard-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
    -   [Create or manage a shared preset](https://www.servicenow.com/docs/access?context=unified-map-manage-shared-preset&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Save Unified Map filter settings as shared presets that any user on the team can access. This task requires the sn\_cmdb\_admin, sm\_admin, or admin role.
    -   [Access Unified Map from the main navigation panel](https://www.servicenow.com/docs/access?context=cmdb-workspace-unified-map&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). Access Unified Map from the main navigation panel by navigating to **All** &gt; **CMDB Workspace** &gt; **Unified Map**.
    -   Archival and destroy processes of certification policy related records, are now separated from those processes for records of all other policy types. This separation facilitates the extension of the retention period of certification policy records, as follows:
        -   The table cleanup rule for table CMDB Data Management Policy Executions \[cmdb\_data\_management\_policy\_execution\], which is stored in the Auto Flushes \[sys\_auto\_flush\] table, now excludes certification policy execution records from recurring cleanups.

            Retaining certification policy execution records instead of deleting them after 7 days is useful in situations where those records are needed for audits and are also useful for the Data Certification Dashboard, which is populated by these records.

        -   The Archive CMDB Data Management Tasks archive rule, that applied to all CMDB Data Manager policy execution records, now excludes certification policy records. At each archive run, this archive rule is configured to also automatically archive its related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] \(Archive Related Records\).
        -   The archive rule, Archive Certification Instances, is added to specifically archive certification policy execution records from the CMDB Data Management Policy Execution \[cmdb\_data\_management\_policy\_execution\] table. This new archive rule is configured to archive certification policy execution records 2 years after creation, and to destroy those records 7 years after they are archived.
        -   The archive rule, Archive Certification tasks, is added to specifically archive certification task records from the CMDB Data Management Task \[cmdb\_data\_management\_task table\].
        -   The archival of related records in table CMDB Data Management Certification Task To Document \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\] is now moved as an Archive Related Records entry from the Archive CMDB Data Management Tasks archive rule to the new Archive Certification tasks archive rule.
-   **[CMDB Health Dashboard](https://www.servicenow.com/docs/access?context=c_MonitorCMDBHealth&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The CMDB Health Dashboard is now built using UI Builder components and is fully integrated into the CMDB Workspace. When you select either of its views, it opens in CMDB Workspace. The CMDB Health Dashboard has a modernized look and feel of the Next Experience user interface

    CI health is now reported on CI forms within the CI Health tile in CMDB Workspace.

-   **[CSDM and the CMDB Data Foundations Dashboards](https://www.servicenow.com/docs/access?context=csdm-cmdb-foundations-dashboards&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Starting with version 4.0, the CSDM and the CMDB Data Foundations Dashboards store app is built using UI Builder components. You can also now access the CSDM Data Foundations Dashboard from Management tools in the Management view in CMDB Workspace.

-   **[CMDB Integrations Dashboard in the Next Experience user interface](https://www.servicenow.com/docs/access?context=cmdb-integ-dashboard&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The CMDB Integrations Dashboard has a modernized look and feel with the Next Experience user interface. Starting with Xanadu release, the CMDB Integrations Dashboard is automatically migrated to the Next Experience user interface. For more information on the Next Experience user interface, see [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

-   ****

    The ServiceNow® Now Assist for CMDB application brings generative AI to CMDB. The Now Assist for CMDB application provides the following skills:

    -   CI summarization: Shows CI details such as discovery and class, and tallies of records that are related to the CI such as incidents, alerts, and security vulnerabilities, directly on CI forms.
    -   Manage duplicate CIs: Guides you step-by-step through the process of reviewing de-duplication tasks, and then creating and running de-duplication templates to remediate tasks that you choose. As you respond to choices presented by the manage duplicate CIs skill, you receive clear guidance for what should be your next step in the remediation process. This skill also provides root cause analysis to help you prevent future generation of duplicate CIs.
-   ****

    The ServiceNow® Now Assist for Service Graph Connectors \(SGC\) application brings in generative AI capabilities to resolve issues within Service Graph Connectors. The Now Assist for SGC application provides the Service Graph Connector diagnosis skill. This skill enables you to troubleshoot issues in a failed import set associated with a Service Graph Connector.

-   **[Quick start tests for CMDB](https://www.servicenow.com/docs/access?context=quick-start-tests-cmdb&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    After upgrades and deployments of new applications or integrations, run quick start tests to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


## UI changes

-   **[Relationship Health Dashboard](https://www.servicenow.com/docs/access?context=t_ViewRelationshipsHealth&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The Relationship Health tab is no longer available on the CMDB Health Dashboard. Instead, you must access the Relationship Health Dashboard from the CMDB Workspace Home page by selecting the **Relationship Health Dashboard** link in the Quick links section.

    Aggregated relationship metrics appear as pie charts on the dashboard.

-   **[Setting up and configuring CMDB Health](https://www.servicenow.com/docs/access?context=c_CMDBHealthSetupandConfig&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The **CMDB Health settings** button on the CMDB Health Dashboard replaces the CMDB Health Dashboard jobs tab for configuring CMDB Health-related system properties, scheduled jobs, and KPIs and metrics.

-   **[CI health reporting](https://www.servicenow.com/docs/access?context=t_ViewCIHealth&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   The CI Health tile on CI forms has been expanded to include widgets with health scores of KPIs and metrics, as calculated by CMDB Health for the CI.
    -   The CI dashboard has been removed and the **Open in CMDB Workspace** button on CI forms replaces the **Dashboard** button to access CI health reporting in CMDB Workspace. This new button is available only to users with the sn\_cmdb\_user role.

## Changed in this release

-   **[Access changes for the sn\_cmdb\_editor and sn\_cmdb\_admin user roles](https://www.servicenow.com/docs/access?context=installed-with-cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   Starting with Xanadu Patch 9 \(zbooted or upgraded\), access has been reduced for the sn\_cmdb\_editor \(CMDB Editor\) and the sn\_cmdb\_admin \(CMDB Admin\) user roles which are used in [CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). The sn\_cmdb\_editor and sn\_cmdb\_admin user roles no longer have create, update, or delete access to records in the Configuration Item \[cmdb\_ci\] class.
    -   Starting with Xanadu Patch 10 \(zbooted or upgraded\), you must manually run the scheduled job '**Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the permissions that are necessary for performing some CMDB Workspace tasks.

        This scheduled job modifies user roles as follows:

        -   Updates the itil user role to no longer contain the sn\_cmdb\_editor user role, and updates the itil\_admin user role to no longer contain the sn\_cmdb\_admin user role.
        -   If those permissions don't exist, updates the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with create, update, and delete access to the Configuration Item \[cmdb\_ci\] class. For more information about the 'Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles' scheduled job, see [Remove sn\_cmdb\_admin from itil\_admin and sn\_cmdb\_editor from itil, and then add create/update/delete access to cmdb\_ci table for sn\_cmdb\_admin / sn\_cmdb\_editor \[KB2290506\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB2290506).
-   **[CMDB Health](https://www.servicenow.com/docs/access?context=c_CMDBHealth&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   Configuring and using CMDB Health is simplified by the removal of some concepts such as overall health scores.
    -   Sections on the CMDB Health Dashboard reporting on compliant CIs are clearly separated from report sections for non-compliant CIs that require your attention.
    -   Failure thresholds for KPIs and metrics enforce an upper limit of 100,000 to avoid excessive processing when a large number of CIs fail the specified metric tests.
    -   The CMDB Health Dashboard still shows non-compliance data that was gathered even if the process is stopped due to excessive failures so you can fix the specific failures already detected.
    -   CI health reporting is integrated into CI forms in CMDB Workspace.
-   **[CMDB Workspace store app](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   [CMDB 360](https://www.servicenow.com/docs/access?context=cmdb360-exp-cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US):
        -   Manage performance by filtering the data included in Coverage charts in the CMDB 360 dashboard in CMDB Workspace by principal class setting or by whether tables are within the CMDB hierarchy.
        -   Manage the scope of data processed by CMDB 360 by setting a maximum threshold for the number of multisource records per class and tracking those classes that exceed that threshold in a table so that those classes are excluded from future CMDB 360 calculations. You can override this exclusion to include selected classes even if they exceed the threshold.
    -   [Data Certification](https://www.servicenow.com/docs/access?context=data-cert-exp-cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

        When reviewing Data Certification tasks in CMDB Workspace, use a single click to select all the records associated with a task, to certify or fail the certification in bulk.

    -   [CI timeline in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

        When a CI timeline on the CI details pane in CMDB Workspace fails to load, the error message that appears now includes a link that you can select to go to the CI timeline in the base system.

-   **[CSDM and the CMDB Data Foundations Dashboards](https://www.servicenow.com/docs/access?context=csdm-cmdb-foundations-dashboards&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**
    -   Limit the performance impact of some of the CMDB and CSDM metrics such as the **CIs Processed via IRE** and **Business Application with Application Service Relationship** by adjusting the settings for triggering the system to automatically deactivate those metrics.
    -   Identify current and non-current metric data by viewing the **Updated** column in the list views of CMDB.
    -   Access the CSDM Data Foundations dashboard from the [Management view in CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace-mangmnt-view&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   **[Select a parent class in an IRE identification rule](https://www.servicenow.com/docs/access?context=t_CreateCIIdentificationRule&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Avoid the unnecessary creation of a duplicate CI by setting the **Search On Table** field in an identification rule to one of the parent classes of the current class. When Identification and Reconciliation \(IRE\) identifies a CI in a parent class that matches a CI in the payload, IRE updates that CI with the details from the payload without creating a duplicate CI.

-   **[Improved migration and ongoing sync of CSDM life-cycle data](https://www.servicenow.com/docs/access?context=csdm-life-cycle-standard-values&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The one-time operation aligns CSDM life-cycle values in asset and CI tables. After the initial alignment, business rules can run on regular schedules to ensure that life-cycle values for the asset, CI, and IBI tables remain aligned. Using standard life-cycle values significantly improves data accuracy to help optimize value for many ServiceNow AI Platform applications.

-   **[Application Services dashboard](https://www.servicenow.com/docs/access?context=app-service-dashboard&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Internal queries on the Application Services dashboard that filters for application services now checks not only for all the records in the Application Service \[cmdb\_ci\_service\_auto\] class, but for those records in which the value of **Service classification** is **Application Service**.


## Removed in this release

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

## Deprecations

-   Starting with the Xanadu release, the Data Certification plugin \(com.snc.certification\_v2\) is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. The [CMDB Workspace store app](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB0867184]) article in the Now Support knowledge base.
-   ServiceNow hosted Service Graph Connector for ExtraHop is now deprecated and no longer supported or available for new activation. Service Graph Connector for ExtraHop provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

CMDB is a ServiceNow AI Platform feature that is active by default.

## Related ServiceNow applications and features

-   **[Common Service Data Model \(CSDM\)](https://www.servicenow.com/docs/access?context=csdm-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Common Service Data Model \(CSDM\) provides prescriptive guidelines for service modeling within CMDB and is the standard for all ServiceNow products that use the CMDB. CSDM provides a framework for mapping data from your IT services and other products to the CMDB. Following the CSDM framework helps ensure that the required data for your ServiceNow application maps correctly to the appropriate CMDB tables.

-   **[Service Graph Connectors](https://www.servicenow.com/docs/access?context=cmdb-third-party-integrations&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Use predefined ServiceNow® Service Graph connectors to import data from third-party applications, such as Microsoft SCCM, into your CMDB. In addition, you can use the [IntegrationHub ETL](https://www.servicenow.com/docs/access?context=integrationhub-etl&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) store app to create and manage custom ETL transform maps so that you can integrate third-party data into the CMDB without compromising its integrity.

-   **[CMDB Workspace](https://www.servicenow.com/docs/access?context=cmdb-workspace&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Use the CMDB Workspace store app to search, explore, and gain insights into the CMDB. The CMDB Workspace is a store app that provides a central place for working with the CMDB. In the CMDB Workspace, you can examine health and recent activity related to CMDB, and access various CMDB dashboards and tools to support tasks in your organization.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

