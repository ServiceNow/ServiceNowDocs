---
title: Create a CI class
description: Create a CI class \(table\) that is an extension of an existing CI class. Then create identification and reconciliation rules for the new class.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [CMDB classifications and class dependency, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CI class

Create a CI class \(table\) that is an extension of an existing CI class. Then create identification and reconciliation rules for the new class.

## Before you begin

The class that is being extended must have its **Is\_Extendable** field checked, indicating that the class is extendable.

Role required:

-   sn\_cmdb\_admin or Itil\_admin, and personalize\_dictionary: Required for editing the dictionary table
-   sn\_cmdb\_admin or admin: Full access

## About this task

The CI Class Manager is a centralized location for managing CMDB tables and for creating a class that is derived from another CMDB class. Creating a class requires basic details such as a label and a name. Identification and reconciliation rules are also required to ensure that the class can be successfully identified by the identification engine.

For more information about extending a class and how attributes are derived from a parent class in that process, see Table extension and classes.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Click **Hierarchy** to expand the CI Classes list.

3.  Select the class that the new class is extended from.

4.  Click **Add Child Class**.

    The **Add Child Class** option appears only if the selected class is extendable.

5.  On the **Provide Basic Info** tab, fill out the information and then click **Next**.

<table id="table_mqb_32s_y1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

A unique label for the class \(such as Laptops or Thin Clients\). The label appears on list and form views for the class. Updating the **Label** field also updates the label record in the language file for the current language. See Field Labels in Data dictionary tables.Maximum string length is 80 characters.

</td></tr><tr><td>

Table name

</td><td>

Automatically populated based on the table label and the prefix string 'u\_cmdb\_ci'.

 You cannot modify the prefix; however, you can modify the rest of the table name. The name can contain only lowercase, alphanumeric ASCII characters and underscores \(\_\).

 Maximum string length is 80 characters.

</td></tr><tr><td>

Description

</td><td>

Explanation of the use purpose of the class.

</td></tr><tr><td>

Icon

</td><td>

The icon associated with the class.

</td></tr><tr><td>

Extensible

</td><td>

Indicator of whether this class can be extended.

</td></tr><tr><td>

Principal Class

</td><td>

Denotes whether this class is included in the [Principal Class filter](update-principal-class-filter.md). If this class is included in the Principal Class filter, then CIs from this class appear in CI list views when the Principal Class filter is applied.

</td></tr></tbody>
</table>6.  On the **Add Attributes** tab, click the + sign and enter details for each new class column.

7.  Click **Next**.

    For description of the different columns in the list view, see Dictionary entry form. To designate an attribute as a CI identifier for class identification, double-click the attribute's Identification Rule column and set it to **true**.

8.  On the **Set Identification Rule** tab, examine the **Derived** identification rule and its **Identifier Entries**.

    You can click **Replace** to replace the derived rule with a new identification rule and new identifier entries specific to the new class. See [Identification rules](t_CreateCIIdentificationRule.md) for details about identification rules and identifier entries.

9.  On the **Dependencies** tab, click **Add dependency** to add [dependent rules](../concept/c_ServiceRulesMetadata.md).

    The **Dependencies** tab appears only if there are dependent identification rules for the selected class.

10. On the **Add Reconciliation Rules** tab, click **Add** to create the following rules:

    1.  [Reconciliation Rules](../concept/create-reconciliation-rule.md#)

    2.  [Data Refresh Rules](create-datasource-staleness-rule.md)

11. On the **Add Suggested Relationships** tab, review the diagram of the class derived suggested relationships.

12. Use the filter to display only inbound, outbound, or specific relationship types.

13. To add a suggested relationship for the class:

    1.  Click **New**.

    2.  In the Add Suggested Relationship dialog box, select a **Relationship** and a **Target Class** for the relationship. **This Class** and the **Target Class** become parent or child in the suggested relationship, based on your selection of the **Relationship**.

    3.  Click **Save**.

    When building relationships for the class in the Query Builder, the list of suggested relationships is updated.

14. Click **Done**.


**Parent Topic:**[CMDB classifications and class dependency](../concept/c_CMDBClassifications.md)

**Related topics**  


[Dependent CIs management](../concept/manage-dependent-ci.md)

[CMDB record types](../reference/r_CMDBRecordTypes.md)

[Related Lists of CI components](../reference/r_RelatedListsOfCIComponents.md)

[Reclassify a CI](t_ManuallyReclassifyCI.md)

[Delete CIs](delete-class-records-ci-class-mgr.md)

[View and edit class definitions and metadata](t_ViewTableDefinitions.md)

[Update the list of classes in the Principal Class filter](update-principal-class-filter.md)

[CMDB Identification and Reconciliation \(IRE\)](../concept/c_CMDBIdentifyandReconcile.md)

