---
title: Property API - ServiceNow Fluent
description: The Property API defines system properties \[sys\_properties\] that control instance behavior.Add a system property \[sys\_properties\] for configuring an aspect of an application.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Property API - ServiceNow Fluent

The Property API defines system properties \[sys\_properties\] that control instance behavior.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about system properties, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Property object

Add a system property \[sys\_properties\] for configuring an aspect of an application.

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

Required. The name of the property beginning with the application scope in the following format: `<scope>.<name>`.

</td></tr><tr><td>

value

</td><td>

Any

</td><td>

A value for the property. The value must be the correct data type.All property values are stored as strings. When retrieving properties via the gs.getProperty\(\) method, treat the results as strings. For example, a true\|false property returns 'true' or 'false' \(strings\), not the Boolean equivalent.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

A data type for the property value.Valid values: string, integer, boolean, choicelist, color, date\_format, image, password, password2, short\_string, time\_format, timezone, uploaded\_image

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of what the property does.

</td></tr><tr><td>

choices

</td><td>

Array

</td><td>

A comma-separated list of choice values. This property only applies if the type property is set to `choicelist`. If you need a different choice label and value, use an equal sign \(=\) to separate the label from the value. For example, `['Blue=0000FF', 'Red=FF0000', 'Green=00FF00']` displays **Blue**, **Red**, and **Green** in the list, and saves the corresponding hex value in the property value field.

</td></tr><tr><td>

roles

</td><td>

Object

</td><td>

The variable identifiers of Role objects or names of roles that have read or write access to the property. For example:```javascript
roles: {
   read: [activity_admin, 'app_user'],
   write: [admin]
}
```

For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

ignoreCache

</td><td>

Boolean

</td><td>

Flag that indicates whether to cache flush when the value of the property is set.The system stores system property values in server-side caches to avoid querying the database for configuration settings. When you change a system property value, the system flushes the cache for the System Properties \[sys\_properties\] table. Use this field to determine whether to flush this property's value from all other server-side caches.

Valid values:

-   true: The system ignores flushing some server-side caches, thus flushing only the cache for the System Properties \[sys\_properties\] table and preserving the prior property value in all other caches. This option avoids the performance cost of flushing all caches and retrieving new property values. Generally, you should only set this property to `true` when you have a system property that changes more frequently than once a month, and the property value is only stored in the System Properties \[sys\_properties\] table table.
-   false: The system flushes all server-side caches and retrieves the current property value from the database. Set this property to `false` for all caches to have the current property value.

Default: false

</td></tr><tr><td>

isPrivate

</td><td>

Boolean

</td><td>

Flag that indicates whether to exclude the property from being imported via update sets.Keeping system properties private helps prevent settings in one instance from overwriting values in another instance. For example, you might not want a system property in a development instance to use the same value as a production instance.

Valid values:

-   true: The property isn’t included in update sets.
-   false: The property is included in update sets.

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
import { Property } from '@servicenow/sdk/core'

Property({
   $id: Now.ID['1234'],
   name: 'x_snc_app.some.new.prop',
   type: 'string',
   value: 'hello',
   description: 'A new property',
   roles: {
      read: ['admin'],
      write: [adminRole, managerRole],
   },
   ignoreCache: false,
   isPrivate: false,
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

