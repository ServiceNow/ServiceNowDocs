---
title: Create a CI identification rule
description: Identification rules are used to uniquely identify CIs in the CMDB, as part of Identification and Reconciliation \(IRE\) processes. Each CMDB class can be associated with a single identification rule.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Identification rules, Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CI identification rule

Identification rules are used to uniquely identify CIs in the CMDB, as part of Identification and Reconciliation \(IRE\) processes. Each CMDB class can be associated with a single identification rule.

## Before you begin

You can update a CI identification rule only at the class level that the rule is defined for. You can't update a derived rule.

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

## About this task

In a CI identification rule, specify a CI identifier, and identifier entries and related entries that uniquely identify the CI.

Review the following before creating identification rules:

-   [Identification rules](../concept/c_IdentificationRules.md)
-   [General guidelines for using CMDB Identification](../concept/best-practices-id-reconcile.md)
-   Explore predefined identification rules:
    1.  Navigate to **All** &gt; **CI Class Manager**.
    2.  Select **Hierarchy** and then search and select, for example, the Hardware class.
    3.  In the Hardware bar, expand **Class Info** and select **Identification Rule**.
    4.  Examine all the sections and tiles with the settings of the Hardware class identification rule.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to show the CI Classes list and then select the class for which to create an identification rule.

3.  In the class navigation bar, expand **Class Info** and then select **Identification Rule**.

4.  Select **Edit**, **Add**, or **Replace** \(for a class that has derived the CI identification rule\), in the Identification Rule section to create one.

5.  Fill out the form, and then select **Save**.

<table id="table_rzx_pty_wr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Independent/Dependent

</td><td>

