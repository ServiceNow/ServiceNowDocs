---
title: CMDB glossary
description: Texts associated with CMDB, such as UI text and core CMDB documentation, use many terms that are important to understand in the context of CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Reference, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB glossary

Texts associated with CMDB, such as UI text and core CMDB documentation, use many terms that are important to understand in the context of CMDB.

## CMDB hierarchy

The CMDB hierarchy is a structured, tree-like, data store where all data related to CMDB is stored, used, and managed. The following terms are best explained in the context of the CMDB hierarchy:

-   **Class/Table**

    Stores data about a specific IT physical, logical, or conceptual item, such as a computer, in your organization. The CMDB hierarchy contains many classes where each class stores a set of similar IT infrastructure items that share similar attributes. Each class in the CMDB hierarchy has a set number of attributes that are common for the IT items stored in that class, such as CPU of a computer. A class consists of rows, where each row represents a single IT item referred to as a Configuration Item \(CI\). Initially, a class has no rows until actual IT items are stored in the class using one of the methods of populating the CMDB. The number of rows \(CIs\) in a class dynamically changes, reflecting on the number of IT items of that type in your organization. A class can be specified as independentor dependent, which determines the dependency of the class CIs on one another within the CMDB hierarchy.

-   **Attribute/Column**

    A class table is defined by a set number of columns, each designed for storing a specific attribute of IT items using a specific data type such as string or integer. A column in a class table contains the attribute values of actual IT items.

-   **Configuration Item \(CI\)**

    A basic unit of data, stored as a row in a class, and that represents an actual IT infrastructure item in your organization, such as a computer. The number of rows in a class is the number of CIs of that class. All CIs of a specific class, have the same collection of columns, where each column holds the actual value of the respective attribute for the IT item. For example, the computer class has an operating system attribute, therefore a Computer CI has an operating system attribute, which can have the value of Windows 10.0 for a specific computer in your organization. Any CI that is being added to a class has all of the class attributes where you can then enter the actual values of the CI.

-   **CI class/CI type**

    The actual table name in the instance database that a CI belongs to. CI type is a friendly name for a CI's class, such as computer, router, or printer.

-   **Relationship**

    Type of connection between a CI and either another CI, a user, or a group. Relationship types are defined twice, once from the perspective of the child CI and once from the parent CI's perspective. For example, a parent CI that powers a child CI uses the relationship type Powers::Is Powered By.

-   **Parent class/Child class**

    Each class in the CMDB hierarchy is created as a child of another class \(parent class\), creating a parent-child relationship between classes. A child class automatically derives all the columns specified at the parent class, as well as some other feature-specific definitions. In addition to the derived attributes, you can add to the child class unique attributes which don't exist at the parent class.


The CMDB hierarchy is the entire collection of pre-defined and user-defined classes that serve as a detailed map of all IT items in your organization, including their attributes and the relationships between them. Throughout the CMDB hierarchy, classes derive attributes from each other and are connected by relationships to form a web of classes in a tree-like structure. The class at the top of the CMDB hierarchy is the Configuration Item \[cmdb\_ci\] class, which holds the basic attributes that are common to all classes in the CMDB hierarchy. Hundreds of classes are fully defined in the base system and are ready to be populated with CIs that represent actual IT items in your environment.

## Key terms

The following terms are key in CMDB:

-   **Configuration Management Database \(CMDB\)**

    ServiceNow® application that stores the logical configuration of your organization's infrastructure and gives you full visibility into your IT environment to support needed services. This application lets you monitor your network and support stability and best performance.

-   **Dependent CI**

    CIs that depend on a relationship to another CI and can't exist on their own in the absence of the dependent relationship. A class can be independent or dependent, which determines the dependency or independence of the class CIs.

-   **Independent CI**

    CIs, such as Server CIs, which exist on their own and aren't dependent on any other CIs.

-   **Principal Class**

    Class who's CIs are included in various CI list views. A Principal Class designation is used to restrict the list of CIs in list views across CMDB features, to only specific classes that you need.

    For more information, see [Update the list of classes in the Principal Class filter](../task/update-principal-class-filter.md).

-   **Related table**

    A table that isn't part of the CMDB hierarchy but which still qualifies as CMDB data, such as the Serial Number \[cmdb\_serial\_number\] table. A related table doesn't derive from the Configuration Item \[cmdb\_ci\] table, but has at least one column that references a CMDB CI. Information about related tables is stored in the Related Entries \[cmdb\_related\_entry\] table.

-   **Duplicate CI**

    One or more CIs in which key attributes have identical values and can occur, for example, when multiple discovery sources attempt to import the same CI. Duplicate CIs in the CMDB interfere with its integrity and efficiency and therefore, as a general guideline, should be avoided.

    For more information, see [Detecting duplicate CIs](../concept/id-detect-dup-ci.md) and [Duplicate CIs remediation](../concept/de-duplication-tasks.md).

