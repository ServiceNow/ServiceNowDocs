---
title: System components installed with Telecom Discrepancy Identification &amp; Reconciliation
description: The system properties are part of the TSOM Visibility plugin \(sn\_tsom\_core\) and control the Telecom Discrepancy Identification &amp; Reconciliation log \(TSOM CMDB Audit\). The TSOM Visibility plugin serves as an enabler for the TSOM Visibility applications, containing logic that is shared across the Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation solution.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# System components installed with Telecom Discrepancy Identification &amp; Reconciliation

The system properties are part of the TSOM Visibility plugin \(sn\_tsom\_core\) and control the Telecom Discrepancy Identification &amp; Reconciliation log \(TSOM CMDB Audit\). The TSOM Visibility plugin serves as an enabler for the TSOM Visibility applications, containing logic that is shared across the Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation solution.

<table id="table_c1p_wmd_b2c"><thead><tr><th>

Property Name

</th><th>

Recommended / Default Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_tsom\_core.audit.log.level

</td><td>

Telecom Discrepancy Audits' Logging.

</td><td>

debug,info,warn Default value: info

</td></tr><tr><td>

sn\_tsom\_core.audit.relationship\_types

</td><td>

Displayed Names of Relationship Types that will be handled by Telecom Discrepancy Audit.

</td><td>

Comma separated list of relationship types namesDefault value: Contains::Contained by

</td></tr><tr><td>

sn\_tsom\_core.audit.discovered\_date.diff.threshold.in.days

</td><td>

Most recent discovered date threshold in days. Used for Telecom Discrepancy Audit.

</td><td>

StringDefault value: 2.5

</td></tr><tr><td>

sn\_tsom\_core.audit.suppress\_CI\_Model\_missing\_discrepancy\_task\_creation

</td><td>

Suppress creation of CI Model missing discrepancy task for the tables.Used for Telecom Discrepancy Audit.

</td><td>

cmdb\_ci\_ni\_telco\_equipment, cmdb\_ci\_ip\_switch, cmdb\_ci\_ip\_router, cmdb\_ci\_container\_slot,cmdb\_ci\_container\_subslot,cmdb\_ci\_interface\_card,cmdb\_ci\_ni\_interface

</td></tr><tr><td>

sn\_tsom\_core.audit.equipment\_tables

</td><td>

Equipment tables that will be handled by Telecom Discrepancy Audit.

</td><td>

Comma separated list of equipment tables namesDefault value: cmdb\_ci\_netgear

</td></tr><tr><td>

sn\_tsom\_core.audit.interface\_card\_tables

</td><td>

Interface Cards tables that will be handled by Telecom Discrepancy Audit.

</td><td>

Comma separated list of card tables names.Default value: cmdb\_ci\_interface\_card

</td></tr><tr><td>

sn\_tsom\_core.audit.interface\_tables

</td><td>

Network Interface tables that will be handled by Telecom Discrepancy Audit.

</td><td>

Comma separated list of interface tables namesDefault value: cmdb\_ci\_ni\_interface

</td></tr><tr><td>

sn\_tsom\_core.audit.slot\_tables

</td><td>

Slot tables names that will be handled by Telecom Discrepancy Audit.

</td><td>

Comma separated list of slot tables namesDefault value: cmdb\_ci\_container\_slot

</td></tr><tr><td>

sn\_tsom\_core.audit.subslot\_tables

</td><td>

Subslot tables names that will be handled by Telecom Discrepancy Audit.

</td><td>

Comma separated list of subslot tables namesDefault value is cmdb\_ci\_container\_subslot

</td></tr></tbody>
</table><table id="table_ydx_rcb_yfc"><thead><tr><th>

Audit Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Telecom Discrepancy Audit

</td><td>

Audits records in the `cmdb_rel_ci` table. For each relationship record discovered by Nokia Altiplano or NSP, it validates the parent and child CIs based on: - Most recent discovery date - CI model - CI model relationship \(if TNI Core is installed\). **Note:** All discrepancy audits use a filtering mechanism that applies to equipment CIs. By default, the filter condition is: `discovery_source CONTAINS TSOM`.

</td></tr><tr><td>

Telecom Logical Connections Discrepancy Audit

</td><td>

Audits records in the `cmdb_ci_ni_logical_path` table. For each logical connection discovered by Nokia Altiplano or NSP, it checks: - Empty endpoint \(Port A or Port Z\) - Each endpoint must be connected to only one unique logical connection.

</td></tr><tr><td>

Telecom Network Topology Discrepancy Audit

</td><td>

Audits records in the `cmdb_ci_network_topology` table. For each network topology CI discovered by Nokia Altiplano or NSP, it verifies: - At least one Contains:Contained By relationship with equipment - At least one Members:Member Of relationship with a logical connection.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Service Operations Management reference](../reference/components-installed-with-tsom.md)

**Related topics**  


[Telecom Discrepancy Identification and Reconciliation](exploring-telecom-reconciliation.md)

[Activate Telecom Discrepancy Identification and Reconciliation](../task/configure-telecom-reconciliation.md)

[Run Telecom Discrepancy audit](../task/run-audits.md#)

