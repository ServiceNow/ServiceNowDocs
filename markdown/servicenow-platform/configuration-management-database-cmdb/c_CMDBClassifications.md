---
title: CMDB classifications and class dependency
description: CMDB classifications are groups of CIs that share attributes and are stored in their own class table. Classifications let administrators to define a class hierarchy for the CIs within the CMDB.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB classifications and class dependency

CMDB classifications are groups of CIs that share attributes and are stored in their own class table. Classifications let administrators to define a class hierarchy for the CIs within the CMDB.

A CI class refers to the actual table name in the instance database. In that context, 'CI type' is a friendly name that a CI is known by, such as computer, router, or printer.

One of the characteristics of a CMDB class is its dependency on other classes. A class can be independent or dependent, which determines the dependency or independence of the class CIs.

-   **Independent CIs**

    CIs from an independent class, such as Linux Server CIs, have their own identity, exist by themselves, and aren't dependent on any other CIs.

-   **Dependent CIs**

    CIs from a depended class have relationships with CIs from other classes and exist meaningfully only if these relationships exist. Dependent CIs don't exist on their own in the absence of the dependent relationship. For example:

    -   Network Adapter CIs don't exist meaningfully without the Hardware CIs that contain them.
    -   Application CIs don't exist on their own without the Server CI they are hosted on.

Identification processes in the [Identification and Reconciliation engine \(IRE\)](ire.md) CMDB feature extensively use CIs dependency classification. To find out the dependency classification of a class, open the Identification Rule page for a class in [CI Class Manager](../task/t_CreateCIIdentificationRule.md). To establish CI dependency, use the CI Class Manager to specify [dependent relationship rules](create-dependent-relationship.md#) for a CI class.

For more information, see [Identification rules](c_IdentificationRules.md).

-   **[Dependent CIs management](manage-dependent-ci.md)**  
A life cycle update for a CI affects its dependent CIs. For example, when the CI that a dependent CI depends on is deleted, the dependent CI becomes orphan with no further use. To maintain the integrity and health of the CMDB, the system applies cascade-cleanup processes to dependent CIs that are affected by a life cycle update.
-   **[CMDB record types](../reference/r_CMDBRecordTypes.md)**  
The CMDB contains the following major record types.
-   **[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)**  
Related lists in CI records display additional components contained by that CI, such as disk drives on a server and the rules that control the behavior of a network router.
-   **[Create a CI class](../task/t_CreateCIType.md)**  
Create a CI class \(table\) that is an extension of an existing CI class. Then create identification and reconciliation rules for the new class.
-   **[Reclassify a CI](../task/t_ManuallyReclassifyCI.md)**  
You can upgrade, downgrade, or switch the class of a CI by modifying its **Class** attribute.
-   **[Delete CIs](../task/delete-class-records-ci-class-mgr.md)**  
You can use the CI Class Manager to delete CIs that are no longer needed.
-   **[View and edit class definitions and metadata](../task/t_ViewTableDefinitions.md)**  
Use the CI Class Manager as a central location to explore the CMDB class hierarchy, CI table definitions, and class CIs. View the details of each table such as its label and fields, relationships, and all related metadata definitions.
-   **[Update the list of classes in the Principal Class filter](../task/update-principal-class-filter.md)**  
Manage the list of classes that are included in the Principal Class filter to restrict the CIs that appear in CIs list views to only specific classes that you need. You can add or remove CMDB classes from the Principal Class filter.

**Parent Topic:**[Exploring CMDB](explore-cmdb.md)

