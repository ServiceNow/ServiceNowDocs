---
title: Activate Telecom Discrepancy Identification and Reconciliation
description: Activate the Telecom Discrepancy Identification and Reconciliation feature \(part of the Telecom Visibility plugin\) to ensure consistency between telecom network resources discovered in the live network and the data represented in the CMDB or Telecom Network Inventory \(TNI\). This feature helps detect and remediate mismatches automatically, supporting service accuracy and data integrity across your telecom environment.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Activate Telecom Discrepancy Identification and Reconciliation

Activate the Telecom Discrepancy Identification and Reconciliation feature \(part of the Telecom Visibility plugin\) to ensure consistency between telecom network resources discovered in the live network and the data represented in the CMDB or Telecom Network Inventory \(TNI\). This feature helps detect and remediate mismatches automatically, supporting service accuracy and data integrity across your telecom environment.

## Before you begin

Role required: admin

To use this feature, your organization must have an active subscription to TSOM. Telecom Discovery, Telecom Visibility, and this feature are licensed together.

## About this task

Plugin dependencies - Ensure the following plugins are installed and activated:

|Plugin|ID / App ID|Type|
|------|-----------|----|
|Telecom Service Operation Core|`sn_tsom_core`|Store|
|CMDB CI Class Models|`sn_cmdb_ci_class`|Store|
|Expanded Model and Asset Classes|`sn_ent`|Store|
|Visibility Content|`sn_pattern_design`|Store|
|Integration Commons for CMDB|`sn_cmdb_int_util`|Store|
|Discovery Core|`com.snc.discovery.core`|Family|
|ITOM Discovery License|`com.snc.itom.discovery.license`|Family|
|ITOM Licensing|`com.snc.itom.license`|Family|

## Procedure

1.  Ensure the sn\_tsom\_core plugin is automatically installed when you install Telecommunications Discovery Patterns or the Nokia Altiplano Service Graph Connector.

2.  Ensure the mentioned dependent plugins are activated.


**Related topics**  


[Discrepancy identification – types of discrepancies](../concept/discrepancy-identification-types-of-discrepancies.md)

[System components installed with Telecom Discrepancy Identification &amp; Reconciliation](../concept/system-properties-affecting-telecom-discrepancy-identification-reconciliation.md)

[Telecom Discrepancy Identification and Reconciliation](../concept/exploring-telecom-reconciliation.md)

[Run Telecom Discrepancy audit](run-audits.md#)

[Control CI attribute updates using Reconciliation rules](control-ci-attribute-updates-using-reconciliation-rules.md)

