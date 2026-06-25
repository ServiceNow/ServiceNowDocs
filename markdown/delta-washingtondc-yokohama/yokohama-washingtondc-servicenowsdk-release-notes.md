---
title: Combined ServiceNow SDK release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for ServiceNow SDK from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-servicenowsdk-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined ServiceNow SDK release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for ServiceNow SDK from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow SDK release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow SDK to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

Upgrade to the latest version of the ServiceNow SDK with the `now-sdk upgrade` command. For more information, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Upgrade to the latest version of the ServiceNow SDK with the `now-sdk upgrade` command. For more information, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=yokohama&ft:locale=en-US).

 ServiceNow SDK version 3.0 supports integrating with ServiceNow instances beginning with the Washington DC release.

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow IDE, SDK, and Fluent articles](https://www.servicenow.com/community/servicenow-ide-sdk-and-fluent/tkb-p/ide-sdk-fluent-articles) in the ServiceNow Community.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for ServiceNow SDK.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Turn off synchronizing changes to ServiceNow Fluent code](https://www.servicenow.com/docs/access?context=servicenow-fluent&family=xanadu&ft:locale=en-US)**

Turn off synchronizing changes to ServiceNow Fluent objects or files using the `@fluent-disable-sync` or `@fluent-disable-sync-for-file` comment directives.


-   **[Authenticate to an instance using OAuth 2.0](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&family=xanadu&ft:locale=en-US)**

Authenticate to a ServiceNow instance using OAuth 2.0 by setting the `type` parameter on the `now-sdk auth` command to `oauth`.

-   **[Ignore ServiceNow Fluent diagnostics](https://www.servicenow.com/docs/access?context=servicenow-fluent&family=xanadu&ft:locale=en-US)**

Suppress ServiceNow Fluent and TypeScript diagnostics using the `@fluent-ignore` comment directive.


-   **[Build scoped applications in source code](https://www.servicenow.com/docs/access?context=servicenow-fluent&family=xanadu&ft:locale=en-US)**

Write source code to define the metadata that makes up applications using ServiceNow Fluent. ServiceNow Fluent is a domain-specific programming language with APIs for defining the different types of application metadata. Developing applications in source code enables you to work in familiar development environments, create and modify complex applications, manage code in source control more easily, and catch errors at build time.

-   **[ServiceNow Fluent Language server in Visual Studio Code](https://www.servicenow.com/docs/access?context=install-fluent-language-extension-vs-code&family=xanadu&ft:locale=en-US)**

Get language processing and validation for ServiceNow Fluent in Visual Studio Code by installing the ServiceNow Fluent Language server from the Visual Studio Code Marketplace.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Init command replaces create and convert commands](https://www.servicenow.com/docs/access?context=now-sdk-create-command&family=yokohama&ft:locale=en-US)**

Create a custom scoped application or convert an existing scoped application from a ServiceNow instance or local directory to support development in source code using the `now-sdk init` command.

-   **[Download application metadata and transform it into source code](https://www.servicenow.com/docs/access?context=now-sdk-transform-command&family=yokohama&ft:locale=en-US)**

Download application metadata \(XML\) from a ServiceNow instance and transform the metadata into ServiceNow Fluent source code.

-   **[Refer to content from a file in ServiceNow Fluent APIs](https://www.servicenow.com/docs/access?context=servicenow-fluent&family=yokohama&ft:locale=en-US)**

Use content from files in ServiceNow Fluent APIs by referring to the file from a property using the syntax `Now.include('path/to/file')`.

-   **[Map metadata to custom directories](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&family=yokohama&ft:locale=en-US)**

Map any application metadata to output directories that load only in specific circumstances using the `$meta` property in ServiceNow Fluent APIs.

-   **[Specify a path to a custom tsconfig.json file](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=yokohama&ft:locale=en-US)**

Use the `tsconfigPath` parameter in the `now.config.json` file for your application to specify the location of a `tsconfig.json` file with custom options for transpiling TypeScript into JavaScript during the build process.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing ServiceNow SDK features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Convert command uses module project type by default](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&family=xanadu&ft:locale=en-US)**

The `projectType` parameter is set to `module` by default. By converting an application with the module project type, you can gradually migrate application metadata into ServiceNow Fluent code rather than converting all application metadata into code initially.


-   **[transpiledSourceDir parameter replaced with modulePaths parameter in now.config.json file](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=xanadu&ft:locale=en-US)**

Use the `modulePaths` parameter in the `now.config.json` file for your application to map the source directory for modules to the output directory for modules instead of the deprecated `transpiledSourceDir` parameter. The `modulePaths` parameter is used to compile TypeScript source files into JavaScript modules.


-   **[Table API includes label object](https://www.servicenow.com/docs/access?context=table-api-now-ts&family=xanadu&ft:locale=en-US)**

Configure field labels \[sys\_documentation\] for tables and columns with the label object in the Table API.


-   **[Create and convert commands include template parameter](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&family=xanadu&ft:locale=en-US)**

Specify whether to use JavaScript or TypeScript in modules with the `template` parameter on the `now-sdk create` and `now-sdk convert` commands. This parameter determines the configuration of the `package.json` and `now.config.json` files and adds a `tsconfig.json` file for TypeScript projects.


-   **[Default application structure](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=xanadu&ft:locale=en-US)**

The default application structure includes some changes to directories and files, including the addition of a `.gitignore` file and moving the `now` object configuration in `package.json` to its own `now.config.json` file.

-   **[Create and convert commands include project-type parameter](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&family=xanadu&ft:locale=en-US)**

Specify the type of application to create or convert with the `project-type` parameter on the `now-sdk create` and `now-sdk convert` commands. This parameter determines the default application structure based on whether you want to use ServiceNow Fluent and JavaScript modules and third-party libraries in the application \(`fluent`\) or only use JavaScript modules and third-party libraries \(`module`\).

-   **[Fetch command includes debug parameter](https://www.servicenow.com/docs/access?context=now-sdk-fetch-command&family=xanadu&ft:locale=en-US)**

Return debug logs generated during the fetch process by setting the `debug` parameter to true with the `now-sdk fetch` command.

-   **[Deploy command includes reinstall parameter](https://www.servicenow.com/docs/access?context=now-sdk-deploy-command&family=xanadu&ft:locale=en-US)**

Uninstall and reinstall the application on the instance by setting the `reinstall` parameter to true with the `now-sdk deploy` command. Reinstalling an application ensures that the metadata on the instance matches the metadata in the deployment package.

**Warning:** Metadata that is on the instance but not in your local application is removed.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Subcommands replaced with parameters on the auth command](https://www.servicenow.com/docs/access?context=now-sdk-auth-command&family=yokohama&ft:locale=en-US)**

Configure authentication credentials with the `--add`, `--delete`, `--list`, and `--use` parameters of the `now-sdk auth` command.

-   **[Dependencies command installs type definitions](https://www.servicenow.com/docs/access?context=now-sdk-dependencies-command&family=yokohama&ft:locale=en-US)**

Download TypeScript type definitions for Glide APIs and script includes from a ServiceNow instance based on the scripts in your application.

-   **[Build command includes --frozenKeys parameter](https://www.servicenow.com/docs/access?context=now-sdk-build-command&family=yokohama&ft:locale=en-US)**

Validate that the auto-generated `keys.ts` file is up to date for continuous integration \(CI\) builds by setting the `--frozenKeys` parameter to true with the `now-sdk build` command.

-   **[Deploy command renamed install](https://www.servicenow.com/docs/access?context=now-sdk-deploy-command&family=yokohama&ft:locale=en-US)**

Install or update an application on a ServiceNow instance using the `now-sdk install` command.

-   **[Automated Test Framework Test API supports two-way synchronization](https://www.servicenow.com/docs/access?context=atf-test-now-ts&family=yokohama&ft:locale=en-US)**

Synchronize changes to Automated Test Framework tests made outside of source code into source code definitions and back to metadata.

-   **[Table API supports licensing configurations](https://www.servicenow.com/docs/access?context=table-api-now-ts&family=yokohama&ft:locale=en-US)**

Create a licensing configuration \[ua\_table\_licensing\_config\] to track subscription counts for a table with the licensing\_config object in the Table API.

-   **[Table API supports remote tables](https://www.servicenow.com/docs/access?context=table-api-now-ts&family=yokohama&ft:locale=en-US)**

Create a remote table with the scriptable\_table property in a Table object.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some ServiceNow SDK features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   The `scopeId` parameter was removed from the `now-sdk convert` command, which supported converting global applications. Only scoped applications can be converted.
-   The `mode` parameter was removed from the `now-sdk fetch` and `now-sdk deploy` commands. A complete fetch or deploy are always executed.

</td></tr><tr><td>

Yokohama

</td><td>

-   The `now-sdk convert` command has been removed. Use the `now-sdk init` and `now-sdk transform` commands instead.
-   The `now-sdk fetch` command has been removed. Use the `now-sdk transform` command instead.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some ServiceNow SDK features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow SDK.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

The ServiceNow SDK is available as an npm package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see [Install the ServiceNow SDK](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

The ServiceNow SDK is available as a Node Package Manager \(npm\) package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see [Install the ServiceNow SDK](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow SDK we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

You must have Node.js and npm installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow SDK we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow SDK, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow SDK we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow SDK we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

Write source code to define the metadata that makes up applications with ServiceNow Fluent.

 See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Create and develop applications in source code using an upgraded ServiceNow SDK CLI workflow.
-   Refer to content from a file from properties in ServiceNow Fluent APIs.

 See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

