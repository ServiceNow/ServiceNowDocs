---
title: Building applications in source code
description: Create and develop custom applications in source code using familiar development tools and processes.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Building pro-code applications, Developing your application, Building applications]
---

# Building applications in source code

Create and develop custom applications in source code using familiar development tools and processes.

## Overview of development in source code

You can create scoped applications in code using the ServiceNow IDE on the ServiceNow AI Platform or locally in Visual Studio Code Desktop with the ServiceNow SDK.

In either development environment, you use ServiceNow Fluent, a domain-specific programming language, to define the metadata that makes up applications. ServiceNow Fluent includes APIs for defining the different types of metadata.

With the ServiceNow IDE or ServiceNow SDK, you can also create JavaScript modules and use third-party libraries in your application to optimize code reuse in scripts within a scoped application.

Developing and maintaining applications in source code enables you to work in familiar development environments, create and modify complex applications, manage code in source control more easily, and catch errors at build time.

**Note:** The ServiceNow IDE and ServiceNow SDK don't support the Global scope or global applications in the Xanadu release.

<table id="table_hmf_wtt_3bc" class="nav-card"><tbody><tr><td>

[ServiceNow IDE![](../../servicenow-ide/image/servicenow-ide-logo.png)Develop applications in code in an IDE on the ServiceNow AI Platform.](../../servicenow-ide/concept/servicenow-ide-landing.md)

</td><td>

[ServiceNow SDK![](../../servicenow-sdk/image/servicenow-sdk-logo.png)Develop applications in code locally and upload changes to an instance.](../../servicenow-sdk/concept/servicenow-sdk-landing.md)

</td></tr></tbody>
</table>## Comparison of the ServiceNow IDE and the ServiceNow SDK

<table id="table_tqv_dfc_jbc"><thead><tr><th>

Feature

</th><th>

ServiceNow IDE

</th><th>

ServiceNow SDK

</th></tr></thead><tbody><tr><td>

Development environment

</td><td>

Online ServiceNow instance

</td><td>

Local development and the ability to work offline

</td></tr><tr><td>

User interface

</td><td>

IDE based on Visual Studio Code for the Web

</td><td>

Visual Studio Code Desktop

</td></tr><tr><td>

Collaboration

</td><td>

View any user's changes in real time in code or embedded ServiceNow AI Platform user interfaces from the Metadata Explorer.Collaborate with other developers on applications in source control.

</td><td>

Download changes from an instance and install local changes to an instance using the ServiceNow SDK CLI to collaborate with other users. Collaborate with other developers on applications in source control.

</td></tr><tr><td>

Source control

</td><td>

Supports the most common Git functionality and integrating with a Git provider of your choice.One concurrent branch per repository per instance\(or developer sandbox\).

</td><td>

Full support

</td></tr><tr><td>

Application conversion

</td><td>

Support for converting existing scoped applications not created with the ServiceNow IDE or ServiceNow SDK.

</td><td>

Support for converting existing scoped applications not created with the ServiceNow IDE or ServiceNow SDK.

</td></tr><tr><td>

ServiceNow Fluent

</td><td>

Full supportThe ServiceNow Fluent Language server is included with the ServiceNow IDE.

</td><td>

Full supportThe ServiceNow Fluent Language server can be installed from the Visual Studio Code Extension Marketplace.

</td></tr><tr><td>

JavaScript modules and third-party libraries

</td><td>

Full support

</td><td>

Full support

</td></tr><tr><td>

Now Assist for Code

</td><td>

