---
title: Configuration Management Database \(CMDB\) release notes
description: The ServiceNow Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
---

# Configuration Management Database \(CMDB\) release notes

The ServiceNow® Configuration Management Database \(CMDB\) application stores data about the infrastructure of your organization. CMDB was enhanced and updated in the Australia release.

## CMDB highlights for the Australia release

-   Users with CMDB related roles can perform all CMDB functions as access to CMDB tables is no longer restricted to users with elevated privileges.
-   Switch into using the Service Graph Workspace instead of CMDB Workspace. The Service Graph Workspace provides access to data such as company, location, user and CMDB. The new workspace is specifically organized to help CMDB administrators, data owners, and analysts work efficiently with the CMDB.
-   Simplify duplicate CI remediation by using the Now Assist for CMDB remediation option in the Duplicate CI Remediator, and using the automatically-filled remediation options.
-   Use Dynamic Identification and Reconciliation Engine \(IRE\) that eliminates the need for manually-created identification rules and reduces incorrect detection of duplicate CIs in the CMDB.
-   Protect sensitive information with domain separation that supports key CMDB tables such as the Key Value \[cmdb\_key\_value\] table.

See Configuration Management for more information.

## Important information for upgrading CMDB to Australia

Due to changes in the Configuration Item \[cmdb\_ci\] table, if you're upgrading to Australia, you might experience an increased upgrade time. To learn more about this change and reducing its impact, see the [Increased Australia Upgrade Time due to cmdb\_ci composite index addition \[KB2588894\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2588894) article in the Now Support Knowledge Base.

If you're upgrading from Xanadu or Yokohama directly to the Australia release, you must run the **Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** scheduled job to correctly configure some user roles, such as CMDB Admin and CMDB Editor. For more information about this scheduled job and its use, see the [CMDB Zurich release notes](https://www.servicenow.com/docs/bundle/zurich-release-notes/page/release-notes/now-platform-capabilities/cmdb-rn.html).

The Australia release introduces enhanced protections for read‑only fields across the ServiceNow AI Platform®. These changes include a new “read\_only\_option” field with granular control levels, including “strict\_read\_only” and “client\_script\_modifiable". The changes occur in the back end and maintain backward‑compatible behavior. This update helps strengthen your instance security while preserving the flexibility you need. Refer to [KB2718122](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2718122) for additional technical details on how to identify affected fields and adjust their settings. For more information about granular read-only security options, see Configuring read-only security options.

## New in the Australia release

-   **CMDB Workspace v8.0:**

    Create a CI with a lookup identifier entry that contains mandatory attributes in the CMDB Workspace. When you select a lookup identifier entry on the Required attributes page, you can set those mandatory attribute values for proper IRE processing. For more information, see Create a CI manually in CMDB Workspace.

-   **CMDB Workspace v9.0:**
    -   Use the Service Graph Workspace to view data, such as company, location, user, and CMDB data, using panels and dashboards. The Service Graph Workspace is specifically organized to help CMDB administrators, data owners, and analysts work with the CMDB. You can search the CMDB in Service Graph Workspace without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation.
    -   Configure de-duplication remediation processes for related tables to turn off automated workflows, such as ignoring errors and skipping business rules, that might block referenced duplicate CIs from updating to the main CI. Skipping automated workflows for related tables enables de-duplication tasks, which would otherwise fail, to complete successfully. For more information, see Effects on related tables \(such as Change\) and Turn off workflows of related tables during remediation.
-   **Dynamic IRE**

    Use Dynamic IRE to accurately identify CIs across multiple data sources, and by so, minimize duplicate CIs. Dynamic IRE is applicable only to the Hardware \[cmdb\_ci\_hardware\] class and its descending class, using a dynamic identification process which eliminates the need to manually create and maintain identification rules.

-   **Simplify resolving de-duplication tasks by using a Now Assist for CMDB skill**

    Use the De-duplication task resolution assistant skill in the Duplicate CI Remediator to use preselected remediation options instead of manually making selections. An AI agent preselects the options to resolve the task, such as the choice of the main CI. Then, before initiating the remediation, you can review all suggested options with supported reasoning.

    To use the De-duplication task resolution assistant skill, you must install the Now Assist for CMDB version v3.0.

-   **Quick start tests for CMDB**

    Run quick start tests after upgrades and deployments of new applications or integrations to verify that CMDB works as expected. If you customized CMDB, copy the quick start tests and configure them for your customizations.


## Changed in this release

