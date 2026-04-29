---
title: Components installed with Identification and Reconciliation
description: Several types of components are installed with Identification and Reconciliation \(included in the com.snc.cmdb plugin\), including tables.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Reference, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed with Identification and Reconciliation

Several types of components are installed with Identification and Reconciliation \(included in the com.snc.cmdb plugin\), including tables.

## Tables installed

<table id="table_ugt_x3x_ft"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Identifier\[cmdb\_identifier\]

</td><td>

Identification rule sets defined for different classes of CIs.

</td></tr><tr><td>

Reconciliation Definition\[cmdb\_reconciliation\_definition\]

</td><td>

Static reconciliation rules defined for different classes of CIs at the table and field level.

</td></tr><tr><td>

Dynamic Reconciliation Definitions \[cmdb\_dynamic\_reconciliation\_definition\]

</td><td>

Dynamic reconciliation rules defined for different attributes and classes.

</td></tr><tr><td>

Identifier Entry\[cmdb\_identifier\_entry\]

</td><td>

Rule entries with different priorities assigned to each identifier.

</td></tr><tr><td>

Duplicate Audit Result\[duplicate\_audit\_result\]

</td><td>

Duplicate audit results corresponding to a specific duplicate task. These results are generated automatically during the identification process and should not be added manually.

</td></tr><tr><td>

Remediate Duplicate Task\[reconcile\_duplicate\_task\]

</td><td>

Task to address duplication that is detected during the identification process. Records are generated automatically, and users should not add records manually.

</td></tr><tr><td>

Reclassification Task\[reclassification\_task\]

</td><td>

Reclassification tasks that were generated during the identification process.

</td></tr><tr><td>

Data Source History \[cmdb\_datasource\_last\_update\]

</td><td>

Information about the last data source that updated each attribute. Used to determine if a data source can update a stale CI.

</td></tr><tr><td>

Data Source Staleness Definition\[cmdb\_datasource\_staleness\]

</td><td>

Effective duration per data source. When effective duration is exceeded, then CMDB Health determines that the information provided by that data source is stale.

</td></tr><tr><td>

Identification Engine Context\[cmdb\_ie\_context\]

</td><td>

Input payload, and data source \(cmdb\_ci’s discovery\_source\) that will be used as input for a specific identification engine API. Stores information about which specific identification engine API will be called \(**identifyCI** or **createOrUpdateCI** API\). Also stores information about enhanced IRE options used in Identification Simulation.

 **Note:** Internal table used by identification simulation.

</td></tr><tr><td>

Identification Engine Run\[cmdb\_ie\_run\]

</td><td>

Specific cmdb\_ie\_context record that was used to run against the identification engine. Also details about the output payload returned by APIs, such as start and end time of the run and whether the run was successful.

 **Note:** Internal table used by identification simulation.

</td></tr><tr><td>

Identification Engine Log\[cmdb\_ie\_log\]

</td><td>

Identification engine logs for a specific cmdb\_ie\_run simulated in the identification simulation. Also details about logs level and order.

 **Note:** Internal table used by identification simulation.

</td></tr><tr><td>

IRE Data Source Rule \[cmdb\_ire\_data\_source\_rule\]

</td><td>

[IRE data source rules](../task/create-ire-data-source-rule.md).

</td></tr><tr><td>

CMDB IRE Partial Payloads \[cmdb\_ire\_partial\_payloads\]

</td><td>

Payload items that were determined to be partial, and which might be later matched with an incoming payload. If a partial payload is matched and processed, it is deleted from the CMDB IRE Partial Payloads table.

 Partial payloads older than 90 days are deleted from the table.

 For more information about usage of this table in IRE processes, see [Identification and Reconciliation engine \(IRE\)](../concept/ire.md).

</td></tr><tr><td>

CMDB IRE Partial Payloads Index\[cmdb\_ire\_partial\_payloads\_index\]

</td><td>

Identifier keys associated with partial items. IRE uses those keys to try to match with identifier keys of incoming payloads.

 For more information about usage of this table in IRE processes, see [Identification and Reconciliation engine \(IRE\)](../concept/ire.md).

</td></tr><tr><td>

CMDB IRE Incomplete Payloads\[cmdb\_ire\_incomplete\_payloads\]

</td><td>

Incomplete items, stored using JSON format as incomplete payloads. Incomplete items are stored for the purpose of logging payloads with irrecoverable errors, and are never processed again.

 The table is configured for [table rotation](https://www.servicenow.com/docs/access?context=c_TableRotation&version=australia&pubname=australia-platform-administration&ft:locale=en-US), with duration of one day and seven table rotations.

 For more information about usage of this table in IRE processes, see [Identification and Reconciliation engine \(IRE\)](../concept/ire.md).

</td></tr><tr><td>

IRE Output Aggregate Stats\[cmdb\_ire\_output\_aggregate\_stats\]

</td><td>

This table is populated when RTE invokes IRE, for example, when processing integrations.

 Details about data inserted by Import Sets or Robust Transform Engine \(RTE\) to the CMDB \(via IRE\). Numbers of items inserted, partial items, and updated items, are stored for each type of CI, per run.

</td></tr><tr><td>

IRE Output Target Items\[cmdb\_ire\_output\_target\_item\]

</td><td>

This table is populated when RTE invokes IRE, for example, when processing integrations.

 Details about data inserted by Import Sets or Robust Transform Engine \(RTE\) to the CMDB \(via IRE\). Target class and the sys\_id are stored per ImportSet row id, within a run.

 For this table to populate, RTE must pass the **ire\_output\_detailed\_stats** property.

</td></tr><tr><td>

Reclassification Restrictions\[cmdb\_ire\_reclassification\_restriction\]

</td><td>

Reclassification restriction rules. These rules prevent switch and downgrade reclassification updates for specific source and target classes. For more information, see [Configure CI reclassification during IRE processing](../concept/c_CIReclassification.md#).

</td></tr><tr><td>

CMDB Deduplication Task Lookup or Related item allowed classes \[cmdb\_duplicate\_lookup\_related\_allowed\_class\]

</td><td>

Configuration table \(typically included in a CI Class Models app\) with entries for related and lookup tables for which you want IRE to generate de-duplication tasks during identification. You can then process those de-duplication tasks to remediate the duplication.

 For more information about using this table, see [Detecting duplicate CIs](../concept/id-detect-dup-ci.md).

</td></tr></tbody>
</table>## User roles installed

|Role|Description|
|----|-----------|
|cmdb\_payload\_admin|Automatically assigned to users with the cmdb\_admin role for internal use only.|

**Related topics**  


[Properties for Identification and Reconciliation](properties-id-reconciliation.md)

