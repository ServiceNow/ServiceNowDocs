---
title: Access Control List API - ServiceNow Fluent
description: The Access Control List API defines access control lists \[sys\_security\_acl\] that secure parts of an application.Configure a custom ACL rule \[sys\_security\_acl\] to secure access to new objects or to change the default security behavior.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Access Control List API - ServiceNow Fluent

The Access Control List API defines access control lists \[sys\_security\_acl\] that secure parts of an application.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about access control lists \(ACLs\), see [Access Control List Rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/access-control-rules.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## ACL object

Configure a custom ACL rule \[sys\_security\_acl\] to secure access to new objects or to change the default security behavior.

ACLs must include one or more roles, a security attribute, a condition, or a script.

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

operation

</td><td>

String

</td><td>

Required. The operation that this ACL rule secures. An ACL rule can only secure one operation. To secure multiple operations, create a separate ACL rule for each.The operation must be `execute` if the type property is client\_callable\_flow\_object, client\_callable\_script\_include, graphql, processor, or rest\_endpoint.

Valid values:

-   execute: Allow users to execute scripts on a record or UI page.
-   create: Allow users to insert new records \(rows\) into a table.
-   read: Allow users to display records from a table.
-   write: Allow users to update records in a table.
-   delete: Allow users to remove records from a table or drop a table.
-   conditional\_table\_query\_range: Enables users to give partial ACL-access based on read ACLs. Created for the tables that have the read ACLs without Data condition and script.
-   data\_fabric: Enable users to allow Data Fabric connectors to access data on a particular table.
-   query\_match: Enables users to submit match queries \(such as "is", "is not", and "is empty"\).
-   query\_range: Enables users to submit range queries \(such as "starts with", "ends with", and "contains"\) and sorting is unrestricted.
-   edit\_task\_relations: Allow users to extend the Task \[task\] table.
-   edit\_ci\_relations: Allow users to extend the Configuration Item \[cmdb\_ci\] table.
-   save\_as\_template: Allow users to save a record as a template.
-   add\_to\_list: Allow users from viewing or personalizing specific columns in the list mechanic. Conditions and scripts aren't supported.
-   report\_on: Allow users to report on tables.
-   list\_edit: Allow users to update records \(rows\) from a list.
-   report\_view: Allow users to report on field ACLs.
-   personalize\_choices: Allow users to configure the table or field.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

Required. The type of object that this ACL rule secures. The type determines which operations are available. After creating an ACL rule, if you want to change the type, you must delete the ACL and create a new one with the correct type.

Valid values:

-   record
-   rest\_endpoint
-   ui\_page
-   processor
-   graphql
-   pd\_action
-   ux\_data\_broker
-   ux\_page
-   ux\_route
-   client\_callable\_flow\_object
-   client\_callable\_script\_include

Default: record

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the ACL rule is enforced.Valid values:

-   true: The ACL rule is enforced.
-   false: The ACL rule isn't enforced.

Default: true

</td></tr><tr><td>

adminOverrides

</td><td>

Boolean

</td><td>

Flag that indicates whether users with the admin role automatically pass the permissions check for this ACL rule.Valid values:

-   true: Administrators automatically pass the permissions check.

If true, admin users pass the permissions check regardless of what script or role restrictions apply. However, the nobody role, which only ServiceNow personnel can assign, takes precedence over the admin override option. If an ACL is assigned the nobody role, admin users cannot access the resource even when adminOverrides is true. For more information, see [Base system roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/r_BaseSystemRoles.md).

-   false: Administrators must meet the permissions defined in this ACL rule to gain access to the secured object. Use the condition or script properties to create a permissions check that administrators must pass.

Default: true

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

A custom script that defines the permissions required to access the object. This property supports a function from a JavaScript module, a reference to another file in the application that contains a script, or inline JavaScript. ACLs must include one or more roles, a security attribute, a condition, or a script.

**Note:** If the type property is `graphql`, scripts aren't supported.

The script can use the values of the `current` and `previous` global variables and system properties. The script must generate a true or false response in one of two ways:

-   return an `answer` variable set to a value of true or false
-   evaluate to true or false

In either case, users only gain access to the object when the script evaluates to true and the user meets any conditions the ACL rule has. Both the conditions and the script must evaluate to true for a user to access the object.

**Note:** If the evaluated item is in a related list, `current` points to the item the related list is on, not to the current item the ACL is for. However, If the item you are evaluating the ACL for is not in a related list, `current` points to the actual item.

Format:

-   For functions, use the name of a function, function expression, or default function exported from a JavaScript module and import it into the `.now.ts` file. For information about JavaScript modules, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the object or permissions this ACL rule secures.

</td></tr><tr><td>

localOrExisting

</td><td>

String

</td><td>

The type of security attribute to apply.Valid values:

-   Local: A security attribute based on the condition property that is saved only for the ACL it is created in.
-   Existing: An existing security attribute to reference in the security\_attribute property.

Default: Local

</td></tr><tr><td>

decisionType

</td><td>

String

</td><td>

An option for whether the ACL should allow or deny access.Valid values:

-   allow: The ACL allows access.
-   deny: The ACL denies access.

Default: allow

</td></tr><tr><td>

condition

</td><td>

String

</td><td>

A filter query that specifies the fields and values that must be true for users to access the object. For more information, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md).ACLs must include one or more roles, a security attribute, a condition, or a script.

</td></tr><tr><td>

roles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or sys\_ids of roles that a user must have to access the object. For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).ACLs must include one or more roles, a security attribute, a condition, or a script.

**Note:** Users with the admin role always pass this permissions check because the admin role automatically grants users all other roles.

</td></tr><tr><td>

securityAttribute

</td><td>

String

</td><td>

Pre-defined conditions for the ACL to use. For example, whether a user is impersonating another user. For more information about security attributes, see [OOB \(Out-of-Box\) Security Attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/oob-security-attributes.md).ACLs must include one or more roles, a security attribute, a condition, or a script.

**Note:** For security attributes with the **Is localized** field set to true, the localOrExisting property of the ACL should be set to Local. If the **Is localized** field is false, the localOrExisting property should be set to Existing.

</td></tr><tr><td>

table

</td><td>

String

</td><td>

The name of the table to which the ACL applies.This property only applies and is required if the type property is one of the following values: ux\_data\_broker, ux\_page, ux\_route, pd\_action, or record.

</td></tr><tr><td>

field

</td><td>

String

</td><td>

The name of a field on the table to secure. You can use the wildcard character \(`"*"`\) to select all fields.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

The name of the ACL.This property only applies and is required if the type property is one of the following values: rest\_endpoint, ui\_page, processor, graphql, client\_callable\_flow\_object, or client\_callable\_script\_include.

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
import { Acl } from "@servicenow/sdk/core";

export default Acl({
    $id: Now.ID['task_delete_acl'],
    active: true,
    adminOverrides: true,
    type: 'record',
    table: 'task',
    field: 'description',
    operation: 'delete',
    roles: [adminRole, managerRole],
})
```

The roles referenced are defined using the Role object:

```javascript
import { Role } from "@servicenow/sdk/core";

const managerRole = Role({ 
   $id: Now.ID['manager_role'], 
   name: 'x_snc_example.manager' 
})

const adminRole = Role({ 
   $id: Now.ID['admin_role'], 
   name: 'x_snc_example.admin', 
   containsRoles: [managerRole] 
})
```

