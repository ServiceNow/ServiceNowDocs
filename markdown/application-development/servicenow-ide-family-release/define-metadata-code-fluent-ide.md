---
title: Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE
description: Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Develop applications, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE

Define application metadata in code with ServiceNow Fluent in the ServiceNow IDE.

## Before you begin

Create, convert, or clone an application and add it to your workspace. For more information, see [Adding applications in ServiceNow IDE](../concept/creating-applications-servicenow-ide.md).

Role required: admin

## About this task

ServiceNow Fluent is a domain-specific language \(DSL\) based on TypeScript for defining the metadata files \[sys\_metadata\] that make up applications and includes APIs for the different types of metadata, such as tables, roles, ACLs, business rules, and Automated Test Framework tests. For more information about ServiceNow Fluent APIs and examples, see [ServiceNow Fluent API reference](../../servicenow-sdk/reference/servicenow-fluent-api-reference.md). The ServiceNow IDE has language processing and validation for ServiceNow Fluent APIs and applications by default.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow IDE**.

2.  Open a workspace with an application.

3.  From the Activity Bar, select the File Explorer view \(![File Explorer](../image/servicenow-ide-file-explorer-icon.png)\).

4.  In the `src/fluent` directory, add a file with the `.now.ts` extension.

    You can define application metadata in a single file or as many `.now.ts` files as you want and organize files in directories within the `fluent` directory.

    **Tip:** In the `fluent` directory, you can refer to an example file named `index.now.ts`.

5.  In the `.now.ts` file, use objects in the ServiceNow Fluent APIs to define metadata in the application.

    For example, to create a table \[sys\_db\_object\] in the application, use the Table API. The following example includes a simple table for to-do lists using a Table object with the necessary properties and values.

    ```javascript
    export const x_snc_example_to_do = Table({
        name: 'x_snc_example_to_do',
        schema: {
            deadline: DateColumn({ label: 'Deadline' }),
            state: StringColumn({
                label: 'State',
                choices: {
                    ready: { label: 'Ready' },
                    completed: { label: 'Completed' },
                    inProgress: { label: 'In Progress' },
                },
            }),
            task: StringColumn({ label: 'Task', maxLength: 120 }),
        },
    })
    ```

    **Note:** You can use the Record API to define application metadata that doesn't have a dedicated API.

6.  Add the required imports for the APIs from `@servicenow/sdk/core`.

    For example, to define a table with a date column and string column, import the corresponding objects to use from the Table API:

    ```javascript
    import { Table, DateColumn, StringColumn } from '@servicenow/sdk/core'
    ```

7.  For ServiceNow Fluent APIs that use server-side scripts, such as business rules, import code from JavaScript modules to call them from an object's script property.

    This example imports the `showStateUpdate` function, which can then be referenced from the script property.

    ```javascript
    import { showStateUpdate } from '../server/script.js'
    ```

8.  Save your changes.

9.  Build and install your application to compile source code into application metadata and make your changes available across the instance. For more information, see [Build and install an application in the ServiceNow IDE](build-applications-servicenow-ide.md).


**Tip:** You can use the following directives in a code comment to help manage your code:

-   `@fluent-ignore`: Suppresses ServiceNow Fluent diagnostic warnings and errors in the following line of code.
-   `@fluent-disable-sync`: Turns off syncing changes to a ServiceNow Fluent object. Use before a call expression \(for example, `Record({ ... })`\) to turn off syncing for that object and its child objects. Only use this directive if you want to ignore changes made outside of the source code to the object and never update it when syncing.
-   `@fluent-disable-sync-for-file`: Turns off syncing changes to a ServiceNow Fluent file \(`.now.ts`\). Use in the first line of the file to turn off syncing for all code in the file. Only use this directive if you want to ignore changes made outside of the source code to the file and never update it when syncing.

## Defining application metadata in source code with ServiceNow Fluent

In files with the `.now.ts` extension, use objects in the ServiceNow Fluent APIs to define metadata in the application. You must also include the required imports for the APIs from `@servicenow/sdk/core`. For objects with server-side scripts, such as the BusinessRule object, you can import and use code from JavaScript modules.

The following example includes the definitions of a table, client script, and business rule in the application. The client script uses a script from the `client-script.js` file.The business rule uses a function from the `script.js` JavaScript module.

```javascript
import '@servicenow/sdk/global'
import { BusinessRule, ClientScript, DateColumn, StringColumn, Table } from '@servicenow/sdk/core'
import { showStateUpdate } from '../server/script.js'

//creates todo table, with three columns (deadline, status and task)
export const x_snc_example_to_do = Table({
    name: 'x_snc_example_to_do',
    schema: {
        deadline: DateColumn({ label: 'Deadline' }),
        state: StringColumn({
            label: 'State',
            choices: {
                ready: { label: 'Ready' },
                completed: { label: 'Completed' },
                inProgress: { label: 'In Progress' },
            },
        }),
        task: StringColumn({ label: 'Task', maxLength: 120 }),
    },
})

//creates a client script that pops up 'Table loaded successfully!!' message everytime todo record is loaded
ClientScript({
    $id: Now.ID['cs0'],
    name: 'my_client_script',
    table: 'x_snc_example_to_do',
    active: true,
    appliesExtended: false,
    global: true,
    uiType: 'all',
    description: 'Custom client script generated by Now SDK',
    isolateScript: false,
    type: 'onLoad',
    script: Now.include\('../client/client-script.js'\),
})

//creates a business rule that pops up state change message whenever a todo record is updated
BusinessRule({
    $id: Now.ID['br0'],
    action: ['update'],
    table: 'x_snc_example_to_do',
    script: showStateUpdate,
    name: 'LogStateChange',
    order: 100,
    when: 'after',
    active: true,
})
```

After building the application, this source code generates the following application metadata files on the instance.

![Application files generated from the example code.](../../servicenow-sdk/image/servicenow-ide-app-files.png "Application metadata generated from ServiceNow Fluent code")

**Parent Topic:**[Developing applications with the ServiceNow IDE](../concept/developing-applications-servicenow-ide.md)

**Related topics**  


[ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md)

