---
title: UI Action API - ServiceNow Fluent
description: The UI Action API defines custom user interface \(UI\) actions \[sys\_ui\_action\], such as buttons, links, and context menu items on forms and lists.Create a UI action \[sys\_ui\_action\] to display on a form.Configure how a UI action appears on a form.Configure how a UI action appears on the list view.Configure options to execute the UI action script in the browser.Configure how a UI action functions and appears in workspaces.
locale: en-US
release: zurich
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# UI Action API - ServiceNow Fluent

The UI Action API defines custom user interface \(UI\) actions \[sys\_ui\_action\], such as buttons, links, and context menu items on forms and lists.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about UI actions, see [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## UiAction object

Create a UI action \[sys\_ui\_action\] to display on a form.

<table id="table_qyv_1pj_4fc" class="parameters"><thead><tr><th>

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

Required. The name of the table on which the UI action is available. By default, the UI action also appears on tables that extend the selected table. For example, Task actions appear on the Incident table. Set the value to `global` to make the action available on all tables.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. The text that appears on the button, link, or context menu item. The name must be unique within the table specified.

</td></tr><tr><td>

actionName

</td><td>

String

</td><td>

A unique name to use when referencing the UI action in scripts.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI action is enabled.Valid values:

-   true: The UI action appears and executes.
-   false: The UI action is hidden.

Default: true

</td></tr><tr><td>

form

</td><td>

Object

</td><td>

Options for how UI actions appear on forms. For more information, see [form object](fluent-ui-action-api.md#).

</td></tr><tr><td>

list

</td><td>

Object

</td><td>

Options for how UI actions appear on the list view. For more information, see [list object](fluent-ui-action-api.md#).

</td></tr><tr><td>

client

</td><td>

Object

</td><td>

Options to execute the script in the browser. For more information, see [client object](fluent-ui-action-api.md#).

</td></tr><tr><td>

workspace

</td><td>

Object

</td><td>

Options for how UI actions function and appear in workspaces. For more information, see [workspace object](fluent-ui-action-api.md#).

</td></tr><tr><td>

overrides

</td><td>

Reference or String

</td><td>

The name or variable identifier of another UI action that the UI action overrides.

</td></tr><tr><td>

showInsert

</td><td>

Boolean

</td><td>

Flag that indicates whether to show a button on new records before they're inserted.Valid values:

-   true: The button appears on records before they're inserted.
-   false: The button doesn't appear on records that haven't been inserted.

Default: false

</td></tr><tr><td>

showUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to show a button on existing records.Valid values:

-   true: The button appears on existing records.
-   false: The button doesn't appear on existing records.

Default: true

</td></tr><tr><td>

showQuery

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI action is visible on a list when a filter query is applied.Valid values:

-   true: The UI action appears when a filter query is applied.
-   false: The UI action doesn't appear a filter query is applied.

Default: false

</td></tr><tr><td>

showMultipleUpdate

</td><td>

Boolean

</td><td>

Flag that indicates whether to show a button when multiple records are selected.Valid values:

-   true: The button appears when multiple records are selected.
-   false: The button doesn't appear when multiple records are selected.

Default: false

</td></tr><tr><td>

condition

</td><td>

String

</td><td>

A JavaScript conditional statement that specifies the fields and values that must be true for the script to run.**Note:**

-   Don't use this property if you include the condition statement with the script property.
-   The current object isn't available for conditions on a list context menu. If the list's showContextMenu property is true, any use of `current` on these actions is ignored.
-   You can reference the parent record for the UI action conditions on a related list button. For example, to disable the **New** and **Edit** buttons on the Affected CIs related list for closed changes, copy the global m2m UI actions to the task\_ci table and add a condition of **parent.active**.
-   If you leave one of the fields that you specify in your condition statement empty, that condition defaults to true.

Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

A client-side or server-side script that runs when the UI action is executed. Function names must be unique. This property supports inline JavaScript or a reference to another file in the application that contains a script.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

comments

</td><td>

String

</td><td>

Internal notes about the UI action.

</td></tr><tr><td>

messages

</td><td>

String

</td><td>

Text strings that the UI action can use as a key to look up a localized message alternative from the Message \[sys\_ui\_message\] table. Each message key is on a separate line in the Messages field. The instance looks for a localized message string anytime the UI action makes a getmessage\('\[message\]'\) call where the message string matches a key in the Messages field. For more information, see [Translate a client script message](https://www.servicenow.com/docs/access?context=t_TranslateAClientScriptMessage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

hint

</td><td>

String

</td><td>

A short description of the UI action that displays as tooltip when hovering over it.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

The order in which the UI action appears. The order applies to buttons from left to right and to menu actions from top to bottom.Default: 100

</td></tr><tr><td>

isolateScript

</td><td>

Boolean

</td><td>

Flag that indicates whether the script runs in strict mode, with access to direct DOM, jQuery, prototype, and the window object turned off.Valid values:

-   true: Isolate the script and don't run it in strict mode.
-   false: Run the script in strict mode.

Default: false

</td></tr><tr><td>

roles

</td><td>

Array

</td><td>

A list of variable identifiers of Role objects or names of roles required for the UI action to apply. For more information, see [Role API - ServiceNow Fluent](role-api-now-ts.md#).

</td></tr><tr><td>

includeInViews

</td><td>

Array

</td><td>

A list of names of views in which the UI action is included.

</td></tr><tr><td>

excludeFromViews

</td><td>

Array

</td><td>

A list of names of views from which the UI action is excluded.

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
import { UiAction } from '@servicenow/sdk/core'
        
UiAction({
    $id: Now.ID['car_info'],
    table: 'x_snc_ts_custom_cars',
    actionName: 'Car Information',
    name: 'View car info',
    active: true,
    showInsert: true,
    showUpdate: true,
    hint: 'View car info',
    condition: "current.type == 'SUV'",
    form: {
        showButton: true,
        showLink: true,
        showContextMenu: false,
        style: 'destructive',
    },
    list: {
        showLink: true,
        style: 'primary',
        showButton: true,
        showContextMenu: false,
        showListChoice: false,
        showBannerButton: true,
        showSaveWithFormButton: true,
    },
    workspace: {
        isConfigurableWorkspace: true,
        showFormButtonV2: true,
        showFormMenuButtonV2: true,
        clientScriptV2: `function onClick(g_form) {
                        }`,
    },
    script: `current.name =  "updated by script";
                current.update();`,
    roles: ['u_requestor'],
    client: {
        isClient: true,
        isUi11Compatible: true,
        isUi16Compatible: true,
        },
    order: 100,
    showQuery: false,
    showMultipleUpdate: false,
    isolateScript: false,
    includeInViews: ['specialView'],
    excludeFromViews: [],
})
```

## form object

Configure how a UI action appears on a form.

The form object is a property within the UiAction object.

<table id="table_qyv_1pj_4fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

showButton

</td><td>

Boolean

</td><td>

Flag that indicates whether to include a button on a form.Valid values:

-   true: A button appears on forms.
-   false: A button doesn't appear on forms.

Default: false

</td></tr><tr><td>

showLink

</td><td>

Boolean

</td><td>

Flag that indicates whether to include a link in the Related Links section of a form.Valid values:

-   true: A link appears in the Related Links section.
-   false: A link doesn't appear in the Related Links section.

Default: false

</td></tr><tr><td>

showContextMenu

</td><td>

Boolean

</td><td>

Flag that indicates whether to include an item in the context menu of a form.Valid values:

-   true: An item appears in the context menu.
-   false: An item doesn't appear in the context menu.

Default: false

</td></tr><tr><td>

style

</td><td>

String

</td><td>

A style that defines how UI action buttons appear on a form.Valid values:

-   primary: Colors the UI action blue.
-   destructive: Colors the UI action red.
-   unstyled: The UI action isn’t styled.

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
form: {
  showButton: true,
  showLink: true,
  showContextMenu: false,
  style: 'destructive',
}
```

## list object

Configure how a UI action appears on the list view.

The list object is a property within the UiAction object.

<table id="table_qyv_1pj_4fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

showButton

</td><td>

Boolean

</td><td>

Flag that indicates whether to include a button at the bottom of a list.**Note:** Buttons at the bottom of a list appear regardless of condition and are evaluated per record on execution.

Valid values:

-   true: A button appears at the bottom of lists.
-   false: A button doesn't appear at the bottom of lists.

Default: false

</td></tr><tr><td>

showLink

</td><td>

Boolean

</td><td>

Flag that indicates whether to include a link in the Related Links section of a list.Valid values:

-   true: A link appears in the Related Links section.
-   false: A link doesn't appear in the Related Links section.

Default: false

</td></tr><tr><td>

showContextMenu

</td><td>

Boolean

</td><td>

Flag that indicates whether to include an item in the context menu of a list.Valid values:

-   true: An item appears in the context menu.
-   false: An item doesn't appear in the context menu.

Default: false

</td></tr><tr><td>

style

</td><td>

String

</td><td>

A style that defines how UI action buttons appear on the list view.Valid values:

-   primary: Colors the UI action blue.
-   destructive: Colors the UI action red.
-   unstyled: The UI action isn’t styled.

</td></tr><tr><td>

showListChoice

</td><td>

Boolean

</td><td>

Flag that indicates whether to include a choice in the Actions list of a list.**Note:** Choices in the Actions list appear regardless of condition and are evaluated per record on execution.

Valid values:

-   true: A choice appears in the Actions list.
-   false: A choice doesn't appear in the Actions list.

Default: false

</td></tr><tr><td>

showBannerButton

</td><td>

Boolean

</td><td>

Flag that indicates whether to include a button on the banner of a list.**Note:** Buttons on the banner of a list aren’t intended to support record-specific conditions. Only the first row is considered when the condition is evaluated to determine whether the button appears for the list. Don't use record-specific conditions, such as `current.getValue('state') === 'closed'`.

Valid values:

-   true: A button appears on the banner of lists.
-   false: A button doesn't appear on the banner of lists.

Default: false

</td></tr><tr><td>

showSaveWithFormButton

</td><td>

Boolean

</td><td>

Flag that indicates whether the form is saved when accessed from a list before executing the UI action button.Valid values:

-   true: The form must be saved before the UI action executes.
-   false: The form doesn't have to be saved before the UI action executes.

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
list: {
  showButton: true,
  showLink: true,
  showContextMenu: false,
  style: 'primary',
  showListChoice: false,
  showBannerButton: true,
  showSaveWithFormButton: true,
}
```

## client object

Configure options to execute the UI action script in the browser.

The client object is a property within the UiAction object.

<table id="table_qyv_1pj_4fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isClient

</td><td>

Boolean

</td><td>

Flag that indicates where the UI action script runs.Valid values:

-   true: The script runs on the client \(the user's browser\).
-   false: The script runs on the server.

Default: false

</td></tr><tr><td>

isUi11Compatible

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI action is supported in the legacy UI 11.Valid values:

-   true: The UI action is supported in the legacy UI 11.
-   false: The UI action isn't supported in the legacy UI 11.

Default: false

</td></tr><tr><td>

isUi16Compatible

</td><td>

Boolean

</td><td>

Flag that indicates whether the UI action is supported in the Core UI. Valid values:

-   true: The UI action is supported in the Core UI.
-   false: The UI action isn't supported in the Core UI.

Default: false

</td></tr><tr><td>

onClick

</td><td>

String

</td><td>

The name of the JavaScript function to run when the UI action is executed. The function is defined with the script property.

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
client: {
  isClient: true,
  isUi11Compatible: true,
  isUi16Compatible: true,
  onClick: 'reopenIncident()'
}
```

## workspace object

Configure how a UI action functions and appears in workspaces.

The workspace object is a property within the UiAction object.

<table id="table_qyv_1pj_4fc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isConfigurableWorkspace

</td><td>

Boolean

</td><td>

Flag that indicates the type of workspace in which a UI action applies.Valid values:

-   true: The UI action applies to Configurable Workspaces.
-   false: The UI action applies to Legacy Workspaces.

Default: false

</td></tr><tr><td>

showFormButtonV2

</td><td>

Boolean

</td><td>

Flag that indicates whether to include a button on forms in a workspace.Valid values:

-   true: A button appears on forms.
-   false: A button doesn't appear on forms.

Default: false

</td></tr><tr><td>

showFormMenuButtonV2

</td><td>

Boolean

</td><td>

Flag that indicates whether to include an item in the More Actions menu in a workspace.Valid values:

-   true: An item appears in the More Actions menu.
-   false: An item doesn't appear in the More Actions menu.

Default: false

</td></tr><tr><td>

clientScriptV2

</td><td>

String

</td><td>

A script that runs when the UI action is executed in workspaces. This property supports inline JavaScript or a reference to another file in the application that contains a script.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

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
workspace: {
  isConfigurableWorkspace: true,
  showFormButtonV2: true,
  showFormMenuButtonV2: true,
  clientScriptV2: `function onClick(g_form) {
  }`,
}
```

