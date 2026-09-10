---
title: Configuration Management Database \(CMDB\) release notes
description: The ServiceNow Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.The ServiceNow Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.The ServiceNow Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.The ServiceNow Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.The ServiceNow Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 7
---

# Configuration Management Database \(CMDB\) release notes

The ServiceNow® Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.

## About Configuration Management Database \(CMDB\)

-   Use CMDB success advisor to achieve Data Foundations, Hardware Asset Management \(HAM\), and Software Asset Management \(SAM\) target outcomes.
-   Users with CMDB related roles can perform all CMDB functions as access to CMDB tables is no longer restricted to users with elevated privileges.
-   Switch into using the Service Graph Workspace instead of CMDB Workspace. The Service Graph Workspace provides access to data such as company, location, user and CMDB. The new workspace is specifically organized to help CMDB administrators, data owners, and analysts work efficiently with the CMDB.
-   Simplify duplicate CI remediation by using the ServiceNow Otto for CMDB remediation option in the Duplicate CI Remediator, and using the automatically-filled remediation options.
-   Use Dynamic Identification and Reconciliation Engine \(IRE\) that eliminates the need for manually-created identification rules and reduces incorrect detection of duplicate CIs in the CMDB.
-   Protect sensitive information with domain separation that supports key CMDB tables such as the Key Value \[cmdb\_key\_value\] table.

See [Configuration Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/manage-cmdb.md) for more information.

## Activation and other requirements

-   **Activation information**

    Configuration Management Database \(CMDB\) is a ServiceNow AI Platform feature that is active by default.

    The Australia release includes an installation of CMDB Workspace. However, you can download the latest version of CMDB Workspace store app \(which includes Service Graph Workspace\) so that you can use its latest features in your Australia instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

-   **Upgrade information**

    Due to changes in the Configuration Item \[cmdb\_ci\] table, if you're upgrading to Australia, you might experience an increased upgrade time. To learn more about this change and reducing its impact, see the [Increased Australia Upgrade Time due to cmdb\_ci composite index addition \[KB2588894\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2588894) article in the Now Support Knowledge Base.

    If you're upgrading from Xanadu or Yokohama directly to the Australia release, you must run the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job to correctly configure some user roles, such as CMDB Admin and CMDB Editor. For more information about this scheduled job and its use, see the [CMDB Zurich release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/cmdb-rn.md).

    The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see [Configuring read-only security options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/read-only-option.md).


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-capabilities-rn-landing.md)

## September 2026

The ServiceNow® Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.

### What's new

-   **CMDB success advisor summary on the Governance view**

    Review a ServiceNow Otto for CMDB-generated summary of the top data quality issues for Data Foundations, Hardware Asset Management \(HAM\), and Software Asset Management \(SAM\), directly on the Governance view in Service Graph Workspace. Select **View remediations** or **View insights** on a card to open the corresponding dashboard in CMDB success advisor.


### What's changed

-   **Cleaner category grouping for Data Foundations advisor**

    The CI class categories filter and the Set principal classes dialog box hide Data Model Navigator child categories that are already nested under a parent category, so the top-level list doesn't repeat categories.


## June 2026

The ServiceNow® Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.

### What's new

-   **[CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-sa-landing-page.md)**

    Use CMDB success advisor to achieve Data Foundations, HAM, and SAM target outcomes. The store app monitors and improves CMDB data quality through dedicated dashboards for principal CI classes, hardware assets, and software installs. Dashboards provide targeted recommendations and remediation actions to address data gaps and are accessible directly from the Service Graph Workspace.


## Australia Early Availability

The ServiceNow® Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.

### What's new

