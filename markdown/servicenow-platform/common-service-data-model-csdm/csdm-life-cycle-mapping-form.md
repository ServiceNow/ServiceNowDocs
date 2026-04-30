---
title: Life cycle mapping form
description: Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(life cycle stage and life cycle stage status\). You map both asset and CI legacy status values to life-cycle value pairs.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle mapping form

Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(**life cycle stage** and **life cycle stage status**\). You map both asset and CI legacy status values to life-cycle value pairs.

## Fields on the Life cycle mapping form

<table id="table_o5j_vd5_hnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mapping for table

</td><td>

Legacy CMDB table and descending tables that this mapping applies to. Applies to a descending table unless there is a mapping configured specifically to the descending table.

</td></tr><tr><td>

Priority

</td><td>

Priority of applying this mapping definition for the table.

 The **Priority** value on the life cycle mapping table is used when a record update triggers the “legacy-to-life-cycle” sync, and multiple legacy value states on the record match with mapping rules. Of the multiple values, the highest priority \(lowest numerical value\) entry is used to set the life-cycle value pairs. If the highest priority entry can't be used, the system uses the next record in priority.

 **Note:** Priority is not used if **Reverse sync** is active because there should be a maximum of one reverse-sync choice for each life-cycle value per class.

</td></tr><tr><td>

Active

</td><td>

Denotes whether to apply this mapping definition.

 Deactivation results in lower-priority mappings being used or setting standard life cycle fields to **TBD**.

</td></tr><tr><td>

Legacy field name

</td><td>

Legacy field in the specified **Mapping for table** that is currently being used to store a life cycle stage. The value should be used as the source for the life cycle mapping.

</td></tr><tr><td>

Legacy subfield name

</td><td>

Value to set if the **Legacy field name** has a subfield. For example, if hardware **Status** has a substatus, then specify the name of the substatus here.

</td></tr><tr><td>

Legacy field value

</td><td>

Legacy value in the specified **Mapping for table** that is currently being used store life cycle stage. The value should be used as the source for the life cycle mapping.

</td></tr><tr><td>

Legacy subfield value

</td><td>

Value that is set if the **Legacy field value** has a subfield. For example, if hardware **Status** has a substatus, then specify the value of the substatus here.

</td></tr><tr><td>

Life cycle control

</td><td>

Class and life cycle stage and life cycle stage status that are used as the authoritative source of valid combinations for life cycle mapping.

</td></tr><tr><td>

Table

</td><td>

Standard object table that the Life cycle control belongs to.

</td></tr><tr><td>

Life cycle stage

</td><td>

Standard life cycle stage to map the specified **Legacy field value** to.

 **Note:** The **Life cycle control** setting determines that this particular life cycle stage is appropriate for the mapping.

 If there is no match in the life\_cycle\_mapping table, the value is set to **TBD**.

</td></tr><tr><td>

Life cycle stage status

</td><td>

Standard life cycle stage status to map the specified **Legacy field value** to.

 **Note:** The **Life cycle control** setting determines that this particular life cycle stage status is appropriate for the mapping.

 If there is no match in the life\_cycle\_mapping table, the value is set to **TBD**.

</td></tr></tbody>
</table>**Parent Topic:**[CSDM reference](../../csdm-implementation/concept/csdm-content-frame-reference.md)

