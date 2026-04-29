---
title: Create a reconciliation rule for a non-CMDB table
description: Create a static or a dynamic CI reconciliation rule for a non-CMDB table.A static reconciliation rule specifies class attributes that data sources are authorized to update, and prevents unauthorized data sources from overwriting the attributes' values. A static reconciliation rule also specifies the prioritization among multiple data sources. Without static reconciliation rules, data sources can overwrite each other's updates to attribute values.A dynamic reconciliation rule for non-CMDB table uses CMDB 360 data to choose a value such as the largest value that is reported, for updating a record.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [IRE support for non-CMDB tables, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a reconciliation rule for a non-CMDB table

Create a static or a dynamic CI reconciliation rule for a non-CMDB table.

For information about static reconciliation rules, dynamic reconciliation rules, and other principals related to reconciliation rules, see [Reconciliation rules](../reference/r_ReconciliationRulesPrinciples.md).

If both, static and dynamic reconciliation rules exist for the same record attribute, the dynamic rule has precedence.

**Note:** You can't create a reconciliation rule for system fields or for Identification and Reconciliation Engine \(IRE\) specific fields such as the Discovery source \(discovery\_source\) field. Also, reconciliation rules can't be dot-walked using reference fields.

**Parent Topic:**[IRE support for non-CMDB tables](ire-support-non-cmdb-tables.md)

## Create a static reconciliation rule for a non-CMDB table

A static reconciliation rule specifies class attributes that data sources are authorized to update, and prevents unauthorized data sources from overwriting the attributes' values. A static reconciliation rule also specifies the prioritization among multiple data sources. Without static reconciliation rules, data sources can overwrite each other's updates to attribute values.

### Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

### About this task

Static reconciliation rules are used in conjunction with [data refresh rules](../task/create-non-cmdb-data-refresh-rule.md) to determine reconciliation steps for a record. These rules determine if, when, and by which data source a record can be updated. If multiple data sources are authorized to update the same attributes, assign a priority to each of these data sources to prevent them from overwriting each other's updates.

After an authorized data source updates an attribute, subsequent updates are accepted only from the same data source or from a data source with a higher priority. Updates from a data source with a lower priority are rejected, unless these two conditions are met:

-   The lower priority source is the first source updating the record.
-   The record became stale based on data refresh rules for the class.

Precedence order of static reconciliation rules:

-   Rule configured for a specific attribute, has precedence over rule set with **Apply to all attributes** \(regardless of priority value\).
-   Between two rules for the same attribute or between two rules set with **Apply to all attributes**, the rule that is specific directly for the class has precedence over the derived rule.​
-   Between two rules for the same attribute or between two rules set with **Apply to all attributes** at the same class level, precedence is determined by rule priorities.

Information about the last discovery source that updates each attribute is stored in the Data Source History \[cmdb\_datasource\_last\_update\] table, but only after enabling the reconciliation rule. Therefore, there might be unexpected updates after you enable the rule until the highest priority data source has updated the CI.

Static reconciliation rules affect reconciliation of stale attributes. During reconciliation, the information in the Data Source History table is considered along with the data refresh rules for the CI's class, to determine if a CI attribute is stale. A CI attribute is determined to be stale if it was not updated by the latest discovery source to update the CI, within a time period. The time period is specified by the Effective Duration time in the data refresh rule for the class for the discovery source. In this case, if another authorized discovery source, with a lower priority attempts to update the stale CI attribute, the update is allowed.

If there is a dynamic reconciliation rule for the same record attribute as in a static reconciliation rule, the dynamic rule takes precedence.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Reconciliation Definitions**.

2.  In the Reconciliation Definitions list view, click **New**.

3.  Fill out the Reconciliation Definition form.

<table id="table_md4_3cz_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

The data source that you are configuring this rule for.

</td></tr><tr><td>

Priority

</td><td>

Priority of **Data source** within other data sources for the specified attributes. Smaller numbers designate higher priority. Data sources without a reconciliation rule are assigned the lowest priority.

</td></tr><tr><td>

Applies to

</td><td>

Authorizes the specified data source to update all attributes of the specified non-CMDB table. **Note:** This setting will be overridden by any setting that applies to a specific attribute. In which case, instead of using this option, you can directly include all attributes for **Attributes**.

</td></tr><tr><td>

Filter condition

</td><td>

Conditions that records must meet for the rule to be applicable.

 For example, to apply this rule only to records that are associated with the Finance department, select this condition: **\[Department\] \[is\] \[Finance\]**.

 **Note:** The [glide.identification\_engine.enable\_reconciliation\_filter\_before\_update](../reference/properties-id-reconciliation.md) system property determines when filter conditions are applied. By default, those filter conditions are applied after attribute values have changed during payload processing. Set this property to **true** so that Identification and Reconciliation Engine \(IRE\) applies the filter conditions before attribute values change.

</td></tr><tr><td>

Attributes

</td><td>

Attributes from the current or from a parent class, that the specified data source is authorized to update.

 Available only if **Apply to all attributes** is not selected.

</td></tr><tr><td>

Update with null

</td><td>

Attributes that the specified data source can update with a null value. By default, authorized data sources cannot overwrite a non-null value with a null value.

 Attributes in this list, which are not in the **Attributes** list, are not included with the attributes that the data source can update with a null value.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Create a dynamic reconciliation rule for a non-CMDB table

A dynamic reconciliation rule for non-CMDB table uses CMDB 360 data to choose a value such as the largest value that is reported, for updating a record.

### Before you begin

[CMDB 360](multisource-cmdb.md) must be enabled.

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

### About this task

If the same CI attribute has both, a static reconciliation rule and a dynamic reconciliation rule, the dynamic reconciliation rule has precedence.

A dynamic reconciliation rule supports several rule types, such as largest reported value and most reported value. When applying a dynamic reconciliation rule, IRE processes the current payload and then examines the CMDB 360 data store to select a value with which to update the CMDB. Depending on the dynamic reconciliation rule type, selecting the appropriate value might not be immediately conclusive. For example, there might not be a single value that is most reported, or for some values, the last discovered timestamp isn't reported. Therefore, when necessary, IRE falls back to examining additional details such as last reported, last discovered, and last updated values to select the most appropriate value.

**Note:** You can't add a dynamic reconciliation rule when creating a new child class in the CI Class Manager. You must first save the new child class and then add the dynamic reconciliation rule.

### Procedure

1.  Click **All**.

2.  In the Filter navigator, enter `cmdb_dynamic_reconciliation_definition.list` to open the Dynamic Reconciliation Definitions table.

3.  In the Dynamic Reconciliation Definitions list view, click **New**.

4.  Fill out the Dynamic Reconciliation Definition form.

<table id="table_mqc_22z_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

 

</td></tr><tr><td>

Attributes

</td><td>

Attributes for which to apply the rule. Attributes that the specified rule type can't be applied to and attributes for which a dynamic reconciliation rule already exists for, don’t appear.

</td></tr><tr><td>

Filter condition

</td><td>

Conditions that CIs must meet for the rule to be applicable.

 For example, to apply a rule only to CIs that are associated with the Finance department, select this condition: **\[Department\] \[is\] \[Finance\]**.

</td></tr><tr><td>

Applies to

</td><td>

Non-CMDB table that this rule applies to.

</td></tr><tr><td>

Dynamic Rule Type

</td><td>

Rule type which is based on CMDB 360 data.

</td></tr></tbody>
</table>5.  Click **Submit**.


