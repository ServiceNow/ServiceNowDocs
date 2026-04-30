---
title: Downloading dependencies with the ServiceNow SDK
description: Download application dependencies and TypeScript definitions from an instance for IntelliSense and validation of scripts and ServiceNow Fluent code.Download TypeScript definitions for dependencies in other application scopes to get IntelliSense support and validation for ServiceNow Fluent code.Download TypeScript definitions for module and script dependencies to get IntelliSense support and validation for Glide APIs and script includes.
locale: en-US
release: yokohama
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Develop applications, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Downloading dependencies with the ServiceNow SDK

Download application dependencies and TypeScript definitions from an instance for IntelliSense and validation of scripts and ServiceNow Fluent code.

Throughout the development process, you should download dependencies and TypeScript definitions from an instance to support coding against those dependencies in an application.

To download all script and ServiceNow Fluent dependencies for an application, you can use the `dependencies` command with no parameters. If needed, provide the application directory and authentication alias too.

```cmd
now-sdk dependencies [--directory <package path>] [--auth <alias>]
```

**Parent Topic:**[Developing applications with the ServiceNow SDK](developing-applications-sdk.md)

## Download ServiceNow Fluent application dependencies

Download TypeScript definitions for dependencies in other application scopes to get IntelliSense support and validation for ServiceNow Fluent code.

### Before you begin

Add an application to your local system with the ServiceNow SDK. For more information, see [Adding applications with the ServiceNow SDK](creating-applications-servicenow-sdk.md).

Role required: admin

### About this task

This procedure uses the ServiceNow SDK command-line interface \(CLI\). From a command-line tool, enter `now-sdk --help` to get information about the available commands and global options. To get additional information about a command and its parameters, enter the command and `--help` or `-h`. For example, `now-sdk auth --help`. For more information about the CLI, see [ServiceNow SDK CLI](../reference/servicenow-sdk-cli-commands.md#).

### Procedure

1.  In Visual Studio Code, open your scoped application directory.

2.  In the `now.config.json` file, add the items that your application depends on in the `dependencies` object.

    The `dependencies` object has the following structure. You must specify the application scope and the dependency type and names or sys\_ids. Only tables and roles can be specified by name. You can use a wildcard \(`*`\) to add all items from a specified table and scope.

    ```json
    "dependencies": {
        "<scope>": {
          "<type>": ["<sys_id or name>"],
          ...
        },
        ...
    }
    ```

    For example:

    ```json
    {
      "dependencies": {
        "global": {
          "tables": ["incident", "problem"],
          "roles": ["admin"],
          "sys_script_client": ["fa776f6d97700100f309124eda2975bc"]
        },
        "x_custom": {
          "tables": ["custom_table"],
          "sys_security_acl": "*",
        }
      }
    }
    ```

3.  Save your changes.

4.  From the application directory, open an integrated Terminal window.

5.  Download dependencies of the application with the `dependencies` command.

    ```cmd
    now-sdk dependencies --auth <alias> --fluent-only
    ```

    **Note:** If you want to download script dependencies too, exclude the `--fluent-only` parameter.

    The `dependencies` command downloads the dependencies specified in the `now.config.json` file and generates TypeScript definitions for them in the `@types/servicenow/fluent` directory with the `.d.now.ts` file extension. When building the application, these files aren't compiled like source code files.


### What to do next

You can reference dependencies in ServiceNow Fluent files using the `#now:{scope}/{category}` subpath import format. For example:

```json
// Import roles from global scope
import { role as globalRole } from '#now:global/security'

// Import roles from custom app scope  
import { role as xExampleAppRole } from '#now:x_example_app/security'

// Use in ACLs, flows, etc.
Acl({
    $id: Now.ID['my_acl'],
    type: 'record',
    table: 'incident',
    operation: 'read',
    roles: [globalRole.admin, xExampleAppRole.xExampleAppCool],
})
```

Your application's `package.json` file must include the following `imports` configuration to do so:

```json
{
  "imports": {
    "#now:*": "./@types/servicenow/fluent/*/index.js"
  }
}
```

## Download module andscript dependencies

Download TypeScript definitions for module andscript dependencies to get IntelliSense support and validation for Glide APIs and script includes.

### Before you begin

Add an application to your local system with the ServiceNow SDK. For more information, see [Adding applications with the ServiceNow SDK](creating-applications-servicenow-sdk.md).

Role required: admin

### About this task

This procedure uses the ServiceNow SDK command-line interface \(CLI\). From a command-line tool, enter `now-sdk --help` to get information about the available commands and global options. To get additional information about a command and its parameters, enter the command and `--help` or `-h`. For example, `now-sdk auth --help`. For more information about the CLI, see [ServiceNow SDK CLI](../reference/servicenow-sdk-cli-commands.md#).

### Procedure

1.  In Visual Studio Code, open your scoped application directory.

2.  From the application directory, open an integrated Terminal window.

3.  Download dependencies for scripts in the application with the `dependencies` command.

    ```cmd
    now-sdk dependencies --auth <alias> --type-defs-only
    ```

    **Note:** If you want to download application dependencies too, exclude the `--type-defs-only` parameter.

    The `dependencies` command downloads type definitions for all Glide APIs and scans the modules and scripts in your application and creates type definitions for the script includes that they use. Type definitions are added in the `@types/servicenow` directory. To add any other type definitions, you can create them manually. For more information, see [Add type definitions for APIs](using-typescript.md#).

4.  In the `src/fluent` directory, create a `tsconfig.server.json` file for server-side scripts.

    In the `include` object, include the type definitions that you downloaded for server-side Glide APIs \(`glide.server.d.ts`\) and script includes \(`script-includes.server.d.ts`\).

    ```json
    {
      "compilerOptions": {
        "lib": [
          "ES2021"
        ],
        "noEmit": true,
        "checkJs": false,
        "allowJs": true,
        "noEmitHelpers": true,
        "esModuleInterop": false,
        "module": "None",
        "types": []
      },
      "include": [
        "./**/*.server.js",
        "../../@types/servicenow/*.server.d.ts",
      ]
    }
    ```

5.  In the `src/fluent` directory, create a `tsconfig.client.json` file for client-side scripts.

    In the `include` object, include the type definitions that you downloaded for client-side Glide APIs \(`glide.client.d.ts`\).

    ```json
    {
      "compilerOptions": {
        "target": "ES6",
        "lib": [
          "DOM",
          "ES6"
        ],
        "checkJs": false,
        "allowJs": true,
        "noEmit": true,
        "noEmitHelpers": true,
        "esModuleInterop": false,
        "module": "None",
        "types": []
      },
      "include": [
        "./**/*.client.js",
        "../../@types/servicenow/*.client.d.ts",
      ]
    }
    ```

6.  In the `src/fluent` directory, create a `tsconfig.json` file.

    **Note:** This `tsconfig.json` file is separate from a `tsconfig.json` file used for applications that use TypeScript to create JavaScript modules.

    In the `references` object, add the paths to the `tsconfig.server.json` and `tsconfig.client.json` files.

    ```json
    {
      "files": [],
      "references": [
        {
          "path": "./tsconfig.server.json"
        },
        {
          "path": "./tsconfig.client.json"
        }
      ]
    }
    ```

7.  Save your changes.


### Result

With this configuration, you can use the `.server.js` file extension for server-side scripts and `.client.js` file extension for client-side scripts and get type-ahead support during development.

