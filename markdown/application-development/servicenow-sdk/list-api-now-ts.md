---
title: List API - ServiceNow Fluent
description: The List API defines list views \[sys\_ui\_list\] for tables.Configure lists \[sys\_ui\_list\] and their views.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# List API - ServiceNow Fluent

The List API defines list views \[sys\_ui\_list\] for tables.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about lists, see [ServiceNow AI Platform® list administration](https://www.servicenow.com/docs/access?context=p_ListAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## List object

Configure lists \[sys\_ui\_list\] and their views.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

table

</td><td>

String

</td><td>

Required. The name of the table to which the list applies.

</td></tr><tr><td>

view

</td><td>

Reference or String

</td><td>

Required. The variable identifier or name of the UI view \[sys\_ui\_view\] which applies, or the default view. To define a UI view, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).To use the default view \(`default_view`\), you must import it:

```javascript
import { default_view } from '@servicenow/sdk/core'
```

</td></tr><tr><td>

columns

</td><td>

Array

</td><td>

Required. A list of columns in the table to display in the list, specified using the column name and position in the list.

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
import { List } from "@servicenow/sdk/core";

List({
    $id: Now.ID["app_task_view_list"],
    table: "cmdb_ci_server",
    view: app_task_view,
    columns: [
        { element: "name", position: 0 },
        { element: "business_unit", position: 1 },
        { element: "vendor", position: 2 },
        { element: "cpu_type", position: 3 },
    ],
});

```

The UI view definition referenced is defined using the Record object:

```javascript
import { Record } from "@servicenow/sdk/core";

const app_task_view = Record({
   $id: Now.ID['app_task_view'],
   table: 'sys_ui_view',
   data: {
        name: 'app_task_view',
        title: 'app_task_view'
   }
})
```

