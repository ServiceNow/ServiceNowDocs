---
title: Use third-party libraries in applications in the ServiceNow IDE
description: Call third-party libraries in your application to use existing open-source functionality with the ServiceNow IDE.
locale: en-US
release: zurich
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Develop applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Use third-party libraries in applications in the ServiceNow IDE

Call third-party libraries in your application to use existing open-source functionality with the ServiceNow IDE.

## Before you begin

Create a JavaScript module. For more information, see [Create and use JavaScript modules in applications in the ServiceNow IDE](create-use-javascript-modules-ide.md).

To install and use packages from private registries, you must configure your Package Manager user settings in the ServiceNow IDE. For more information, see [Install an npm package from a private registry with the ServiceNow IDE](use-library-private-npm-registry.md).

Role required: admin

## About this task

Third-party libraries are added to applications as JavaScript modules. For general information about the syntax used to create JavaScript modules, see the [JavaScript modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) page on the MDN Web Docs website.

**Important:** You can't use third-party libraries that rely on unsupported functionality, such as unsupported APIs or ECMAScript features. For more information about unsupported functionality, see [Third-party library support in Zurich](../../servicenow-sdk/reference/third-party-library-support.md) and [JavaScript modules and third-party libraries](../../servicenow-sdk/concept/javascript-modules-third-party-libraries.md).

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace with an application.

3.  From the Activity Bar, select the File Explorer view \(![File Explorer](../image/servicenow-ide-file-explorer-icon.png)\).

4.  Open the `package.json` file for the application.

5.  Add the `dependencies` field with the package name and version of any third-party libraries to use.

    ```json
    "dependencies": {
        "<package name>": "<version>"
      }
    ```

6.  Install the third-party library packages.

    1.  Use one of the following keyboard shortcuts to open the command palette:

        -   Windows: Ctrl-Shift-P
        -   Mac: Cmd-Shift-P
    2.  Enter `Package Manager: Install Dependencies` and press Enter.

    Packages are installed in the `node_modules` directory.

7.  In a JavaScript module, import the library using an import statement.

    In this example, the module includes a namespace import for the lodash module.

    ```javascript
    import * as lodash from "lodash"
    ```

    In this example, the module includes a named import for the camelCase function in the lodash module.

    ```javascript
    import camelCase from 'lodash'
    ```

8.  Call code imported from the library in your module to reuse it.

9.  From the Status Bar, select **Build and Install**.

    ![Build and Install](../image/servicenow-ide-build-icon.png)

    The active file that's open in the editor determines which application to build. If no files are open, select the application to build when prompted.

    After building, the modules are added to the EcmaScript Module \[sys\_module\] table.


-   **[Install an npm package from a private registry with the ServiceNow IDE](use-library-private-npm-registry.md)**  
Install Node Package Manager \(npm\) packages from a private registry as dependencies in your application to use them as third-party libraries.

**Parent Topic:**[Developing applications with the ServiceNow IDE](../concept/developing-applications-servicenow-ide.md)

**Related topics**  


[JavaScript modules and third-party libraries](../../servicenow-sdk/concept/javascript-modules-third-party-libraries.md)

