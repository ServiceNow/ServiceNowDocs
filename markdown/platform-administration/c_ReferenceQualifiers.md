---
title: Reference qualifiers
description: Use reference qualifiers to filter the data that is returned for a reference field.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Reference field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Reference qualifiers

Use reference qualifiers to filter the data that is returned for a reference field.

A [reference field](../../../administer/field-administration/concept/c_ReferenceField.md) stores a link \(reference\) to a field on another table, making the records/fields in the referenced table available to the form containing the reference field.

For example, the **Assigned to** field on the Incident table is a reference to the User \[sys\_user\] table. By default, all values for the field that is being referenced appear in the [reference lookup](../../../administer/field-administration/concept/c_ReferenceLookup.md) and can be directly accessed through the reference field \(type ahead\). Expanding on the prior example, if a reference qualifier is not defined, all users in the User table appear in the reference lookup. Including those users that are inactive. Sometimes, this might be the desired functionality. In other cases however, only a subset of the available values may be desired. In this case, create a reference qualifier to filter the available data so that only the desired values are returned and made available to the form. Such as only the active users or users that have a specific role. Reference qualifiers are robust and can consist of simple AND/OR conditions, inline JavaScript, or complex [script include](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

You can modify the reference qualifier for a table, and any table based on that table \(parent or extended\), by defining a reference qualifier through the [Dictionary Entry](../../../administer/managing-data/concept/c_DataDictionaryTables.md) form. You can also modify the reference qualifier only on an extended table and its children \(not the parent table\), through a [dictionary override](../../../administer/data-dictionary-tables/concept/c_DictionaryOverrides.md). You can only define a single reference qualifier per field, per form/table. Reference qualifiers are not applicable to condition builders. For information on using filtering in condition builders, see [Create a dynamic filter option](https://www.servicenow.com/docs/access?context=t_DynamicFilterOptions&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

**Note:**

-   Creating reference qualifiers requires knowledge of the underlying ServiceNow [data model](../../../administer/table-administration/concept/c_TableAdministration.md) \(tables and fields\) and knowledge of the [Web services](https://www.servicenow.com/docs/access?context=r_AvailableWebServices&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) and [Scripts](https://www.servicenow.com/docs/access?context=c_Script&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).
-   To restrict what data specific users can access, use ACLs not reference qualifiers.

You can define a reference qualifier using one of the following methods.

## Simple reference qualifier

Simple reference qualifiers use AND/OR statements \(conditions\) to create simple filters. Use simple reference qualifiers when filtering on conditions such as whether a company is active, a user has a specific role, and/or a caller is in a specific time zone. Simple reference qualifiers can have a maximum of 13 reference qualifier conditions. For additional information on how to use condition builders, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

![Simple reference qualifier](../image/SimpleRefQualifier.png "Simple reference qualifier example")

## Dynamic reference qualifiers

Dynamic reference qualifiers enable you to use a [Create a dynamic filter option](https://www.servicenow.com/docs/access?context=t_DynamicFilterOptions&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to run a query against a reference field to filter the returned data set. Dynamic filter options are stored filters that can contain [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US), JavaScript, or script includes, and can be used in multiple dynamic reference qualifiers. Changes made to a dynamic filter option automatically apply to all reference qualifiers that use the same dynamic filter option. Use this type of reference qualifier when you want to use the same filter on multiple forms or to provide filter functionality to "non-code savvy" implementers.

The base instance provides several OOB dynamic filter options. If a dynamic filter option that meets your needs does not exist, you can create a new dynamic filter option that is specific to your requirements. An example of an OOB dynamic filter option is the reference qualifier on the **Model ID** field on a configuration item form, such as the Computer form. The reference qualifier calls the **CI Model Qualifier** dynamic filter option, which in turn calls the ModelAndCategoryFilters script include. This script include filters the data set based on the class of the CI. The only options for the model ID are options that belong to the same class as the current CI. For example, only CIs that belong to the Computer class are available in the **Model ID** field on the Computer form.

To locate the available dynamic filter options, navigate to **System Definition** → **Dynamic Filter Options**. In the right-corner of the Dynamic Filter Options list, click the filter icon and create the filter condition `Available for ref qual is true`. All dynamic filter options that can be used in dynamic reference qualifiers appear.

![Dynamic reference qualifier](../image/DynamicRefQualifier.png "Dynamic reference qualifier example")

## Advanced reference qualifier

Advanced reference qualifiers enable you to define an inline encoded query string or JavaScript \(actual code or the name of an existing script include or business rule\) filter directly in the **Reference qual** field of the reference qualifier. Similar to the other reference qualifier types, when the form loads, the filter is executed, and only the records that match the filter appear in the reference field. Use this type of reference qualifier for implementations that only require a simple, unique filter, that cannot be handled by a simple reference qualifier, and is not used across multiple reference fields.

**Note:** As a good practice, make JavaScript calls to functions in a script include instead of a global business rule.

An example of an encoded query string is `vendor=true`, which returns all companies that are designated as vendors. Entering this string is the same as using the condition builder as shown in the example for the simple reference qualifier. For additional information on valid encoded query string syntax and examples, see [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

![Encoded query string in an advanced referenced qualifier](../image/AdvancedRefQualifierString.png "Advanced reference qualifier examples")

An example of a JavaScript call is `javascript:new myScriptInclude().my_refqual()`. This code calls the function my\_refqual\(\) in the script include myScriptInclude\(\). The function must return a query string that can filter the options available on a reference field.

**Note:** You can also use encoded JavaScript filters such as `javascript:'u_active=true^' + "u_hr_service="+current.hr_service` in reference qualifiers.

In another example, if you are trying to filter based on the current company, you don't have use a lookup script but can simply add this line to your dynamic qualifier:

```
return "company=" + current.company;
```

You can also simplify this and use an advanced reference qualifier instead of a dynamic one:

```
javascript:"company=" + current.company
```

![Encoded query string in an advanced referenced qualifier example 2](../image/Business_service_advanced_view.png)

For an additional example, configuring the reference field to show only users of a specific group, see the [How to select only users of a specific group into a reference field \[KB0831564\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0831564) article in the Now Support Knowledge Base

.

## Related lists and reference qualifiers

When a field appears on multiple [Related lists](https://www.servicenow.com/docs/access?context=c_RelatedLists&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) on a single form view, it may be necessary to validate which related list is being referenced to properly build the reference qualifier for the field. In this situation, [configure the list control](../../../administer/list-administration/task/t_ConfigureListControls.md#) for the related list and enter a unique tag in the **List edit tag** field. This tag value is available to filter scripts as a variable named *listEditRefQualTag*. The following script include code is an example of a function that uses this type of tag.

```
// Advanced reference qualifier on the CI Relationship Child field that takes into account
// the related list that we are editing the child field on, if the field is being edited
// from a tagged related list. 
 
 cmdb_rel_ci_child_refQual:function(){ 
 
  if(listEditRefQualTag =="application") return "sys_class_name = cmdb_ci_appl";
 
  if(listEditRefQualTag =="database") return "sys_class_name = cmdb_ci_database"
 
  }
```

## Using Javascript current syntax in reference qualifiers

`current` is a JavaScript object that contains the fields and field values of the active \(current\) record. For forms, this is the record that is displayed \(loaded\) in the form. Within advanced and dynamic reference qualifiers, you can use the JavaScript `current` object to define filters such as `javascript:"company=" + current.company`.

This JavaScript, within a reference qualifier, only returns the records from the referenced table that are equal to the company field value of the current record. So, if the value that appears in the **Company** field is Acme, the JavaScript returns all reference field records whose company value is equal to Acme \(company="Acme"\). If you then bring up a record whose company value is "ViewRite", the JavaScript resolves to company="ViewRite."

All fields within the currently loaded form \(tables\) are available for use with the `current` object. Use [dot-walking](https://www.servicenow.com/docs/access?context=c_DotWalking&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to access values in a table, including the referenced table. For example, on the Incident form, the **Assigned To** field references the User table. To access the email address of the user, use the following syntax: `javascript:"emailAddress=" + current.assigned_to.email`.

**Related topics**  


[Create a dynamic filter option](https://www.servicenow.com/docs/access?context=t_DynamicFilterOptions&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

[Create scripted filters](https://www.servicenow.com/docs/access?context=t_ScriptedFilters&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

[CMDB classifications](https://www.servicenow.com/docs/access?context=c_CMDBClassifications&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

