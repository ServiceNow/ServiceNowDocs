---
title: Identification rules
description: The CMDB identification process relies on identification rules to uniquely identify CIs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Identification rules

The CMDB identification process relies on identification rules to uniquely identify CIs.

An identification rule applies to a CI class and consists of a single CI identifier and one or more identifier entries and related entries, each with a different priority. Each identifier entry defines a unique attribute set with a specific priority and each related entry defines rules for identifying related items. Create strong identification rules that are set with the highest priority for the strongest identifier entries and related entries.

The identification process and identification rules use the CI's attributes for identification:

-   **Unique attributes**

    Designated sets of criterion attribute values of a CI that can be used to uniquely identify the CI. Unique attributes can be from the same table or from derived tables.

-   **Required attributes**

    Designated attributes of a CI that cannot be empty.


## Derivation across the CMDB hierarchy

If no identification rule is explicitly defined for a child class, then the child class derives its identification rule, including any associated identification entries and related entries, from its parent class. Later, an own identification rule can be explicitly defined for the child class. In that case, the identification rule that was initially derived from the parent class, including any associated identification entries and related entries, is no longer in effect at the child class. Also, you must explicitly add identification entries and related entries in the newly created identification rule at the child class.

For example: The **Hardware** class identification rule has a related entry for the **Software Instance** table. This identification rule, including its associated related entry for the **Software Instance** table, is derived by the **Computer** class. If you then create a new identification rule for the **Computer** class, it overwrites the identification rule that was derived from the **Hardware** class. Therefore, the **Hardware** class identification rule, including its associated related entry for the **Software Instance** table, is no longer in effect for the **Computer** class. If the same related entry is needed, you must explicitly add a related entry for the **Software Instance** table in the newly created identification rule for the **Computer** class.

## Identification rule types

CI dependency is specified in the CI Class Manager by the dependent relationship rules for the CI's class:

-   **Independent CIs**

    CIs, such as Server CIs, which exist on their own and are not dependent on any other CIs.

-   **Dependent CIs**

    CIs which depend on a relationship to another CI and can't exist on their own in the absence of the dependent relationship. For example:

    -   **Network Adapter** CIs can't exist meaningfully without the **Hardware** CIs that contain them.
    -   **Application** CIs can't exist on their own without the **Server** CI they are hosted on.

The steps for identifying dependent CIs can be different from the steps for identifying independent CIs. This difference is reflected in the differences between dependent identification rules and independent identification rules:

-   **Independent identification rule**

    A rule that identifies a CI based on the CI's own attributes, independently of other CIs or relationship.

-   **Dependent identification rule**

    A rule in which identifying a CI requires identifying a dependent CI first. A CI can have dependency on one or more CIs, and a dependent CI can have only a single parent CI with dependency. The relationship types between the CI and its dependent CIs are also included in the identification process. To help with the identification process of dependent CIs, [create dependent relationships](create-dependent-relationship.md#) that define the dependency chain within CI types.

    The payload used for identification of a dependent CI, can include a relationship with a qualifier chain. For such relationship, if there is a matching parent/child pair, the system compares the qualifier chain in the payload, with the qualifier chain of the CIs in the database. If there is a difference, the qualifier chain in the database is updated to match the qualifier chain in the payload for that relationship.


## Identifier entries

You can configure an identifier entry to match a CI not only based on the CI's own attributes \(field-based identification\) but also based on the CI's related list \(lookup-based identification\) such as **Serial Numbers** or **Network Adapters**. The lookup table that is used for identification, needs to have a reference field that points to **cmdb\_ci**.

There are three types of identifier entries:

-   **Regular identifier entry**

    Identification is based on CI's own attributes that uniquely identify the CI.

-   **Lookup identifier entry**

    Identification uses a lookup table \(related table\) which can be any table that has a reference to the CI that is being identified. After you select a related lookup table, you select identifier attributes from the related table that reference either the cmdb\_ci table itself, or one of its descendants.

    If the lookup records don't already exist, then they are inserted in the lookup table referenced in the identifier entry.

-   **Hybrid identifier entry**

    A combination of both, a regular identifier entry and a lookup identifier entry.

    Example: When discovering virtual machines in a cloud environment which might contain two virtual machines with an identical set of serial numbers. A lookup identifier entry for the Hardware table such as `[Table: Serial Number, Criterion Attributes: Serial Number, Serial Number Type]` cannot uniquely identify these two virtual machines. However, a hybrid identifier entry such as `[Table: Serial Number, Criterion Attributes: Serial Number, Serial Number Type + (Name field from main Hardware table)]` can uniquely identify the two virtual machines.


## Guidelines for lookup tables

Follow these guidelines when specifying a lookup table in an identifier entry.

1.  Ensure that lookup tables reference the cmdb\_ci table.
2.  It is preferable to enforce exact count match \(check box **Enforce exact count match \(Lookup\)**\) for a stronger identification rule. During lookup identification, this option enforces matching only on exact lookup records count match. See [Create a CI identification rule](../task/t_CreateCIIdentificationRule.md) for more details.
3.  Do not create conflicting identification rules especially for lookup-based rule.

    Example: In a CI Identifier for the Hardware class, you specify a lookup-based rule for the Network Adapter class and you also define a CI Identifier for the Network Adapter class. Duplicates might potentially be created in the Network Adapter table, because there are contradicting rules to identify a unique CI in that table:

    -   One rule that looks only at criterion attributes \(CI identifier rule\)
    -   Another rule that looks at criterion attributes and referenced sys\_id \(lookup rule\).

Example: CI with related items that needs to be inserted - sysId is available.

```
var payload = {
    items: [{
        className:'cmdb_ci_linux_server',
       related: [{
              className:'cmdb_ci_spkg',
              values: {
                name:'package1',
                version:'version1'
                }
        }],
        values: {
            sys_id:'194876usytrr65378098'
        }
}]
};
```

## Related entries

You can define related entries which are rules that are based on related CIs. A related entry is based on a related table which can be any table \(CMDB or non-CMDB\) that has a reference to the CI that is being identified. Related entries let you create or update records on other tables in which the data is associated with the CI being identified by the identifier entries. Related entries are not used to directly identify CIs.

After you select a related table for the rule, the list in **Referenced field** is populated with fields from the related table that reference either the cmdb\_ci table itself, or one of its descendants.

A related entry for a class is derived by child classes for which no related entries are specified.

-   **[Create a CI identification rule](../task/t_CreateCIIdentificationRule.md)**  
Identification rules are used to uniquely identify CIs in the CMDB, as part of Identification and Reconciliation \(IRE\) processes. Each CMDB class can be associated with a single identification rule.
-   **[Create an identification inclusion rule](../task/create-id-inclusion-rule.md)**  
Narrow the scope of CIs that are included in the identification process by creating an identification inclusion rule.
-   **[General guidelines for using CMDB Identification](best-practices-id-reconcile.md)**  
Review the following general guidelines for using CMDB Identification effectively.

**Parent Topic:**[Configuring CMDB Identification and Reconciliation](configuring-ire.md)

**Related topics**  


[Relation qualifier](c_RelationQualifier.md)

