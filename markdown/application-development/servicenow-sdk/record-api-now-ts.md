---
title: Record API - ServiceNow Fluent
description: The Record API defines records in any table. Use the Record API to define application metadata that doesn't have a dedicated ServiceNow Fluent API.Add data to any table with a record.
locale: en-US
release: xanadu
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Record API - ServiceNow Fluent

The Record API defines records in any table. Use the Record API to define application metadata that doesn't have a dedicated ServiceNow Fluent API.

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Record object

Add data to any table with a record.

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

table

</td><td>

String

</td><td>

Required. The name of the table to which the record belongs.

</td></tr><tr><td>

data

</td><td>

Object

</td><td>

Fields and their values in the table. For example:```javascript
data: {
   state: 'Ready',
   task: 'Add demo data'
}
```

To use text content from another file, refer to a file in the application using the `Now.include` syntax. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).

```javascript
data: {
   script: Now.include('./script-file.js'),
   html: Now.include('./html-file.html'),
   css: Now.include('./css-file.css')
 }
```

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
</table>In this example, a record defining a menu category is added to the Menu Category \[sys\_app\_category\] table. The menu category style is defined in the `css-file.css` file.

```javascript
import { Record } from "@servicenow/sdk/core";

export const appCategory = Record({
   table: 'sys_app_category',
   $id: Now.ID[9],
   data: {
      name: 'example',
      style: Now.include\('./css-file.css'\),
   },
})
```

In this example, a record defining an incident is added to the Incident \[incident\] table.

```javascript
import { Record } from '@servicenow/sdk/core';

export const incident1 = Record({
  $id: Now.ID['incident-1'],
  table: 'incident',
  data: {
    active: 'true',
    approval: 'not requested',
    description: 'Unable to send or receive emails.',
    incidentState: '1',
    shortDescription: 'Email server is down.',
    subcategory: 'email',
    callerId: '77ad8176731313005754660c4cf6a7de',
  }
})
```

In this example, a record defining a server is added to the Server \[cmdb\_ci\_server\] table.

```javascript
import { Record } from '@servicenow/sdk/core';

export const ciserver1 = Record({
  $id: Now.ID['cmdb-ci-server-1'],
  table: 'cmdb_ci_server',
  data: {
    assetTag: 'P1000199',
    attested: 'false',
    canPrint: 'false',
    company: 'e7c1f3d53790200044e0bfc8bcbe5deb',
    cost: '2160',
    costCc: 'USD',
    cpuSpeed: '633',
    cpuType: 'GenuineIntel',
    diskSpace: '100',
    manufacturer: 'b7e7d7d8c0a8016900a5d7f291acce5c',
    name: 'DatabaseServer1',
    os: 'Linux Red Hat',
    shortDescription: 'DB Server',
    subcategory: 'Computer',
  }
})
```

