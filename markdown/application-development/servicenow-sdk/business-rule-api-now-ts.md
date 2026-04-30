---
title: Business Rule API - ServiceNow Fluent
description: The Business Rule API defines server-sides scripts \[sys\_script\] that run when a record is displayed, inserted, updated, or deleted, or when a table is queried.Create a business rule \[sys\_script\] that automatically changes values in form fields when certain server-side conditions are met.
locale: en-US
release: yokohama
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Business Rule API - ServiceNow Fluent

The Business Rule API defines server-sides scripts \[sys\_script\] that run when a record is displayed, inserted, updated, or deleted, or when a table is queried.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about business rules, see [Classic Business rules](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## BusinessRule object

Create a business rule \[sys\_script\] that automatically changes values in form fields when certain server-side conditions are met.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

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

Required. A name for the business rule.

</td></tr><tr><td>

table

</td><td>

String

</td><td>

Required. The name of the table on which the business rule runs.

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

A custom script runs when the defined conditions are true. This property supports a function from a JavaScript module, a reference to another file in the application that contains a script, or inline JavaScript. Format:

-   For functions, use the name of a function, function expression, or default function exported from a JavaScript module and import it into the `.now.ts` file. For information about JavaScript modules, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

A number indicating the sequence in which the business rule should run. If there are multiple rules on a particular activity, the rules run in the order specified, from lowest to highest.Default: 100

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the business rule is enabled.Valid values:

-   true: The business rule is enforced.
-   false: The business rule isn't enforced.

Default: true

</td></tr><tr><td>

when

</td><td>

String

</td><td>

The time that the business rule should execute. For more information about when business rules run, see [How business rules work](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=yokohama&pubname=yokohama-api-reference&section=r_HowBusinessRulesWork&ft:locale=en-US).Valid values:

-   before
-   after
-   async
-   display

Default: before

</td></tr><tr><td>

action

</td><td>

Array

</td><td>

The record options that the business rule applies to. For more information about business rule actions, see [How business rules work](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=yokohama&pubname=yokohama-api-reference&section=r_HowBusinessRulesWork&ft:locale=en-US).Valid values:

-   insert
-   update
-   delete
-   query

</td></tr><tr><td>

addMessage

</td><td>

Boolean

</td><td>

Flag that indicates whether to add a message that appears when the business rule runs.Valid values:

-   true: Displays a message.
-   false: Doesn't display a message.

Default: false

</td></tr><tr><td>

abortAction

</td><td>

Boolean

</td><td>

Flag that indicates whether to abort the current database transaction. For example, on a before insert business rule, if the conditions are met, don't insert the record into the database.Valid values:

-   false: Doesn't abort the current database transaction.
-   true: Aborts the current database transaction. You can't perform additional actions on the record, such as setting field values and running scripts. You can still display a message to users with the addMessage and message properties.

Default: false

</td></tr><tr><td>

message

</td><td>

String

</td><td>

A message that appears when the business rule runs.

</td></tr><tr><td>

roleConditions

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects that users who are modifying records in the table must have for the business rule to run. For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

condition

</td><td>

String

</td><td>

A JavaScript conditional statement that specifies the fields and values that must be true for the script to run. This property supports inline JavaScript or a reference to another file in the application that contains a script.**Note:** Don't use this property if you include the condition statement with the filterCondition or script properties.

By specifying the condition statement with this property, the condition is evaluated separately, and the business rule runs only if the condition is true. To have the condition statement reevaluated a second time before running an async business rule, set the **glide.businessrule.async\_condition\_check** system property to true.

Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

filterCondition

</td><td>

String

</td><td>

A filter query that specifies the fields and values that must be true for the business rule to run. For more information, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

setFieldValue

</td><td>

String

</td><td>

The values to set for fields in the table. This can be provided as an encoded query, such as `setFieldValue: 'sec_created=false^EQ'`.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of what the business rule does.

</td></tr><tr><td>

protectionPolicy

</td><td>

String

</td><td>

A policy that determines whether someone can view or edit the script include after the application is installed on their instance. If undefined, other application developers can customize the script include.Valid values:

-   read: Allows anyone to read values from this downloaded or installed script include. No one can change script values on the instance on which they download or install the script include.
-   protected: Provides intellectual property protection for application developers. Customers who download the script include cannot see the contents of the script field. The script is encrypted in memory to prevent unauthorized users from seeing it in plain text.

</td></tr><tr><td>

$meta

</td><td>

Object

</td><td>

Metadata for the application metadata.With the installMethod property, you can map the application metadata to an output directory that loads only in specific circumstances.

```javascript
$meta: {
      installMethod: 'String'
}
```

Valid values for installMethod:

-   demo: Outputs the application metadata to the `metadata/unload.demo` directory to be installed with the application when the **Load demo data** option is selected.
-   first install: Outputs the application metadata to the `metadata/unload` directory to be installed only the first time an application is installed on an instance.

</td></tr></tbody>
</table>```javascript
import { BusinessRule } from '@servicenow/sdk/core'
import { FunctionExport, FunctionExpression } from '../server/scripts.js'
import DefaultExportFunction from '../server/scripts.js'

const BR1 = BusinessRule({
    name: 'exportedFunction',
    table: 'x_snc_table',
    when: 'after',
    action: ['update', 'delete', 'insert'],
    script: FunctionExport,
    order: 100,
    active: true,
    addMessage: false,
    message: '<p>message</p>',
    abortAction: false,
    $id: Now.ID[0],
})

const BR2 = BusinessRule({
    name: 'businessrule2',
    table: 'x_snc_table',
    script: FunctionExpression,
    when: 'after',
    action: ['update'],
    $id: Now.ID[1],
})

const BR3 = BusinessRule({
    name: 'businessrule3',
    table: 'x_snc_table',
    script: DefaultExportFunction,
    when: 'after',
    action: ['update'],
    filterCondition: `sys_updated_onSTARTSWITHb^sys_updated_bySTARTSWITHm^EQ
    <item goto="false" or="false" field="sys_updated_on" endquery="false" value="b" operator="STARTSWITH" newquery="false"/>
    <item goto="false" or="false" field="sys_updated_by" endquery="false" value="m" operator="STARTSWITH" newquery="false"/>
    <item goto="false" or="false" field="" endquery="true" value="" operator="=" newquery="false"/>`,
    $id: Now.ID[2],
})

const BR4 = BusinessRule({
    name: 'templateBR',
    action: ['insert'],
    when: 'after',
    table: 'x_snc_table',
    roleConditions: [admin],
    order: 100,
    active: true,
    addMessage: true,
    message: '<p>message</p>',
    script: `gs.info('info')`,
    abortAction: false,
    $id: Now.ID[3],
})

```

