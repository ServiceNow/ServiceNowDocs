---
title: ServiceNow Fluent language constructs
description: ServiceNow Fluent language constructs provide additional functionality for development in source code with ServiceNow Fluent APIs.
locale: en-US
release: xanadu
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# ServiceNow Fluent language constructs

ServiceNow Fluent language constructs provide additional functionality for development in source code with ServiceNow Fluent APIs.

## Now.ID

The Now.ID construct is used to specify human-readable unique IDs for metadata defined in source code. Now.ID uses the format `Now.ID['String' or Number]` with the $id property in ServiceNow Fluent APIs. When you build an application, the ID is hashed into a unique sys\_id.

You can use Now.ID only to define IDs for metadata and not to reference other metadata in an application. To reference other metadata within the same application, you can assign the object to a const variable and reference the variable identifier in other objects.

```javascript
import { Role } from "@servicenow/sdk/core"

const managerRole = Role({ 
   $id: Now.ID['manager_role'], 
   name: 'x_snc_example.manager' 
})

Record({
  table: 'some_table',
  data: {
     role: managerRole //"role" is a reference field to sys_user_role
  }
})
```

## Now.ref

The Now.ref construct is used to reference metadata in a different application that's not defined in source code. Now.ref uses the format `Now.ref['table', 'sys_id' or {column: 'value'}, {column: 'value'}]` with Reference properties in ServiceNow Fluent APIs.

```javascript
import { Role } from "@servicenow/sdk/core"

Role({
    name: 'x_test.admin',
    contains_roles: [
        'x_test.manager',
        Now.ref('sys_user_role', { name: 'x_test.itil' }),           // Coalescing ID reference
        Now.ref('sys_user_role', '${itomId}'),                       // GUID-based reference
        Now.ref('sys_user_role', '3D82d1a88947942a90b6d8aa25126d439b', { name: 'x_test.csm' }),   // GUID with coalescing ID reference
    ],
})
```

## Now.include

The Now.include construct is used to refer to text content in another file in the same application rather than including the content inline. Now.include uses relative file paths in the format `Now.include('./path/to/file')` with any property in ServiceNow Fluent APIs. Using Now.include allows you to code with the appropriate syntax highlighting for the file type and is especially helpful with properties that support other languages like JavaScript, HTML, CSS, and more.

Now.include supports two-way synchronization so that changes to fields from other ServiceNow AI Platform user interfaces are synced into the referenced file's source code and changes to the source code are synced back to metadata across the instance.

```javascript
import { ScriptInclude } from '@servicenow/sdk/core'

ScriptInclude({
    $id: Now.ID['my-script-include'],
    name: 'MyScriptInclude',
    active: true,
    apiName: 'x_scriptincludes.MyScriptInclude',
    script: Now.include('./MyScriptInclude.server.js') //The actual content of the "script" field is contained in the file specified
})
```

## Now.attach

The Now.attach construct is used to refer to an image file in the same application and attach it to records associated with metadata defined in source code. Now.attach uses relative file paths in the format `Now.attach('./path/to/file')` with properties that support user images \(the user\_image field type\) in ServiceNow Fluent APIs. Now.attach supports the following file formats: `.jpg`, `.jpeg`, `.png`, `.gif`, `.bmp`, `.ico`, and `.svg`.

Now.attach supports two-way synchronization so that changes to image files from other ServiceNow AI Platform user interfaces are synced into the application in source code and changes to image files in source code are synced back to metadata across the instance.

```javascript
import { Record } from '@servicenow/sdk/core'

Record({
    $id: Now.ID['sample-service-portal'],
    table: 'sp_portal',
    data: {
        title: 'Sample Portal',
        url_suffix: 'sample',
        icon: Now.attach('../../assets/servicenow.jpg')
    }
})
```

You can also reuse an image in an application by assigning the Now.attach construct to a const variable and referencing the variable identifier in other properties. For example:

```javascript
import { Record } from '@servicenow/sdk/core'

const image = Now.attach('../../assets/servicenow.jpg')

Record({
    $id: Now.ID['test'],
    table: 'sp_portal',
    data: {
        title: 'Test Portal',
        url_suffix: 'test',
        icon: image,
        logo: image,
    }
})
```

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

