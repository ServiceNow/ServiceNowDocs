---
title: Building apps in source code in ServiceNow Studio
description: Developing and maintaining applications in source code enables you to create and modify complex applications, manage code in source control more easily, and catch errors at build time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/building-apps-in-source-code-sn-studio.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-07-15"
reading_time_minutes: 3
keywords: [Source code, custom applications, pro-code development, servicenow studio]
breadcrumb: [Use, ServiceNow Studio, Developing your application, Building applications]
---

# Building apps in source code in ServiceNow Studio

Developing and maintaining applications in source code enables you to create and modify complex applications, manage code in source control more easily, and catch errors at build time.

To create apps in ServiceNow Studio, you use ServiceNow Fluent, a domain-specific programming language, to define the metadata that makes up applications. ServiceNow Fluent includes APIs for defining the different types of metadata. For more information, see [ServiceNow Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-fluent.md).

## Application structure

Fluent applications created or converted in ServiceNow Studio include source code files and metadata XML files. The `package.json` and `now.config.json` files define the application structure, which is similar to that of Node.js applications or Node Package Manager \(npm\) packages.

\[Omitted image "servicenow-ide-app-structure.png"\] Alt text: Structure of a source code application created in ServiceNow Studio

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

File containing the ServiceNow application configuration. The `now.config.json` file must be in the base directory for an application. You can configure aspects of an application by adding support parameters. For more information, see [Custom application configuration in source code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/app-config-source-code.md).

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
</table>-   **[Create a workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-a-workspace.md)**  
Create a workspace to view and organize the applications you're working on in ServiceNow Studio.
-   **[Create an app in source code](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/create-an-app-in-source-code.md)**  
Create an application to develop in source code in ServiceNow Studio.
-   **[Convert an application to Fluent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/convert-app-to-fluent.md)**  
Convert an existing application to support development in source code with ServiceNow Studio.
-   **[Build and install a Fluent app in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/build-install-fluent-app-sns.md)**  
Build an application to compile its source code and install application changes across an instance from ServiceNow Studio.
-   **[Synchronizing Fluent apps in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/synchronizing-fluent-apps.md)**  
Synchronizing an application in ServiceNow Studio downloads and transforms application metadata into ServiceNow Fluent code.

**Parent Topic:**[Using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/using-servicenow-studio.md)

