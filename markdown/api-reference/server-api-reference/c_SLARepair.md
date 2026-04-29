---
title: SLARepair - Global
description: The SLARepair script include provides methods that delete the existing SLAs and then recreates them from each task's history.Repair the task SLAs associated with the passed-in filter and source table.Repair the task SLAs associated with the passed in GlideRecord.Repair the task SLAs associated with the passed in sys\_id and source table.Enables or disables auditing when running a repair.Enables or disables running a workflow for each of the Task SLA records being repaired.Validates the repair request.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SLARepair- Global

The SLARepair script include provides methods that delete the existing SLAs and then recreates them from each task's history.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SLARepair - repairByFilter\(String filter, String sourceTable\)

Repair the task SLAs associated with the passed-in filter and source table.

|Name|Type|Description|
|----|----|-----------|
|filter|String|Encoded query that is used to retrieve a set of records from the source table.|
|sourceTable|String|Name of a table that is \(or extends\) contract\_sla, task\_sla, or task.|

|Type|Description|
|----|-----------|
|void| |

Repair SLAs for problems created last month with a priority of 2.

```
var now_GR = new GlideRecord("problem");
now_GR.addQuery("sys_created_on", "ON", "Last Month@javascript:gs.beginningOfLastMonth()@javascript:gs.endOfLastMonth()");
now_GR.addQuery("priority", "2");
now_GR.query();

var repair = new SLARepair();
repair.repairByFilter(now_GR.getEncodedQuery(), now_GR.getRecordClassName());
```

## SLARepair - repairByGlideRecord\(GlideRecord now\_GR\)

Repair the task SLAs associated with the passed in GlideRecord.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|GlideRecord for a table that is \(or extends\) contract\_sla, task\_sla, or task.|

|Type|Description|
|----|-----------|
|void| |

Repair SLAs for problems created last month with a priority of 2.

```
var now_GR = new GlideRecord("problem");
now_GR.addQuery("sys_created_on", "ON", "Last Month@javascript:gs.beginningOfLastMonth()@javascript:gs.endOfLastMonth()");
now_GR.addQuery("priority", "2");
now_GR.query();

var repair = new SLARepair();
repair.repairByGlideRecord(now_GR);
```

## SLARepair - repairBySysId\(String sysId, String sourceTable\)

Repair the task SLAs associated with the passed in sys\_id and source table.

|Name|Type|Description|
|----|----|-----------|
|sysId|string|Specify the ID of a table that is \(or extends\) contract\_sla, task\_sla, or task.|
|sourceTable|string|Specify the name of a table that is \(or extends\) contract\_sla, task\_sla, or task.|

|Type|Description|
|----|-----------|
|void| |

Find problems created last month with a priority of 2.

```
var now_GR = new GlideRecord("problem");
now_GR.addQuery("sys_created_on", "ON", "Last Month@javascript:gs.beginningOfLastMonth()@javascript:gs.endOfLastMonth()");
now_GR.addQuery("priority", "2");
now_GR.query();

var repair = new SLARepair();
repair.repairBySysId(now_GR.sys_id + "",  now_GR.getRecordClassName());

```

## SLARepair - setAuditEnabled\(Boolean onOrOff\)

Enables or disables auditing when running a repair.

By default, auditing is set to the value in the property **com.snc.sla.repair.audit**. You can override this by passing in true to enable or false to disable auditing.

<table id="table_p1z_b1c_sr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

onOrOff

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable auditing.Valid values:

-   true: Enable auditing.
-   false: Disable auditing.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|this|Self-reference to allow for method chaining.|

```
var builder = new SLARepair();
  builder.setAuditEnabled(true);

```

## SLARepair - setRunWorkflow\(Boolean onOrOff\)

Enables or disables running a workflow for each of the Task SLA records being repaired.

By default, when a Task SLA is repaired the workflow is run during the repair process. To override this, you can pass in false to disable running of the workflow.

<table id="table_f32_21c_sr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

onOrOff

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable workflow.Valid values:

-   true: Enable workflow.
-   false: Disable workflow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|this|Self-reference to allow for method chaining.|

```
var repair = new SLARepair();
repair.setRunWorkflow(false);
```

## SLARepair - setValidateOnly\(Boolean onOrOff\)

Validates the repair request.

If false is passed in, the task SLAs are repaired. If true is passed in, calls to repair don't alter any task SLAs, they only validate the supplied parameters and generate a count of records to be repaired.

<table id="table_xlw_c1c_sr" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

onOrOff

</td><td>

Boolean

</td><td>

Flag that indicates whether to enable validation.Valid values:

-   true: Enable validation.
-   false: Disable validation.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|this|Self-reference to allow for method chaining.|

```
var repair = new SLARepair();
  repair.setValidateOnly(true);
```

