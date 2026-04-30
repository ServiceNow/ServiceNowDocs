---
title: Exploring field administration
description: You can enter data in fields by using the list editor or by using a form. In form view, fields appear as fields in the form, and in list view they appear as columns of data in the table. Administrators can create new fields or change the type of existing fields.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Exploring field administration

You can enter data in fields by using the list editor or by using a form. In form view, fields appear as fields in the form, and in list view they appear as columns of data in the table. Administrators can create new fields or change the type of existing fields.

## Field administration considerations

-   If you edit a field on a child table that is present on the parent table, it's also changed in the parent table and all other child tables.
-   Kanji characters aren't currently supported. If a table column identifier is created using Kanji characters, it's ignored in any update or insert operation from a form.
-   When you create a custom field, use one of the supported field types described in [Field types reference](../reference/r_FieldTypes.md). Other field types, such as User Input, are for internal use only and aren't supported for custom fields.
-   The Field Name and Table Name field types have a built-in dependency relationship. For example, Field Name fields don't exist independently; they require a Table Name field. Also, Field Name fields always contain a value, which is sys\_id by default. You can't set the value for a Field Name field to None, even if you apply the attribute allow\_null=true.
-   If you need to change the data type for a field, create a new column using the new data type, copy the data from the old column to the new column via a background script, and then rename the original column label.
-   Various conditions can cause a field to be read-only. For more information, see the [Determining why a field is Read Only \(grayed out and not editable\) \[KB0783470\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0783470) article in the Now Support Knowledge Base.
-   Fields may not display on forms as expected. For more information, see the [Troubleshooting fields not appearing on forms \[KB0547219\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547219) article in the Now Support Knowledge Base.

