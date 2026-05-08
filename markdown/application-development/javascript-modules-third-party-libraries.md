---
title: JavaScript modules and third-party libraries
description: Optimize your code base using JavaScript modules to group related code or add third-party libraries and reuse their code within applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# JavaScript modules and third-party libraries

Optimize your code base using JavaScript modules to group related code or add third-party libraries and reuse their code within applications.

## Overview of using JavaScript modules

A module is a JavaScript file that contains related code that's shared and reused within applications on an instance. You can add JavaScript modules and third-party libraries in applications that are created or convertedwith the ServiceNow IDE or ServiceNow SDK. You can also use TypeScript to create modules and compile them to JavaScript before building your application. After installing an application on an instance, JavaScript modules are stored in the EcmaScript Module \[sys\_module\] table.

In a module, you identify code for reuse with export statements. Then, use import or require statements to reuse the code elsewhere in your applications. You must add third-party Node Package Manager \(npm\) libraries to applications as dependencies to use their module code. For general information about the syntax used to create JavaScript modules, see the [JavaScript modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules) page on the MDN Web Docs website.

**Note:** To use global Glide Server APIs in modules, they must be imported from the `@servicenow/glide` package. For more information, see [Importing server APIs](javascript-modules-third-party-libraries.md#section_pn3_lsk_cfc).

## Limitations

-   Application customizations aren't supported.
-   Modules can be used only within the application scope in which they're added. They can't be used across application scopes.
-   A subset of ECMAScript features are supported in modules in accordance with the JavaScript engine feature support.
-   Node.js APIs aren’t supported in modules. The ServiceNow SDK build process polyfills any Node.js built-in modules while packaging modules, otherwise modules are resolved from the `node_modules` directory.
-   Global variables related to web APIs aren’t supported.
-   CommonJS modules from third-party libraries aren't supported unless they define exports. Subpath imports aren't supported with CommonJS modules. ECMAScript modules from third-party libraries are supported.
-   import and export statements are only supported in modules. To import module code in scripts, such as business rules or script includes, use require statements.​
-   JavaScript modules \[sys\_module\] can be modified only in the ServiceNow IDE or in Visual Studio Code with the ServiceNow SDK.

**Important:** You can't use third-party libraries that rely on unsupported functionality, such as unsupported APIs or ECMAScript features. For more information, see [Third-party library support in Australia](../reference/third-party-library-support.md).

## Exporting modules

In a module, identify code for reuse with export statements. You can use named exports or default exports. Named exports can be for variables, constants, functions, or classes whereas default exports can be for functions or classes only. The following example is one way of adding a named export for multiple features \(a function and a variable\) in a module:

```javascript
export { myFunction, myVariable };
```

## Importing modules

To import the module code you want to reuse, use import statements in other modules or require statements in server-side scripts.

The following example is one way that you could import an exported feature in a module:

```javascript
import { feature } from 'path/to/module';
```

The following example is one way that you could import an exported feature in a script:

```javascript
const { feature } = require('path/to/module');
```

**Note:** To import code from one TypeScript file to another TypeScript file, you must include the `.ts` file extension. For example, `import { feature } from './module.ts'`.

To use shorthand to import module code, you can use subpaths in the imports field of the application's `package.json` file. For example:

```json
{
	"name": "math",
	"version": "1.0.0",
	"exports": {
		"./functions/*.js": "./src/functions/*.js",
		"./functions/private-functions/*": null
	},
	"imports": {
		"#calc": "calculus",
		"#derivative": "calculus/derivative"
	},
	"dependencies": {
		"calculus": "1.0.0"
	}
}
```

Based on that example, instead of writing out the relative path to `derivative.js` every time you want to import it in the `math` application, you can use the `#derivative` shorthand instead. Subpaths can also be used in the imports field to use shorthand for dependencies, such as `#calc`.

```javascript
import { derivative } from '#derivative';
import * as calculus from '#calc';
```

## Adding third-party libraries

Applications must declare dependencies on third-party libraries to use their module code. In an application's `package.json` file, include the package name and version for any dependencies. For example, to use modules from the "math" library in the "test" application, add the "math" package as a dependency:

```json
{
	"name": "test",
	"version": "1.0.0",
	"dependencies": {
		"math": "1.0.0"
	}
}
```

## Importing server APIs

To import server APIs and use them in a module, use import statements. Glide APIs can be imported from the `@servicenow/glide` package or their namespace in the package.

For example:

```javascript
import { API } from '@servicenow/glide';
import { API } from '@servicenow/glide/<namespace>';
```

In the following example, the gs \(GlideSystem\) and GlideRecord APIs are imported in a module:

```javascript
import { gs } from '@servicenow/glide';
import { GlideRecord } from '@servicenow/glide';
```

In the following example, the RESTAPIRequest and RESTAPIResponse APIs are imported from the `sn_ws_int` namespace in a module because they run in that namespace:

```javascript
import { RESTAPIRequest, RESTAPIResponse } from '@servicenow/glide/sn_ws_int';
```

To access server APIs in a third-party library module, you must add the module as a trusted module with the trustedModules parameter in your application's `now.config.json` file. For more information, see [Custom application configuration in source code](../reference/app-config-source-code.md).

For more information about available server APIs, see Server API reference.

## Importing script includes

To import script includes and use them in a module, use import statements. Script includes can be imported from their application scope or the global scope in the `@servicenow/glide` package.

For example:

```javascript
import { global } from '@servicenow/glide/global';
import { ScriptInclude } from '@servicenow/glide/<scope>';
```

For more information about script includes, see Script includes.

**Related topics**  


[Create and use JavaScript modules in applications in the ServiceNow IDE](../../servicenow-ide/task/create-use-javascript-modules-ide.md)

[Create and use JavaScript modules in applications with the ServiceNow SDK](../task/create-use-javascript-modules.md)

