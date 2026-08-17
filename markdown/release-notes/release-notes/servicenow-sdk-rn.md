---
title: ServiceNow SDK release notes
description: The ServiceNow software development kit \(SDK\) enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. ServiceNow SDK was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# ServiceNow SDK release notes

The ServiceNow® software development kit \(SDK\) enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. ServiceNow SDK was enhanced and updated in the Yokohama release.

## ServiceNow SDK highlights for the Yokohama release

-   Create and develop applications in source code using an upgraded ServiceNow SDK CLI workflow.
-   Refer to content from a file from properties in ServiceNow Fluent APIs.

See  for more information.

## Important information for upgrading ServiceNow SDK to Yokohama

Upgrade to the latest version of the ServiceNow SDK with the `now-sdk upgrade` command. For more information, see .

ServiceNow SDK version 3.0 supports integrating with ServiceNow instances beginning with the Washington DC release.

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow IDE, SDK, and Fluent articles](https://www.servicenow.com/community/servicenow-ide-sdk-and-fluent/tkb-p/ide-sdk-fluent-articles) in the ServiceNow Community.

## New in the Yokohama release

-   **Init command replaces create and convert commands**

    Create a custom scoped application or convert an existing scoped application from a ServiceNow instance or local directory to support development in source code using the `now-sdk init` command.

-   **Download application metadata and transform it into source code**

    Download application metadata \(XML\) from a ServiceNow instance and transform the metadata into ServiceNow Fluent source code.

-   **Refer to content from a file in ServiceNow Fluent APIs**

    Use content from files in ServiceNow Fluent APIs by referring to the file from a property using the syntax `Now.include('path/to/file')`.

-   **Map metadata to custom directories**

    Map any application metadata to output directories that load only in specific circumstances using the `$meta` property in ServiceNow Fluent APIs.

-   **Specify a path to a custom tsconfig.json file**

    Use the `tsconfigPath` parameter in the `now.config.json` file for your application to specify the location of a `tsconfig.json` file with custom options for transpiling TypeScript into JavaScript during the build process.


## Changed in this release

-   **Subcommands replaced with parameters on the auth command**

    Configure authentication credentials with the `--add`, `--delete`, `--list`, and `--use` parameters of the `now-sdk auth` command.

-   **Dependencies command installs type definitions**

    Download TypeScript type definitions for Glide APIs and script includes from a ServiceNow instance based on the scripts in your application.

-   **Build command includes --frozenKeys parameter**

    Validate that the auto-generated `keys.ts` file is up to date for continuous integration \(CI\) builds by setting the `--frozenKeys` parameter to true with the `now-sdk build` command.

-   **Deploy command renamed install**

    Install or update an application on a ServiceNow instance using the `now-sdk install` command.

-   **Automated Test Framework Test API supports two-way synchronization**

    Synchronize changes to Automated Test Framework tests made outside of source code into source code definitions and back to metadata.

-   **Table API supports licensing configurations**

    Create a licensing configuration \[ua\_table\_licensing\_config\] to track subscription counts for a table with the licensing\_config object in the Table API.

-   **Table API supports remote tables**

    Create a remote table with the scriptable\_table property in a Table object.


## Removed in this release

-   The `now-sdk convert` command has been removed. Use the `now-sdk init` and `now-sdk transform` commands instead.
-   The `now-sdk fetch` command has been removed. Use the `now-sdk transform` command instead.

## Activation information

The ServiceNow SDK is available as a Node Package Manager \(npm\) package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see .

## Additional requirements

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see .

## Related ServiceNow applications and features

-   ****

    The ServiceNow IDE uses the ServiceNow SDK as its application packaging service to build applications, and the ServiceNow SDK provides the ServiceNow Fluent APIs for developing applications in source code in the ServiceNow IDE. Scoped applications created or converted with the ServiceNow SDK or ServiceNow IDE can be developed with either application.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/build-automate-rn-landing.md)

