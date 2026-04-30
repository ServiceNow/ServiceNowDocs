---
title: Create an application with the ServiceNow SDK
description: Create a scoped application to develop in source code with the ServiceNow SDK.
locale: en-US
release: zurich
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Add applications, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Create an application with the ServiceNow SDK

Create a scoped application to develop in source code with the ServiceNow SDK.

## Before you begin

Use the ServiceNow SDK to authenticate to a ServiceNow instance. For more information, see [Authenticating to a ServiceNow instance with the ServiceNow SDK](../concept/authenticate-instance-now-sdk.md).

Role required: admin

## About this task

This procedure uses the ServiceNow SDK command-line interface \(CLI\). From a command-line tool, enter `now-sdk --help` to get information about the available commands and global options. To get additional information about a command and its parameters, enter the command and `--help` or `-h`. For example, `now-sdk auth --help`. For more information about the CLI, see [ServiceNow SDK CLI](../reference/servicenow-sdk-cli-commands.md#).

## Procedure

1.  Create a local directory for your application.

2.  In Visual Studio Code, open the directory.

3.  From the application directory, open an integrated Terminal window.

4.  Create an application following a guided set of prompts with the `init` command:

    ```cmd
    npx @servicenow/sdk init
    ```

    **Note:** Using the `npx` command installs the ServiceNow SDK in your application directory instead of globally.

5.  Respond to the following series of prompts.

<table id="table_ivh_lzn_pdc"><thead><tr><th>

Prompt

</th><th>

Response

</th></tr></thead><tbody><tr><td>

`Select a template`

</td><td>

Select a template that determines the default application structure, such as whether to create a full-stack application that supports UI development ands whether to use JavaScript or TypeScript to create modules.

</td></tr><tr><td>

`Name of ServiceNow Application`

</td><td>

Enter a name for the application.

</td></tr><tr><td>

`NPM package name`

</td><td>

Enter a name for the application package used in the `package.json` file.The package name must adhere to Node Package Manager \(npm\) package naming standards.

</td></tr><tr><td>

`Create a Global/Scoped App?`

</td><td>

Select whether to create a scoped or global application.-   Scoped: Create a scoped application that is protected by identifying and restricting access to application files and data.
-   Global: Create an application in the global scope to allow it to be accessible to other global applications. Global applications are supported only with instances beginning with the Australia release.


</td></tr><tr><td>

`Scope name`

</td><td>

For scoped applications, enter the scope of the application.The scope name must be unique on the instance, begin with x\_&lt;prefix&gt;, and be 18 characters or fewer. For more information, see [Namespace identifier](../../applications/concept/c_NamespaceIdentifier.md).

</td></tr></tbody>
</table>    In the following example, a scoped application named Example App \(x\_snc\_example\_app\) is created.

    ```cmd
    $ npx @servicenow/sdk init
    [now-sdk] Bootstrapping a new ServiceNow application project...
    ? Select a template: now-sdk + basic
    ? Name of ServiceNow Application:  Example App
    ? NPM package name:  example-app
    ? Scope name:  x_snc_example_app
    [now-sdk] Application created successfully.
              Install the required dependencies with your preferred package manager before running "$now-sdk build".
              Ex: Run "npm install" if using npm.
    ```

6.  Install the required third-party dependencies using your preferred package manager.

    For example, if you use Node Package Manager \(npm\), run `npm install`.

7.  Build the application with the `build` command:

    ```cmd
    now-sdk build
    ```

8.  Install the application on an instance with the `install` command:

    ```cmd
    now-sdk install --auth <alias>
    ```


## Result

A scoped application with the default application structure is available locally. For information about the application structure, see the [Application structure](../../custom-application/concept/building-applications-source-code.md#application-structure) section of the Building applications in source code topic.

If you installed the application successfully, it’s available on the instance. For more information about installing applications, see [Build and install an application with the ServiceNow SDK](build-deploy-application-now-sdk.md).

## What to do next

In Visual Studio Code, start developing your application in source code with ServiceNow Fluent, writing custom JavaScript modules, or adding third-party libraries. For more information, see [Developing applications with the ServiceNow SDK](../concept/developing-applications-sdk.md).

