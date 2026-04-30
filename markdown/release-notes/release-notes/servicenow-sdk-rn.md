---
title: ServiceNow SDK release notes
description: The ServiceNow software development kit \(SDK\) enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. ServiceNow SDK was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# ServiceNow SDK release notes

The ServiceNow® software development kit \(SDK\) enables developers to create scoped applications in source code locally in Visual Studio Code Desktop and upload changes to a ServiceNow instance. ServiceNow SDK was enhanced and updated in the Xanadu release.

## ServiceNow SDK highlights for the Xanadu release

Write source code to define the metadata that makes up applications with ServiceNow Fluent.

See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) for more information.

## Important information for upgrading ServiceNow SDK to Xanadu

Upgrade to the latest version of the ServiceNow SDK with the `now-sdk upgrade` command. For more information, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow IDE, SDK, and Fluent articles](https://www.servicenow.com/community/servicenow-ide-sdk-and-fluent/tkb-p/ide-sdk-fluent-articles) in the ServiceNow Community.

## New in the Xanadu release

-   **[Turn off synchronizing changes to ServiceNow Fluent code](https://www.servicenow.com/docs/access?context=servicenow-fluent&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Turn off synchronizing changes to ServiceNow Fluent objects or files using the `@fluent-disable-sync` or `@fluent-disable-sync-for-file` comment directives.


-   **[Authenticate to an instance using OAuth 2.0](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Authenticate to a ServiceNow instance using OAuth 2.0 by setting the `type` parameter on the `now-sdk auth` command to `oauth`.

-   **[Ignore ServiceNow Fluent diagnostics](https://www.servicenow.com/docs/access?context=servicenow-fluent&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Suppress ServiceNow Fluent and TypeScript diagnostics using the `@fluent-ignore` comment directive.


-   **[Build scoped applications in source code](https://www.servicenow.com/docs/access?context=servicenow-fluent&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Write source code to define the metadata that makes up applications using ServiceNow Fluent. ServiceNow Fluent is a domain-specific programming language with APIs for defining the different types of application metadata. Developing applications in source code enables you to work in familiar development environments, create and modify complex applications, manage code in source control more easily, and catch errors at build time.

-   **[ServiceNow Fluent Language server in Visual Studio Code](https://www.servicenow.com/docs/access?context=install-fluent-language-extension-vs-code&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Get language processing and validation for ServiceNow Fluent in Visual Studio Code by installing the ServiceNow Fluent Language server from the Visual Studio Code Marketplace.


## Changed in this release

-   **[Convert command uses module project type by default](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    The `projectType` parameter is set to `module` by default. By converting an application with the module project type, you can gradually migrate application metadata into ServiceNow Fluent code rather than converting all application metadata into code initially.


-   **[transpiledSourceDir parameter replaced with modulePaths parameter in now.config.json file](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US#application-structure)**

    Use the `modulePaths` parameter in the `now.config.json` file for your application to map the source directory for modules to the output directory for modules instead of the deprecated `transpiledSourceDir` parameter. The `modulePaths` parameter is used to compile TypeScript source files into JavaScript modules.


-   **[Table API includes label object](https://www.servicenow.com/docs/access?context=table-api-now-ts&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Configure field labels \[sys\_documentation\] for tables and columns with the label object in the Table API.


-   **[Create and convert commands include template parameter](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Specify whether to use JavaScript or TypeScript in modules with the `template` parameter on the `now-sdk create` and `now-sdk convert` commands. This parameter determines the configuration of the `package.json` and `now.config.json` files and adds a `tsconfig.json` file for TypeScript projects.


-   **[Default application structure](https://www.servicenow.com/docs/access?context=building-applications-source-code&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US#application-structure)**

    The default application structure includes some changes to directories and files, including the addition of a `.gitignore` file and moving the `now` object configuration in `package.json` to its own `now.config.json` file.

-   **[Create and convert commands include project-type parameter](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Specify the type of application to create or convert with the `project-type` parameter on the `now-sdk create` and `now-sdk convert` commands. This parameter determines the default application structure based on whether you want to use ServiceNow Fluent and JavaScript modules and third-party libraries in the application \(`fluent`\) or only use JavaScript modules and third-party libraries \(`module`\).

-   **Fetch command includes debug parameter**

    Return debug logs generated during the fetch process by setting the `debug` parameter to true with the `now-sdk fetch` command.

-   **[Deploy command includes reinstall parameter](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&version=xanadu&pubname=xanadu-application-development&section=now-sdk-deploy-command&ft:locale=en-US)**

    Uninstall and reinstall the application on the instance by setting the `reinstall` parameter to true with the `now-sdk deploy` command. Reinstalling an application ensures that the metadata on the instance matches the metadata in the deployment package.

    **Warning:** Metadata that is on the instance but not in your local application is removed.


## Removed in this release

-   The `scopeId` parameter was removed from the `now-sdk convert` command, which supported converting global applications. Only scoped applications can be converted.
-   The `mode` parameter was removed from the `now-sdk fetch` and `now-sdk deploy` commands. A complete fetch or deploy are always executed.

## Activation information

The ServiceNow SDK is available as an npm package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Additional requirements

You must have Node.js and npm installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK in an application](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    The ServiceNow IDE uses the ServiceNow SDK as its application packaging service to build applications, and the ServiceNow SDK provides the ServiceNow Fluent APIs for developing applications in source code in the ServiceNow IDE. Scoped applications created with the ServiceNow SDK or ServiceNow IDE can be developed with either application.


**Parent Topic:**[Hyperautomation and Low-code release notes](build-automate-rn-landing.md)

