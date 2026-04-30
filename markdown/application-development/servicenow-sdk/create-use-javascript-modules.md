---
title: Create and use JavaScript modules in applications with the ServiceNow SDK
description: Optimize your codebase by defining reusable code blocks with JavaScript modules and the ServiceNow SDK.
locale: en-US
release: xanadu
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Develop applications, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Create and use JavaScript modules in applications with the ServiceNow SDK

Optimize your codebase by defining reusable code blocks with JavaScript modules and the ServiceNow SDK.

## Before you begin

Add an application to your local system with the ServiceNow SDK. For more information, see [Adding applications with the ServiceNow SDK](../concept/creating-applications-servicenow-sdk.md).

Role required: admin

## About this task

To learn about support for using JavaScript modules in scoped applications, including some limitations, see [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md). For general information about the syntax used to create JavaScript modules, see the [JavaScript modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) page on the MDN Web Docs website.

## Procedure

1.  In Visual Studio Code, open your scoped application directory.

2.  In the `src/server` directory of the application, create a JavaScript or TypeScript file to contain the module code you want to reuse.

3.  Import server APIs or script includes to call them from your module.

    Glide APIs can be imported from the `@servicenow/glide` package or their namespace in the package. Script includes can be imported from their application scope or the global scope in the `@servicenow/glide` package.

    For example:

    ```javascript
    import { API } from "@servicenow/glide";
    import { API } from "@servicenow/glide/<namespace>";
    import { ScriptInclude } from "@servicenow/glide/<scope>";
    import { global } from "@servicenow/glide/global";
    ```

4.  In the module, identify the code to export with export statements.

    You can use a named export or default export. Named exports can be variables, constants, functions, or classes whereas default exports can be functions or classes only.

    The following example is one way of adding a named export for multiple features \(a function and a variable\) in a module:

    ```javascript
    export { myFunction, myVariable };
    
    ```

5.  Use code from the exported module in other modules or server-side scripts.

<table id="choicetable_kjx_xnm_pzb"><thead><tr><th align="left" id="d83971e162">

File

</th><th align="left" id="d83971e165">

Steps

</th></tr></thead><tbody><tr><td id="d83971e171">

**Module**

</td><td>

1.  From the `src/server` directory, create or open a JavaScript module.
2.  Import the module code with import statements.

The following example is one way that you could import an exported feature in a module:

    ```javascript
import { feature } from "path/to/module";

    ```

**Note:** To import code from one TypeScript file to another TypeScript file, you must include the `.ts` file extension. For example, `import { feature } from './module.ts'`.

3.  Call the module code from this module to reuse it.


</td></tr><tr><td id="d83971e210">

**Server-side script in source code**

</td><td>

1.  Create or open the definition of application metadata that includes a server-side script, such as a business rule, in source code \(`.now.ts` file\).
2.  In the script property, import and call the module code to reuse it.

You can import a function or provide an inline script.

    -   Import an exported function, function expression, or default function. For example:

        ```javascript
script: FunctionExport,
        ```

    -   Inline scripts must use require statements to import the module code. For example:

        ```javascript
script: `
    const { process } = require('./dist/modules/server/handler.js')
    process(request, response)`,
        ```

For more information about server-side scripts in source code, see [ServiceNow Fluent API reference](../reference/servicenow-fluent-api-reference.md).

</td></tr><tr><td id="d83971e270">

**Server-side script record**

</td><td>

1.  Open the record for a server-side script, such as a business rule.
2.  Import the module code with require statements.

The following example is one way that you could import an exported feature in a script:

    ```javascript
const { feature } = require("path/to/module");

    ```

3.  Call the module code from this script to reuse it.


</td></tr></tbody>
</table>6.  Save your changes.


## What to do next

To use third-party libraries in a JavaScript module, see [Use third-party libraries in applications with the ServiceNow SDK](use-third-party-libraries.md).

To build your application and add the modules to the EcmaScript Module \[sys\_module\] table, see [Build and install an application with the ServiceNow SDK](build-deploy-application-now-sdk.md).

-   **[Using TypeScript in JavaScript modules with the ServiceNow SDK](../concept/using-typescript.md#)**  
Use TypeScript when creating JavaScript modules with the ServiceNow SDK.

**Parent Topic:**[Developing applications with the ServiceNow SDK](../concept/developing-applications-sdk.md)

**Related topics**  


[JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md)

