---
title: Field administration
description: The individual pieces of data in a record are called fields. You enter data in fields on the form or by using the list editor. Administrators can create new or modify existing fields.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Field administration

The individual pieces of data in a record are called fields. You enter data in fields on the form or by using the list editor. Administrators can create new or modify existing fields.

You can enter data in fields by using the list editor or by using a form. In form view, fields appear as fields in the form, and in list view they appear as columns of data in the table. Administrators can create new fields or change the type of existing fields.

## Field administration considerations

-   If you edit a field on a child table that is present on the parent table, it's also changed in the parent table and all other child tables.
-   Kanji characters aren't currently supported. If a table column identifier is created using Kanji characters, it's ignored in any update or insert operation from a form.
-   When you create a custom field, use one of the supported field types described in [Field types](../reference/r_FieldTypes.md). Other field types, such as User Input, are for internal use only and aren't supported for custom fields.
-   The Field Name and Table Name field types have a built-in dependency relationship. For example, Field Name fields don't exist independently; they require a Table Name field. Also, Field Name fields always contain a value, which is sys\_id by default. You can't set the value for a Field Name field to None, even if you apply the attribute allow\_null=true.
-   If you need to change the data type for a field, create a new column using the new data type, copy the data from the old column to the new column via a background script, and then rename the original column label.
-   Various conditions can cause a field to be read-only. For more information, see the [Determining why a field is Read Only \(grayed out and not editable\) \[KB0783470\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0783470) article in the Now Support Knowledge Base.
-   Fields may not display on forms as expected. For more information, see the [Troubleshooting fields not appearing on forms \[KB0547219\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547219) article in the Now Support Knowledge Base.

-   **[Field types](../reference/r_FieldTypes.md)**  
These field types are available to administrators when creating fields or changing the type of existing fields.
-   **[Add and customize a field in a table](../../field-administration/task/t_CreatingNewFields.md)**  
Administrators can add new fields to a table to store and display data.
-   **[Field normalization and transformation](../../field-administration/concept/c_FieldNormalization.md)**  
Field Normalization includes normalization and transformation, which are two different ways to alter field values for increased data integrity and reduced duplication.
-   **[Data policy](../../field-administration/concept/c_DataPolicy.md)**  
Data policies enable you to enforce data consistency by setting mandatory and read-only states for fields.
-   **[Data lookup and record matching support](../../field-administration/concept/c_DataLookRecMatchSupport.md)**  
The data lookup and record matching feature enables administrators to define rules that automatically set one or more field values when certain conditions are met.
-   **[Dynamic Schema](../../field-administration/concept/dynamic-schema.md)**  
Define a hierarchy of categories, groups, and attributes and enable users to select groups of attributes on a record.

**Parent Topic:**[ServiceNow AI Platform forms, fields, and lists](../../general/concept/now-platform-forms-fields-lists.md)