-   **[CMDB Workspace v9.0 \(including Service Graph Workspace\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sg-workspace.md)**
    -   Use Service Graph Workspace which is included in the CMDB Workspace store app, to view data, such as company, location, user, and CMDB data, using panels and dashboards. The Service Graph Workspace is specifically organized to help CMDB administrators, data owners, and analysts work with the CMDB. You can search the CMDB in Service Graph Workspace without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation.
    -   Configure de-duplication remediation processes for related tables to turn off automated workflows, such as ignoring errors and skipping business rules, that might block referenced duplicate CIs from updating to the main CI. Skipping automated workflows for related tables enables de-duplication tasks, which would otherwise fail, to complete successfully. For more information, see [Effects on related tables \(such as Change\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/de-duplication-tasks.md) and [Turn off workflows of related tables during remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dedup-ci-disable-workflow.md).
-   **[Simplify resolving de-duplication tasks by using a ServiceNow Otto for CMDB skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/reconcile-dup-task.md)**

    Use the De-duplication task resolution assistant skill in the Duplicate CI Remediator to use preselected remediation options instead of manually making selections. An AI agent preselects the options to resolve the task, such as the choice of the main CI. Then, before initiating the remediation, you can review all suggested options with supported reasoning.

    To use the De-duplication task resolution assistant skill, you must install the ServiceNow Otto for CMDB version v3.0.


## Australia

The ServiceNow® Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.

### What's new

-   **[Dynamic IRE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dynamic-ire.md)**

    Use Dynamic IRE to accurately identify CIs across multiple data sources, and by so, minimize duplicate CIs. Dynamic IRE is applicable only to the Hardware \[cmdb\_ci\_hardware\] class and its descending class, using a dynamic identification process which eliminates the need to manually create and maintain identification rules.

-   **[Quick start tests for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/quick-start-tests-cmdb.md)**

    Run quick start tests after upgrades and deployments of new applications or integrations to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


### What's changed

-   **[Elevated user roles are no longer required for CMDB tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/manage-cmdb.md)**

    Access to CMDB tables is no longer restricted to users with elevated privileges. Instead, for improved security, users with access privileges that are trimmed to CMDB features can complete any administrative or end-user CMDB task:

    -   CMDB tables that required the admin or itil\_admin roles are now also accessible to the sn\_cmdb\_admin user role.
    -   CMDB tables that required the itil role are now also accessible to the sn\_cmdb\_editor user role.
-   **[Automatically generate de-duplication tasks for lookup and related tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/id-detect-dup-ci.md)**

    Configure IRE to automatically generate de-duplication tasks for specific lookup or related tables during the identification process. You can then process those de-duplication tasks to remediate any duplications.

-   **[Remediate duplicate related items in lookup tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/id-detect-dup-ci.md)**

    Configure IRE to create de-duplication tasks for duplicate related items in a lookup table, detected during a lookup-based identification. Sort which duplicates do or don't require remediation by configuring the system property **glide.identification\_engine.lookup\_match.create\_duplicate\_task\_ci.enabled**. For more information, see [Detecting duplicate CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/id-detect-dup-ci.md#section_unn_yjr_xgc).

-   **[Domain separation for key CMDB tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainSeparationSetup.md)**

    The following tables now support domain separation on instances which are configured with domain separation:

    -   Key Value \[cmdb\_key\_value\]
    -   Printer Instance \[cmdb\_print\_queue\_instance\]
    -   Software Instance \[cmdb\_software\_instance\]
    -   Client Access \[samp\_client\_access\]
    -   Oracle Options \[samp\_oracle\_options\]
    Domain separation can help protect sensitive information by supporting domain-specific data segregation.

    For more information about domain separation and how to activate it, see [Domain separation setup and administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainSeparationSetup.md).

-   **[CMDB Query Builder engine execution modes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/query-builder-engine-execution-mode.md)**

    The CMDB Query Builder expanded its support for various types of query structures that can run in V2 engine mode. Also, the performance of running queries in V2 mode is improved. Query structures that aren't supported include related list conditions, NOT operators combined with filters, certain Service Mapping relationships, and OR operators unless explicitly enabled by the **glide.cmdb.query.or\_execution\_mode** system property.


### What's deprecated or removed

The Multisource Report Builder has been removed. Use CMDB 360 in CMDB Workspace or in Service Graph Workspace to generate reports for multisource data. For more information, see [CMDB 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multisource-cmdb.md).

### Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    Service Graph Workspace - Content \(sn\_cmdb\_sgw\_conten\): Provides the contexts definitions and the quick class filters, and enables the associated option to explore data by contexts in the Search and Explore view in Service Graph Workspace.

-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release:

    Service Graph Connector for OpenTelemetry \(com.snc.cmdb.lightstep\_integration\): Planned for deprecation in C. There is no replacement for this application.


