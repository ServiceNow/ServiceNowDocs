---
title: Building applications in source code
description: Create and develop custom applications in source code using familiar development tools and processes.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Building pro-code applications, Developing your application, Building applications]
---

# Building applications in source code

Create and develop custom applications in source code using familiar development tools and processes.

## Overview of development in source code

You can create scoped applications in code using the ServiceNow IDE on the ServiceNow AI Platform or locally in Visual Studio Code Desktop with the ServiceNow SDK.

In either development environment, you use ServiceNow Fluent, a domain-specific programming language, to define the metadata that makes up applications. ServiceNow Fluent includes APIs for defining the different types of metadata.

With the ServiceNow IDE or ServiceNow SDK, you can also create JavaScript modules and use third-party libraries in your application to optimize code reuse in scripts within a scoped application.

Developing and maintaining applications in source code enables you to work in familiar development environments, create and modify complex applications, manage code in source control more easily, and catch errors at build time.

**Note:** The ServiceNow IDE and ServiceNow SDK don't support the Global scope or global applications in the Yokohama release.

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

Code auto-complete support for scripts.For information about activation, see [Now Assist for code generation](https://www.servicenow.com/docs/access?context=now-assist-code-landing&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

</td><td>

Not supported

</td></tr></tbody>
</table>## Application structure

Custom scoped applications created with the ServiceNow IDE or ServiceNow SDK include source code files and metadata XML files. The `package.json` and `now.config.json` files define the application structure, which is similar to that of Node.js applications or Node Package Manager \(npm\) packages.

![Structure of an application created in the ServiceNow IDE](../../servicenow-ide/image/servicenow-ide-app-structure.png "Default structure of an application created in the ServiceNow IDE")

By default, applications include the following directories and files. You can modify certain aspects of the application structure to suit your needs in the `now.config.json` file.

<table id="table_ws5_flw_53c"><thead><tr><th>

Directory or file

</th><th>

Description

</th></tr></thead><tbody><tr><td>

.vscode

</td><td>

Directory containing recommended Visual Studio Code extensions.

</td></tr><tr><td>

dist

</td><td>

Directory containing the build artifacts for packaging. This directory includes the following subdirectories:-   `app`: Directory containing the built metadata XML files.
-   `static`: Directory containing the built static asset files.

</td></tr><tr><td>

metadata

</td><td>

Directory containing the application metadata \(XML\) of the application, such as table schemas and business rules, organized in the same directory structure as existing ServiceNow applications.

 **Note:** Application metadata shouldn't be edited from the XML files. Edit application metadata in the source code or on the ServiceNow AI Platform.

</td></tr><tr><td>

node\_modules

</td><td>

Directory containing the third-party Node.js modules on which your application depends.

</td></tr><tr><td>

src

</td><td>

Directory containing the source code of your application. This directory includes the following subdirectories:-   `client`: Directory containing the client-side files for developing user interfaces.
-   `fluent`: Directory containing ServiceNow Fluent code in `.now.ts` files. The `generated` subdirectory contains the application files converted to ServiceNow Fluent.
-   `server`: Directory containing JavaScript module code in `.js` or `.ts` files.

</td></tr><tr><td>

target

</td><td>

Directory containing an installable package \(`.zip` file\) to upload to an instance.

</td></tr><tr><td>

.eslintrc

</td><td>

File containing the ESLint configuration. ESLint helps identify and fix issues in the application code.

</td></tr><tr><td>

.gitignore

</td><td>

File containing a list of directories or files for Git to ignore. These files aren't tracked in source control.

</td></tr><tr><td>

now.config.json

</td><td>

File containing the ServiceNow application configuration. The `now.config.json` file must be in the base directory for an application. You can configure aspects of an application by adding support parameters. For more information, see [Custom application configuration in source code](../../servicenow-sdk/reference/app-config-source-code.md).

</td></tr><tr><td>

now.prebuild.mjs

</td><td>

Auto-updated file containing complete information about dependencies and their versions. This file is only available with the ServiceNow SDK.

</td></tr><tr><td>

package-lock.json

</td><td>

Auto-updated file containing complete information about dependencies and their versions. This file is only available with the ServiceNow SDK.

</td></tr><tr><td>

package.json

</td><td>

File containing information about your application and custom or third-party module dependencies. The `package.json` file must be in the base directory for an application. On an instance, the `package.json` path is specified in the **Package JSON** field of the custom application record \[sys\_app\] in the format `<scope>/<package-name>/<version>/package.json`.

</td></tr></tbody>
</table>## Related applications and features

-   **[JavaScript APIs](https://www.servicenow.com/docs/access?context=api-reference&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)**

    Use JavaScript APIs in scripts that you write to change the functionality of applications or when you create applications.


**Related topics**  


[ServiceNow Fluent](../../servicenow-sdk/concept/servicenow-fluent.md)

[JavaScript modules and third-party libraries](../../servicenow-sdk/concept/javascript-modules-third-party-libraries.md)

[User interface development with React](../../servicenow-sdk/concept/ui-development-react.md)

[Custom application configuration in source code](../../servicenow-sdk/reference/app-config-source-code.md)

