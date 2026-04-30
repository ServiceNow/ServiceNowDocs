---
title: Using TypeScript in JavaScript modules with the ServiceNow SDK
description: Use TypeScript when creating JavaScript modules with the ServiceNow SDK.Use TypeScript in JavaScript modules by adding support for TypeScript in your application.Get type-ahead support for APIs and scriptable objects outside of Glide APIs.
locale: en-US
release: xanadu
product: ServiceNow SDK
classification: servicenow-sdk
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Create and use JavaScript modules, Develop applications, ServiceNow SDK, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Using TypeScript in JavaScript modules with the ServiceNow SDK

Use TypeScript when creating JavaScript modules with the ServiceNow SDK.

TypeScript uses static typing and type annotations to support developers catching errors earlier while writing code in Visual Studio Code.

For general information about using TypeScript, see the [TypeScript Documentation](https://www.typescriptlang.org/docs/) on the typescriptlang.org website.

**Parent Topic:**[Create and use JavaScript modules in applications with the ServiceNow SDK](../task/create-use-javascript-modules.md)

## Use TypeScript in JavaScript modules

Use TypeScript in JavaScript modules by adding support for TypeScript in your application.

### Before you begin

Install TypeScript version 4.8.4 or later. For installation instructions, see [Download TypeScript](https://www.typescriptlang.org/download) on the typescriptlang.org website.

Role required: admin

### About this task

Follow this procedure to update existing applications that weren't created using a TypeScript template to use TypeScript in modules. Beginning with the ServiceNow SDK version 3.0, applications support using TypeScript in JavaScript modules by default using default compiler options. To use a `tsconfig.json` file with custom options for transpiling TypeScript into JavaScript during the build process, configure the `tsconfigPath` parameter in the `now.config.json` file. If you want to use a custom transpilation step before building the application, configure the `modulePaths` parameter in the `now.config.json` file.

### Procedure

1.  In Visual Studio Code, open your scoped application directory.

2.  Open the application's `package.json` file and in the `devDependencies` object, add the TypeScript package and version.

    ```json
    "devDependencies": {
        "typescript": "<version>",
        "@servicenow/sdk": "2.0.0",
        "@servicenow/glide": "26.0.1",
        "eslint": "8.50.0",
        "@servicenow/eslint-plugin-sdk-app-plugin": "2.0.0"
      }
    ```

3.  In your application's `src/server` directory, add a `tsconfig.json` file that defines the options for compiling the application.

    ```json
    {
        "compilerOptions": {
            "rootDir": "./",
            "outDir": "../../dist/server",
            "module": "es2022",
            "target": "es2022",
            "moduleResolution": "bundler",
            "allowJs": true,
            "declaration": false,
            "sourceMap": false,
            "skipLibCheck": true,
            "allowImportingTsExtensions": true,
            "noEmit": true
        },
        "include": [
            "./**/*.ts",
            "../../@types/\*\*/\*.modules.d.ts"
        ],
        "exclude": [
            "**/*.now.ts"
        ]
    }
    ```

4.  In the application's `now.config.json` file, set the `tsconfigPath` parameter to the location of the `tsconfig.json` for JavaScript modules..

    ```json
    {
      "scope": "x_snc_example_app",
      "scopeId": "2f8400eb07426110f736e28f69d3017a",   
      "name": "ExampleApp",
      "tsconfigPath": "./src/server/tsconfig.json"
      
    }
    ```

5.  In the `src/server` directory, add at least one `.ts` file to contain module code.

    For information about creating modules, see [Create and use JavaScript modules in applications with the ServiceNow SDK](../task/create-use-javascript-modules.md).


### What to do next

Build and install the application to compile the TypeScript files into JavaScript modules and add the modules to the EcmaScript Module \[sys\_module\] table. For more information, see [Build and install an application with the ServiceNow SDK](../task/build-deploy-application-now-sdk.md).

## Add type definitions for APIs

Get type-ahead support for APIs and scriptable objects outside of Glide APIs.

### Before you begin

Role required: admin

### About this task

**Note:** You can download type definitions for most APIs, script includes, and other scriptable objects using the `now-sdk dependencies` command. For more information, see [Download module and script dependencies](downloading-dependencies-now-sdk.md#).

Follow this procedure to manually add types definitions that the `now-sdk dependencies` doesn't download. You can declare modules directly in the ServiceNow SDK application to stub access to the APIs for type-ahead support. These modules aren't packaged in the application package, but they can be tracked in a source control repository for the application and shared between developers.

### Procedure

1.  In Visual Studio Code, open your scoped application directory.

2.  In your application, add a TypeScripe \(`.ts`\) file for type definitions.

3.  In your TypeScript file, declare modules for APIs and scriptable objects.

    This example declares a module for an API using the API namespace \(`sn_app_api`\):

    ```javascript
    declare module '@servicenow/glide/sn_app_api' {
    	class AppStoreAPI {
    		static canUpgradeAnyStoreApp(): boolean
    	}
    } 
    ```

    This example declares a module to access objects defined in script includes using the scope of the script include \(`x_1234_scope`\):

    ```javascript
    declare module '@servicenow/glide/x_1234_scope' {
    	class MyLogItemClass {
    		myLogFunction()
    	}
    }
    ```

4.  In JavaScript modules in your application, import the declared modules.

    This example imports the declared module for the AppStoreAPI.

    ```javascript
    import { gs } from '@servicenow/glide'
    import { AppStoreAPI } from '@servicenow/glide/sn_app_api'
    
    export const canUpgradeStoreApp = function () {
    	var canUpgrade = AppStoreAPI.canUpgradeAnyStoreApp()
    	if (canUpgrade) {
    		gs.addInfoMessage(`You can upgrade store apps!`)
    	} else {
    		gs.addInfoMessage(`You cannot upgrade store apps!`)
    	}
    }
    ```

    This example imports the declared module for the MyLogItemClass object.

    ```javascript
    import { MyLogItemClass } from '@servicenow/glide/x_1234_scope'
    
    export const myLogFunction = function (status) {
    	const myLogItem = new MyLogItemClass()
    	myLogItem.myLogFunction(status)
    }
    ```

    **Note:** Modules can access only global scriptable objects or scriptable objects in the same application scope.


