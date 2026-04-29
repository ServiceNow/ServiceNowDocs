---
title: Cross-Scope Privilege API - ServiceNow Fluent
description: The Cross-Scope Privilege API defines cross-scope privileges \[sys\_scope\_privilege\] for runtime access tracking.Configure cross-scope privileges \[sys\_scope\_privilege\] that determine which script operations and targets the system allows to run in the application.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Cross-Scope Privilege API - ServiceNow Fluent

The Cross-Scope Privilege API defines cross-scope privileges \[sys\_scope\_privilege\] for runtime access tracking.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

Runtime access tracking allows administrators to manage script access to application resources by creating a list of script operations and targets that the system authorizes to run. For general information about cross-scope privileges, see [Cross-scope privilege record](../../applications/reference/c_CrossScopePrivilegeRecord.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## CrossScopePrivilege object

Configure cross-scope privileges \[sys\_scope\_privilege\] that determine which script operations and targets the system allows to run in the application.

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

status

</td><td>

String

</td><td>

Required. The authorization for this record.Valid values:

-   requested
-   allowed
-   denied

</td></tr><tr><td>

operation

</td><td>

String

</td><td>

Required. The operation that the script performs on the target. The target type determines the available operations. Tables \[sys\_db\_object\] support the read, write, create, and delete operations. Script includes \[sys\_script\_include\] and script objects \[sys\_db\_object\] only support the execute operation.

Valid values:

-   create
-   delete
-   read
-   write
-   execute

</td></tr><tr><td>

targetName

</td><td>

String

</td><td>

Required. The name of the table, script include, or script object being requested.

</td></tr><tr><td>

targetScope

</td><td>

String

</td><td>

Required. The application scope from which resources are requested.

</td></tr><tr><td>

targetType

</td><td>

String

</td><td>

Required. The type of request: script include, script object, or table.Valid values:

-   sys\_script\_include
-   scriptable
-   sys\_db\_object

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
import { CrossScopePrivilege } from '@servicenow/sdk/core'

CrossScopePrivilege({
   $id: Now.ID['cross_1'],
   status: 'allowed',
   operation: 'execute',
   targetName: 'Script type',
   targetScope: 'x_snc_example',
   targetType: 'scriptable',
})
```

