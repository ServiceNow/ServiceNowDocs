---
title: Discrepancy identification – types of discrepancies
description: The Telecom Discrepancy Identification and Reconciliation capability identifies and classifies mismatches between the network state \(as discovered through TSOM Discovery or Service Graph Connectors\) and the inventory data stored in the CMDB or TNI.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Identify and reconcile discrepancies, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Discrepancy identification – types of discrepancies

The Telecom Discrepancy Identification and Reconciliation capability identifies and classifies mismatches between the network state \(as discovered through TSOM Discovery or Service Graph Connectors\) and the inventory data stored in the CMDB or TNI.

Discrepancy identification is powered by the CMDB Compliance Certification Audit, which:

-   Runs on CI and relationship data.
-   Compares discovered and inventoried records.
-   Generates Follow-on tasks when mismatches are detected.

## Discrepancy types

The audit process identifies discrepancies by comparing discovered network data with the existing inventory in the CMDB/TNI. Discrepancies fall into four categories:

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

-   **Missing in CMDB — entities discovered on the network but not present in inventory**

    Definition: A CI is discovered on the network through TSOM Discovery or a Service Graph Connector, but no corresponding record exists in the CMDB. This indicates that the equipment is physically present and operational but has not yet been inventoried. For example, Discovery detects a Fortinet FortiGate-80F device on the network, but no matching CI exists in the CMDB.

    Impact:

    -   The audit identifies the CI as new when its creation date matches its discovery date.
    -   A single follow-on task is created at the equipment level to prompt review. Individual tasks are not generated for each underlying child CI \(such as IP addresses\) associated with the equipment, keeping the task list focused and actionable.
    -   The follow-on task includes the short description **New CI has been discovered**, along with the CI reference and associated product model.
    -   You can enable or disable follow-on task creation for this discrepancy type using a system property.

-   **SD-WAN discrepancy identification**

    In addition to telecom-specific discrepancies, the Telecom SD-WAN Network Discrepancy Audit identifies mismatches in your SD-WAN inventory. Standard telecom discrepancy detection focuses on CI classes such as slot, card, and interface. The SD-WAN audit targets a different set of CI classes and validates them against rules specific to the SD-WAN data model.

    By default, the audit scopes to CIs whose discovery source contains TSOM. The audit compares discovered SD-WAN data with the inventory in the CMDB and generates follow-on tasks when mismatches are detected.

<table id="table_fdt_yst_m3c"><thead><tr><th>

CI class

</th><th>

Validation requirements

</th><th>

Relationship type

</th></tr></thead><tbody><tr><td>

Group \(cmdb\_ci\_group\)

</td><td>

-   Company reference
-   At least 1 Service child
-   At least 1 Site child


</td><td>

Members::Member of

</td></tr><tr><td>

Site \(cmdb\_ci\_ni\_site\)

</td><td>

-   Company reference
-   Location reference
-   Exactly 1 Group parent


</td><td>

Members::Member of

</td></tr><tr><td>

Service \(cmdb\_ci\_network\_service\_instance\)

</td><td>

-   Company reference
-   Exactly 1 Group parent


</td><td>

Members::Member of

</td></tr><tr><td>

Equipment \(sn\_tsom\_core.audit. equipment\_tables\)

</td><td>

-   Company reference
-   Max 1 Service parent
-   Max 1 Site parent
-   At least 1 IP Address child
-   Each IP Address child has max 1 Equipment parent


</td><td>

-   Service/Site:
-   Contains::Contained by
-   IP Address: Owns::Owned by


</td></tr></tbody>
</table>    The SD-WAN audit validates the following CI classes. For each CI, the audit checks that required references are populated and that relationships match the expected structure. A CI that meets all requirements is marked as Certified. If one or more requirements are not met, the CI is marked as Failed and a follow-on task is created.

-   **SD-WAN discrepancy types**

    The SD-WAN audit detects the same categories of discrepancy as the telecom audit, applied to the SD-WAN CI classes listed above:

    Missing reference: A required reference \(such as Company or Location\) is not populated on the CI. A follow-on task is created with the description identifying which reference is missing.

    Incorrect relationships: A required relationship is missing or exceeds the allowed count. For example, a Site CI without a Group parent, or an Equipment CI with more than one Service parent. A follow-on task is created with the description identifying the relationship issue.

    Missing in CMDB: A CI is discovered on the network but no corresponding record exists in the CMDB. The audit identifies the CI as new when its creation date matches its discovery date, and creates a single follow-on task at the equipment level. For details on this discrepancy type, see the section **Missing in CMDB** above.


**Related topics**  


[Activate Telecom Discrepancy Identification and Reconciliation](../task/configure-telecom-reconciliation.md)

[Run Telecom Discrepancy audit](../task/run-audits.md#)

