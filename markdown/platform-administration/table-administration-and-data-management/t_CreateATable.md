---
title: Create a table
description: Administrators and application developers can create custom tables to store application data. After you create a table, you can also modify field types and field labels.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a table

Administrators and application developers can create custom tables to store application data. After you create a table, you can also modify field types and field labels.

## Before you begin

Role required: admin

Check your custom table entitlements before creating custom tables. See [Managing custom tables and applications in Subscription Management](../../subscription-management/concept/allocating-custom-tables-subscr-apps-v2.md).

## About this task

ServiceNow AI Platform application subscriptions include custom table entitlements. You can create custom tables for any purpose, up to the entitlement limit in the subscription. To learn more about how your usage administrator maps the custom tables that you create to subscriptions, see [Map custom tables to a product subscription in Subscription Management](../../subscription-management/task/allocate-custom-table-subsc-app-v2.md).

**Note:** It is best to create tables when building applications with tools. To learn more, see Building applications. To minimize the existence of unneeded and extraneous tables in an instance, don't overdo table creation. Create only those tables you need to minimize administration tasks and shorten upgrade times. Do not extend the \[sys\_choice\] table. Extending the \[sys\_choice\] table is not supported.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_yxx_ndv_tr"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Enter a unique label for the table \(such as **Laptops** or **Thin Clients**\). The label appears on list and form views for the table. Updating the **Label** field also updates the label record in the language file for the current language. See Field Labels in [Data dictionary tables](../../managing-data/concept/c_DataDictionaryTables.md).

</td></tr><tr><td>

Name

</td><td>

Edit the table name, which is automatically populated based on the table label and a prefix as follows:

-   For a table in a scoped application, the name is prefixed with a namespace identifier to indicate that it is part of an application.
-   For a table in the global application, the name is prefixed with the string u\_.
-   For a remote table in a scoped application, the name is prefixed with a namespace identifier and the string st\_ to indicate that it’s remote and part of an application.
-   For a remote table in the global application, the name is prefixed with the string u\_st\_.
 You cannot modify the prefix; however, you can modify the rest of the table name. The name can contain only lowercase, alphanumeric ASCII characters and underscores \(\_\).

</td></tr><tr><td>

Extends Table

</td><td>

Select the table to extend. Extending a base table incorporates all the fields of the original table and creates system fields for the new table. If they are in the same scope or if they can be configured from other scopes, you can extend tables that are marked as extensible.

 This option is not available if you select the **Scriptable Table** check box to designate that this table is scriptable.

</td></tr><tr><td>

Application

</td><td>

\[Read only\] Displays the application associated with this table. If you are working on an application or are creating a table from an application record, the field defaults to that application. Otherwise, the field defaults to **Global**. Any records that are created from the table record, such as modules and security rules, are assigned to this application by default.

</td></tr><tr><td>

Remote Table

</td><td>

Option to designate this table as a remote table. A remote table is a table to which you can associate a script definition for retrieval of data from an external data source. Unlike a standard internal table, the data doesn’t come from records in the current instance. If you select this check box, you cannot access the **Extends Table** option because scriptable tables cannot be extended from other tables.

 **Note:** To learn more about scriptable tables, see:

-   Retrieving and caching external data using remote tables
-   Create a remote table
-   Create a script definition for a remote table


</td></tr><tr><td>

Create module

</td><td>

Select the check box and then complete the **Add module to menu** field to create a list module in the application menu.

 This option is available only when creating a table.

</td></tr><tr><td>

Add module to menu

</td><td>

Select an existing menu or select **Create new** and enter a new menu name. This option is available only when the **Create module** check box is selected.

</td></tr></tbody>
</table>4.  In the **Columns** section, use the **Table Columns** embedded list to add columns to the table.

<table id="table_myw_mmy_wt"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Column label

</td><td>

Define a unique label for the column. The label appears on list headers and form fields for the column. When you update the **Column label** field, the system also updates the label in the language file for the current language.

</td></tr><tr><td>

Type

</td><td>

\[Mandatory\] Define the field type for the column. See [Field administration](../../reference-pages/concept/c_IntroductionToFields.md) and [Field types](../../reference-pages/reference/r_FieldTypes.md). To preserve existing data, only change fields between the same basic type \(for example, **Choice** and **String**\). A warning appears if a change to a custom field results in data loss. You cannot change a base system field, that results in data loss.

</td></tr><tr><td>

Reference

</td><td>

Make the field into a [Reference field type](../../field-administration/concept/c_ReferenceField.md) by entering the referenced table name.

 **Note:** Dynamic reference creation is enabled for this field. So, if you enter a table name that does not match an existing table, a new table is created when you save changes to the current table record. If the current table has a module in the application navigator, then a module for the newly created table is automatically created in the same application menu.

</td></tr><tr><td>

Max length

</td><td>

\[String fields only\] Limit the length of the field. A length of under 254 appears as a single-line text field. Anything 255 characters or over appears as a multi-line text box.

 **Note:**

