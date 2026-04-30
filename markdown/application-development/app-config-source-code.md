---
title: Custom application configuration in source code
description: Configure a custom application \[sys\_app\] in the now.config.json file for an application in source code.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-20"
reading_time_minutes: 7
breadcrumb: [Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Custom application configuration in source code

Configure a custom application \[sys\_app\] in the `now.config.json` file for an application in source code.

You can configure the application settings and aspects specific to developing the application in source code, such as the directory structure. In the `now.config.json` file, add the following parameters to configure the application settings.

<table id="table_upn_kqw_zbc"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appOutputDir

</td><td>

String

</td><td>

Directory to output the build artifacts to for packaging. The pack and install commands refer to this directory to package the artifacts. Default: `dist/app`

</td></tr><tr><td>

clientDir

</td><td>

String

</td><td>

Directory containing the client-side files for developing user interfaces with React.Default: `src/client`

</td></tr><tr><td>

dependencies

</td><td>

Object

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

For more information, see [Download ServiceNow Fluent application dependencies](../concept/downloading-dependencies-now-sdk.md#).

</td></tr><tr><td>

fluentDir

</td><td>

String

</td><td>

Directory containing ServiceNow Fluent files \(`.now.ts`\) that define application metadata in source code.Default: `src/fluent`

</td></tr><tr><td>

generatedDir

</td><td>

String

</td><td>

Directory containing generated ServiceNow Fluent files, including existing application metadata converted into ServiceNow Fluent code. This directory is relative to the directory defined with the **fluentDir** parameter.Default: `generated`

</td></tr><tr><td>

ignoreTransformTableList

</td><td>

Array

</td><td>

A list of tables to ignore when transforming application metadata into source code.

</td></tr><tr><td>

metadataDir

</td><td>

String

</td><td>

Directory containing the application's metadata as XML files.Default: `metadata`

</td></tr><tr><td>

modulePaths

</td><td>

Object

</td><td>

A map of the module source files to their equivalent output files for if you use a custom transpilation step before building the application. For more information, see [Using TypeScript in JavaScript modules with the ServiceNow SDK](../concept/using-typescript.md#).**Warning:** You can't use this parameter and the `tsconfigPath` parameter. Configuring both results in an error.

</td></tr><tr><td>

packOutputDir

</td><td>

String

</td><td>

Directory to output the installable package \(`.zip` file\) when building the application. The install command refers to this directory to install the package.Default: `target`

</td></tr><tr><td>

serverModulesDir

</td><td>

String

</td><td>

Directory containing the JavaScript or TypeScript files to be built into JavaScript modules for use in server-side scripts.Default: `src/server`

</td></tr><tr><td>

serverModulesExcludePatterns

</td><td>

Array

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

serverModulesIncludePatterns

</td><td>

Array

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

staticContentDir

</td><td>

String

</td><td>

Directory to output the static asset files used for developing user interfaces.Default: `dist/static`

</td></tr><tr><td>

staticContentPaths

</td><td>

Object

</td><td>

A map of the client-side source files to the output paths for static asset files.

</td></tr><tr><td>

tableDefaultLanguage

</td><td>

String

</td><td>

The BCP 47 code of a default language for field labels \[sys\_documentation\] in a table or column. The default language is used to resolve field labels with multiple languages.Default: en

</td></tr><tr><td>

tableOutputFormat

</td><td>

String

</td><td>

The type of build artifacts for table metadata XML generated from ServiceNow Fluent code.Valid values:

-   bootstrap: The build process outputs a bootstrap XML file with the `<database>` root element for the table, field label XML files \[sys\_documentation\], licensing configuration XML files \[ua\_table\_licensing\_config\], and auto-numbering XML files \[sys\_number\].
-   component: The build process outputs XML files for each component of the Table API.

Default: `bootstrap`

</td></tr><tr><td>

taxonomy

</td><td>

Object

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

</td></tr><tr><td>

trustedModules

</td><td>

Array

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

tsconfigPath

</td><td>

String

</td><td>

A path to a `tsconfig.json` file with custom options for transpiling TypeScript into JavaScript during the build process. Specifying a `tsconfigPath` generates diagnostic results from TypeScript using the `tsconfig.json` file.**Warning:** You can't use this parameter and the `modulePaths` parameter. Configuring both results in an error.

Default: `.`

</td></tr><tr><td>

applicationRuntimePolicy

</td><td>

String

</td><td>

The runtime policy. For more information about runtime policies, see [Runtime access tracking](../../applications/concept/c_RuntimeAccessTracking.md).Valid values:

-   none: The system does not track runtime access requests.
-   tracking: During development, the system creates a Cross-Scope Privilege record for each runtime access request. After installation, the system no longer tracks new runtime access requests.
-   enforcing: During development, the system creates a Cross-Scope Privilege record for each runtime access request. After installation, the system no longer tracks new runtime access requests.

Default: none

</td></tr><tr><td>

networkPolicies

</td><td>

Array

</td><td>

A list of network access policy \[sys\_arp\_network\_policy\] definitions.-   policyType: Required. The type of network policy.

Valid values: csp\_script\_src, csp\_connect\_src, now\_inbound\_scoped, now\_inbound\_global, now\_outbound.

-   status: Required. The enforcement status of the policy.

Valid values: requested, allowed, denied

-   $id: A unique ID for the metadata object in the format `Now.ID['String' or Number]`.
-   active: Flag that indicates whether the policy is active.
-   host: Host address including the scheme, hostname, and optional port but not including the path.
-   scheme: The protocol scheme. Required if the policy type is now\_inbound\_global and must be empty for all other types.

Valid values: http, https, ws, wss

-   path: A list of paths. Each path must start with a slash `(/)`. Use the `/*` suffix to allow for sub-paths \(`/api/*`\). If the policy type is now\_inbound\_scoped, provide either a path or resource.
-   resource: A resource identifier for cross-scope access if the policy type is now\_inbound\_scoped. For example, `processor.subprocessor.context`. Provide either a path or resource.
-   shortDescription: A short description of what the policy does.

```json
"networkPolicies": [
  { 
      "policyType": "String",
      "status": "String",
      "$id": "String" or Number,
      "active": Boolean,
      "host": "String",
      "scheme": "String",
      "path": [Array],
      "resource": "String",
      "shortDescription": "String"
  }
]
```

</td></tr><tr><td>

wildcardPolicy

</td><td>

Object

</td><td>

A wildcard, or exemption, policy \[sys\_arp\_segment\_policy\] definition.-   $id: A unique ID for the metadata object in the format `Now.ID['String' or Number]`.
-   active: Flag that indicates whether the policy is active.
-   network: The network pillar configuration that includes the network wildcard selections.

Valid values for `networkWildcard`: now\_outbound, now\_inbound\_global, now\_inbound\_scoped, csp\_connect\_src, csp\_script\_src

-   scripting: The scripting pillar configuration that includes the scripting wildcard selections.

Valid values for `scriptingWildcard`: sys\_script\_include, scriptable

-   arl: The application resource limit \(ARL\) pillar configuration that includes the network wildcard selections.

Valid values for `arlWildcard`: scheduled\_job\_limit, event\_handler, api\_transaction\_limit, interactive\_transaction\_limit

-   record: Flag that indicates whether to allow record pillar access.
-   shortDescription: A short description of what the policy does.

```json
"wildcardPolicy": {
  "$id": "String" or Number,
  "active": Boolean,
  "network": {
      "active": Boolean,
      "networkWildcard": [Array]
  },
  "scripting": {
      "active": Boolean,
      "scriptingWildcard": [Array]
  },
  "arl": {
      "active": Boolean,
      "arlWildcard": [Array]
  },
  "record": Boolean,
  "shortDescription": "String"
}
```

</td></tr><tr><td>

performancePolicy

</td><td>

Object

</td><td>

A performance quota template \[sys\_app\_resource\_limit\_template\] definition.-   $id: A unique ID for the metadata object in the format `Now.ID['String' or Number]`.
-   apiTransactionLimit: The API transaction quota percentage.

Default: 30

-   eventHandlerLimit: The event handler quota percentage.

Default: 20

-   interactiveTransactionLimit: The interactive transaction quota percentage.

Default: 30

-   mode: The enforcement mode for quota thresholds. If this parameter is not set, the value is determined by the value of the `applicationRuntimePolicy` parameter.
-   scheduledJobLimit: The scheduled job quota percentage.

Default: 20

-   name: A name for the performance quota template.

```json
"performancePolicy": {
  "$id": "String" or Number,
  "apiTransactionLimit": Number,
  "eventHandlerLimit": Number,
  "interactiveTransactionLimit": Number,
  "mode": "String",
  "scheduledJobLimit": Number,
  "name": "String"
}
```

</td></tr></tbody>
</table>## Application configuration in source code

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

**Related topics**  


[Application access settings](../../applications/concept/c_ApplicationAccessSettings.md)

