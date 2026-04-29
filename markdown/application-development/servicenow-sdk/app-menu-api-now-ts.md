---
title: Application Menu API - ServiceNow Fluent
description: The Application Menu API defines menus in the application navigator \[sys\_app\_application\].Create a menu for an application \[sys\_app\_application\].
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Application Menu API - ServiceNow Fluent

The Application Menu API defines menus in the application navigator \[sys\_app\_application\].

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about application menus, see [Create an application menu](../../../administer/auto-test-framework/reference/test-steps-app-navigator-category.md#).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## ApplicationMenu object

Create a menu for an application \[sys\_app\_application\].

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

title

</td><td>

String

</td><td>

Required. The label for the menu in the application navigator.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the menu appears in the application navigator.Valid values:

-   true: The menu appears.
-   false: The menu is hidden.

Default: true

</td></tr><tr><td>

roles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or names of roles that can access the menu. For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

category

</td><td>

Reference

</td><td>

The variable identifier of a menu category \[sys\_app\_category\] that defines the navigation menu style. To define a menu category, use the [Record API - ServiceNow Fluent](record-api-now-ts.md#).For general information about menu categories, see [Customize menu categories](https://www.servicenow.com/docs/access?context=customize-menu-categories&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

hint

</td><td>

String

</td><td>

A short description of the menu that displays as tooltip when hovering over it.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

Additional information about what the application does.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

An internal name to differentiate between applications with the same title.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The relative position of the application menu in the application navigator.Default: 100

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
import { ApplicationMenu } from "@servicenow/sdk/core";

ApplicationMenu({
   $id: Now.ID['my_app_menu'],
   title: 'My App Menu',
   hint: 'This is a hint',
   description: 'This is a description',
   category: appCategory,
   roles: ['admin'],
   active: true,
})
```

The category referenced is defined using the Record object:

```javascript
import { Record } from "@servicenow/sdk/core";

export const appCategory = Record({
   table: 'sys_app_category',
   $id: Now.ID[9],
   data: {
      name: 'example',
      style: 'border-color: #a7cded; background-color: #e3f3ff;',
   },
})
```

