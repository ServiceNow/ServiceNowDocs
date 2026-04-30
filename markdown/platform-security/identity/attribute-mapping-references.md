---
title: Attribute Mapping references
description: The attribute mappings enables you to use the attributes as a single source of resource to the ServiceNow table fields.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a SCIM Provider Resource Mapping, SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Attribute Mapping references

The attribute mappings enables you to use the attributes as a single source of resource to the ServiceNow table fields.

## Attribute

The attribute for which mapping needs to be defined. For example, **userName**.

![Attribute - userName](../images/attribute-username.png)

## Sub-Attribute

Select the sub-attribute, if any, for which a mapping needs to be defined.

For example, if there is a complex type attribute like **name.familyName**, then the attribute is **name** and the sub-attribute is **familyName**.

For simple attributes like user name, the **Sub-Attribute** value would be **None**.

![Attribute Name and Sub-Attribute Family Name](../images/attribute-name.png)

## Filter Condition

A multi-valued attribute can have additional information that can be specified by using a Filter Condition. The choices for the filter condition are populated using the schemas defined by the SCIM Provider.

For example, the **phoneNumbers** attribute has multiple types like work, mobile, home, and so on.

You can specify a Filter Condition from a set of possible values. For example, the **phoneNumber** attribute can have the Filter Condition as **type eq "mobile"**.

![Attribute Phone Number with Filter Condition Mobile](../images/attribute-phonenumber-mobile.png)

The **phoneNumber** attribute can instead have a Filter Condition as **type eq "work"**.

![Attribute Phone Number with Filter Condition Work](../images/attribute-phonenumber-work.png)

## Database Field Name

If the direct attribute mapping option is chosen, then this attribute needs to be defined. The **Database Field Name** field represents the ServiceNow field name that is mapped with the SCIM Attribute.

For example, the **username** SCIM Attribute can be mapped to a user as the **Database Table Name** field, and to the user ID field as the **Database Field Name** field.

![Database Field Name](../images/attribute-databasename.png)

You can also dot-walk using the **Database Field Name**. For example, the **department** SCIM Attribute can be mapped to the **Department Name** field.

![Attribute - Dot walk](../images/attribute-dot-mapping.png)

Here the Database Table is **User** and the Database field Name is **Department Name**.

![Attribute - Department Name](../images/attribute-departmentname.png)

## Default Value

The default value is passed to the SCIM Provider if direct attribute mapping of that field returns null. The default value can also be used to return a hard-coded value.

In the case of a hard-coded value, the database table name and field name should be **None**.

For example, the primary sub-attribute value of work email can be hard coded as **true**.

![Attribute Default Value](../images/attribute-default-value.png)

## Script

The script is used to fetch the attribute value. The return type of the script should be always a string, or a JSON converted as a string. The output of the script should be in the proper format as expected by the provider for that attribute.

The following is a sample script for a multi-valued attribute.

![Attribute Script](../images/attribute-script.png)

The output of the script should have a stringified JSON Array.

The following is a sample Script of a simple-valued Attribute.

![Attribute Employee Number - Run script](../images/attribute-employeenumberscript.png)

The output of the script should be a string.

