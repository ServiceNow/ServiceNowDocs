---
title: Client Script API - ServiceNow Fluent
description: The Client Script API defines client-side scripts \[sys\_script\_client\] that run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.Create a client script \[sys\_script\_client\] to configure forms, form fields, and field values while the user is using the form.
locale: en-US
release: yokohama
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Client Script API - ServiceNow Fluent

The Client Script API defines client-side scripts \[sys\_script\_client\] that run JavaScript on the client \(web browser\) when client-based events occur, such as when a form loads, after form submission, or when a field changes value.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about client scripts, see [Client scripts](https://www.servicenow.com/docs/access?context=client-scripts&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## ClientScript object

Create a client script \[sys\_script\_client\] to configure forms, form fields, and field values while the user is using the form.

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

Required. The name of the table on which the client script runs.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. The name of the client script.

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script is enabled.Valid values:

-   true: The script is enabled.
-   false: The script isn't enabled.

Default: true

</td></tr><tr><td>

appliesExtended

</td><td>

Boolean

</td><td>

Flag that indicates whether the client script applies to tables extended from the specified table.Valid values:

-   true: The script applies to extended tables.
-   false: The script doesn't apply to extended tables.

Default: false

</td></tr><tr><td>

uiType

</td><td>

String

</td><td>

The user interface to which the client script applies.Valid values:

-   desktop
-   mobile\_or\_service\_portal
-   all

Default: desktop

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the functionality and purpose of the client script.

</td></tr><tr><td>

messages

</td><td>

String

</td><td>

Text strings that are available to the client script as localized messages using getmessage\('\[message\]'\). For more information, see [Translate a client script message](https://www.servicenow.com/docs/access?context=t_TranslateAClientScriptMessage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

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

script

</td><td>

Script

</td><td>

A client-side script that runs in the browser. This property supports inline JavaScript or a reference to another file in the application that contains a script.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

global

</td><td>

Boolean

</td><td>

Flag that indicates on which views of the table the client script runs.Valid values:

-   true: The script runs on all views.
-   false: The script runs only on the specified views.

Default: true

</td></tr><tr><td>

view

</td><td>

String

</td><td>

The views of the table on which the client script runs. This property applies only when the global property is set to false.

</td></tr><tr><td>

type

</td><td>

String

</td><td>

The type of client script, which defines when it runs. For more information about the supported types, see [Client scripts](https://www.servicenow.com/docs/access?context=client-scripts&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).Valid values:

-   onCellEdit: Runs when the list editor changes a cell value.
-   onChange: Runs when a particular field value changes on the form.
-   onLoad: Runs when the system first renders the form and before users can enter data. Typically, onLoad\(\) client scripts perform client-side-manipulation of the current form or set default record values.
-   onSubmit: Runs when a form is submitted. Typically, onSubmit\(\) scripts validate things on the form and ensure that the submission makes sense. An onSubmit\(\) client script can cancel form submission by returning a value of false.

</td></tr><tr><td>

field

</td><td>

String

</td><td>

A field on the table that the client script applies to. This property applies only when the type property is set to onChange or onCellEdit.

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
import { ClientScript } from '@servicenow/sdk/core'

export const cs = ClientScript({
   $id: Now.ID['my_scripts'], 
   name: 'my_scripts',
   table: 'incident',
   active: true, 
   appliesExtended: false, 
   global: true,
   uiType: 'all', 
   messages: '', 
   isolateScript: false, 
   type: 'onLoad',
   script: Now.include\('../client/client-script.js'\),
})
```

The client script is defined in the `client-script.js` file referenced from the script property. For example:

```javascript
function onLoad() { 
    const x = 'util' g_form.addInfoMessage(x) 
}
```

