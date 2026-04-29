---
title: Script Action API - ServiceNow Fluent
description: The Script Action API defines script actions \[sysevent\_script\_action\] that run when an event occurs.Create a script action \[sysevent\_script\_action\] that performs a task when triggered by an event.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Script Action API - ServiceNow Fluent

The Script Action API defines script actions \[sysevent\_script\_action\] that run when an event occurs.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For general information about scheduled script executions, see [Script actions](https://www.servicenow.com/docs/access?context=r_ScriptActions&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## ScriptAction object

Create a script action \[sysevent\_script\_action\] that performs a task when triggered by an event.

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

name

</td><td>

String

</td><td>

Required. A unique name for the script action.

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

Required. A server-side script that runs when triggered by an event. This property supports a function from a JavaScript module, a reference to another file in the application that contains a script, or inline JavaScript.Format:

-   For functions, use the name of a function, function expression, or default function exported from a JavaScript module and import it into the `.now.ts` file. For information about JavaScript modules, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).
-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

eventName

</td><td>

String

</td><td>

Required. The event that triggers the script action to run. For information about creating events, see [Create an event](https://www.servicenow.com/docs/access?context=t_CreateYourOwnEvent&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the script action is enabled.Valid values:

-   true: The script action executes when triggered by the event.
-   false: The script action doesn't execute.

Default: false

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the functionality and purpose of the script action.

</td></tr><tr><td>

order

</td><td>

Number

</td><td>

A number indicating the sequence in which the script action should run. If there are multiple script actions on a particular event, the script actions run in the order specified, from lowest to highest.Default: 100

</td></tr><tr><td>

conditionScript

</td><td>

String

</td><td>

A JavaScript conditional statement that specifies the fields and values that must be true for the script to run.**Note:** Don't use this property if you include the condition statement with the script property.

Format:

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
import { ScriptAction } from '@servicenow/sdk/core'
import { insertIncident } from '../server/scripts.js'

ScriptAction({
    $id: Now.ID['sample-script-action'],
    name: 'SampleScriptAction',
    active: true,
    description: 'Insert an incident',
    script: insertIncident,
    eventName: 'sample.event',
    order: 100,
    conditionScript: "gs.hasRole('my_role')"
})
```

The script property refers to a function from the `scripts.js` module. For example:

```javascript
import { GlideRecord } from '@servicenow/glide'

export const insertIncident = () => {
    var gr = new GlideRecord('incident')
    gr.initialize()
    gr.setValue('short_description', 'New incident from event')
    gr.insert()
}
```

