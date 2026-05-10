---
title: Create CI types for Service Mapping and Discovery
description: Create CI types \(or CI classes\) for applications and devices, which Service Mapping and Discovery do not support by default.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create CI types for Service Mapping and Discovery

Create CI types \(or CI classes\) for applications and devices, which Service Mapping and Discovery do not support by default.

## Before you begin

Role required: service\_mapping\_admin, personalize\_dictionary, or admin

Verify that there is no existing CI type for this application or device.

## About this task

All applications and hosts in your organization must have a corresponding configuration item \(CI\) type, which is necessary for discovering and processing applications and hosts correctly.

**Note:** The Discovery and the CMDB interface refers to CI types as CI classes.

A wide range of preconfigured CI types that cover most commonly used applications are available to you. If your organization uses a less known or proprietary application that does not have a corresponding CI type, you must create it.

A CI type is a generic notion that is used by several ServiceNow applications, but there are some attributes that are specific to Service Mapping and Discovery.

A CI type \(or class\) contains several important definitions that apply to all CIs belonging to it, such as:

-   CI attributes are added as fields to the CMDB tables.
-   Identifiers help Service Mapping and Discovery to differentiate between new and existing CIs. For example, if there is an Apache Web Server CI type defined in the CMDB, and Service Mapping and Discovery both discover an Apache Web Server CI, it processes it using identifiers. It then recognizes it as an updated version of the Apache Web Server CI that already exists in the system, not a new Apache Web Server CI.
-   There are [reconciliation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/r_ReconciliationRulesPrinciples.md) that help the ServiceNow platform to consolidate CI attributes received from different applications correctly. These rules are necessary for organizations where more than one application participates in the discovery process. Reconciliation rules define how attributes of the same CI discovered by different discovery sources are merged. For example, Service Mapping discovers the version and home directory attributes of an Apache Web Server CI, while Discovery discovers the version and patch level attributes for the same Apache Web Server CI. The ServiceNow AI Platform applies the reconciliation rule and as a result Service Mapping does not overwrite the attributes found by Discovery.
-   Related items, both CIs and non-CIs, serve as a reference and provide additional information about the CI. For example, you can define a serial number, a port and an network APR table as related items for a hardware server. The system does not use these items for identification. After you configure related items for the CI type, you can use horizontal discovery for CIs of this type together with their related items. For information, see [Discover related items together with the main CI](add-related-cis-to-the-main-ci-pattern.md).

    **Note:** Non-CIs are items that do not extend the Configuration Item \[cmdb\_ci\] table. Examples of non-CIs are ports, serial numbers, or Network ARP tables.

-   CMDB stores CI class in the form of a hierarchy where some CI classes are parents to other CI classes, who automatically derive their parent's attributes in addition to attributes you configure specifically for child CI classes. CI class hierarchy is used widely for configuring CI behavior, relationships, and display. In this example, the Apache Web Server CI is a child of the Web Server CI and derives many attributes from its parent, such as name, version, model ID. By default, child CI classes inherit identifiers from their parent CI classes.

In addition to these CI type definitions, the horizontal discovery process uses a CI classification to define to which CI type a CI belongs. Create a device CI classification if you create a CI type for devices using SNMP and a process CI classification for an application CI type.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  To use an existing CI type as a parent for the new CI type, click **Hierarchy** to display the CI Classes list.

3.  Click the context menu for the required CI type and select **Add Child Class**.

4.  [Create a table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/t_CreateATable.md)to store the CI type attributes:

<table id="table_fcb_myv_dt"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

CI type name. For example, Apache Web Server.

</td></tr><tr><td>

Name

</td><td>

The table name. For example, cmdb\_ci\_apache\_web\_server.

 Use a name similar to the other CMDB classes \(for example, `u_cmdb_ci_laptop`\).

</td></tr><tr><td>

Extends table

</td><td>

The table name of the parent CI type.All CI types are extensions of the Configuration Item \[cmdb\_ci\] table or its child tables. For example, if the new class is Laptops, which is a subclass of Computers, select the cmdb\_ci\_computer table. If the new class is a top-level class, select the cmdb\_ci table.

 The most commonly used parent CI types are:

-   cmdb\_ci - basic
-   cmdb\_ci\_database - for databases
-   cmdb\_ci\_app\_server - for application servers
-   cmdb\_ci\_infra\_service - for infrastructure services
-   cmdb\_ci\_endpoint\_inclusion - for entry points of the inclusion type
-   cmdb\_ci\_appl - for applications
-   cmdb\_ci\_web\_server - for web servers
-   cmdb\_ci\_lb - for load balancers
-   cmdb\_ci\_endpoint - for entry points


</td></tr></tbody>
</table>5.  Configure how the instance determines if a discovered CI is an upgraded CI existing in the instance or a brand new CI.

    See [Create or edit a CI identification rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_CreateCIIdentificationRule.md) for detailed procedure.

    **Warning:** If there is no CI identification rule for a CI type, Service Mapping discovers CIs belonging to this type, but cannot interpret the results of the discovery process. In this case, the ServiceNow AI Platform rejects the discovery results for these CIs and their information is not updated.

    1.  On the **Identifiers** page, configure the parameters as follows:

        |Field|Description|
        |-----|-----------|
        |Name|Use a meaningful name.|
        |Applies to|Enter the CI type.|
        |Active|Select the check box.|
        |Independent|Clear the check box.|

    2.  Configure the identifier entry parameters as follows:

        |Field|Description|
        |-----|-----------|
        |Criterion attributes|Select the attribute that you want to use for identifying the CI. For example, **Class**, **Installation directory**, or **Serial number**.|
        |Allow null attribute|Select the check box.|
        |Priority|If there is more than one identifier entry, add priority to determine the order in which Service Mapping applies these entries. If none of the identification criteria matches the discovered CI, this CI is new.|

6.  Configure references to other CIs or non-CIs as related items for the CI type.

<table id="table_jdn_c2j_m3b"><thead><tr><th>

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
</table>7.  Configure the instance to consolidate CI attributes received from different data sources correctly.

    See [Create or edit a CI reconciliation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/create-reconciliation-rule.md).

    Configure the following Service Mapping related parameters correctly:

    |Field|Description|
    |-----|-----------|
    |Data source|Select `ServiceWatch`.|
    |Applies to|Select the relevant CI type.|
    |Optional condition|Set a condition if necessary.|

    **Note:** If you do not create a CI reconciliation rule, data discovered by patterns is used to update CI attributes.

8.  Configure the CI classification for your CI type:

    -   For CI types representing applications, perform configuration as described in [Create a Discovery process classification](../../discovery/task/t_CreateAProcessClassification.md).
    -   For CI types representing SNMP devices, perform configuration as described in [Create a Discovery CI classification](../../discovery/task/create-discovery-ci-classification.md).
    **Note:** There is no need to create CI classifications for hosts because these classifications are included in the base system.

9.  For CI types that represent inclusions, define the hierarchy for the new CI type.

    Clear the **Reverse Relationship Direction** check box while performing this configuration.

    See [Create dependent relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/create-dependent-relationship.md).

10. If necessary, customize icons that represent CIs in maps.

    See [Create or modify map icons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dependency-views/t_CreateModifyNGBSMMapIcons.md).


**Parent Topic:**[Discovery patterns used by ITOM Visibility](../concept/c_MappingPatternsCustomization.md)

**Previous topic:**[Password2 encryption for patterns](../concept/password2-encryption-patterns.md)

**Next topic:**[Create entry point types for Service Mapping](t_CreateEntryPoint.md)

