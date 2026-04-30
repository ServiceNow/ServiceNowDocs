---
title: Field normalization and transformation
description: Field Normalization includes normalization and transformation, which are two different ways to alter field values for increased data integrity and reduced duplication.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Field normalization and transformation

Field Normalization includes normalization and transformation, which are two different ways to alter field values for increased data integrity and reduced duplication.

## Normalization

Normalization searches for variations of the same field value and converts them into a single preferred value. By consolidating multiple variations of the same value into a single simple recognizable value, the system eliminates duplicate records and provides better search results. When a process or a user enters a value in a normalized field, the system determines whether to replace it with a normal value. Normalization also automatically adjusts queries to return normalized results and normalizes values in scripts.

While normalization is available for every field in the platform, it works best for descriptive values such as names or standard units of measurement. For example, you might create normalization rules to:

-   Set the CPU type of a computer CI to a standard model name such as Xeon.
-   Set the suffix used for the names of corporations to a standard format such as ServiceNow, Inc..

## Transformation

Transformation converts raw field input values into standardized values that are more meaningful to an organization. Administrators control when transformation happens by defining rules and conditions for specific fields. For example, you might create transformation rules to:

-   Remove suffixes from user names such as Jr. and II.
-   Round computer CI RAM sizes to the nearest whole number such as rounding 4112 MB to 4000 MB.

Transform records make up the rules that define how a field transformation is executed. Order values determine the order in which each rule is evaluated. A check box on each transform enables an administrator to determine where processing stops when a rule evaluates to true.

## Enabling normalization and transformation by field type

Field type records specify which data types are available for normalization and transformation. By default, the system supports normalization and transformation for these field types.

|Field type|Use to normalize|Use to transform|
|----------|----------------|----------------|
|Decimal|false|true|
|Float|false|true|
|Integer|false|true|
|Numeric|false|true|
|String|true|true|
|URL|true|true|

A field type entry applies to all fields whose dictionary entry data type matches the field type entry. Administrators can create additional field type records for other data types as needed.

**Warning:** Avoid creating field type records for fields that store a Sys ID value such as a reference field, field name field, or a table name field. Directly altering a Sys ID value is more likely to produce data corruption and broken references than to produce meaningful standard values. Instead, normalize or transform the display value associated with the Sys ID. For example, normalize the user name instead of the Sys ID of a specific user.

## Identifying normalized fields

The system displays the normalization icon ![Normalization icon](../image/IconNormalization.png) on fields with an associated normalization or transformation record. Users with the normalizer role can click the icon to access the associated normalization or transformation record. Users without the normalizer role instead see a help page. Administrators can configure who sees the normalization icon with a preference called **Restrict to roles**.

-   **[Activate Field Normalization](../task/activate-field-normalization.md)**  
Activate the Field Normalization \[com.snc.field\_normalization\] plugin to install demo data and activate related plugins if they are not already active.
-   **[Enable a field type for normalization or transformation](../task/t_CreateAFieldType.md)**  
Create or modify a normalization field type record to enable a specific field data type for use with normalization or transformation.
-   **[Create a raw field](../task/t_CreateARawField.md)**  
A raw field is a custom field created by an administrator to show the original \(raw\) input in a field on a form after it has been normalized or transformed.
-   **[Normalization and transformation data jobs](normalization-data-jobs.md)**  
The system uses data jobs to change field values during normalization and transformation.
-   **[Normal values](c_WhatFieldNormalizationDoes.md)**  
A normal value replaces similar but ambiguous field values with one standard value.
-   **[Transforms](c_FieldTransformations.md)**  
Transforms update field values by applying a transformation definition to the field contents such as replace text, change case, or round value.
-   **[Default Transform Definitions](../reference/r_DefsIncludedWFieldTransformation.md)**  
The system offers default transform definitions for fields containing text, text numeric, and numeric values.
-   **[Regular expressions and patterns in field normalization rules](c_RegExpsAndPattFldNormalizeRls.md)**  
Field Transformation definitions support the use of regular expressions \(referred to in the platform as **regex**\) and pattern matching for determining the position of characters in a string.
-   **[Domain separation and Field Normalization](domain-separation-field-normalization.md)**  
Domain separation is unsupported in Field Normalization. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Field administration](../../reference-pages/concept/c_IntroductionToFields.md)

