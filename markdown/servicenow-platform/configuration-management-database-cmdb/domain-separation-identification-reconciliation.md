---
title: Domain separation and CMDB Identification and Reconciliation
description: Domain separation is supported in the CMDB Identification and Reconciliation feature. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and CMDB Identification and Reconciliation

Domain separation is supported in the CMDB Identification and Reconciliation feature. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Overview of domain separation in IRE

Domain separation is enforced during the [CMDB Identification and Reconciliation](c_CMDBIdentifyandReconcile.md) \(IRE\) process. IRE processes are domain aware and domain separation is applied to the Identification and Reconciliation rules.

For more information about domain separation, see [domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainSeparation.md).



## How domain separation works in Identification and Reconciliation

Domain separation in the identification engine is enforced when users activate the domain separation plugin. Domain separation for IRE has two modes of operation in domain separated instances:

-   Strict mode \(enabled by default\): In this mode, identification processes only those CIs in which the domain ID is identical to the domain of the currently logged in user. If duplicate CIs exist across domains \(including parent and child domains\), then those CIs aren't considered duplicate CIs because their domain IDs don't match.
-   Platform domain separation mode \(disabled by default\): In this mode, IRE follows the platform domain separation behavior. So during identification, parent domains can access all CIs within their child domains or any of the domains it has visibility into. For more information, see [Visibility domains and Contains domains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainVisibility.md).

    Platform domain separation mode is intended to be used by advanced users for very specific or advanced use cases.

    **Note:**

    Platform domain separation mode introduces some risks that are greater on upgraded instances and much lesser on zBooted instances.

    Depending on how IRE processes are configured on a domain separated instance, setting IRE to use platform domain separation mode might result in unexpected and undesirable behavior if not used carefully. One of the risks is if enabling platform domain separation mode is followed by running IRE processes from a different domain than the one on which IRE processes were previously run. In this situation, CIs that were previously identified as unique, might get identified as duplicate CIs and might cause some applications to start failing.

    If any application is already using IRE effectively in domain separated environment, then there's no advantage in switching to platform domain separation mode that might create some risk.


Use the [glide.identification\_engine.platform\_domain\_separation\_enabled](../reference/properties-id-reconciliation.md) system property to switch between those two modes for IRE domain separation. By default, this property is set to **false**.

## Platform domain separation mode

Set the system property [glide.identification\_engine.platform\_domain\_separation\_enabled](../reference/properties-id-reconciliation.md) to **true** to enable the platform domain separation mode for IRE processing. With the platform domain separation mode, parent domains can access all of their child domains during IRE processing. For example, IRE can detect a matching CI in a child domain and then update that CI instead of creating a new one.

In the platform domain separation mode for IRE:

-   IRE run from a parent domain can access CIs contained within their domain, child domains that are lower in the domain hierarchy, and global domain.​
-   IRE run from the global domain can access all CIs.
-   [Visibility domains and Contains domains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainVisibility.md) are supported.

**Note:** When platform domain separation mode is enabled, there might be a sudden increase in IRE detection of duplicate CIs.

## Domain separation during the Identification Process

Domain separation during the Identification process is enforced as follows:

-   Regardless of the setting of the [glide.identification\_engine.platform\_domain\_separation\_enabled](../reference/properties-id-reconciliation.md) system property:
    -   Domain IDs don't need to be explicitly sent in the input payload of the identification engine APIs. Internally, the identification engine causes the current domain ID of the user to call the identification engine APIs.
    -   During matching, if no records are found and a CI is inserted, the CI domain ID is the same as the domain ID of the logged-in user’s domain. When updating a CI, the CI domain ID doesn't change.
    -   During matching, if duplicates are found, De-Duplication tasks created in the \[reconcile\_duplicate\_task\] table have the same domain ID as of the duplicate CIs.
    -   During matching, if reclassification of the CI isn't allowed, reclassification tasks are created in the \[reclassification\_task\] table, with the same domain ID as the CI for which reclassification is needed.
-   When the system property [glide.identification\_engine.platform\_domain\_separation\_enabled](../reference/properties-id-reconciliation.md) is set to **false**:
    -   Only CIs that have the same domain ID as the currently logged-in user's domain are used during matching.
    -   Duplicate CIs that exist across domains \(including parent and child domains\) aren't considered as duplicate CIs by IRE.
-   When the system property [glide.identification\_engine.platform\_domain\_separation\_enabled](../reference/properties-id-reconciliation.md) is set to **true**:
    -   Duplicate CIs that exist across domains \(such as parent and child domains\) are considered as duplicate CIs by IRE.
    -   CIs from the logged in user domain and child domains are used during matching.

## Domain separation and Identification Rules

The identification rules and identification inclusion rules used during the identification process are always defined at the global level. For example, the following tables don't have a sys\_domain field:

-   Identifier \(cmdb\_identifier\)
-   Identifier Entries \(cmdb\_identifier\_entry\)
-   Related Entries \(cmdb\_related\_entry\)
-   Identification Inclusion Rules \(cmdb\_ie\_active\_config\)

## Domain separation and Reconciliation Rules

The reconciliation definition rules that are used during the reconciliation process can be defined for different domains. For example, the following tables do have sys\_domain, sys\_overrides, sys\_domain\_path fields:

-   Reconciliation Definition \(cmdb\_reconciliation\_definition\)
-   Datasource Precedence \(cmdb\_datasource\_precedence\)
-   Data Source Staleness Definitions \(cmdb\_datasource\_staleness\)

