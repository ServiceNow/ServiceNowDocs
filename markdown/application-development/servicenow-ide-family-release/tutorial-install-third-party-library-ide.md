---
title: Tutorial part 4: Install and use a third-party library
description: Install a third-party library from Node Package Manager \(npm\) and use it in a JavaScript module.
locale: en-US
release: xanadu
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Getting started: Create your first application in the ServiceNow IDE, Explore, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Tutorial part 4: Install and use a third-party library

Install a third-party library from Node Package Manager \(npm\) and use it in a JavaScript module.

## Before you begin

Complete [Tutorial part 3: Define a table in ServiceNow Fluent code](tutorial-define-table-fluent-ide.md).

Role required: admin

## About this task

Installing third-party libraries allows you to use existing open-source functionality in JavaScript modules to accelerate application development. Then you can refer to JavaScript modules that call third-party code from server-side script definitions in your source code, such as the business rule in the `index.now.ts` file.

In this example, you install a Lodash library to get common JavaScript utilities and methods. You use one of these methods, snakeCase, in the showStateUpdate function in a sample JavaScript module to display a message string in snake case, which separates words with underscores instead of spaces. In the `index.now.ts` file, the sample business rule is configured to use the showStateUpdate function for its script and to run after a record is updated in the To-do Items \[x\_snc\_hello\_world\_to\_do\] table.

## Procedure

1.  Install the snakeCase method from the Lodash library in your application.

    1.  From the Activity Bar, select the File Explorer view \(![File Explorer](../image/servicenow-ide-file-explorer-icon.png)\).

    2.  Open the `package.json` file for the application.

    3.  After the `devDependencies` field, add the `dependencies` field with the package name and version of the library.

        ```json
        },
            "dependencies": {
                "lodash.snakecase": "4.1.1"
            }
        }
        ```

    4.  For applications that use TypeScript in JavaScript modules, add the lodash.snakecase types to the `devDependencies` field to get the type annotations for the library.

        ```json
        "devDependencies": {
                "@types/lodash.snakecase": "4.1.1",
                "typescript": "5.5.4",
                "@servicenow/sdk": "2.2.4",
                "@servicenow/glide": "26.0.1",
                "eslint": "8.50.0",
                "@servicenow/eslint-plugin-sdk-app-plugin": "2.2.4"
            }
        ```

    5.  Save your changes.

    6.  When prompted, select **Install missing dependencies**.

        **Tip:** You can also select the Install Dependencies icon \(![Install dependencies](../image/servicenow-ide-install-deps-icon.png)\) or use the `Package Manager: Install Dependencies` command from the command palette.

        ![Options to install dependencies in the ServiceNow IDE.](../image/servicenow-ide-install-deps.png)

        Libraries are installed as modules in the `node_modules` directory.

2.  Use code from the Lodash library in a JavaScript module in your application.

    1.  Navigate to the `src/server` directory in your application.

    2.  Open the `script.ts` sample module.

    3.  In the addInfoMessage method, wrap the message string in the snakeCase method from Lodash to convert it to snake case.

        ```javascript
        gs.addInfoMessage(snakeCase(`state updated from "${previousState}" to "${currentState}"`))
        ```

    4.  In line 2, add an import for the snakeCase method in the lodash module.

        ```javascript
        import snakeCase from 'lodash.snakecase'
        ```

        **Note:** The global Glide APIs are also imported so that you can use methods like addInfoMessage in your module code.

        ```javascript
        import { gs } from '@servicenow/glide'
        ```

    5.  Save your changes.

3.  From the Status Bar, select **Build and Install**.

    If the installation completes successfully, the Lodash libraries are added to the EcmaScript Module \[sys\_module\] table, and the `script.ts` module is updated in the EcmaScript Module \[sys\_module\] table.


## Result

After you update any field on a record in the To-do Items \[x\_snc\_hello\_world\_to\_do\] table, the sample business rule runs and displays the message in snake case, with the words separated by underscores instead of spaces.

![The message string from the showStateUpdate function in snake case](../image/servicenow-ide-snakecase.png)

## What to do next

Continue to [Tutorial part 5: Clone the application on a different instance](tutorial-clone-application-ide.md).

**Parent Topic:**[Getting started: Create your first application in the ServiceNow IDE](../concept/getting-started-create-application-ide.md)

