---
title: Use third-party libraries in applications with the ServiceNow SDK
description: Call third-party libraries in your application to use existing open-source functionality with the ServiceNow SDK.
locale: en-US
release: australia
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Develop applications, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Use third-party libraries in applications with the ServiceNow SDK

Call third-party libraries in your application to use existing open-source functionality with the ServiceNow SDK.

## Before you begin

Create a JavaScript module. For more information, see [Create and use JavaScript modules in applications with the ServiceNow SDK](create-use-javascript-modules.md).

Role required: admin

## About this task

Third-party libraries are added to applications as JavaScript modules. For general information about the syntax used to create JavaScript modules, see the [JavaScript modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) page on the MDN Web Docs website.

**Important:** You can't use third-party libraries that rely on unsupported functionality, such as unsupported APIs or ECMAScript features. For more information about unsupported functionality, see [Third-party library support in Australia](../reference/third-party-library-support.md) and [JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md).

## Procedure

1.  In Visual Studio Code, open your scoped application directory.

2.  From the application directory, open an integrated Terminal window.

3.  Install the npm package for the library.

    ```cmd
    npm install <package name>
    ```

    The library's packages are added to your application in the `node_modules` directory, and the library is added as a dependency in the `package.json` file for the application.

    ```json
    "dependencies": {
        "<package name>": "<version>"
      }
    ```

4.  In a JavaScript module, import the library using an import statement.

    In this example, the module includes a namespace import for the lodash module.

    ```javascript
    import * as lodash from "lodash"
    ```

    In this example, the module includes a named import for the camelCase function in the lodash module.

    ```javascript
    import camelCase from 'lodash'
    ```

5.  Call code imported from the library in your module to reuse it.


## What to do next

Build and install your changes on an instance. For more information, see [Build and install an application with the ServiceNow SDK](build-deploy-application-now-sdk.md).

**Parent Topic:**[Developing applications with the ServiceNow SDK](../concept/developing-applications-sdk.md)

**Related topics**  


[JavaScript modules and third-party libraries](../concept/javascript-modules-third-party-libraries.md)

