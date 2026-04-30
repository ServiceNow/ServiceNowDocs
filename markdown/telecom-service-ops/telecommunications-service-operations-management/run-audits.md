---
title: Run Telecom Discrepancy audit
description: The Telecom Discrepancy Audit validates the integrity of configuration items \(CIs\) and relationships across your telecom inventory using the CMDB Compliance framework.The following example illustrates how the audit works in a scenario.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use, Telecommunications Service Operations Management]
---

# Run Telecom Discrepancy audit

The Telecom Discrepancy Audit validates the integrity of configuration items \(CIs\) and relationships across your telecom inventory using the CMDB Compliance framework.

## Before you begin

Role required: admin

## About this task

The Telecom Discrepancy Audit is part of the CMDB Compliance framework and supports phased auditing to detect and address discrepancies in CI relationships and attributes discovered through ServiceNow Discovery or Service Graph Connectors \(for example, Nokia Altiplano\).

You can run the audit manually or set it to run at regular intervals. During manual execution, you can select from existing filters to limit the audit scope to specific CIs—helpful for testing or targeted reconciliation.

The Telecom Discrepancy Audit works in two phases:

1.  Initial compliance run: Validates CI relationships and selected CI tables using the following default criteria:
    -   Supported CI classes: Slot, Subslot, Card, Interface, Network Gear \(includes all extension tables\).
    -   Source: CI was discovered via Discovery \(For example `discovery_source = SG-TSOM-Altiplano`\).
    -   Relationship type: `Contains::Contained By` \(customizable via `sn_tsom_core.audit.relationship_types` property\).
2.  Subsequent compliance runs: In addition to initial checks, evaluates whether the Updated timestamp of the relationship or related CIs is more recent than the Last run date in the audit record.

    **Note:** Each failed audit creates a Follow-On Task for manual or automated remediation, confirming telecom CMDB data stays aligned with the network state.


The following screenshot helps you understand the Telecom Discrepancy Audit.![The user interface of the telecom discrepancy audit.](../images/telecom-discrepancy-audit.png)

## Procedure

1.  Navigate to **All** &gt; **Compliance** &gt; **Audits**

2.  Open the Telecom Discrepancy Audit \(cert\_audit table\) record.

3.  Select a filter.

    -   If multiple audit filters have been defined during configuration, you can choose one before running the audit.
    -   Filters enable you to restrict the audit scope based on criteria such as discovery source, CI class, or specific CI attributes.
    -   This step is especially useful when troubleshooting a subset of records or validating specific discovery results.
4.  Do either of the following to run the audit.

    -   Click **Run Audit** to trigger a manual execution.
    -   Configure the audit to run on a scheduled basis by setting up a recurring job.
    The audit uses CMDB Compliance to validate relationship and CI integrity across telecom inventory.


## Result

Review audit results

-   The audit identifies compliance failures such as missing relationships or misaligned attributes.
-   For each failed audit record, a Follow-On Task is automatically generated.
-   Tasks include recommended or automated remediation actions such as updating or decommissioning CIs.

Example use case: The configured filters can be used for different discovery sources. For example, the Nokia Altiplano. When running the audit manually, you can select the appropriate filter to validate only those CIs discovered by that specific source—confirming targeted and efficient auditing.

**Parent Topic:**[Using Telecommunications Service Operations Management](../concept/using-tsom.md)

**Related topics**  


[Configure filter for audit](configure-certification-filter-for-audit.md)

[Example for Telecom Discrepancy Audit and Remediation](run-audits.md#)

## Example for Telecom Discrepancy Audit and Remediation

The following example illustrates how the audit works in a scenario.

### Before you begin

Role required: admin

### About this task

A card \(Card04\) was initially discovered in Slot04. Later, Card04 was replaced by Card05 in the physical network, but the CMDB still shows Card04 in Slot04. When a new discovery run executes, Card05 is discovered and added to the same slot, creating a data conflict in CMDB.

Audit Behavior:

-   The Telecom Discrepancy Audit detects this inconsistency and creates a failed audit record \(e.g., `AUDR0001283`\).
-   A Follow-On Task is created automatically \(e.g., `TASK0020215`\) with a detailed description of the discrepancy.

Task Description Example \(Incorrect Number of Relationships\):

Card04 was last discovered more than 2.5 days ago.

|CI|Model|
|---|-----|
|Slot04|DEMO 20532Tree|
|Card04|Nokia 7360 FANT-F CARD MODULE|
|Card05|&lt;model not identified&gt;|

### Procedure

1.  Navigate **All** &gt; **Compliance** &gt; **Audits** &gt; **Telecom Discrepancy Audit** &gt; **Run Audits**.

    A Follow-on Task is automatically created for each failed audit record \(for example, TASK0020215\).

2.  Select **TASK0020215** and review the discrepancy description.

    **Note:** This is an example of the TASK0020215 description created for the "Incorrect number of relationships" scenario. Other scenarios and environments might have different descriptions.

    The Follow-On Task contains a detailed description of the discrepancy. As you can see in the description, the Card04 CI is in discrepancy.

3.  To remediate, perform the following steps:

    1.  Navigate **All** &gt; **System Definition** &gt; **UI Actions**.

    2.  Select **Remediate**.

        The Remediate button is a UI action that triggers the `TSOM CI Decommission` subflow. This subflow:

        -   Retires the outdated Card04 CI.
        -   Removes the incorrect Slot04 → Card04 relationship.
        -   Synchronizes CMDB records with the network state.

### Result

After remediation:

-   The Follow-On Task \(`TASK0020215`\) updates with work notes summarizing the resolution steps.
-   The Card04 CI is marked as retired, and incorrect relationships are removed.
-   CMDB is now aligned with the latest discovered state from the network.

**Note:** Customize Remediation - The Telecom Discrepancy Audit ships with example remediation subflows. You can create and attach custom subflows using Flow Designer to suit your operational requirements.

**Related topics**  


[Telecom Discrepancy Identification and Reconciliation](../concept/exploring-telecom-reconciliation.md)

[Discrepancy identification – types of discrepancies](../concept/discrepancy-identification-types-of-discrepancies.md)

[System components installed with Telecom Discrepancy Identification &amp; Reconciliation](../concept/system-properties-affecting-telecom-discrepancy-identification-reconciliation.md)

[Activate Telecom Discrepancy Identification and Reconciliation](configure-telecom-reconciliation.md)

[Defining UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

