---
title: Tutorial part 3: Define a table in ServiceNow Fluent code
description: Create a table and reference it in sample script definitions using the ServiceNow Fluent APIs.
locale: en-US
release: yokohama
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Getting started: Create your first application in the ServiceNow IDE, Explore, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Tutorial part 3: Define a table in ServiceNow Fluent code

Create a table and reference it in sample script definitions using the ServiceNow Fluent APIs.

## Before you begin

Complete [Tutorial part 2: Initialize a repository for your application](tutorial-initialize-repository-ide.md).

Role required: admin

## About this task

ServiceNow Fluent is a domain-specific language \(DSL\) based on TypeScript for defining the metadata files \[sys\_metadata\] that make up applications and includes APIs for the different types of metadata, such as tables, roles, ACLs, business rules, and Automated Test Framework tests. You use objects in the ServiceNow Fluent APIs to define metadata in files with the `.now.ts` extension. The ServiceNow IDE has language processing and validation for ServiceNow Fluent APIs and applications by default. For more information about ServiceNow Fluent, see [ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md).

In this example, you create a simple table for a to-do list using objects in the ServiceNow Fluent Table API. Then, you update the sample code for business rule and client script definitions to reference the new table. Lastly, you review your changes from the Metadata Explorer. For more information about the Table API, see [Table API - ServiceNow Fluent](../../servicenow-sdk/reference/table-api-now-ts.md#).

## Procedure

1.  From the Activity Bar, select the File Explorer view \(![File Explorer](../image/servicenow-ide-file-explorer-icon.png)\).

2.  Navigate to the `src/fluent` directory in your application.

3.  Open the `index.now.ts` sample file.

    **Tip:** You can write ServiceNow Fluent code in a single file or as many `.now.ts` files as you want and organize files in directories within the `fluent` directory.

4.  On a new line at the end of the file, enter `Table({})` to add the Table object.

5.  From the Status Bar, select the diagnostics icon \(![Diagnostics](../image/servicenow-ide-diagnostics-icon.png)\) to open the Problems panel and check for issues in the code.

    ![Quick Fix menu with options for quick fixes](../image/servicenow-ide-open-panel.png)

6.  Right-click the error that appears and select the **Update import from "@servicenow/sdk/core"** quick fix.

    ![Quick fix to add the Table import from @servicenow/sdk/core in the Problems panel](../image/servicenow-ide-add-import.png)

    In line 2, the Table object is added to the list of imports from `@servicenow/sdk/core`:

    ```javascript
    import { BusinessRule, ClientScript, Table } from '@servicenow/sdk/core'
    ```

    **Tip:** After fixing this issue, you can close the Problems panel while you proceed through the following steps. In a later step, you return to it if any issues remain.

7.  In the Table object, add the following properties.

    -   name: The table name must begin with the application scope and use all lowercase letters in the following format: `<scope>_<name>`. You can find the scope in the `now.config.json` file for the application.
    -   label: The label should be unique and appears for the table in list and form views.
    -   extends: The name of another table on which the table is based.
    ```javascript
    Table({
        name: 'x_snc_hello_world_to_do', //ensure that the name begins with the correct scope (<scope>_<name>)
        label: 'To-do Items',
        extends: 'task',
    })
    ```

    **Tip:** Hover over an object to see its in-product documentation.

    ![Documentation for the Table API appears when hovering over the Table object.](../image/servicenow-ide-jsdocs.png)

8.  For type-ahead support when defining columns in the table, before the Table object, add an exported variable with the same name as the name property.

    ```javascript
    export const x_snc_hello_world_to_do = Table({
        name: 'x_snc_hello_world_to_do',
        label: 'To-do Items',
        extends: 'task',
    })
    ```

9.  In the Table object, add the schema property to define columns in the table.

    ```javascript
    export const x_snc_hello_world_to_do = Table({
        name: 'x_snc_hello_world_to_do',
        label: 'To-do Items',
        extends: 'task',
        schema: {
            //define columns here
        }
    })
    ```

    The schema property is an array of Column objects. There are many types of columns based on the field type. Column objects use the format &lt;Type&gt;Column where *&lt;Type&gt;* is the field type.

    Use the following details to define three columns in the table: Deadline, Matrix, and Task. Refer to the [Column object](../../servicenow-sdk/reference/table-api-now-ts.md#) documentation to help you configure each column.

<table id="table_b33_tq4_32c"><thead><tr><th>

Column name

</th><th>

Details

</th></tr></thead><tbody><tr><td>

deadline

</td><td>

-   Label: Deadline
-   Type: Date/Time


</td></tr><tr><td>

matrix

</td><td>

-   Label: Matrix
-   Type: String
-   Choices:
    -   Label: Urgent and Important
    -   Label: Important but Not Urgent
    -   Label: Urgent but Not Important
    -   Label: Neither Urgent nor Important


</td></tr><tr><td>

task

</td><td>

-   Label: Task
-   Type: String
-   Max length: 120


</td></tr></tbody>
</table>    With these details, the schema property should look similar to this example. The keys that you use for the choices can be any string.

    ```javascript
    export const x_snc_hello_world_to_do = Table({
        name: 'x_snc_hello_world_to_do',
        label: 'To-do Items',
        extends: 'task',
        schema: {
            deadline: DateColumn({ label: 'Deadline' }),
            matrix: StringColumn({
                label: 'Matrix',
                choices: {
                    do: { label: 'Urgent and Important' },
                    decide: { label: 'Important but Not Urgent' },
                    delegate: { label: 'Urgent but Not Important' },
                    delete: { label: 'Neither Urgent nor Important' },
                },
            }),
            task: StringColumn({ label: 'Task', maxLength: 120 }),
        },
    })
    ```

10. In line 2, add imports for the DateColumn and StringColumn objects.

    ```javascript
    import { BusinessRule, ClientScript, Table, DateColumn, StringColumn } from '@servicenow/sdk/core'
    ```

11. Update the existing business rule and client script definitions to reference the table you created.

    1.  In the ClientScript object, change the value of the table property to the table name \(`x_snc_hello_world_to_do`\).

    2.  Repeat the previous step for the BusinessRule object.

12. If the diagnostics icon \(![Diagnostics](../image/servicenow-ide-diagnostics-icon.png)\) shows any errors or warnings, select it to open the Problems panel and review the diagnostic messages and quick fixes to resolve them.

13. Save your changes using one of the following keyboard shortcuts.

    -   Windows: Ctrl-S
    -   Mac: Cmd-S
    **Note:** If you have unsaved changes in a file, a dot icon appears on the file tab.

14. From the Status Bar, select **Build and Install**.

    If the installation completes successfully, the updated ServiceNow Fluent source code is compiled into Application Files \[sys\_metadata\] on the instance.

15. Review your changes as metadata.

    1.  From the Activity Bar, select the Metadata Explorer view \(![Metadata Explorer](../image/servicenow-ide-metadata-explorer-icon.png)\).

    2.  Select your application to expand it.

    3.  Navigate to **Data** &gt; **Table** and select **To-do Items**.

        The table opens in Table Builder.

        ![The To-do Items table in Table Builder accessed from the Metadata Explorer in the ServiceNow IDE.](../image/servicenow-ide-table-builder.png)

16. Edit the metadata and synchronize your changes into the source code.

    From the Metadata Explorer, you can simulate another user editing the metadata outside of the source code to see changes transformed back into the code you added.

    1.  In Table Builder, search for the Task field and change the Column label from "Task" to "To Do".

    2.  Select **Save**.

    3.  From the Activity Bar, select the Now SDK view \(![Now SDK](../image/servicenow-ide-sdk-icon.png)\).

    4.  Select **Sync Changes**.

        ![The Sync command in the Now SDK view.](../image/servicenow-ide-sync.png)

        In the `index.now.ts` file, you should see the label property of the task column changed to `'To Do'`.

        ```javascript
        task: StringColumn({ label: 'To Do', maxLength: 120 }),
        ```


## Result

You have created your first application metadata using ServiceNow Fluent APIs. The To-do Items \[x\_snc\_hello\_world\_to\_do\] table can be modified in source code by other ServiceNow IDE users or from other ServiceNow AI Platform user interfaces.

From the ServiceNow AI Platform, you can navigate to the list view of the table by entering `x_snc_hello_world_to_do.list` in the navigation filter. Because you updated the client script definition to run on the To-do Items \[x\_snc\_hello\_world\_to\_do\] table, if you select **New** to add a record to the table, the message from the client script appears when the record loads.

![The message string from the client script definition appears when a new record is added to the To-do Items table](../image/servicenow-ide-client-script.png)

## What to do next

Continue to [Tutorial part 4: Install and use a third-party library](tutorial-install-third-party-library-ide.md).

**Parent Topic:**[Getting started: Create your first application in the ServiceNow IDE](../concept/getting-started-create-application-ide.md)

