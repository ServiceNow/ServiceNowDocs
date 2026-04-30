---
title: ServiceNow SDK release notes
description: The ServiceNow software development kit \(SDK\) enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. ServiceNow SDK was enhanced and updated in the 4.0 release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# ServiceNow SDK release notes

The ServiceNow® software development kit \(SDK\) enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. ServiceNow SDK was enhanced and updated in the 4.0 release.

## ServiceNow SDK highlights for the Zurich release

-   Develop a user interface \(UI\) with React to build a full-stack application in source code.
-   Define flows, service catalogs, UI pages and more in source code with ServiceNow Fluent APIs.

See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

## Important information for upgrading ServiceNow SDK to Zurich

To upgrade to the latest version of the ServiceNow SDK globally or within an application, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

ServiceNow SDK version 4.0 supports integration with ServiceNow instances beginning with the Washington DC release.

On Windows systems, after upgrading to ServiceNow SDK version 4.3 or later, existing stored credentials aren’t supported due to the deprecation of Keytar. Users on Windows systems must add their user credentials again using the `now-sdk auth --add` command to authenticate with instances. For more information, see [Authenticating to a ServiceNow instance with the ServiceNow SDK](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow SDK repository](https://github.com/ServiceNow/sdk/releases) on GitHub.

## New in the Zurich release

-   **[Flow API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Flow API to create flows and subflows \[sys\_hub\_flow\] that automate business processes with reusable multiple-step components.

-   **[Service Catalog API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Service Catalog API to define catalog items \[sc\_cat\_item\] and related aspects of service catalogs.

-   **[Email Notification API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Email Notification API to define notifications \[sysevent\_email\_action\] that send automated emails.

-   **[Service Level Agreement API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Service Level Agreement API to define service level agreements \(SLAs\) \[contract\_sla\] that set the amount of time for a task to reach a specified condition.

-   **[Dashboard API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Dashboard API to define dashboards \[par\_dashboard\] for organizing and sharing data visually.

-   **[Workspace API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Workspace API to define configurable workspace experiences for organizing and sharing data visually.

-   **[Allow access to ServiceNow APIs for third-party modules](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=zurich&pubname=zurich-application-development&ft:locale=en-US#application-structure)**

    Configure which third-party library modules to identify as trusted and have access to ServiceNow APIs with the `trustedModules` parameter in an application's `now.config.json` file.


-   **[Import Sets API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-import-sets-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Import Sets API to define transform maps \[sys\_transform\_map\] that specify how to transform and map data from the import set staging table to target tables.

-   **[UI Policy API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-ui-policy-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the UI Policy API to define user interface policies \[sys\_ui\_policy\] that dynamically change the behavior of information on a form and control custom process flows for tasks.

-   **[Attach user images to records from source code](https://www.servicenow.com/docs/access?context=fluent-constructs&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Attach user images to records associated with metadata defined in source code with the `Now.attach` construct.

-   **[Use utility functions for additional type validation](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use utility types that help validate values for properties that support the Duration \(Duration\(\)\), Time \(Time\(\)\), Field List \(FieldList\(\)\), and Template Value \(TemplateValue\(\)\) field types in ServiceNow Fluent APIs. Utility types provide validation at build time for tables both within and outside of an application.

-   **[Generated ServiceNow Fluent code organized in taxonomy-based directories](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=zurich&pubname=zurich-application-development&ft:locale=en-US#application-structure)**

    Configure a custom directory structure for metadata transformed into ServiceNow Fluent code with the `taxonomy` parameter in an application's `now.config.json` file. By default, generated ServiceNow Fluent files are organized in a taxonomy-based directory structure within the `fluent/generated` directory.


-   **[Specify which files to build as JavaScript modules](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=zurich&pubname=zurich-application-development&ft:locale=en-US#application-structure)**

    Configure which files to include or exclude when building JavaScript modules with the `serverModulesIncludePatterns` and `serverModulesExcludePatterns` parameters in an application's `now.config.json` file.


-   **[Develop a user interface with React](https://www.servicenow.com/docs/access?context=ui-development-react&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Develop a user interface with the React library and the UI Page API to build a full-stack application in source code.

-   **[Script Action API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-script-action-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Script Action API to define script actions \[sysevent\_script\_action\] that run when an event occurs.

-   **[Script Include API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-script-include-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Script Include API to define script includes \[sys\_script\_include\] that store JavaScript functions and classes for use by server-side scripts.

-   **[Service Portal API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-service-portal-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the Service Portal API to create custom widgets \[sp\_widget\] for portal pages.

-   **[UI Action API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-ui-action-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the UI Action API to configure custom user interface actions \[sys\_ui\_action\], such as buttons, links, and context menu items on forms and lists.

-   **[UI Page API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=fluent-ui-page-api&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the UI Page API to configure custom user interface pages \[sys\_ui\_page\] that display forms, dialogs, lists, and other UI components.

-   **[Download application metadata from an instance](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Download application metadata \(XML\) from a ServiceNow instance to compare it with the metadata in your local application using the `now-sdk download` command.

-   **[Clean or package an application](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Remove the build artifacts that were output with the previous build using the `now-sdk clean` command. You can also package the build artifacts that were output with the previous build into an installable ZIP file using the `now-sdk pack` command.


## Changed in this release

-   **[Get type checking and validation of client-side TypeScript files](https://www.servicenow.com/docs/access?context=ui-development-react&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Full-stack TypeScript applications support type checking and validation of `.ts` and `.tsx` files in the `src/client` directory when building applications.


-   **[Manage dependencies with additional parameters on the dependencies command](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&section=now-sdk-dependencies-command&ft:locale=en-US)**

    Control which dependencies and TypeScript definitions to download with additional parameters on the `now-sdk dependencies` command.

-   **[Use additional column types with ServiceNow Fluent](https://www.servicenow.com/docs/access?context=table-api-now-ts&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the following additional types of table columns with ServiceNow Fluent APIs: Password2Column, GuidColumn, JsonColumn, NameValuePairsColumn, UrlColumn, EmailColumn, HTMLColumn, FloatColumn, MultiLineTextColumn, DurationColumn, TimeColumn, FieldListColumn, SlushBucketColumn, TemplateValueColumn, and ApprovalRulesColumn.


-   **[Download TypeScript definitions for script includes used in JavaScript modules](https://www.servicenow.com/docs/access?context=downloading-dependencies-now-sdk&version=zurich&pubname=zurich-application-development&section=download-script-dependencies&ft:locale=en-US)**

    Download TypeScript definitions for script includes imported in JavaScript modules from an instance using the `now-sdk dependencies` command.

-   **[Apply a template to an existing application](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&section=now-sdk-create-command&ft:locale=en-US)**

    Add template files and directories for development in ServiceNow Fluent using the `--template` parameter with the `now-sdk init` command in an existing application.


-   **[Automated Test Framework API supports additional test steps](https://www.servicenow.com/docs/access?context=atf-test-now-ts&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the following test steps with the ServiceNow Fluent Automated Test Framework API.

    -   atf.form.addAttachmentsToForm
    -   atf.form\_SP.addAttachmentsToForm
    -   atf.server.addAttachmentsToExistingRecord
    -   atf.server.runServerSideScript
    -   atf.server.setOutputVariables
-   **[Build command doesn't package build artifacts](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    Use the `now-sdk pack` or `now-sdk install` commands to package build artifacts. The `now-sdk build` command compiles the source files but doesn't package the build artifacts.


## Removed in this release

-   The `now-sdk upgrade` command has been removed. To upgrade the version of the ServiceNow SDK, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Deprecations

-   The $id property is deprecated in the List API and Role API.
-   Property names that use snake case are deprecated in all ServiceNow Fluent APIs. Use the equivalent property name in camel case instead.

## Activation information

The ServiceNow SDK is available as a Node Package Manager \(npm\) package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Additional requirements

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    The ServiceNow IDE uses the ServiceNow SDK as its application packaging service to build applications, and the ServiceNow SDK provides the ServiceNow Fluent APIs for developing applications in source code in the ServiceNow IDE. Scoped applications created or converted with the ServiceNow SDK or ServiceNow IDE can be developed with either application.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