-   You can only change this value if the **Type** of the field is **String**. Changes for any other type of field are ignored.
-   On an Oracle instance, you cannot increase the maximum length of a string field to greater than 4000 because it requires the CLOB datatype in Oracle. To increase beyond this size, log an incident with ServiceNow Technical Support to request the change.
-   To prevent data from being lost, only decrease the length of a string field when you are developing a new application and not when a field contains data. A warning appears if a change to a custom field results in data loss. For a base system field, you cannot make a change that results in data loss.


</td></tr><tr><td>

Default value

</td><td>

Specify the default value of the field for any new record. Ensure that this value uses the correct field type. For example, an integer field can use a default value of 2 but cannot use a default value of two. These values can be overridden with [dictionary overrides](../../data-dictionary-tables/concept/c_DictionaryOverrides.md).

</td></tr><tr><td>

Display

</td><td>

Indicate whether this field is the [Display values](../../field-administration/concept/c_DisplayValues.md) \(appears on records that reference this table\).

 **Note:** This option does not control whether this field is displayed on lists or forms.

</td></tr></tbody>
</table>5.  In the **Controls** section, define additional table options.

    |Control|Description|
    |-------|-----------|
    |Extensible|Select the check box to enable other tables to extend this table. Clear the check box to prevent the creation of additional child tables; existing child tables remain unchanged.|
    |Live feed|Select the check box to enable record feeds for the table. This option adds the **Show Live Feed** icon \(![Show Live Feed icon](../image/LiveCompanyFeed.png)\) in the form header.|
    |Auto-number|Select the check box, and then define the number format to add an auto-numbered field to the table. The check box is available only when a number format does not exist for the table. Otherwise, you can edit the existing number format.|
    |Create access controls|Select the check box and then complete the **User role** field to create basic security rules for the table.|
    |User role|Enter a new name or select an existing user role that is required to access this table. This option is available only when the **Create access controls** check box is selected.|

6.  In the **Application Access** section, define the scope protection for the table.

    For more information, see Application access settings.

<table id="table_xwp_pny_wt"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accessible from

</td><td>

Specify which application scopes can access the table:

-   **All application scopes**

Can be accessed from any application scope.

-   **This application scope only**

Can be accessed only from the current application scope.

</td></tr><tr><td>

Can read

</td><td>

Select the check box to enable script objects from other application scopes to read records stored in this table. This option offers runtime protection. For example, a script in another application can query data on this table. First select read access to grant any other API record operation.

</td></tr><tr><td>

Can create

</td><td>

Select the check box to enable script objects from other application scopes to create records in this table. This option offers runtime protection. For example, a script in another application can insert a new record in this table. This option is available only when the **Can read** check box is selected.

 Clear the check box to prevent script objects from other application scopes from creating records in this table.

</td></tr><tr><td>

Can update

</td><td>

Select the check box to enable script objects from other application scopes to modify records stored in this table. This option offers runtime protection. For example, a script in another application can modify a field value on this table. This option is available only when the **Can read** check box is selected.

 Clear the check box to prevent script objects from other application scopes from modifying data stored in this table.

</td></tr><tr><td>

Can delete

</td><td>

Select the check box to enable script objects from other application scopes to delete records from this table. This option offers runtime protection. For example, a script in another application can remove a record from this table. This option is available only when the **Can read** check box is selected.

 Clear the check box to prevent script objects from other application scopes from deleting records from this table.

</td></tr><tr><td>

Allow access to this table via web services

</td><td>

Select the check box to enable users to make inbound Web services web service queries to this table. This option offers both design-time and runtime protection. The user performing the query must have the correct permissions to access this table, even when this check box is selected.

 Clear the check box to prevent users from making web service queries to this table.

</td></tr><tr><td>

Allow configuration

</td><td>

Select the check box to enable applications from other application scopes to create configuration records for this table that change its functionality. For example, an application designer can select this table from the **Tables** list on business rules, client scripts, or UI actions. This option offers design-time protection.

 Clear the check box to prevent application designers from selecting this table when creating configuration records.

</td></tr></tbody>
</table>7.  Click **Submit**.


## What to do next

To change the field labels in your table or the label of the table itself, perform the following task:

1.  Navigate to the Field Label \[sys\_documentation\] table, and filter the table to show the table that has the fields you want to change. To find the label that represents the table itself, filter the records where **Element** is empty.
2.  Open the field record that you want to change, and make your updates. For a description of each field, see [Field Label table](../../localization/reference/r_FieldLabelTable.md).

-   **[Global default fields](../../../build/applications/reference/r_GlobalDefaultFields.md)**  
When you create a new custom table, several fields appear in the **Table Columns** embedded list. For all tables, required system fields are added automatically. You cannot delete or modify these fields.

**Parent Topic:**[Managing tables and indexes](../concept/using-table-administration.md)

