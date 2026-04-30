---
title: Create a SCIM attribute mapping
description: Create a SCIM attribute mapping and use it as a single source of resource to the ServiceNow table fields.
locale: en-US
release: zurich
product: Identity
classification: identity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create a SCIM Provider Resource Mapping, SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Create a SCIM attribute mapping

Create a SCIM attribute mapping and use it as a single source of resource to the ServiceNow table fields.

## Before you begin

Roles required: admin

## About this task

The following are the attribute mapping types and their descriptions.

|Attribute mapping type|Description|
|----------------------|-----------|
|Direct|The SCIM attribute is populated with the help of the **Database Table Name** and **Database Field Name** fields.|
|Constant|The SCIM attribute is populated with the help of a specified default value.|
|Script/Custom|The SCIM attribute is populated with the help of the return value of a script. This attribute requires enabling the run script option.|

**Note:**

-   The password attribute is not supported
-   A sample attribute mapping for the User and Group resources is part of the base system. You can use and configure the mappings based on your requirements, or you can create a new record.

## Procedure

1.  Navigate to **All** &gt; **SCIM Client** &gt; **SCIM Provider Resource Mapping**.

2.  Selected the SCIM Resource Mapping that is created for the configuration.

3.  In the  SCIM Attribute Mappings  related list, click  **New**.

    ![SCIM Provider Resource Mapping](../images/new-attribute-mappings.png)

4.  On the form, fill in the fields.

<table id="table_qrj_kgy_ctb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider Resource Mapping

</td><td>

Attribute mapping for a Provider-resource combination.

 If this field is not populated automatically, then use the search option. Select the Provider Resource Mapping record.

</td></tr><tr><td>

Schema Name

</td><td>

Schema name of the SCIM attribute for which the mapping must be defined.

 For example, **urn:ietf:params:scim:schemas:core:2.0:User**.

</td></tr><tr><td>

Attribute

</td><td>

[Attribute](../reference/attribute-mapping-references.md#section_sbw_3jm_htb) for which the mapping must be defined. For example, **userName**.

</td></tr><tr><td>

Sub-Attribute

</td><td>

[Sub-Attribute](../reference/attribute-mapping-references.md#section_o4h_cmm_htb) \(if any\) for which the mapping must be defined.

 For example, if there is a complex type attribute like **name.familyName**, then the attribute is **name** and the sub-attribute is **familyName**.

</td></tr><tr><td>

Field Type

</td><td>

The SCIM Attribute data type. This field is auto-populated from the schemas defined by the SCIM Provider.

 For example, **boolean**.

</td></tr><tr><td>

Multi-Value

</td><td>

Multiple values that are assigned to the attribute. An attribute can have multiple values like work email, home email, or another email.

 For example, **emails**.

 This field is populated using the schemas defined by SCIM Provider.

</td></tr><tr><td>

Filter Condition

</td><td>

Some multi-valued attributes can have additional information that can be specified by using a [Filter Condition](../reference/attribute-mapping-references.md#section_gfm_ymm_htb). The choices of filter condition are populated using the schemas defined by the SCIM Provider.

 For example, the **phoneNumbers** attribute has multiple types like work, mobile, home, and so on

</td></tr><tr><td>

Unique

</td><td>

Option to uniquely identify a resource between the SCIM Client and SCIM Provider systems. Multi-valued attributes cannot be marked as unique.

 For example, for a User Resource, the **username** attribute can be made unique.

</td></tr><tr><td>

Database Table Name

</td><td>

Use this field to map the attribute table name to the ServiceNow table name. If you choose direct attribute mapping, you must define this field.For example, the **username** SCIM Attribute can be mapped to the **User** field in the **Database Table Name** field.

</td></tr><tr><td>

Database Field Name

</td><td>

The[Database Field Name](../reference/attribute-mapping-references.md#section_a1t_4sm_htb) field maps the SCIM attribute to the ServiceNow field name to be mapped with the SCIM Attribute. If you choose direct attribute mapping, you must define this field.

 For example, the **username** SCIM Attribute can be mapped to the **User ID** field in the **Database Field Name** field.

</td></tr><tr><td>

Default Value

</td><td>

Details about the [default value](../reference/attribute-mapping-references.md#section_e2t_zvm_htb) that is passed to the SCIM Provider.

 Can be used if the direct attribute mapping of the field returns null, or if the default can be used to return a hard-coded value.

 In the case of a hard-coded value, the database table name and field name should be **None**.

 For example, the primary sub-attribute value of work email can be hard-coded as **true**.

</td></tr><tr><td>

Run Script

</td><td>

Option to fetch the value of the attribute via script.

 This option is required for the multi-valued attributes that don’t contain a filter condition. For a complex type of attribute, a script can supply the value at an attribute or sub-attribute level.

 For example, the **Members** attribute of group resource has no filter condition. So, the script option should be defined on the parent attribute level of the **Members** attribute.

</td></tr><tr><td>

[Script](../reference/attribute-mapping-references.md#section_hpd_1wm_htb)

</td><td>

Script that is used to fetch the attribute value.

 The return type of script should be a string, or a JSON converted as a string.

 The output of the script should be in the proper format as expected by the provider for that attribute.

</td></tr></tbody>
</table>5.  Click **Submit**.


