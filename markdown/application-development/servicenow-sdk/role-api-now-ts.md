---
title: Role API - ServiceNow Fluent
description: The Role API defines roles \[sys\_user\_role\] that grant specific permissions to users of an application.Create a role \[sys\_user\_role\] to control access to applications and their features.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Role API - ServiceNow Fluent

The Role API defines roles \[sys\_user\_role\] that grant specific permissions to users of an application.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about user roles, see [Managing roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/ua-creating-roles.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Role object

Create a role \[sys\_user\_role\] to control access to applications and their features.

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

A name for the role beginning with the application scope in the following format: `<scope>.<name>`.

</td></tr><tr><td>

assignableBy

</td><td>

String

</td><td>

Other roles that can assign this role to users.

</td></tr><tr><td>

canDelegate

</td><td>

Boolean

</td><td>

Flag that indicates if the role can be delegated to other users. For more information, see [Delegating roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_DelegateRoles.md).Valid values:

-   true: The role can be delegated to other users.
-   false: The role can't be delegated to other users.

Default: true

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of what the role can access.

</td></tr><tr><td>

elevatedPrivilege

</td><td>

Boolean

</td><td>

Flag that indicates whether manually accepting the responsibility of using the role before you can access the features of the role is required. For more information about elevated privileges, see [Elevated privilege roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_ElevatedPrivilege.md).Valid values:

-   true: You must manually accept the responsibility of using the role before you can access its features.
-   false: You don't need to manually accept the responsibility of using the role to access its features.

Default: false

</td></tr><tr><td>

grantable

</td><td>

Boolean

</td><td>

Flag that indicates whether the role can be granted independently.Valid values:

-   true: The role can be granted independently.
-   false: The role can't be granted independently.

Default: true

</td></tr><tr><td>

containsRoles

</td><td>

Array

</td><td>

The variable identifiers of other Role objects that this role contains.

</td></tr><tr><td>

scopedAdmin

</td><td>

Boolean

</td><td>

Flag that indicates whether the role is an Application Administrator role. For general information about application administration roles, see [Application administration](../../applications/concept/application-administration.md).Valid values:

-   true: The role is an Application Administrator.
-   false: The role isn't an Application Administrator.

Default: false

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

