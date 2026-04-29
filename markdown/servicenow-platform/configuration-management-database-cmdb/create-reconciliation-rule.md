---
title: Create a CI reconciliation rule
description: Create a static or a dynamic CI reconciliation rule.A static reconciliation rule specifies class attributes that discovery sources are authorized to update, and prevents unauthorized discovery sources from overwriting the attributes' values. A static reconciliation rule also specifies the prioritization among multiple discovery sources. Without static reconciliation rules, discovery sources can overwrite each other's updates to attribute values.A dynamic reconciliation rule uses CMDB 360 data to choose a value such as the largest value that is reported, for updating a CI.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Reconciliation rules, Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CI reconciliation rule

Create a static or a dynamic CI reconciliation rule.

If both, static and dynamic reconciliation rules exist for the same CI attribute, the dynamic rule has precedence.

**Note:** You can't create a reconciliation rule for system fields or for Identification and Reconciliation Engine \(IRE\) specific fields such as the Discovery source \(discovery\_source\) field. Also, reconciliation rules can't be dot-walked using reference fields.

**Parent Topic:**[Reconciliation rules](../reference/r_ReconciliationRulesPrinciples.md)

**Related topics**  


[Create a data refresh rule](../task/create-datasource-staleness-rule.md)

## Create a static reconciliation rule

A static reconciliation rule specifies class attributes that discovery sources are authorized to update, and prevents unauthorized discovery sources from overwriting the attributes' values. A static reconciliation rule also specifies the prioritization among multiple discovery sources. Without static reconciliation rules, discovery sources can overwrite each other's updates to attribute values.

### Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

### About this task

Static reconciliation rules are used in conjunction with [data refresh rules](../task/create-datasource-staleness-rule.md) to determine reconciliation steps for a CI. These rules determine if, when, and by which discovery source a CI can be updated. If multiple discovery sources are authorized to update the same class attributes, assign a priority to each of these discovery sources to prevent them from overwriting each other's updates.

After an authorized discovery source updates an attribute, subsequent updates are accepted only from the same discovery source or from a discovery source with a higher priority. Updates from a discovery source with a lower priority are rejected, unless these two conditions are met:

-   The lower priority source is the first source updating the CI.
-   The CI became stale based on data refresh rules for the CI class. However, a reconciliation rule that applies to all attributes, doesn’t have precedence over a lower priority reconciliation rule that applies to a specific attribute, even if the CI is stale.

Precedence order of static reconciliation rules:

-   Rule configured for a specific attribute, has precedence over rule set with **Apply to all attributes** \(regardless of priority value\).
-   Between two rules for the same attribute or between two rules set with **Apply to all attributes**, the rule that is specific directly for the class has precedence over the derived rule.​
-   Between two rules for the same attribute or between two rules set with **Apply to all attributes** at the same class level, precedence is determined by rule priorities.

Information about the last discovery source that updates each attribute is stored in the Data Source History \[cmdb\_datasource\_last\_update\] table, but only after enabling the reconciliation rule. Therefore, there might be unexpected updates after you enable the rule until the highest priority data source has updated the CI.

Static reconciliation rules affect reconciliation of stale CI attributes. During reconciliation, the information in the Data Source History table is considered along with the data refresh rules for the CI's class, to determine if a CI attribute is stale. A CI attribute is determined to be stale if it was not updated by the latest discovery source to update the CI, within a time period. The time period is specified by the Effective Duration time in the data refresh rule for the class for the discovery source. In this case, if another authorized discovery source, with a lower priority attempts to update the stale CI attribute, the update is allowed.

If there is a dynamic reconciliation rule for the same CI attribute as in a static reconciliation rule, the dynamic rule takes precedence.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to open the CI Classes hierarchy list.

3.  Select a class for which to create a reconciliation rule.

4.  In the class navigation bar, expand **Class Info** and then select **Reconciliation Rules**.

5.  In the Reconciliation Rules section, select **Add** to create a rule or select an existing rule to edit.

6.  Select the **Static Reconciliation Rule** tile if it appears.

    If [CMDB 360](multisource-cmdb.md) is not enabled, you can't create a dynamic reconciliation rule and the tiles to choose the rule type do not appear.

7.  Fill out the fields on the **Add Data Sources &amp; Prioritize** tab, and then select **Next**.

    |Field|Description|
    |-----|-----------|
    |Active|Check box to activate this reconciliation rule.|
    |Discovery Source|Discovery source that you are configuring this rule for.|
    |Priority|Priority of **Source** within other discovery sources for the specified attributes. Smaller numbers designate higher priority. Discovery sources without a reconciliation rule are assigned the lowest priority.|

    You can add multiple pairs of **Discovery Source** and **Priority**.

8.  Fill out the fields on the **Select Attributes** tab, and then select **Next**.

<table id="table_hlk_ddz_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Apply to all attributes

</td><td>

