---
title: Import Sets API - ServiceNow Fluent
description: The Import Sets API defines transform maps \[sys\_transform\_map\] that specify how to transform and map data from the import set staging table to target tables.Create a transform map \[sys\_transform\_map\] to define the relationships between fields in an import set table and fields in an existing table.Define field mappings \[sys\_transform\_entry\] from the source fields of an import set to the fields of the target table.Define transform scripts \[sys\_transform\_script\] that run at different stages of the import process.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 12
keywords: [servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api]
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Import Sets API - ServiceNow Fluent

The Import Sets API defines transform maps \[sys\_transform\_map\] that specify how to transform and map data from the import set staging table to target tables.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

Every import operation to a production table requires at least one transform map associated with an import set. The transform map specifies the data relationships between the import set and the target table.

To create an import set in ServiceNow Fluent code, you must define the required metadata in the following order:

1.  Define the staging table \[sys\_db\_object\] using the Table API. The table must extend the Import Set Row \[sys\_import\_set\_row\] table. For more information, see [Table API - ServiceNow Fluent](table-api-now-ts.md#).

    The staging table defines all columns that receive imported data.

2.  Define the data source \[sys\_data\_source\] using the Record API. The data source must reference the staging table from its import\_set\_table\_name property. For more information, see [Record API - ServiceNow Fluent](record-api-now-ts.md#).

    The data source defines the connection to external systems \(files, databases, APIs\) and how to load data into import staging tables. For more information, see [Data sources](https://www.servicenow.com/docs/access?context=c_DataSources&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

3.  Define the transform map \[sys\_transform\_map\] using the Import Sets API. The transform map must reference the staging table from its sourceTable property.

**Important:** The string `NULL` is a reserved word. It shouldn’t be used as a field value in import set transform maps or anywhere in the **First name** or **Last name** fields. The reserved word is `NULL` in all capital letters. A field with the value `Null` or `null`, for example, is acceptable. `NULL` should be used only to clear out a particular field.

For general information about import sets, see [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## ImportSet object

Create a transform map \[sys\_transform\_map\] to define the relationships between fields in an import set table and fields in an existing table.

For general information about creating transform maps, see [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

<table id="table_kms_pjc_xhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. An internal name for the transform map.

</td></tr><tr><td>

targetTable

</td><td>

String

</td><td>

Required. The name of the table in which you want the transformed data to be inserted.You can specify only tables within the application scope or the global scope, or tables that grant write access to other applications.

</td></tr><tr><td>

sourceTable

</td><td>

String

</td><td>

Required. The name of the table containing the raw import set data to transform. An import table is any table that extends the Import Set Row \[sys\_import\_set\_row\] table. You can specify only tables within the application scope.**Note:** The value of this property must match the value of the name property in the staging table definition and the import\_set\_table\_name property in the data source definition.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The execution order in which to apply transform maps if more than one map fits the conditions.Default: 100

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the transform map is active.Default: false

</td></tr><tr><td>

runBusinessRules

</td><td>

Boolean

</td><td>

Flag that indicates whether to run business rules, workflows, approval engines, auditing, and field normalization while the transformation inserts or updates data into the target table. If false, GlideRecord.setWorkflow\(\) runs with a value of false.Default: true

</td></tr><tr><td>

enforceMandatoryFields

</td><td>

String

</td><td>

An option to enforce mandatory fields on the target table.Valid values:

-   no: Don’t enforce mandatory fields.
-   onlyMappedFields: Enforce mandatory mapped fields only.
-   allFields: Enforce all mandatory fields.

Default: no

</td></tr><tr><td>

copyEmptyFields

</td><td>

Boolean

</td><td>

Flag that indicates whether to copy empty fields from source and override existing target field values.Default: false

</td></tr><tr><td>

createOnEmptyCoalesce

</td><td>

Boolean

</td><td>

Flag that indicates whether to create a record when coalesce fields are empty, instead of ignoring the record or overwriting an existing record.If createOnEmptyCoalesce is true for any field in the record, the record is coalesced.

Default: false

</td></tr><tr><td>

runScript

</td><td>

Boolean

</td><td>

Flag that indicates whether to execute the transform map script. The system runs the transform map script in addition to any field maps.Default: false

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

A script that transforms field values in the source table to the target table. This property supports a function from a JavaScript module, a reference to another file in the application that contains a script, or inline JavaScript. Expects a function of type `(source, target, map, log, isUpdate) => void`.Format:

-   For functions, use the name of a function, function expression, or default function exported from a JavaScript module and import it into the `.now.ts` file. For information about JavaScript modules, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

fields

</td><td>

Object

</td><td>

Key and value pairs of field mappings where the key is target field name and the value is the source field name or the fields object. Each target field name \(key\) must be unique within the fields object to avoid mapping conflicts.Format:

-   To map a target field name to a source field object, see [fields object](fluent-import-sets-api.md#).
-   To map a target field name to a source field name, use the following format:

    ```javascript
fields: {
    targetFieldName: 'sourceFieldName',
    ...
}
    ```


</td></tr><tr><td>

scripts

</td><td>

Array

</td><td>

A list of transform scripts for additional processing. For more information, see [scripts array](fluent-import-sets-api.md#).

</td></tr></tbody>
</table>```javascript
import '@servicenow/sdk/global'
import { Table, Record, ImportSet } from '@servicenow/sdk/core'

// STEP 1: Create Staging Table Definition (REQUIRED - MUST BE FIRST)
// This creates the actual table structure to hold imported data
export const userStagingTable = Table({
    $id: Now.ID['user-staging-table'],
    name: 'u_user_import_staging',
    label: 'User Import Staging',
    extends: 'sys_import_set_row', // All staging tables extend this
    columns: [
        {
            name: 'u_email_address',
            type: 'email',
            max_length: 100,
            label: 'Email Address'
        },
        {
            name: 'u_full_name',
            type: 'string',
            max_length: 100,
            label: 'Full Name'
        },
        {
            name: 'u_username',
            type: 'string',
            max_length: 40,
            label: 'Username'
        },
    ]
})

// STEP 2: Create Data Source (REQUIRED - MUST BE SECOND)
// The data source defines HOW to get data from external systems
export const userDataSource = Record({
    $id: Now.ID['user-csv-datasource'],
    table: 'sys_data_source',
    data: {
        name: 'User CSV Data Source',
        type: 'File',
        format: 'CSV',
        file_retrieval_method: 'Attachment',
        csv_delimiter: ',',
        header_row: 1,
        // CRITICAL: This must match the table name from STEP 1
        import_set_table_name: 'u_user_import_staging',
        import_set_table_label: 'User Import Staging',
        batch_size: 500,
        active: true,
    },
})

// STEP 3: Create Import Set (Transform Map) (REQUIRED - MUST BE THIRD)
// The import set defines HOW to transform data from staging to target table
export const userImportSet = ImportSet({
    $id: Now.ID['user-import-transform'],
    name: 'User Import Transform',
    targetTable: 'sys_user',
    // CRITICAL: This must match import_set_table_name in Data Source
    sourceTable: 'u_user_import_staging',
    active: true,
    runBusinessRules: true,
    fields: {
        email: {
            sourceField: 'u_email_address',
            coalesce: true,
        },
        name: 'u_full_name',
        user_name: 'u_username',
    }
})
```

## fields object

Define field mappings \[sys\_transform\_entry\] from the source fields of an import set to the fields of the target table.

Use the fields object within the ImportSet object. In the fields object, each key for the target field name must be unique to avoid mapping conflicts.

For general information about creating field maps, see [Create a field map](https://www.servicenow.com/docs/access?context=t_CreatingAFieldMap&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

<table id="table_i5c_fsc_xhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sourceField

</td><td>

String

</td><td>

The name of the source field from the import table to be transformed. This property is required unless you use the `sourceScript` property or a coalesce-only configuration. Field on the source table to be transformed. If the sourceTable contains only raw data, the value can be empty.

</td></tr><tr><td>

choiceAction

</td><td>

String

</td><td>

The action to take if the import set contains a reference or choice value other than those available. This property applies if the target field is a choice list or reference field.Valid values:

-   create: Create a choice or record in the reference table.
-   ignore: Ignore the new value from the source table.
-   reject: Skip the entire row \(record\) containing the new value and continue to the next row.

</td></tr><tr><td>

sourceScript

</td><td>

Script

</td><td>

A script that transforms field values in the source table to the target table. This property supports a function from a JavaScript module, a reference to another file in the application that contains a script, or inline JavaScript. Expects a function of type `(source) => any`.Format:

-   For functions, use the name of a function, function expression, or default function exported from a JavaScript module and import it into the `.now.ts` file. For information about JavaScript modules, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

useSourceScript

</td><td>

Boolean

</td><td>

Flag that indicates whether to use the source script instead of the source field.Default: false

</td></tr><tr><td>

dateFormat

</td><td>

String

</td><td>

The format for transformations when the target field is a Date or Date/Time field.**Note:** To learn more about allowable date formats, see [Global date and time field format](https://www.servicenow.com/docs/access?context=r_FormatDateAndTimeFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Format: `'dd-MM-yyyy'`, `'yyyy-MM-dd'`, `'yyyy-dd-MM'`, `'MM-dd-yyyy HH:mm:ss z'`, `'yyyy-MM-dd HH:mm:ss'`, `'HH:mm:ss'`, `'MM-dd-yyyy HH:mm:ss'`, `'dd-MM-yyyy HH:mm:ss z'`, `'MM-dd-yyyy'`, or `'dd-MM-yyyy HH:mm:ss'`

</td></tr><tr><td>

referenceValueField

</td><td>

String

</td><td>

The reference value field when the target field is a reference field. The transform map needs a way to match incoming source values to existing records in the reference field's source table. Because most imports don’t provide a 32-character sys\_id value, you must specify a column from the reference field's source table that contains values that match the incoming source values. For more information, see [Create a field map](https://www.servicenow.com/docs/access?context=t_CreatingAFieldMap&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

coalesce

</td><td>

Boolean

</td><td>

Flag that indicates whether the field is used for record matching. Configuring a target field to coalesce causes the import set to treat the field as a unique key. For more information, see [Create a field map](https://www.servicenow.com/docs/access?context=t_CreatingAFieldMap&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).Default: false

</td></tr><tr><td>

coalesceCaseSensitive

</td><td>

Boolean

</td><td>

Flag that indicates whether to make case-sensitive coalesce values result in the creation of new records.By default, coalesce fields are used in a case-insensitive lookup for existing records. Case-insensitive records update existing records only and don’t cause the creation of new records.

Default: false

</td></tr><tr><td>

coalesceEmptyFields

</td><td>

Boolean

</td><td>

Flag that indicates whether to match an empty source field value to an empty target field value. The coalesce property must be set to true for this property to apply.For example, the User transform map coalesces on the email field. If this property is set to true, a source record containing an empty email address coalesces to a target record containing an empty email address.

Default: false

</td></tr></tbody>
</table>```javascript
fields: {
        email: {
            sourceField: 'email_address',
            coalesce: true,
            useSourceScript: true,
            sourceScript: `answer = (function transformEntry(source) {
                return source.email_address.toLowerCase().trim();
            })(source);`
        },
        department: {
            sourceField: 'dept_code',
            choiceAction: 'create'
        }
}
```

## scripts array

Define transform scripts \[sys\_transform\_script\] that run at different stages of the import process.

<table id="table_i5c_fsc_xhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the script is active and executes.Default: true

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The execution order in which scripts run if more than one script fits the conditions.Default: 100

</td></tr><tr><td>

when

</td><td>

String

</td><td>

The stage of the import process in which to execute the script. For more information, see [Map with transformation event scripts](https://www.servicenow.com/docs/access?context=r_MapWithTransformationEventScripts&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).Valid values: onBefore, onAfter, onReject, onStart, onForeignInsert, onComplete, onChoiceCreate

Default: onAfter

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

A script that modifies the transformation behavior at the stage specified with the when property. This property supports a function from a JavaScript module, a reference to another file in the application that contains a script, or inline JavaScript. Expects a function of type `(source, map, log, target) => void`.Format:

-   For functions, use the name of a function, function expression, or default function exported from a JavaScript module and import it into the `.now.ts` file. For information about JavaScript modules, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr></tbody>
</table>```javascript
scripts: [
        {
            $id: Now.ID['validate-email'],
            active: true,
            order: 100,
            when: 'onBefore',
            script: `(function runTransformScript(source, map, log, target) {
                if (!source.email_address || source.email_address.indexOf('@') === -1) {
                    log.error('Invalid email address: ' + source.email_address);
                    return;
                }
            })(source, map, log, target);`
        },
        {
            $id: Now.ID['validate-user-script'],
            active: true,
            order: 100,
            when: 'onBefore',
            // Using imported function for lifecycle script
            script: validateUserData
        }
    ]
```

