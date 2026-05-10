---
title: Table API - ServiceNow Fluent
description: The Table API defines tables \[sys\_db\_object\] to store data in an application.Create a table \[sys\_db\_object\] in an application.Add a column \[sys\_dictionary\] to a table.Configure choices \[sys\_choice\] for a column in a table.Configure a field label \[sys\_documentation\] for a table or column.Create a licensing configuration \[ua\_table\_licensing\_config\] to track subscription counts for a table.Configure auto-numbering \[sys\_number\] for a table.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Table API - ServiceNow Fluent

The Table API defines tables \[sys\_db\_object\] to store data in an application.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

Create a table using the Table object. From the schema property, add Column objects, such as StringColumn or IntegerColumn, to define the columns.

For general information about tables, see [Table administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_TableAdministration.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Table object

Create a table \[sys\_db\_object\] in an application.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Required. A name for the table beginning with the application scope and in all lowercase letters in the following format: `<scope>_<name>`. The name should match the variable identifier of the Table object.**Note:** To add columns to an existing table in a different application scope, you can provide the name of the table without the application scope followed by `as any`. The column names must begin with the application scope instead.

Maximum length: 80

</td></tr><tr><td>

schema

</td><td>

Array

</td><td>

Required. A list of Column objects. For more information, see [Column object](table-api-now-ts.md#).

</td></tr><tr><td>

extends

</td><td>

String

</td><td>

The name of any other table on which the table is based.Extending a base table incorporates all the fields of the original table and creates system fields for the new table. If they are in the same scope or if they can be configured from other scopes, you can extend tables that are marked as extensible.

</td></tr><tr><td>

label

</td><td>

String or Array

</td><td>

A unique label for the table in list and form views. Field labels can be provided as a string or an array of label objects. For more information, see [label object](table-api-now-ts.md#).Maximum length: 80

Default: the value of the name property

</td></tr><tr><td>

licensingConfig

</td><td>

Object

</td><td>

The licensing configuration \[ua\_table\_licensing\_config\] for a table. For more information, see [licensingConfig object](table-api-now-ts.md#).

</td></tr><tr><td>

display

</td><td>

String

</td><td>

The default display column. Use a column name from the schema property.

</td></tr><tr><td>

extensible

</td><td>

Boolean

</td><td>

Flag that indicates whether other tables can extend the table.Valid values:

-   true: Other tables can extend the table.
-   false: Other tables can't extend the table.

Changing this property from true to false prevents the creation of additional child tables but existing child tables remain unchanged.

Default: false

</td></tr><tr><td>

liveFeed

</td><td>

Boolean

</td><td>

Flag that indicates if live feeds are available for records in the table.Valid values:

-   true: Live feeds are provided for records in the table. This option adds the **Show Live Feed** option \(![Show Live Feed icon](../../../administer/table-administration/image/LiveCompanyFeed.png)\) in the form header.
-   false: Live feeds aren't provided for records in the table.

Default: false

</td></tr><tr><td>

accessibleFrom

</td><td>

String

</td><td>

The application scopes that can access the table.Valid values:

-   public: The table is accessible from all application scopes.
-   package\_private: The table is accessible from only the application scope it's in.

Default: public

</td></tr><tr><td>

callerAccess

</td><td>

String

</td><td>

The access level for cross-scope requests.Valid values:

-   restricted: Calls to the resource must be manually approved. Access requests are tracked in the Restricted Caller Access table with a status of Requested.
-   tracking: Calls to the resource are automatically approved. Calls are tracked in the Restricted Caller Access table with a status of Allowed.
-   none: Cross-scope calls to the resource are approved or denied based on the value of the accessibleFrom property.

For more information, see [Restricted caller access privilege settings](../../applications/concept/restricted-caller-access-privilege.md).

Default: none

</td></tr><tr><td>

actions

</td><td>

Array

</td><td>

A list of access options.Valid values:

-   read: Allow script objects from other application scopes to read records stored in this table. For example, a script in another application can query data on this table. Read access is required to grant any other API record operations.
-   create: Allow script objects from other application scopes to create records in this table. For example, a script in another application can insert a new record in this table.
-   update: Allow script objects from other application scopes to modify records stored in this table. For example, a script in another application can modify a field value on this table.
-   delete: Allow script objects from other application scopes to delete records from this table. For example, a script in another application can remove a record from this table.

Default: read

</td></tr><tr><td>

allowWebServiceAccess

</td><td>

Boolean

</td><td>

Flag that indicates whether web services can make calls to the table.Valid values:

-   true: Web services can make calls to the table.
-   false: Web services can't make calls to the table.

Default: false

</td></tr><tr><td>

allowNewFields

</td><td>

Boolean

</td><td>

Flag that indicates whether to allow design time configuration of new fields on the table from other application scopes.Valid values:

-   true: Allow design time configuration of new fields on the table from other application scopes.
-   false: Don't allow design time configuration of new fields on the table from other application scopes.

Default: false

</td></tr><tr><td>

allowUiActions

</td><td>

Boolean

</td><td>

Flag that indicates whether to allow design time configuration of UI actions on the table from other application scopes.Valid values:

-   true: Allow design time configuration of UI actions on the table from other application scopes.
-   false: Don't allow design time configuration of UI actions on the table from other application scopes.

Default: false

</td></tr><tr><td>

allowClientScripts

</td><td>

Boolean

</td><td>

Flag that indicates whether to allow design time configuration of client scripts on the table from other application scopes.Valid values:

-   true: Allow design time configuration of client scripts on the table from other application scopes.
-   false: Don't allow design time configuration of client scripts on the table from other application scopes.

Default: false

</td></tr><tr><td>

audit

</td><td>

Boolean

</td><td>

Flag that indicates whether to track the creation, update, and deletion of all records in the table.Valid values:

-   true: Track the creation, update, and deletion of all records in the table
-   false: Don't track the creation, update, and deletion of all records in the table.

Default: false

</td></tr><tr><td>

readOnly

</td><td>

Boolean

</td><td>

Flag that indicates whether users can edit fields in the table.Valid values:

-   true: Users can't edit fields in the table.
-   false: Users can edit fields in the table.

Default: false

</td></tr><tr><td>

textIndex

</td><td>

Boolean

</td><td>

Flag that indicates whether search engines index the text in a table.Valid values:

-   true: The table's text is indexed.
-   false: The table's text isn't indexed.

Default: false

</td></tr><tr><td>

attributes

</td><td>

Object

</td><td>

Key and value pairs of any supported dictionary attributes \[sys\_schema\_attribute\]. For example:```javascript
attributes: 
   {
      updateSyncCustom: Boolean,
      nativeRecordLock: Boolean
   }
```

For more information, see [Dictionary Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md).

</td></tr><tr><td>

index

</td><td>

Array

</td><td>

A list of column references to generate indexes in the metadata XML of the table. The value of the element property should match the object key used with the Column object.A database index increases the speed of accessing data from the table with the expense of using additional storage.

```javascript
index: [
    {
        name: 'String',
        element: 'String',
        unique: Boolean
    },
    ...
]
```

</td></tr><tr><td>

autoNumber

</td><td>

Object

</td><td>

The auto-numbering configuration \[sys\_number\] for a table. For more information, see [autoNumber object](table-api-now-ts.md#).

</td></tr><tr><td>

scriptableTable

</td><td>

Boolean

</td><td>

Flag that indicates whether the table is a remote table that uses data retrieved from an external source. For more information, see [Remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/remote-tables/remote-tables.md).Valid values:

-   true: The table is a remote table.
-   false: The table isn't a remote table.

Default: false

</td></tr></tbody>
</table>For typeahead support for columns, assign the Table object to an exported variable with the same name as the name property.

```javascript
import { Table, StringColumn } from "@servicenow/sdk/core";
import { myFunction } from "../server/myFunction.js"

export const x_snc_example_to_do = Table({
    name: 'x_snc_example_to_do',
    label: 'My To Do Table',
    extends: 'task',
    schema: {
        status: StringColumn({ label: 'Status' }),
        deadline: StringColumn({
            label: 'Deadline',
            active: true,
            mandatory: false,
            readOnly: false,
            maxLength: 40,
            dropdown: 'none',
            attributes: { 
                updateSync: false,
            },
            default: 'today',
            dynamicValueDefinitions: {
                type: 'calculated_value',
                calculatedValue: '',
            },
            choices: {
                choice1: {
                    label: 'Choice1 Label',
                    sequence: 0,
                    inactiveOnUpdate: false,
                    dependentValue: '5',
                    hint: 'hint',
                    inactive: false,
                    language: 'en',
                },
                choice2: { label: 'Choice2 Label', sequence: 1 },
            },
        }),
        dynamic1: StringColumn({
            dynamicValueDefinitions: {
                type: 'calculated_value',
                calculatedValue: myFunction,
            },
        }),
        dynamic2: StringColumn({
            dynamicValueDefinitions: {
                type: 'dynamic_default',
                dynamicDefault: `gs.info()`,
            },
        }),
        dynamic3: StringColumn({
            dynamicValueDefinitions: {
                type: 'dependent_field',
                columnName: 'status',
            },
        }),
        dynamic4: StringColumn({
            dynamicValueDefinitions: {
                type: 'choices_from_other_table',
                table: 'sc_cat_item',
                field: 'display',
            },
        }),
    },
    actions: ['create', 'read'],
    display: 'deadline',
    accessibleFrom: 'package_private',
    allowClientScripts: true,
    allowNewFields: true,
    allowUiActions: true,
    allowWebServiceAccess: true,
    extensible: true,
    liveFeed: true,
    callerAccess: 'none',
    autoNumber: {
        number: 10,
        numberOfDigits: 2,
        prefix: 'abc',
    },
    audit: true,
    readOnly: true,
    textIndex: true,
    attributes: {
        updateSync: true,
    },
    index: [
        {
            name: 'idx',
            element: 'status',
            unique: true,
        },
    ],
})
```

## Column object

Add a column \[sys\_dictionary\] to a table.

Add Column objects in the schema property of the Table object.

There are many types of columns based on the field type. Column objects use the format &lt;Type&gt;Column where *&lt;Type&gt;* is the field type. For information about field types, see [Field types reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_FieldTypes.md).

The following types of columns are supported: ListColumn, RadioColumn, StringColumn, ChoiceColumn, ScriptColumn, BooleanColumn, ConditionsColumn, DecimalColumn, IntegerColumn, VersionColumn, DomainIdColumn, FieldNameColumn, ReferenceColumn, TableNameColumn, UserRolesColumn, BasicImageColumn, DocumentIdColumn, DomainPathColumn, TranslatedTextColumn, SystemClassNameColumn, TranslatedFieldColumn, GenericColumn, DateColumn, DateTimeColumn, CalendarDateTime, BasicDateTimeColumn, DueDateColumn, CalendarDateTime, IntegerDateColumn, ScheduleDateTimeColumn, OtherDateColumn, Password2Column, GuidColumn, JsonColumn, NameValuePairsColumn, UrlColumn, EmailColumn, HTMLColumn, FloatColumn, MultiLineTextColumn, DurationColumn, TimeColumn, FieldListColumn, SlushBucketColumn, TemplateValueColumn, and ApprovalRulesColumn.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

String or Array

</td><td>

A unique label for the column that appears on list headers and form fields. Field labels can be provided as a string or an array of label objects. For more information, see [label object](table-api-now-ts.md#).Default: the key used for the column object

</td></tr><tr><td>

maxLength

</td><td>

Number

</td><td>

The maximum length of values in the column.A length of under 254 appears as a single-line text field. Anything 255 characters or over appears as a multi-line text box.

**Note:** To avoid data loss, only decrease the length of a string field when you’re developing a new application and not when a field contains data.

Default: varies depending on the column type

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether to display the field in lists and forms.Valid values:

-   true: Displays the field.
-   false: Hides the field.

Default: true

</td></tr><tr><td>

mandatory

</td><td>

Boolean

</td><td>

Flag that indicates whether the field must contain a value to save a record.Valid values:

-   true: The field must contain a value.
-   false: The field isn't required.

Default: false

</td></tr><tr><td>

readOnly

</td><td>

Boolean

</td><td>

Flag that indicates whether you can edit the field value.Valid values:

-   true: You can't change the value, and the system calculates and displays the data for the field.
-   false: You can change the field value.

Default: false

</td></tr><tr><td>

readOnlyOption

</td><td>

String

</td><td>

Control the ability to edit read-only fields by configuring read-only options.Valid values:

-   instance\_configured: Maintains backwards compatibility and testing read-only behavior in non-production instances.
-   display\_read\_only: Displays the field as read-only in the UI, but allows changes to the read-only field through client scripts and server-side operations such as TableAPI, GraphQL, and GlideRecordSecure\(\).
-   client\_script\_modifiable: Displays the field as read-only in the UI, and allows changes to read-only fields through client scripts but not through background scripts or server-side APIs like TableAPI, GraphQL, and GlideRecordSecure\(\).
-   strict\_read\_only: Displays the field as read-only in the UI, but prevents any changes from both client scripts and server-side APIs.

For more information, see [Configuring read-only security options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/read-only-option.md).

</td></tr><tr><td>

default

</td><td>

Any

</td><td>

The default value of the field when creating a record. The value must use the correct type based on the column type.

</td></tr><tr><td>

choices

</td><td>

Object

</td><td>

A list of choices \[sys\_choice\] for a column. For more information, see [choices object](table-api-now-ts.md#). This property only applies to ChoiceColumn objects and column types that extend choice columns. It can include either an array of primitive values or a series of choice objects.

</td></tr><tr><td>

attributes

</td><td>

Object

</td><td>

Key and value pairs of any supported dictionary attributes \[sys\_schema\_attribute\]. For example:```javascript
attributes: 
   {
      updateSyncCustom: Boolean,
      nativeRecordLock: Boolean
   }
```

For more information, see [Dictionary Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md).

</td></tr><tr><td>

functionDefinition

</td><td>

String

</td><td>

The definition of a function that the field performs, such as a mathematical operation, field length computation, or day of the week calculation.Each definition begins with `glidefunction:`, followed by the operation to be performed \(such as, `concat`\), followed by function parameters. Constants must be enclosed in single quotes.

For example, the following function definition creates a field that shows the short description, followed by a space, followed by the caller name:

```javascript
functionDefinition: 'glidefunction:concat(short_description, ' ', caller_id.name)'
```

For more information about function definitions, see [Function field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/platform-support-functions.md).

</td></tr><tr><td>

dynamicValueDefinitions

</td><td>

Object

</td><td>

Default values that are generated dynamically based on dynamic filters. Provide a combination of a type and a related behavior key to specify dynamic defaults. The following types are supported:-   dynamic\_default: Provide a function from the Dynamic Filter Options \[sys\_filter\_option\_dynamic\] table. For more information, see [Create a dynamic filter option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_DynamicFilterOptions.md). For example:

    ```javascript
dynamicValueDefinitions: {
   type: 'dynamic_default',
   dynamicDefault: `gs.info()`,
},
    ```

-   dependent\_field: Provide another column name from the same table. For example:

    ```javascript
dynamicValueDefinitions: {
   type: 'dependent_field',
   columnName: 'status',
},
    ```

-   calculated\_value: Provide a function for calculating the value. The function can be imported from a JavaScript module or be defined inline. For example:

    ```javascript
dynamicValueDefinitions: {
   type: 'calculated_value',
   calculatedValue: function,
},
    ```

-   choices\_from\_other\_table: Provide choices from a column on another table. For example:

    ```javascript
dynamicValueDefinitions: {
   type: 'choices_from_other_table',
   table: 'sc_cat_item',
   field: 'display',
},
    ```


</td></tr><tr><td>

dropdown

</td><td>

String

</td><td>

An option for how a list of choices displays for list and form views of the table. This property only applies to ChoiceColumn objects and column types that extend choice columns.Valid values:

-   none: The choices aren't enforced.
-   dropdown\_without\_none: A menu without the **-- None --** option. If you select this option, you must configure the default property for the column.
-   dropdown\_with\_none: A menu with the **-- None --** option. The default value is **-- None --**.
-   suggestion: Choices are displayed in a list of suggested values.

Default: none

</td></tr></tbody>
</table>Column names are provided as object keys paired with the column definitions.

```javascript
schema: {
   deadline: DateColumn({ label: 'Deadline' }),
   state: StringColumn({
      label: 'State',
      choices: {
         ready: { label: 'Ready' },
         completed: { label: 'Completed' },
         inProgress: { label: 'In Progress' },
      }   
   }),
   task: StringColumn({ label: 'Task', maxLength: 120 }),
}
```

If the table name doesn't include the application scope, column names must be prefixed with the application scope instead.

```javascript
schema: {
   x_scope_myColumn: StringColumn({...})
}
```

### choices object

Configure choices \[sys\_choice\] for a column in a table.

The choices object is a property within the Column object. Use the choices object with supported column types in the schema property of a Table object. Only certain column types extend the choice column type \(ChoiceColumn\) and can include choices.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

String

</td><td>

Required. The text to display for the choice in the list.

</td></tr><tr><td>

dependentValue

</td><td>

String

</td><td>

A value that you map to the dependentField in the dynamicValueDefinitions property of the Column object.

</td></tr><tr><td>

hint

</td><td>

String

</td><td>

A short description of the choice that displays as tooltip when hovering over it.

</td></tr><tr><td>

language

</td><td>

String

</td><td>

The [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code of the language for the translated choice.Default: en

</td></tr><tr><td>

sequence

</td><td>

Integer

</td><td>

The order in the list of choices that a choice occurs.

</td></tr><tr><td>

inactive

</td><td>

Boolean

</td><td>

Flag that indicates whether to show the choice in the list.Valid values:

-   true: The choice is hidden from the list.
-   false: The choice appears in the list.

Default: false

</td></tr></tbody>
</table>The `choices` object includes a series of choice objects, where the names of the choices are provided as object keys paired with the choices definitions.

```javascript
choices: {
   choice1: {
      label: 'Choice1 Label',
      sequence: 0,
      inactiveOnUpdate: false,
      dependentValue: '5',
      hint: 'hint',
      inactive: false,
      language: 'en',
   },
   choice2: { label: 'Choice2 Label', sequence: 1 },
}
```

## label object

Configure a field label \[sys\_documentation\] for a table or column.

The label object is a property within the Table and Column objects.

|Name|Type|Description|
|----|----|-----------|
|language|String|The [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) code of the language for the field label. A language can have only one label, so each language must be unique within an array of label objects.|
|label|String|The text of the field label in the specified language.|
|hint|String|A short description that displays as a tooltip when hovering over the field label.|
|help|String|Additional information about the field. Help text isn’t displayed in form or list views of the table.|
|plural|String|The plural form of the field label.|
|url|String|A URL for a web page that provides information about the field. When a URL is provided, the label displays as a hyperlink.|
|urlTarget|String|Not used \(deprecated\).|

```javascript
label: [
   { 
      label: 'English description', 
      language: 'en', 
      hint: 'Provide a short description' 
   },
   {
      label: 'Description de español', 
      language: 'es' 
   },
]
```

## licensingConfig object

Create a licensing configuration \[ua\_table\_licensing\_config\] to track subscription counts for a table.

The licensingConfig object is a property within the Table object. If this property isn’t specified, a default licensing configuration with licenseModel set to none is generated for the table on the instance.

**Note:** Specifying a licensing model is not applicable for ServiceNow customers who build custom applications for their own use. Licensing models are used only by partners who sell and monitor the usage of resellable applications on the ServiceNow Store.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

licenseModel

</td><td>

String

</td><td>

The model for tracking subscription usage.Valid values:

-   none: Licensing isn’t used for the table.
-   fulfiller: Fulfiller/requester operations are tracked. This model applies to applications in which users open requests and fulfillers address them. Fulfillment is determined by insert, update, and delete operations on records in one or more key tables in the application under a set of specified conditions. For more information, see [Fulfillment tables](../../applications/reference/r_FulfillmentTables.md).
-   producer: Producer operations are tracked. This model applies to applications in which users can perform insert, update, and delete operations on a table without identifying requesters and fulfillers.

Default: none

</td></tr><tr><td>

licenseRoles

</td><td>

Array

</td><td>

A list of roles for which any operations on records in the table count toward the subscription.

</td></tr><tr><td>

opDelete

</td><td>

Boolean

</td><td>

Flag that indicates whether a subscription is required to delete records for tables with the producer model.Valid values:

-   true: A subscription is required to delete records in the table.
-   false: A subscription isn't required to delete records in the table.

Default: true

</td></tr><tr><td>

opInsert

</td><td>

Boolean

</td><td>

Flag that indicates whether a subscription is required to insert records for tables with the producer model.Valid values:

-   true: A subscription is required to insert records in the table.
-   false: A subscription isn't required to insert records in the table.

Default: true

</td></tr><tr><td>

opUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether a subscription is required to update records for tables with the producer model.-   true: A subscription is required to update records in the table.
-   false: A subscription isn't required to update records in the table.

Default: true

</td></tr><tr><td>

licenseCondition

</td><td>

String

</td><td>

A filter query that determines conditions for counting operations toward a subscription. For the fulfiller model, specify the set of conditions that determine whether the logged-in user is the fulfiller of the record.

For the producer model, specify the set of conditions that determine whether records count toward the subscription.

</td></tr><tr><td>

ownerCondition

</td><td>

String

</td><td>

A filter query that determines whether a user owns a record for the fulfiller model.

</td></tr><tr><td>

isFulfillment

</td><td>

Boolean

</td><td>

Not used \(deprecated\). Flag that indicates whether to disallow updates by users who aren't subscribed to the application.Valid values:

-   true: Users who aren't subscribed to the application can't make updates to the table.
-   false: Users who aren't subscribed to the application can make updates to the table.

Default: false

</td></tr></tbody>
</table>```javascript
licensingConfig: {
  licenseModel: 'fulfiller',
  opInsert: false,
  licenseRoles: ['admin'],
}
```

## autoNumber object

Configure auto-numbering \[sys\_number\] for a table.

The autoNumber object is a property within the Table object. To use the number in a table, you must create a number column, such as IntegerColumn, that uses the number as the default value.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

prefix

</td><td>

String

</td><td>

A prefix for every record number in the table. For example, INC for Incident.Default: pre

</td></tr><tr><td>

number

</td><td>

Integer

</td><td>

The base record number for this table. Record numbers are automatically incremented, and the next number is maintained in the Counter \[sys\_number\_counter\] table.If you set the base number to a value higher than the current counter, the next record number uses the new base number. Otherwise the next record number uses the current counter. The counter doesn’t reset to a base number lower than itself.

Default: 1000

</td></tr><tr><td>

numberOfDigits

</td><td>

Integer

</td><td>

The minimum number of digits to use after the prefix.Leading zeros are added to auto-numbers, if necessary. For example, INC0001001 contains three leading zeros. The number of digits can exceed the minimum length. For example, if numberOfDigits is 2 and more than 99 records are created on the table, the numbers continue past 100 \(such as INC101\).

 **Warning:** Changing this field can update all number values for existing records on a table. Take care when changing this field on a production instance.

Default: 7

</td></tr></tbody>
</table>```javascript
autoNumber: {
   prefix: 'TODO',
   number: 2000,
   numberOfDigits: 9,
}
```

In the following example, a number column uses the auto-numbering as the default value. For example:

```javascript
number: IntegerColumn({             
   default: 'javascript:getNextObjNumberPadded();'
})
```

