---
title: Create an identification rule for a non-CMDB table
description: To use Identification and Reconciliation Engine \(IRE\) features with supported non-CMDB tables, you must first create identification rules that uniquely identify the table records. Each non-CMDB table can be associated with a single identification rule.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [IRE support for non-CMDB tables, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create an identification rule for a non-CMDB table

To use Identification and Reconciliation Engine \(IRE\) features with supported non-CMDB tables, you must first create identification rules that uniquely identify the table records. Each non-CMDB table can be associated with a single identification rule.

## Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

## About this task

Each identification rule consists of a single identifier for the table, one or more identifier entries, and one or more related entries.

Review the following topics before creating identification rules:

-   [Identification rules](../concept/c_IdentificationRules.md)
-   [General guidelines for using CMDB Identification](../concept/best-practices-id-reconcile.md)

When creating identifier entries, you can configure the **Search on table** and **Criterion attributes** fields on the Identifier Entry form to implement one of the following options:

-   **Regular identifier entry**

    Lets you select attributes from the associated identifier table.

-   **Lookup identifier entry**

    Lets you select attributes from any related table \(Lookup table\), other than the currently selected table.

-   **Hybrid identifier entry**

    Lets you select attributes from both the currently main selected table, and from another table \(Lookup table\).


For non-CMDB tables, only independent identification rules are supported.

## Procedure

1.  Navigate to **All** &gt; **Identification/Reconciliation** &gt; **CI Identifiers**.

2.  In the Identifiers list view, click **New**.

3.  Fill out the Identifier form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of CI identifier.|
    |Applies to|Supported non-CMDB table.|
    |Independent|Must be checked to indicate that the identifier can identify a record independently of other records.|

4.  Click **Submit**.

5.  In the Identifiers list view, locate and open the identifier that you just created.

6.  On the Identifier form, select the **Identifier Entries** tab and then click **New**.

7.  Fill out the Identifier Entry form.

<table id="table_vhc_lh2_hfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Identifier

</td><td>

Preset with the name of the table of the associated identifier.

</td></tr><tr><td>

Search on table

</td><td>

Preset with the label of the table of the associated identifier.

 To create:

-   A regular identifier entry: Set to the identifier table and select **Criterion attributes** from that same table.
-   A lookup identifier entry: Set to another table \(lookup table\) and select **Criterion attributes** from that lookup table.
-   A Hybrid identifier entry: Set to another table \(lookup table\) and then do the following steps.
    -   Select **Criterion attributes** from the lookup table.
    -   Add **Hybrid Entry CI Criterion Attributes** from the current table using background scripts, after saving the rule. For more details, see the 'What to do next' section at the end of this task.
 A lookup table should have a reference to the associated identifier table.

</td></tr><tr><td>

Criterion attributes

</td><td>

Set of attributes that uniquely identify the record. Attributes can belong to the current class, or to a parent class.**Note:** It's possible to add reference fields as a criterion attribute. However, such fields might not always be effective:

-   Reference fields store **sys\_id**s that point to a record in another table, and thus is considered a weak criterion attribute \(in terms of uniqueness\) for the current table.
-   The system detects and then replaces invalid values in a reference field with 'Unknown'. For example, an invalid **Model ID** value is replaced with the value 'Unknown'. Also, if several CIs end up having that same reference field set to 'Unknown', then these CIs become duplicate CIs.


</td></tr><tr><td>

Priority

</td><td>

Priority of applying the identifier entry. Rules with lower priority numbers are given higher priority. Identifier entries of identical priorities are applied randomly.You can keep gaps between the priority numbers, so you can assign the unused priority numbers to new entries without modifying the existing priority order.

</td></tr><tr><td>

Active

</td><td>

Specifies whether the identifier entry is active. At least one identifier entry in an identification rule must be active for the rule to apply.

</td></tr><tr><td>

Enforce exact count match

</td><td>

For lookup identification, match a record only on exact lookup records count match.When enforced, all lookup items for a record in the payload must have matching records in the lookup table that reference the same record:

1.  Only matches records that have all the lookup items from the input payload referencing the record in the table.
2.  If there are multiple matches, selects the oldest created record as the final match.
 When not enforced, one lookup item for a record in the payload matching a record in the lookup table, is sufficient to consider a match:

1.  Matches any record that has at least one of the lookup items from the input payload referencing the record in the table.
2.  If there are multiple matches, selects the records with the max number of lookup items from the input payload referencing the record in the table.
3.  If there are still multiple matches, selects the oldest created record as the final match.


</td></tr><tr><td>

Allow null attribute

</td><td>

When selected, then if at least one criterion attribute isn't null, attempt matching with an identifier entry even if there are criterion attributes that are null.

 Otherwise, all criterion attributes must have values to attempt matching with an identifier entry.

</td></tr><tr><td>

Allow fallback to parent's rules

</td><td>

Allows the identification rules of the record's parent table to be used if a match isn't found for this identification rule. Applies only for dependent identification rules.

</td></tr><tr><td>

Optional condition

</td><td>

A filter to narrow the set of records that will be searched for a matching record.

 Available only if the **glide.identification\_engine.enable\_identifier\_optional\_condition** system property is set to **true** \(**false** by default\). In the base system, identifier entries of various classes are pre-configured with advanced options conditions. All these pre-configured conditions in regular identifier entries will automatically apply when you set this property to **true**. Therefore, to prevent unexpected behavior, review those predefined conditions in regular identifier entries before setting this property to **true**.

 For more details about this property, see [Properties for Identification and Reconciliation](../reference/properties-id-reconciliation.md).

</td></tr></tbody>
</table>    **Note:** If criterion attributes have only two attributes and **sys\_class\_name** is one of them \(for example \[name, sys\_class\_name\], \[ip\_address, sys\_class\_name\]\), then the other attribute can't be NULL, even if **Allow null attribute** is enabled. This restriction is due to**sys\_class\_name** being considered a special system matching attribute.

8.  Click **Submit**.

9.  On the Identifier form, select the **Related Entries** tab and then click **New**.

10. Fill out the Related Entry form.

<table id="related-entry-form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Identifier

</td><td>

Preset with the identifier that this related entry is associated with.

</td></tr><tr><td>

Active

</td><td>

Check box that specifies that the related entry is active.

</td></tr><tr><td>

Related table

</td><td>

A related table \(lookup table\) that references the record that is being matched.

</td></tr><tr><td>

Referenced field

</td><td>

A referenced field in **Related table** with a reference to the associated identifier table.

</td></tr><tr><td>

Criterion attributes

</td><td>

The set of attributes to uniquely identify the related item. Attributes can belong to the current class, or to a parent class.**Note:** It's possible to add reference fields as a criterion attribute. However, such fields might not always be effective:

-   Reference fields store **sys\_id**s that point to a record in another table, and thus is considered a weak criterion attribute \(in terms of uniqueness\) for the current table.
-   The system detects and then replaces invalid values in a reference field with 'Unknown'. For example, an invalid **Model ID** value is replaced with the value 'Unknown'. Also, if several CIs end up having that same reference field set to 'Unknown', then these CIs become duplicate CIs.
 Click the lock icon to view, add, or remove attributes from the identification rule.

</td></tr><tr><td>

Allow null attribute

</td><td>

If at least one criterion attribute in the related table isn't null, allow to attempt matching with an identifier entry even if there are criterion attributes which are null.

</td></tr><tr><td>

Priority

</td><td>

Priority of the related entry for the specified **Related table**. Rules with lower priority numbers are given higher priority while matching a related item for a specific related table. Related entries for the specified related table with identical priorities are applied randomly.You can keep gaps between the priority numbers, so you can assign the unused priority numbers to new entries without modifying the existing priority order.

</td></tr><tr><td>

Optional condition

</td><td>

Filter conditions to narrow the set of records that will be searched for a matching related item.

</td></tr></tbody>
</table>11. Click **Submit**.


## What to do next

To add criterion attributes to a **Hybrid Entry CI Criterion Attributes** field in a hybrid identifier entry, instead of using the Identifier Entry form, you must use background scripts. After saving the identification rule, navigate to **System Definitions** &gt; **Scripts - Background**, and then enter a script that adds the attributes and click **Run script**.

Sample script:

```
var gr = new GlideRecord('cmdb_identifier_entry');
// get the identifier entry you want to update
gr.get('<identifier_entry_sys_id>');
// set the attributes you want in the hybrid rule in a comma separated list
// for example: 'name,serial_number'
gr. hybrid_entry_ci_criterion_attributes='<column_name_1>,<column_name_2>,<etc.>';
gr.update();
```

This process requires the admin role.

**Parent Topic:**[IRE support for non-CMDB tables](../concept/ire-support-non-cmdb-tables.md)

