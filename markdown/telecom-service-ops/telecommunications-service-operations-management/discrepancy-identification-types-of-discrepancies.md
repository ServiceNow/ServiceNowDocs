---
title: Discrepancy identification – types of discrepancies
description: The Telecom Discrepancy Identification and Reconciliation capability identifies and classifies mismatches between the network state \(as discovered through TSOM Discovery or Service Graph Connectors\) and the inventory data stored in the CMDB or TNI.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Identify and reconcile discrepancies, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Discrepancy identification – types of discrepancies

The Telecom Discrepancy Identification and Reconciliation capability identifies and classifies mismatches between the network state \(as discovered through TSOM Discovery or Service Graph Connectors\) and the inventory data stored in the CMDB or TNI.

Discrepancy identification is powered by the CMDB Compliance Certification Audit, which:

-   Runs on CI and relationship data.
-   Compares discovered and inventoried records.
-   Generates Follow-on tasks when mismatches are detected.

## Discrepancy types

The audit process identifies discrepancies by comparing discovered network data with the existing inventory in the CMDB/TNI. Discrepancies fall into two main categories:

-   **Missing in network - entities existing in inventory but missing in network**

    Definition: A CI is detected by Discovery but is either missing from the CMDB/TNI or incorrectly represented. For example, Discovery detects Card05 installed in Slot04, but the CMDB still lists Card04, or worse, shows both Card04 and Card05 in the same slot—violating cardinality or model constraints.

    Impact:

    -   A discrepancy task is generated to highlight the data conflict.
    -   Optional remediation subflows may be triggered to reconcile the data by retiring outdated records or updating slot assignments.
-   **Mismatched configuration items \(CIs\) - entities that exist in inventory and network but differ in attribute values and hierarchical relationships**

    Definition: The CI exists in both Discovery and CMDB/TNI, but discrepancies exist in relationships, hierarchy, or attribute values. The following are the sub types:

    -   Hierarchy Mismatches - Occur when the structural relationships between CIs \(e.g., parent-child associations\) are inconsistent. The following are the examples:
        -   A chassis contains more child cards than allowed by the model definition.
        -   A card is incorrectly associated with a slot in the CMDB that does not align with Discovery data. The validation sources are:
            -   `cmdb_rel_ci` records for `Contains::Contained by` relationships.
            -   `sn_ni_core_network_model_relationship` table for enforcing model-specific constraints.
    -   Attribute Value Mismatches - Involve discrepancies in CI field-level properties. The common issues are:

        -   Outdated or incorrect Discovery Dates.
        -   Inaccurate Model Configurations.
        -   Invalid Slot Assignments that breach model rules.
        The impact is the affected records are marked as failed in audit reports. Follow-On Tasks may invoke context-specific remediation subflows to realign inventory data with the actual network state.

        **Note:** For more information, see [Configure attribute value discrepancy in CMDB 360](../task/configure-attribute-value-discrepancy-in-cmdb-360.md).


**Related topics**  


[Activate Telecom Discrepancy Identification and Reconciliation](../task/configure-telecom-reconciliation.md)

[Run Telecom Discrepancy audit](../task/run-audits.md#)