Code auto-complete support for scripts.For information about activation, see [Now Assist for code generation](https://www.servicenow.com/docs/access?context=now-assist-code-landing&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td><td>

Not supported

</td></tr></tbody>
</table>## Application structure

Custom scoped applications created with the ServiceNow IDE or ServiceNow SDK include source code files and metadata XML files. The `package.json` and `now.config.json` files define the application structure, which is similar to that of Node.js applications or Node Package Manager \(npm\) packages.

![Structure of an application created in the ServiceNow IDE](../../servicenow-ide/image/servicenow-ide-app-structure.png "Default structure of an application created in the ServiceNow IDE")

By default, applications include the following directories and files. You can modify certain aspects of the application structure to suit your needs in the `now.config.json` file.

-   **.vscode**

    Directory containing recommended Visual Studio Code extensions.

-   **dist**

    Directory containing the build artifacts for packaging. This directory includes the following subdirectories:

    -   `app`: Directory containing the built metadata XML files.
    -   `static`: Directory containing the built static asset files.
-   **metadata**

    Directory containing the application metadata \(XML\) of the application, such as table schemas and business rules, organized in the same directory structure as existing ServiceNow applications.

    **Note:** Application metadata shouldn't be edited from the XML files. Edit application metadata in the source code or on the ServiceNow AI Platform.

-   **node\_modules**

    Directory containing the third-party Node.js modules on which your application depends.

-   **src**

    Directory containing the source code of your application. This directory includes the following subdirectories:

    -   `client`: Directory containing the client-side files for developing user interfaces.
    -   `fluent`: Directory containing ServiceNow Fluent code in `.now.ts` files. The `generated` subdirectory contains the application files converted to ServiceNow Fluent.
    -   `server`: Directory containing JavaScript module code in `.js` or `.ts` files.
-   **target**

    Directory containing an installable package \(`.zip` file\) to upload to an instance.

-   **.eslintrc.json**

    File containing the ESLint configuration. ESLint helps identify and fix issues in the application code.

-   **.gitignore**

    File containing a list of directories or files for Git to ignore. These files aren't tracked in source control.

-   **now.config.json**

    File containing the ServiceNow application configuration. The `now.config.json` file must be in the base directory for an application.

    You can configure the directory structure for an application by adding the following parameters. For example:

    ```json
    {
      "scope": "x_snc_example_app",
      "scopeId": "2f8400eb07426110f736e28f69d3017a",
      "name": "ExampleApp",
      "dependencies": \{
        "global": \{
          "tables": \["incident"\],
          "roles": \["admin"\],
        \},
        "x\_custom": \{
          "tables": \["custom\_table"\]
        \}
      \},
      "metadataDir": "metadata",
      "fluentDir": "src/fluent",
      "generatedDir": "generated",
      "serverModulesDir": "src/server",
      "clientDir": "src/client",
      "appOutputDir": "dist/app",
      "staticContentDir": "dist/static",
      "packOutputDir": "target",
      "modulePaths": {
          "src/server/*.ts": "dist/server/*.js",
        },
      "staticContentPaths": {
          "src/client/*.html": "dist/static/*.html",
        },
      "ignoreTransformTableList": ["ua_table_licensing_config", "sys_embedded_help_role"],
      "taxonomy": \{
            "mapping": \{
                "sys\_script": "scripts/server/rules",
                "custom\_table": "my-custom-folder/my-nested-folder"
            \},
            "fallbackFolderName": "unclassified" 
        \}
    }
    ```

<table id="table_upn_kqw_zbc"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dependencies

</td><td>

The items in another application scope on which your application depends. You must specify the application scope and the dependency type and names or sys\_ids.```json
"dependencies": {
    "<scope>": {
      "<type>": ["<sys_id or name>"],
      ...
    },
    ...
}
```

For more information, see [Download ServiceNow Fluent application dependencies](../../servicenow-sdk/concept/downloading-dependencies-now-sdk.md#).

</td></tr><tr><td>

metadataDir

</td><td>

Directory containing the application's metadata as XML files.Default: `metadata`

</td></tr><tr><td>

fluentDir

</td><td>

Directory containing ServiceNow Fluent files \(`.now.ts`\) that define application metadata in source code.Default: `src/fluent`

</td></tr><tr><td>

generatedDir

</td><td>

Directory containing generated ServiceNow Fluent files, including existing application metadata converted into ServiceNow Fluent code. This directory is relative to the directory defined with the **fluentDir** parameter.Default: `generated`

</td></tr><tr><td>

serverModulesDir

</td><td>

Directory containing the JavaScript or TypeScript files to be built into JavaScript modules for use in server-side scripts.Default: `src/server`

</td></tr><tr><td>

clientDir

</td><td>

Directory containing the client-side files for developing user interfaces with React.Default: `src/client`

</td></tr><tr><td>

appOutputDir

</td><td>

Directory to output the build artifacts to for packaging. The pack and install commands refer to this directory package the artifacts.

 Default: `dist/app`

</td></tr><tr><td>

staticContentDir

</td><td>

Directory to output the static asset files used for developing user interfaces.Default: `dist/static`

</td></tr><tr><td>

packOutputDir

</td><td>

Directory to output the installable package \(`.zip` file\) when building the application. The install command refers to this directory to install the package.Default: `target`

</td></tr><tr><td>

serverModulesIncludePatterns

</td><td>

A list of file patterns to include when building JavaScript modules.Default:

```json
[
  "**/*.ts",
  "**/*.tsx",  
  "**/*.js",
  "**/*.jsx",
  "**/*.cts",
  "**/*.cjs",
  "**/*.mts",
  "**/*.mjs",
  "**/*.json"
]
```

</td></tr><tr><td>

serverModulesExcludePatterns

</td><td>

A list of file patterns to exclude when building JavaScript modules.Default:

```json
[
  "**/*.test.ts",
  "**/*.test.js",
  "**/*.d.ts"
]
```

</td></tr><tr><td>

trustedModules

</td><td>

A list of npm packages to identify as trusted \(or internal\). Trusted modules have access to ServiceNow APIs. For example:```json
"trustedModules": [
  "<package-name>",  // Specific package
  "@servicenow/*"  // All packages from an organization
]
```

In the EcmaScript Module \[sys\_module\] table, the **External source** field is set to false for trusted modules.

**Warning:** Only add dependencies that you trust completely as trusted modules.

Valid patterns:

-   Fully qualified package names, such as `'@servicenow/sdk'`.
-   Organization prefixes with a wildcard, such as `'@servicenow/*'` or `'@mycompany/*'`.


</td></tr><tr><td>

modulePaths

</td><td>

A map of the module source files to their equivalent output files for if you use a custom transpilation step before building the application. For more information, see [Using TypeScript in JavaScript modules with the ServiceNow SDK](../../servicenow-sdk/concept/using-typescript.md#).**Warning:** You can't use this parameter and the `tsconfigPath` parameter. Configuring both results in an error.

</td></tr><tr><td>

staticContentPaths

</td><td>

A map of the client-side source files to the output paths for static asset files.

</td></tr><tr><td>

tsconfigPath

</td><td>

A path to a `tsconfig.json` file with custom options for transpiling TypeScript into JavaScript during the build process. Specifying a `tsconfigPath` generates diagnostic results from TypeScript using the `tsconfig.json` file.**Warning:** You can't use this parameter and the `modulePaths` parameter. Configuring both results in an error.

Default: `.`

</td></tr><tr><td>

ignoreTransformTableList

</td><td>

A list of tables to ignore when transforming application metadata into source code.

</td></tr><tr><td>

tableDefaultLanguage

</td><td>

The BCP 47 code of a default language for field labels \[sys\_documentation\] in a table or column. Th default language is used to resolve field labels with multiple languages.Default: en

</td></tr><tr><td>

tableOutputFormat

</td><td>

The type of build artifacts for table metadata XML generated from ServiceNow Fluent code.Valid values:

-   bootstrap: The build process outputs a bootstrap XML file with the `<database>` root element for the table, field label XML files \[sys\_documentation\], licensing configuration XML files \[ua\_table\_licensing\_config\], and auto-numbering XML files \[sys\_number\].
-   component: The build process outputs XML files for each component of the Table API.
Default: `bootstrap`

</td></tr><tr><td>

taxonomy

</td><td>

A configuration for organizing generated ServiceNow Fluent files, which maps table names to directories and defines a fallback directory. The default taxonomy configuration uses ServiceNow standard table classifications to add generated ServiceNow Fluent files in a logical directory structure within the `fluent/generated` directory when metadata is initially transformed into ServiceNow Fluent code. For example:-   Business rules \[sys\_script\] are added to the `fluent/generated/server-development/business-rule` directory.
-   Script includes \[sys\_script\_include\] are added to the `fluent/generated/server-development/script-include` directory.
You can override the default mappings or configure additional ones. In the following example, the configuration overrides the default directory for business rules \[sys\_script\] and the fallback folder and configures an additional mapping for metadata from a custom table.

```json
"taxonomy": {
        "mapping": {
            "sys_script": "scripts/server/rules",
            "custom_table": "my-custom-folder/my-nested-folder"
        },
        "fallbackFolderName": "unclassified"
}
```

-   mapping: An object that maps table names to directories. Directory paths are relative to the directory configured with the **generatedDir** parameter and must include only lowercase letters, numbers, hyphens, underscores, and slashes to separate subdirectories.
-   fallbackFolderName: A name for a directory to use for tables that don't have a default or a custom mapping configured. Within this directory, ServiceNow Fluent files are added to subdirectories named after the table, such as `src/fluent/generated/other/x-unmapped-table/`.
Default: Default taxonomy mappings are defined for all standard ServiceNow tables and are automatically applied when no custom configuration is defined in the `now.config.json` for an application. The default value of **fallbackFolderName** is `other`.

</td></tr></tbody>
</table>-   **now.prebuild.mjs**

    Auto-updated file containing complete information about dependencies and their versions. This file is only available with the ServiceNow SDK.

-   **package-lock.json**

    Auto-updated file containing complete information about dependencies and their versions. This file is only available with the ServiceNow SDK.

-   **package.json**

    File containing information about your application and custom or third-party module dependencies. The `package.json` file must be in the base directory for an application. On an instance, the `package.json` path is specified in the **Package JSON** field of the custom application record \[sys\_app\] in the format `<scope>/<package-name>/<version>/package.json`.


## Related applications and features

-   **[JavaScript APIs](https://www.servicenow.com/docs/access?context=api-reference&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)**

    Use JavaScript APIs in scripts that you write to change the functionality of applications or when you create applications.


**Related topics**  


[ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md)

[JavaScript modules and third-party libraries](../../servicenow-sdk/concept/javascript-modules-third-party-libraries.md)

[User interface development with React](../../servicenow-sdk/concept/ui-development-react.md)