-   **Elevated user roles are no longer required for CMDB tasks:**

    Access to CMDB tables is no longer restricted to users with elevated privileges. Instead, for improved security, users with access privileges that are trimmed to CMDB features can complete any administrative or end-user CMDB task:

    -   CMDB tables that required the admin or itil\_admin roles are now also accessible to the sn\_cmdb\_admin user role.
    -   CMDB tables that required the itil role are now also accessible to the sn\_cmdb\_editor user role.
    For more information, see the [CMDB Granular Role EPIC changes \[KB0561055\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0561055) article in the Now Support Knowledge Base.

-   **Automatically generate de-duplication tasks for lookup and related tables**

    Configure IRE to automatically generate de-duplication tasks for specific lookup or related tables during the identification process. You can then process those de-duplication tasks to remediate any duplications.

-   **Remediate duplicate related items in lookup tables**

    Configure IRE to create de-duplication tasks for duplicate related items in a lookup table, detected during a lookup-based identification. Sort which duplicates do or don't require remediation by configuring the system property **glide.identification\_engine.lookup\_match.create\_duplicate\_task\_ci.enabled**. For more information, see Detecting duplicate CIs.

-   **Domain separation for key CMDB tables**

    The following tables now support domain separation on instances which are configured with domain separation:

    -   Key Value \[cmdb\_key\_value\]
    -   Printer Instance \[cmdb\_print\_queue\_instance\]
    -   Software Instance \[cmdb\_software\_instance\]
    -   Client Access \[samp\_client\_access\]
    -   Oracle Options \[samp\_oracle\_options\]
    Domain separation can help protect sensitive information by supporting domain-specific data segregation.

    For more information about domain separation and how to activate it, see Domain separation setup and administration.

-   **CMDB Query Builder engine execution modes**

    The CMDB Query Builder expanded its support for various types of query structures that can run in V2 engine mode. Also, the performance of running queries in V2 mode is improved. Query structures that aren't supported include related list conditions, NOT operators combined with filters, certain Service Mapping relationships, and OR operators unless explicitly enabled by the **glide.cmdb.query.or\_execution\_mode** system property.


## Removed in this release

The Multisource Report Builder has been removed. Use CMDB 360 in CMDB Workspace or in Service Graph Workspace to generate reports for multisource data. For more information, see CMDB 360.

## Activation information

Configuration Management Database \(CMDB\) is a ServiceNow AI Platform feature that is active by default.

The Australia release includes an installation of CMDB Workspace. However, you can download the latest version of CMDB Workspace store app \(which includes Service Graph Workspace\) so that you can use its latest features in your Australia instance. For more information, visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    Service Graph Workspace - Content \(sn\_cmdb\_sgw\_conten\): Provides the contexts definitions and the quick class filters, and enables the associated option to explore data by contexts in the Search and Explore view in Service Graph Workspace.

-   **Plugins planned for deprecation**

    The following plugins are planned for deprecation in a future release:

    Service Graph Connector for OpenTelemetry \(com.snc.cmdb.lightstep\_integration\): Planned for deprecation in C. There is no replacement for this application.


## Related ServiceNow applications and features

-   **Common Service Data Model \(CSDM\)**

    Common Service Data Model \(CSDM\) provides prescriptive guidelines for service modeling within CMDB and is the standard for all ServiceNow products that use CMDB. CSDM provides a framework for mapping data from your IT services and other products to CMDB. Following the CSDM framework helps confirm that the required data for your ServiceNow application maps correctly to the appropriate CMDB tables.

-   **Service Graph Connectors**

    Use predefined ServiceNow® Service Graph Connectors to import data from third-party applications, such as Microsoft SCCM, into your CMDB. In addition, you can use the IntegrationHub ETL store app to create and manage custom ETL transform maps so that you can integrate third-party data into CMDB without compromising its integrity.

-   **CMDB Workspace store app**

    Use the CMDB Workspace store app to search, explore, and gain insights into CMDB. The CMDB Workspace is a store app that provides a central place for working with CMDB. In CMDB Workspace you can examine the health and recent activity related to CMDB, and access various CMDB dashboards and tools to support the tasks in your organization.

-   **Now Assist for Configuration Management Database \(CMDB\)**

    Use ServiceNow® Now Assist for CMDB to improve the quality of CMDB data, get help as you search the CMDB, troubleshoot issues with Service Graph Connector import sets, remediate duplicate CIs, manually create CIs, and view the comprehensive summaries for CIs. For release notes, see [Now Assist for Configuration Management Database \(CMDB\) release notes](now-assist-cmdb-rn.md).


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](now-platform-capabilities-rn-landing.md)

