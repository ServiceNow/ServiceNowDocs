---
title: Components and process of Identification and Reconciliation
description: The CMDB Identification and Reconciliation functionality is supported by the Identification and Reconciliation engine \(IRE\), rules, and tasks. Identification rules, reconciliation rules, IRE data source rules, de-duplication tasks, and reclassification tasks determine how IRE identifies and reconciles CI.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Explore, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components and process of Identification and Reconciliation

The CMDB Identification and Reconciliation functionality is supported by the Identification and Reconciliation engine \(IRE\), rules, and tasks. Identification rules, reconciliation rules, IRE data source rules, de-duplication tasks, and reclassification tasks determine how IRE identifies and reconciles CI.

## Concepts and Components of Identification and Reconciliation

-   **Identification**

    Process of uniquely identifying CIs, to determine if a CI already exists in the CMDB or if it is a newly discovered CI that must be added to the CMDB. Identification processes rely on [identification rules](../task/t_CreateCIIdentificationRule.md), or on unique IDs for CIs that data sources can provide.

-   **Reconciliation**

    Process of reconciling CIs and CI attributes by allowing only designated authoritative data sources to write to the CMDB at the CI table and attribute level. The CMDB is updated in real time as records are being processed. There is no staging area to verify the reconciliation activities before they are committed. Reconciliation processes rely on [reconciliation rules](create-reconciliation-rule.md#) and [IRE data source rules](../task/create-ire-data-source-rule.md).

    Reconciliation is required only for update operations, when the identification process identifies a CI in the CMDB that matches an incoming CI in the payload. When IRE inserts a new CI, reconciliation is not applied.

-   **De-duplication tasks**

    If the instance encounters duplicate CIs during the Identification and Reconciliation process, it groups each set of duplicate CIs into a [de-duplication task](../task/t_ResolveDeDuplicationTask.md). Review the information in these tasks to see how it was determined that these CIs are duplicates.

-   **Reclassification tasks**

    During the CI identification process, a matched CI might need to be upgraded, downgraded, or switched to another CI class. If automatic reclassification is disabled, then the system generates a [reclassification task](c_CIReclassification.md#). Review the information in these tasks, and decide whether a manual reclassification of the CI is appropriate.

-   **APIs**

    The Identification and Reconciliation APIs are a centralized set of APIs that can be used with different sources of data such as Discovery, Monitoring, or Import Sets. You can use it to enforce Identification and Reconciliation before data is stored in the CMDB. Data sources do not directly write to the CMDB. Instead, they call APIs first to ensure that the data being written does not introduce inconsistencies.

    Identification engine APIs are accessible in scoped apps. The Configuration Management For Scoped Apps \(CMDB\) plugin \(com.snc.cmdb.scoped\) allows a scoped app in scripts to use the prefix 'sn\_cmdb.IdentificationEngine.&lt;method&gt;' to access identification engine APIs. The Configuration Management For Scoped Apps \(CMDB\) plugin is activated in base systems.

    -   [createOrUpdateCI\(\)](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US): A scriptable API that creates or updates a CI based on identification and reconciliation rules.
    -   [identifyCI\(\)](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US): Similar to the **createOrUpdateCI** API, but does not commit the result to the database. Use this API with a given payload to find out if the identification engine will perform insert or update operations, without committing the operation.
    -   [CreateOrUpdateCIEnhanced\(\)](https://www.servicenow.com/docs/access?context=IdentificationEngineScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)​: A scriptable API that provides the functionality of enhanced IRE features such as partial payload, partial commit, incomplete payload, and deduplication of payload items. You can select the enhanced features to use. However, if you enable partial payloads, then deduplication of payload items and partial commit are automatically enabled.
    -   [identifyCIEnhanced](https://www.servicenow.com/docs/access?context=c_IdentEngineScriptAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US): Similar to the **createOrUpdateCIEnahnced** API, but does not commit the result to the database. Use this API with a given payload to find out if the identification engine will perform insert or update operations, without committing the operation.
    -   [CMDBTransformUtil](https://www.servicenow.com/docs/access?context=c_CMDBTransformUtilAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US): An API to be used exclusively with Import Sets to [apply Identification and Reconciliation processes to data imported by Import Sets](identification-import-sets.md).

Predefined identification are included for many of the tables in the base system. You can customize these rules for your organization. When a new table is created in the CMDB, it derives identification and reconciliation rules from its parent table if these rules exist. To apply identification and reconciliation rules to a new table, create the rules either at the child level or at its parent level.

![Data Flow from various data sources into the CMDB.](../image/CMDB_IdentificationAndReconciliation.png "Process flow of Identification and Reconciliation")

## Identification and Reconciliation Engine \(IRE\)

[Identification and Reconciliation Engine \(IRE\)](ire.md) is a rule-based engine, operating as an underlying key component in Identification and Reconciliation. IRE provides a centralized framework to perform identification and reconciliation processes across different data sources. IRE uses identification rules, reconciliation rules, and IRE data source rules when processing incoming data before inserting or updating data in the CMDB. IRE processes help maintain data integrity in the CMDB.

-   IRE prevents duplicate CIs by uniquely identifying CIs.​
-   IRE reconciles CI attributes by allowing only authoritative data sources to write to CMDB.