Designation of whether the CI identifier can identify the CI independently of other CIs, or not. **Note:** To set the rule as **Dependent**, you must specify [dependent relationship rules](../concept/create-dependent-relationship.md#) for the selected class.

</td></tr><tr><td>

Name

</td><td>

Name of CI identifier.

</td></tr><tr><td>

Description

</td><td>

Description of the CI identifier.

</td></tr></tbody>
</table>6.  In the Identifier Entries section, select an existing identifier entry to edit, or select **Add** to create one.

7.  In the Identifier Entry dialog box, choose an option and then select **Next**.

    Continue with one of the following three steps according to the option that you selected:

    |Option|Description|
    |------|-----------|
    |Use attributes from main table &lt;table&gt;|Lets you select attributes from the currently selected table \(regular identifier entry\).|
    |Use attributes from another table \(Lookup table\)|Lets you select attributes from any related table, other than the currently selected table \(lookup identifier entry\).|
    |Use attributes from main and another table \(Hybrid\)|Lets you select attributes from both the currently selected table, and from another table \(hybrid identifier entry\).|

8.  **Use attributes from main table &lt;'table'&gt;** option: Set the options on the form and then select **Save**.

    **Search On Table** is preset to the currently selected table in the CI Classes list.

<table id="table_vhc_lh2_hfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Check box that specifies the identifier entry is active. At least one identifier entry in an identification rule must be active for the rule to apply.

</td></tr><tr><td>

Priority

</td><td>

Priority of the identifier entry. Identifier entries are applied based on priority. Rules with lower priority numbers are given higher priority. Identifier entries of identical priorities are applied randomly.You can keep gaps between the priority numbers, so you can assign the unused priority numbers to new entries without modifying the existing priority order.

</td></tr><tr><td>

Criterion Attributes

</td><td>

Set of attributes that uniquely identify the CI. Attributes can belong to the current class, or to a parent class.**Note:** It's possible to add reference fields as a criterion attribute. However, such fields might not always be effective:

-   Reference fields store **sys\_id**s that point to a record in another table, and thus is considered a weak criterion attribute \(in terms of uniqueness\) for the current table.
-   The system detects and then replaces invalid values in a reference field with 'Unknown'. For example, an invalid **Model ID** value is replaced with the value 'Unknown'. Also, if several CIs end up having that same reference field set to 'Unknown', then these CIs become duplicate CIs.


</td></tr><tr><td>

Allow null attribute

</td><td>

When selected, then if at least one criterion attribute isn't null, attempt matching with an identifier entry even if there are criterion attributes that are null.

 Otherwise, all criterion attributes must have values to attempt matching with an identifier entry.

</td></tr><tr><td>

Allow fallback to parent's rules

</td><td>

Allows the identification rules of the CI's parent to be used if a match isn't found for this identification rule. Applies only for dependent identification rules.

</td></tr><tr><td>

Advanced Options

</td><td>

A filter to narrow the set of records that will be searched for a matching CI.

 Available only if the **glide.identification\_engine.enable\_identifier\_optional\_condition** system property is set to **true** \(**false** by default\). In the base system, identifier entries of various classes are preconfigured with advanced options conditions. All these preconfigured conditions in regular identifier entries will automatically apply when you set this property to **true**. Therefore, to avoid unexpected behavior, review those predefined conditions in regular identifier entries before setting this property to **true**.

 For more details about this property, see [Properties for Identification and Reconciliation](../reference/properties-id-reconciliation.md).

</td></tr></tbody>
</table>    **Note:** If criterion attributes have only two attributes and **sys\_class\_name** is one of them \(for example \[name, sys\_class\_name\], \[ip\_address, sys\_class\_name\]\), then the other attribute can't be NULL, even if **Allow null attribute** is enabled. This restriction is due to**sys\_class\_name** being considered a special system matching attribute.

9.  **Use attributes from another table \(Lookup table\)** option:

    1.  Set **Search On Table** to a table other than the currently selected table in the CI Classes list.

        The **Search On Table** must have a reference field to **cmdb\_ci**, otherwise the identifier entry is considered invalid.

    2.  Set the rest of the fields as described in the previous step.

    3.  Select **Advanced options** and enter the information for a lookup identifier \(scroll down if necessary\).

<table id="table_odt_tk2_hfb"><thead><tr><th>

Advanced Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All of these conditions must be met

</td><td>

A filter to narrow the set of records that will be searched for a matching CI.

</td></tr><tr><td>

Enforce exact count match

</td><td>

For lookup identification, match a CI only on exact lookup records count match.When enforced, all lookup items for a CI in the payload must have matching records in the lookup table that reference the same CI:

1.  Only matches CIs that have all the lookup items from the input payload referencing the CI in CMDB.
2.  If there are multiple matches, selects the oldest created CI as the final match.
 When not enforced, one lookup item for a CI in the payload matching a record in the lookup table, is sufficient to consider a match:

1.  Matches any CI that has at least one of the lookup items from the input payload referencing the CI in CMDB.
2.  If there are multiple matches, selects the CIs with the max number of lookup items from the input payload referencing the CI in CMDB.
3.  If there are still multiple matches, selects the oldest created CI as the final match.
For information about how this setting can affect creation of de-duplication tasks for duplicate referenced CIs, see [Detecting duplicate CIs](../concept/id-detect-dup-ci.md).

</td></tr></tbody>
</table>    4.  Select **Save**.

10. **Use attributes from main and another table \(Hybrid\)** option:

    1.  Set the options on the **General Settings** tab as described in previous steps, and then select **Next**.

    2.  On the **Main Table Settings** tab, select the attributes to use from the currently selected table, and then select **Next**.

        **Search On Table** is preset to the currently selected table in the CI Classes list.

    3.  On the **Lookup Table Settings** tab, select a **Search On Table** and then in **Criterion Attributes** select attributes from the specified table. **Search On Table** must have a reference field to **cmdb\_ci**, otherwise the identifier entry is considered invalid.

        You can select **Advanced options** and enter the information for a lookup identifier as described in the previous step \(scroll down if necessary\).

    4.  Select **Save**.

    **Note:** The **Allow null attribute** option in the hybrid option is set to **false**. Therefore, all the selected criterion attributes from both the currently selected table and the lookup table, must have a value. Also, setting optional conditions is available only for the lookup table, and isn't available for the main table.

11. On the Related Entries section, select an existing related entry to edit, or select **Add** to create one.

    1.  Update the Related Entry form and then select **Save**.

<table id="table_h15_brq_m3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Check box that specifies that the related entry is active.

</td></tr><tr><td>

Related table

</td><td>

A related table that references the CI that is being matched.

</td></tr><tr><td>

Referenced field

</td><td>

A referenced field in **Related table** that should store the referenced CI. This field always references the cmdb\_ci table, or a descendent of the cmdb\_ci table.

</td></tr><tr><td>

Priority

</td><td>

Priority of the related entry for the specified **Related table**. Rules with lower priority numbers are given higher priority while matching a related item for specific related table. Related entries for the specified related table with identical priorities are applied randomly.You can keep gaps between the priority numbers, so you can assign the unused priority numbers to new entries without modifying the existing priority order.

</td></tr><tr><td>

Criterion attributes

</td><td>

The set of attributes to uniquely identify the related item. Attributes can belong to the current class, or to a parent class.**Note:** It is possible to add reference fields as a criterion attribute. However, such fields might not always be effective:

-   Reference fields store **sys\_id**s that point to a record in another table, and thus is considered a weak criterion attribute \(in terms of uniqueness\) for the current table.
-   The system detects and then replaces invalid values in a reference field with 'Unknown'. For example, an invalid **Model ID** value is replaced with the value 'Unknown'. Also, if several CIs end up having that same reference field set to 'Unknown', then these CIs become duplicate CIs.
 Select the lock icon to view, add, or remove attributes from the identification rule.

</td></tr><tr><td>

Allow null attribute

</td><td>

If at least one criterion attribute in the related table is not null, allow to attempt matching with an identifier entry even if there are criterion attributes which are null.

</td></tr><tr><td>

Filter conditions

</td><td>

Add conditions to construct a filter to narrow the set of records that will be searched for a matching related item.

</td></tr></tbody>
</table>        **Note:** If criterion attributes have only two attributes and **sys\_class\_name** is one of them \(for example \[name, sys\_class\_name\], \[ip\_address, sys\_class\_name\]\), then the other attribute can't be NULL, even if **Allow null attribute** is enabled. This restriction is due to **sys\_class\_name** being considered a special system matching attribute.


## Example

For example, the pre-defined **Hardware Rule** applies to the Hardware \[cmdb\_ci\_hardware\] table. It has an identifier entry with the criterion attribute **Serial Number, Serial Number Type** and its **Search on table** field is set to **Serial Number**.

The following payload snippet adds a CI to the **cmdb\_ci\_linux\_server** class that is a child of the Hardware class. It also shows how you can add related items in the payload for which you should create **Related Entries** on the CI Identifier page for the Hardware \[cmdb\_ci\_hardware\] table:

```

{
    "items": [
        {
            "className": "cmdb_ci_linux_server",
            "lookup": [
                {
                    "className": "cmdb_serial_number",
                    "values": {
                        "serial_number": "VMware-42 21 e3 da 44 14 5a a6-56 48 2b 0a 28 53 42 4c",
                        "serial_number_type": "system",
                        "valid": "true"
                    }
                },
                {
                    "className": "cmdb_serial_number",
                    "values": {
                        "serial_number": "4221E3DA-4414-5AA6-5648-2B0A2853424C",
                        "serial_number_type": "uuid",
                        "valid": "true"
                    }
                },                }
            ],

    “related": [
                {
                    "className": "cmdb_ci_ucs_chassis",
                    "values": {
                        “name": “chassis1",
                        “category": “category1",
                        “short_description": “My Chassis 1"
                    }
                },
                {
                    "className": "cmdb_ci_ucs_chassis",
                    "values": {
                        “name": "chassis2",
                        "category": "category2",
                        "short_description": "My Chassis 2"
                    }
                },    }
     ],

            "values": {
                ......
                "name": "xpolog2.lab3",
                "os_name": "Linux",
                "output": "Linux xpolog2.lab3 2.6.32-431.el6.x86_64 #1 SMP Fri Nov 22 03:15:09 UTC 2013 x86_64 x86_64 x86_64 GNU/Linux",
                "serial_number": "VMware-42 21 e3 da 44 14 5a a6-56 48 2b 0a 28 53 42 4c",
                "sys_class_name": "cmdb_ci_linux_server"
            }
        }
    ]
}
                         
```

When the **Hardware Rule** is applied, the Serial Number \[cmdb\_serial\_number\] table is searched for a match with the values specified within the `lookup` key. Unless **Enforce exact count match \(Lookup\)** is checked, it isn't necessary for every lookup key to return a match, as long as there is at least one match. If all matches reference the same CI, then that CI is considered to be the existing CI record. If no match is found, then the identification search continues to the next rule entry. If after all the rules are exhausted without finding a match, a new CI record is created in the database.

## What to do next

You can optionally [create an inclusion rule](create-id-inclusion-rule.md) to narrow the scope of CIs that are included in identification.

**Parent Topic:**[Identification rules](../concept/c_IdentificationRules.md)

**Related topics**  


[Create an identification inclusion rule](create-id-inclusion-rule.md)

[General guidelines for using CMDB Identification](../concept/best-practices-id-reconcile.md)

