---
title: Life cycle mapping form
description: Use the Life Cycle Mapping module to specify how existing legacy status values should be converted to CSDM life-cycle value pairs \(life cycle stage and life cycle stage status\). You map both asset and CI legacy status values to life-cycle value pairs.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
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

 The **Priority** value on the life cycle mapping table is used when a record update triggers the “legacy-to-life-cycle” synchronization, and multiple legacy value states on the record match with mapping rules. Of the multiple values, the highest priority \(lowest numerical value\) entry is used to set the life-cycle value pairs. If the highest priority entry can't be used, the system uses the next record in priority.

 **Note:** Priority is not used if **Reverse synchronization** is active because there should be a maximum of one reverse-synchronize choice for each life-cycle value per class.

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
</table>## Life Cycle Stage inheritance for Business Application records

Business Application records define a restricted set of Life Cycle Stage values that are intended to reflect application planning and usage, such as Ideation, Design, Operational, and End of Life. These life cycle definitions are configured using the life\_cycle\_control table specifically for the cmdb\_ci\_business\_application class. When you view or edit a Business Application record, however, additional Life Cycle Stage values such as Deploy and Inventory might also appear. These stages are not defined directly for Business Application, but are inherited from parent CI classes \(for example, cmdb\_ci\) through the aggregation-based inheritance model that is used by life\_cycle\_control. In this model, life cycle definitions from the current CI class are combined with life cycle definitions from all parent classes in the CMDB class hierarchy. Child classes therefore extend parent life cycle definitions rather than overriding them. As a result, Business Application records can display Life Cycle Stage values that are applicable to infrastructure or hardware CIs but might not be semantically meaningful for applications. This behavior is expected and working as designed.

In contrast, in sys\_choice inheritance definitions in child tables override the values in parent tables.

**Parent Topic:**[CSDM reference](../../csdm-implementation/concept/csdm-content-frame-reference.md)

**Related topics**  


[Asset status values aligned to CSDM life cycle values](csdm-lifecycle-map-csdm-to-asset.md)

[bundle-itam.c_ManagingAssets]