-   **Orphan CI**

    In the context of CMDB Health, an orphan CI is a CI that matches CMDB Health orphan rules. Orphan CIs are typically CIs that are missing key attribute values, or key relationships and therefore, as a general guideline, must be remediated or removed.

    In the context of Data Manager, an orphan dependent CI belongs to a dependent class, and is missing the dependent relationship.

    Some scenarios that involve related tables, can result in orphan CIs in related tables. A CI in a related table can, for example, become orphan if the referenced CI in the CMDB is deleted.

    For more information about orphan CIs in the context of CMDB Health, see [CMDB Health KPIs and metrics](r_CMDBHealthMetrics.md).

    For more information about orphan dependent CIs, see [Dependent CIs management](../concept/manage-dependent-ci.md).

-   **Related list**

    Information about additional components contained by a CI, such as disk drives on a server and the rules that control the behavior of a network router.

    A related list can show, for example, active incidents, problems, changes, and outages against the CI. For example, a router can have several Related Lists affected by these filter conditions, including routing rules, disk drives, interfaces, and network adapters. Only those components found during the last Discovery appear in these Related Lists.

-   **CMDB group**

    Collection of CIs that lets you apply actions collectively to all the CIs that are members in the group. There are several methods for populating a CMDB group with CI members. Depending on the group type, you can populate a CMDB group by manually adding individual CIs, selecting saved CMDB queries, or building encoded queries in the CMDB group itself. CI members in a CMDB group of type 'health' can be monitored by CMDB Health, and a CMDB group of type 'CMDB Workspace' appears in CMDB Workspace views.

    For more information, see [CMDB groups](../concept/cmdb-groups.md#).


## Features, tools, store apps

The following terms are for essential features and tools that CMDB provides, some of which are implemented as store apps:

-   **CMDB Identification and Reconciliation \(IRE\)**

    Feature that provides a centralized framework for identifying and reconciling data from different data sources as the data is being imported into the CMDB. Using IRE helps maintain the integrity of the CMDB and some non-CMDB tables when multiple data sources are used to create and update CI records. IRE identification processes extensively use CIs dependency classification.

    For more information, see [CMDB Identification and Reconciliation \(IRE\)](../concept/c_CMDBIdentifyandReconcile.md).

-   **CMDB Health**

    Feature that lets you monitor the health of the CMDB by using health indicators such as duplicate CIs, required CI fields, and audits, and that provides a framework for applying standardized CI remediation. CMDB Health evaluates and aggregates those health indicators into health scores at the class, health group, and service levels, which are then shown on dashboards.

    For more information, see [CMDB Health](../concept/c_CMDBHealth.md).

-   **CMDB Query Builder**

    Tool that lets you build complex infrastructure and service queries that span multiple CMDB classes, non-CMDB tables, and that involve many CIs that are connected by different relationships. Query elements are represented by UI building blocks that you connect and structure on a canvas to query the CMDB and Service Mapping.

    For more information, see [CMDB Query Builder](../concept/cmdb-query-builder-landing-page.md).

-   **CMDB Data Manager**

    An essential comprehensive and integrated solution where you can create, publish, and manage policies that reflect organizational needs for data management. CMDB Data Manager supports bulk management of CI life cycle operations such as deletion, archival, and attestation. The CMDB Data Manager lets you automate and govern those CI life cycle operations to help maintain the CMDB in a healthy and reliable operational state.

    For more information, see [Working with CMDB Data Manager](../concept/cmdb-data-management.md).

-   **CI Class Manager**

    Tool where you can centrally view, create, and edit basic class definitions. You can also view, create, or edit class settings that are used in core CMDB functions such as identification, reconciliation, and essential features such as CMDB Health.

    For more information, see [CI Class Manager](ci-class-manager-landing-page.md).

-   **CMDB Workspace**

    A central, comprehensive, and modernized solution that provides access to a wide range of applications, features, and key CMDB dashboards and tools to support tasks in your organization. CMDB Workspace lets you manage, search, explore, and examine the health state and recent activities in CMDB. CMDB Workspace views and dashboards show high-priority tasks that require your immediate attention, which were generated by various CMDB features such as CMDB Health.

    For more information, see [CMDB Workspace store app](../concept/cmdb-workspace.md).

-   **Service Graph Connectors**

    Collection of pre-defined integrations that ingest data into the CMDB from third-party sources such as Tanium, Jamf, and Microsoft SCCM. Service Graph Connectors help maintain the quality and consistency of third-party data in your CMDB by verifying that the imported data is mapped correctly into your CMDB as specified by the Common Service Data Model \(CSDM\). Service Graph Connectors are delivered as store apps.

    For more information, see [Service Graph Connectors](../concept/cmdb-sgc-available.md).

-   **CMDB CI Class Models**

    Store app that adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. You can use the added classes as any other CMDB class in the base system. Applications such as Discovery and Service Mapping can use these class extensions to populate CIs and discover various technologies and software.

    For more information, see [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).

-   **CSDM and the CMDB Data Foundations Dashboards**

    Store app containing a set of dashboards, complementing each other that together provide insights into key foundational metrics of your CMDB and Common Service Data Model \(CSDM\). In addition, these dashboards provide recommendations to verify that the CMDB and CSDM are properly configured for optimal usage and to mitigate any potential risks.

    For more information, see [Monitor health in CSDM and CMDB Data Foundations Dashboards](../concept/csdm-cmdb-foundations-dashboards.md).


