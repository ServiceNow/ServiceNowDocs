---
title: Template Management for Field Service components
description: Several types of components are installed with the Template Management for Field Service feature, including tables and business rules.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Components installed with additional plugins for Field Service Management, Field Service Management reference, Field Service Management]
---

# Template Management for Field Service components

Several types of components are installed with the Template Management for Field Service feature, including tables and business rules.

## Tables

Template Management for Field Service adds the following tables.

<table id="table_erh_gpl_g5b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[wm\_m2m\_template\_attribute\_map\]

</td><td>

Entity to store the work order template attribute mapping.​

</td></tr></tbody>
</table>## Script Includes

Template Management for Field Service adds the following script includes.

|Script include|Description|
|--------------|-----------|
|FSMTableMapSourceIdentifierDefaultImpl|Implementation class for sn\_fsm\_adv\_tmp.FSMTableMapSourceIdentifier extension point, helps to identify the source of a work order.|
|FSMTableMapSourceIdentifierPlannedWorkMgmtImpl|Implementation class for sn\_fsm\_adv\_tmp.FSMTableMapSourceIdentifier extension point, helps to determine if the source of a work order is using the planned maintenance template or planned work management template.|
|FSMTemplateMgmntDefaultImpl|Implementation class for sn\_fsm\_adv\_tmp.FSMTemplateMgmntExtPoint. extension point, enables the work order template to map information from a source table to the appropriate fields in a work order.|
|FSMTemplateMgmntHelper|Contains utility methods to identify the source record and then map information from the source table to the target table \[wm\_order\].|

## Business rules

Template Management for Field Service adds the following business rules.

<table id="table_bgq_kpl_g5b"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Restrict table map for model

</td><td>

\[wm\_m2m\_template\_attribute\_map\]

</td><td>

Prevents the user from creating a duplicate record of table mapping to the work order template.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

