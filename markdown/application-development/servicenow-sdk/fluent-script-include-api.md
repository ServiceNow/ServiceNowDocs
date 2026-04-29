---
title: Script Include API - ServiceNow Fluent
description: The Script Include API defines script includes \[sys\_script\_include\] that store JavaScript functions and classes for use by server-side scripts.Create a script include \[sys\_script\_include\] to define a server-side script that runs when called from other scripts.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [ServiceNow Fluent API reference, Reference, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Script Include API - ServiceNow Fluent

The Script Include API defines script includes \[sys\_script\_include\] that store JavaScript functions and classes for use by server-side scripts.

**Note:** For the latest ServiceNow Fluent API documentation and examples, see the [ServiceNow Fluent API reference](https://servicenow.github.io/sdk/) and [ServiceNow SDK examples repository](https://github.com/ServiceNow/sdk-examples) on GitHub.

For new scripts, use JavaScript modules instead of script includes when possible to support code reuse and using third-party libraries within an application scope. For more information about JavaScript module support and limitations, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).

For general information about script includes, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=australia&pubname=australia-api-reference&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## ScriptInclude object

Create a script include \[sys\_script\_include\] to define a server-side script that runs when called from other scripts.

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

Required. The name of the script include. If you define a class, the name must match the name of the class, prototype, and type. If you use a classless \(on demand\) script include, the name must match the function name.

</td></tr><tr><td>

script

</td><td>

Script

</td><td>

Required. A server-side script to call from other scripts. The script must define a single JavaScript class or a global function. The class or function name must match the name property. This property supports inline JavaScript or a reference to another file in the application that contains a script.Format:

-   To use text content from another file, refer to a file in the application using the following format: `Now.include('path/to/file')`. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).
-   To provide an inline script, use string literals or template literals for multiple lines of code: `'Script' or `Script``.

</td></tr><tr><td>

apiName

</td><td>

String

</td><td>

An internal name for the script include, which is used to call the script include from out-of-scope applications.Default: &lt;scope&gt;.&lt;name&gt;

</td></tr><tr><td>

description

</td><td>

String

</td><td>

A description of the purpose and function of the script include.

</td></tr><tr><td>

clientCallable

</td><td>

Boolean

</td><td>

Flag that indicates whether client-side scripts can call the script include using GlideAjax.The script include is available to client scripts, list/report filters, reference qualifiers, or if specified as part of the URL. Client callable script includes are invoked from GlideAjax and require users to satisfy an ACL associated with the script include.

Valid values:

-   true: The script include is available to client-side scripts.
-   false: The script include isn't available to client-side scripts.

Default: false

</td></tr><tr><td>

mobileCallable

</td><td>

Boolean

</td><td>

Flag that indicates whether the script include is available to client scripts called from mobile devices.Valid values:

-   true: The script include is available to client scripts called from mobile devices.
-   false: The script include isn't available to client scripts called from mobile devices.

Default: false

</td></tr><tr><td>

sandboxCallable

</td><td>

Boolean

</td><td>

Flag that indicates whether the script include is available to scripts invoked from the script sandbox, such as a query condition.**Important:** Script includes should only be made available to the script sandbox if necessary.

Valid values:

-   true: The script include is available to scripts invoked from the script sandbox.
-   false: The script include isn't available to scripts invoked from the script sandbox.

Default: false

</td></tr><tr><td>

callerAccess

</td><td>

String

</td><td>

An option for how cross-scope access to the script include is permitted. For more information, see [Restricted caller access privilege settings](../../applications/concept/restricted-caller-access-privilege.md).Valid values:

-   restriction: Calls to the script include must be manually approved. Access requests are tracked in the Restricted Caller Access table with a status of Requested.
-   tracking: Calls to the script include are automatically approved. Calls are tracked in the Restricted Caller Access table with a status of Allowed.

</td></tr><tr><td>

accessibleFrom

</td><td>

String

</td><td>

Specifies which applications can access the script include.Valid values:

-   public: All application scopes can call the script include.
-   package\_private: The script include can only be called from the application scope that it's within.

Default: package\_private

</td></tr><tr><td>

active

</td><td>

Boolean

</td><td>

Flag that indicates whether the script include is enabled.Valid values:

-   true: The script include is callable.
-   false: The script include isn't callable.

Default: true

</td></tr><tr><td>

protectionPolicy

</td><td>

String

</td><td>

A policy that determines whether someone can view or edit the script include after the application is installed on their instance. If undefined, other application developers can customize the script include.Valid values:

-   read: Allows anyone to read values from this downloaded or installed script include. No one can change script values on the instance on which they download or install the script include.
-   protected: Provides intellectual property protection for application developers. Customers who download the script include cannot see the contents of the script field. The script is encrypted in memory to prevent unauthorized users from seeing it in plain text.

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
</table>In the following example, the script include uses a script from the `SampleClass.server.js` file.

```javascript
import { ScriptInclude } from '@servicenow/sdk/core';

ScriptInclude({
    $id: Now.ID['sample-script-include'],
    name: 'SampleScriptInclude',
    script: Now.include("./SampleClass.server.js"),
    description: 'some description',
    apiName: 'x_scope.SampleScriptInclude',
    callerAccess: 'tracking',
    clientCallable: true,
    mobileCallable: true,
    sandboxCallable: true,
    accessibleFrom: 'public',
    active: true,
})
```

