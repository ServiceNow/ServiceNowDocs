---
title: UI component CLI extension commands
description: Command syntax, parameters, and examples for the UI component CLI extension, which scaffolds, develops, and deploys Next Experience UI Framework components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/ui-component-cli-extension-commands.html
release: australia
topic_type: reference
last_updated: "2026-10-24"
reading_time_minutes: 3
breadcrumb: [UI component CLI extension reference, UI component CLI extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# UI component CLI extension commands

Command syntax, parameters, and examples for the UI component CLI extension, which scaffolds, develops, and deploys Next Experience UI Framework components.

## Syntax

Run the UI component CLI extension commands with the following syntax:

```
snc ui-component <cmd> [args]
```

To list the available commands, run the following command:

```
snc ui-component --help
```

## project

Creates and scaffolds a new project with all the files needed to start development.

<table id="table_project_parameters"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

name

</td><td>

Project name.Must be a valid and unique npm package name.

</td><td>

None

</td></tr><tr><td>

description

</td><td>

Project description.Appears in the npm registry and the plugins list.

</td><td>

None

</td></tr><tr><td>

scope

</td><td>

Suggested scope name for the project and its components.Scope name requirements:

-   The scope name must be unique.
-   The scope name is limited to 18 characters.
-   The scope name must use snake case.
-   The scope name cannot start with a hyphen. Only CLI options can begin with a hyphen.
-   The scope name must follow the form `x_customerprefix_componentname`. The customer prefix is the value of the `glide.appcreator.company.code` system property on your instance. The component name is the value of the **name** parameter.

When you omit the scope parameter, the extension generates the scope name as `x_{vendor_prefix}_{package_name}`.

</td><td>

Generated from the vendor prefix and package name.

</td></tr><tr><td>

offline

</td><td>

Option that skips connection to the current host during scaffolding, including scope validation. Scope is required when this option is set.

</td><td>

false

</td></tr></tbody>
</table>## project

```
snc ui-component project --name @myorg/movie-quotes --description 'A web component that prints movie quotes.'
```

```
 snc ui-component project --name @myorg/hello-world --scope x_myorg_helloworld --offline
```

```
snc ui-component create --name @myorg/hello-world --scope x_myorg_helloworld --offline
```

## develop

Runs the development server, where you can evaluate and iterate on web components.

|Parameter|Description|Default|
|---------|-----------|-------|
|entry, e|Path to the test module.|example/index.js|
|open|Option that opens the default browser and navigates to the test page.|false|
|port|Port where the development server listens for incoming connections.|8081|
|host, h|Host address that makes the local development server accessible to other users. Typically set to 0.0.0.0.|None|
|cache-build-output, -cb|Option that stores built assets to disk on the first run. Later runs read the built assets from the cache in node\_modules/.cache/webpack.|false|
|clear-cache, cc|Option that clears the build cache before the develop operation.|false|
|fetch-assets-from-instance, fa|Experimental. Resolves import statements through the instance in the profile, and then from the node\_modules directory. Not expected to work in all scenarios.|false|
|typeCheck, tc|Type checking for components written in TypeScript and JavaScript.|true|

## develop

```
snc ui-component develop
```

```
snc ui-component develop --entry example/hello.js --open --port 3000
```

```
snc ui-component develop --host 0.0.0.0
```

```
snc ui-component develop --fetch-assets-from-instance
```

```
snc ui-component develop --cache-build-output
```

```
snc ui-component develop --clear-cache
```

```
snc ui-component develop --type-check false
```

## deploy

Deploys the project to the current ServiceNow host.

|Parameter|Description|Default|
|---------|-----------|-------|
|force|Option that deletes existing component records and recreates all component records.|false|
|strict-validate-now-ui-json, s|Validation of the now-ui.json schema. Any errors cause the deployment to fail.|true|
|fetch-assets-from-instance, fa|Experimental. Resolves import statements through the instance in the profile, and then from the node\_modules directory. Not expected to work in all scenarios.|false|
|typeCheck, tc|Type checking for components written in TypeScript and JavaScript.|true|

## deploy

```
snc ui-component deploy
```

```
snc ui-component deploy --force
```

```
snc ui-component deploy --type-check false
```

```
snc ui-component deploy --fetch-assets-from-instance
```

```
snc ui-component deploy --strict-validate-now-ui-json false
```

## generate-update-set

Generates a single update set XML file that contains all the component build artifacts. The file is stored in the `.now-cli` folder in the project root directory. The aliases for this command are `gus` and `generateUpdateSet`.

|Parameter|Description|Default|
|---------|-----------|-------|
|fetch-assets-from-instance, fa|Experimental. Resolves import statements through the instance in the profile, and then from the node\_modules directory. Not expected to work in all scenarios.|false|
|offline|Option that skips connection to the instance and scope validation during the process.|false|
|typeCheck, tc|Type checking for components written in TypeScript and JavaScript.|true|

## generate-update-set

```
snc ui-component generate-update-set
```

```
snc ui-component generate-update-set --type-check false
```

## capture-metrics

Turns the collection of CLI usage metrics on or off. Collection is enabled by default.

|Parameter|Description|
|---------|-----------|
|enable|Collection of user metrics from the CLI.|
|disable|Collection of user metrics from the CLI, turned off.|

## capture-metrics

```
snc ui-component capture-metrics --enable
```

```
snc ui-component capture-metrics --disable
```