Authorizes the specified discovery sources to update all attributes of the specified class. **Note:** This rule will be overridden by any rule that applies to a specific attribute. In which case, instead of using this option, you can directly include all attributes for **Attributes**.

</td></tr><tr><td>

Attributes

</td><td>

Attributes, from the current or from a parent class, that the specified discovery sources are authorized to update.

 Available only if **Apply to all attributes** is not selected.

</td></tr><tr><td>

Update with Null

</td><td>

Attributes that the specified discovery sources can update with a null value. By default, authorized discovery sources cannot overwrite a non-null value with a null value.

 Attributes in this list, which are not in the **Attributes** list, are not included with the attributes that the discovery sources can update with a null value.

</td></tr></tbody>
</table>9.  Fill out the fields on the **Set Filter Condition** tab, and then select **Save**.

<table id="table_mqc_22z_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filter Condition

</td><td>

Conditions that CIs must meet for the rule to be applicable.

 For example, to apply this rule only to CIs that are associated with the Finance department, select this condition: **\[Department\] \[is\] \[Finance\]**.

</td></tr></tbody>
</table>    **Note:** The [glide.identification\_engine.enable\_reconciliation\_filter\_before\_update](../reference/properties-id-reconciliation.md) system property determines when filter conditions are applied. By default, those filter conditions are applied after attribute values have changed during payload processing. Set this property to **true** so that Identification and Reconciliation Engine \(IRE\) applies the filter conditions before attribute values change.


### What to do next

-   Select the filter icon and then select:
    -   **Attributes**: To show only reconciliation rules for a specific attribute.
    -   **Discovery sources**: To show only reconciliation rules for a specific discovery source.
-   Select **Preview Rule** to see per attribute, the precedence order between any discovery sources that are authorized to update that attribute and any dynamic reconciliation rules.
-   If [CMDB 360](multisource-cmdb.md) is enabled, you can:
    -   Select **Preview Data** to see all attributes for a specific CI. Also, for each attribute, the current CMDB value and discovery sources reported values for the attribute.
    -   Select **Recompute** to [recompute CI attribute values](../task/recompute-attribute-values.md) after changing reconciliation rules.
-   Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Reconciliation Definitions** to see a list view of all definitions of reconciliation rules.

## Create a dynamic reconciliation rule

A dynamic reconciliation rule uses CMDB 360 data to choose a value such as the largest value that is reported, for updating a CI.

### Before you begin

[CMDB 360](multisource-cmdb.md) must be enabled.

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

### About this task

If the same CI attribute has both, a static reconciliation rule and a dynamic reconciliation rule, the dynamic reconciliation rule has precedence.

A dynamic reconciliation rule supports several rule types, such as largest reported value and most reported value. When applying a dynamic reconciliation rule, IRE processes the current payload and then examines the CMDB 360 data store to select a value with which to update the CMDB. Depending on the dynamic reconciliation rule type, selecting the appropriate value might not be immediately conclusive. For example, there might not be a single value that is most reported, or for some values, the last discovered timestamp isn't reported. Therefore, when necessary, IRE falls back to examining additional details such as last reported, last discovered, and last updated values to select the most appropriate value.

**Note:** You can't add a dynamic reconciliation rule when creating a new child class in the CI Class Manager. You must first save the new child class and then add the dynamic reconciliation rule.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to open the CI Classes hierarchy list.

3.  Select a class for which to create a reconciliation rule.

4.  In the class navigation bar, expand **Class Info** and then click **Reconciliation Rules**.

5.  In the Reconciliation Rules section, click **Add** to create a rule or select an existing rule to edit.

6.  Select the **Dynamic Reconciliation Rule** tile.

7.  On the **Select Rule** tab, select a rule type in the **Dynamic Rule Type** list field, and then click **Next**.

8.  On the **Select Attributes** tab, select the attributes for which to apply the rule.

9.  Select **Next**.

    Attributes that the specified rule type can't be applied to and attributes for which a dynamic reconciliation rule already exists for, don’t appear.

10. Fill out the fields on the **Set Filter Condition** tab, and then select **Save**.

<table id="table_mqc_22z_qlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filter Condition

</td><td>

Conditions that CIs must meet for the rule to be applicable.

 For example, to apply a rule only to CIs that are associated with the Finance department, select this condition: **\[Department\] \[is\] \[Finance\]**.

</td></tr></tbody>
</table>
### What to do next

-   Select the filter icon and then select:
    -   **Attributes**: To show only reconciliation rules for a specific attribute.
    -   **Discovery sources**: To show only reconciliation rules for a specific discovery source.
-   Select **Preview Rule** to see per attribute, the precedence order between any discovery sources that are authorized to update that attribute and any dynamic reconciliation rules.
-   Select **Preview Data** to see all attributes for a specific CI. Also, for each attribute, the current CMDB value and discovery sources reported values for the attribute.
-   [Recompute CI attribute values](../task/recompute-attribute-values.md).
-   Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Reconciliation Definitions** to see a list view of all definitions of reconciliation rules.

