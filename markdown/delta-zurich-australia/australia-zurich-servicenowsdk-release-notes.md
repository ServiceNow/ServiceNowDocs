---
title: Combined ServiceNow SDK release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for ServiceNow SDK from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-servicenowsdk-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined ServiceNow SDK release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for ServiceNow SDK from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow SDK release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow SDK to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

To upgrade to the latest version of the ServiceNow SDK globally or within an application, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=zurich&ft:locale=en-US).

 ServiceNow SDK version 4.0 supports integration with ServiceNow instances beginning with the Washington DC release.

 On Windows systems, after upgrading to ServiceNow SDK version 4.3 or later, existing stored credentials aren’t supported due to the deprecation of Keytar. Users on Windows systems must add their user credentials again using the `now-sdk auth --add` command to authenticate with instances. For more information, see [Authenticate](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&family=zurich&ft:locale=en-US).

**Note:** For more information about minor releases of the ServiceNow SDK, see the [ServiceNow SDK repository](https://github.com/ServiceNow/sdk/releases) on GitHub.

</td></tr><tr><td>

Australia

</td><td>

To upgrade to the latest version of the ServiceNow SDK globally or within an application, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=australia&ft:locale=en-US).

 ServiceNow SDK version 4.4 supports integration with ServiceNow instances beginning with the Washington DC release.

 On Windows systems, after upgrading to ServiceNow SDK version 4.3 or later, existing stored credentials aren’t supported due to the deprecation of Keytar. Users on Windows systems must add their user credentials again using the `now-sdk auth --add` command to authenticate with instances. For more information, see [Authenticate](https://www.servicenow.com/docs/access?context=authenticate-instance-now-sdk&family=australia&ft:locale=en-US).

**Important:** For minor releases of the ServiceNow SDK, see the [ServiceNow SDK release notes](https://github.com/ServiceNow/sdk/releases) on GitHub.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow SDK.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Flow API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&family=zurich&ft:locale=en-US)**

Use the Flow API to create flows and subflows \[sys\_hub\_flow\] that automate business processes with reusable multiple-step components.

-   **[Service Catalog API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&family=zurich&ft:locale=en-US)**

Use the Service Catalog API to define catalog items \[sc\_cat\_item\] and related aspects of service catalogs.

-   **[Email Notification API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&family=zurich&ft:locale=en-US)**

Use the Email Notification API to define notifications \[sysevent\_email\_action\] that send automated emails.

-   **[Service Level Agreement API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&family=zurich&ft:locale=en-US)**

Use the Service Level Agreement API to define service level agreements \(SLAs\) \[contract\_sla\] that set the amount of time for a task to reach a specified condition.

-   **[Dashboard API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&family=zurich&ft:locale=en-US)**

Use the Dashboard API to define dashboards \[par\_dashboard\] for organizing and sharing data visually.

-   **[Workspace API - ServiceNow Fluent](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&family=zurich&ft:locale=en-US)**

Use the Workspace API to define configurable workspace experiences for organizing and sharing data visually.

-   **[Allow access to ServiceNow APIs for third-party modules](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=zurich&ft:locale=en-US)**

Configure which third-party library modules to identify as trusted and have access to ServiceNow APIs with the `trustedModules` parameter in an application's `now.config.json` file.


-   **[Import Sets API](https://www.servicenow.com/docs/access?context=fluent-import-sets-api&family=zurich&ft:locale=en-US)**

Use the Import Sets API to define transform maps \[sys\_transform\_map\] that specify how to transform and map data from the import set staging table to target tables.

-   **[UI Policy API](https://www.servicenow.com/docs/access?context=fluent-ui-policy-api&family=zurich&ft:locale=en-US)**

Use the UI Policy API to define user interface policies \[sys\_ui\_policy\] that dynamically change the behavior of information on a form and control custom process flows for tasks.

-   **[Attach user images to records from source code](https://www.servicenow.com/docs/access?context=fluent-constructs&family=zurich&ft:locale=en-US)**

Attach user images to records associated with metadata defined in source code with the `Now.attach` construct.

-   **[Use utility functions for additional type validation](https://www.servicenow.com/docs/access?context=servicenow-fluent-api-reference&family=zurich&ft:locale=en-US)**

Use utility types that help validate values for properties that support the Duration \(Duration\(\)\), Time \(Time\(\)\), Field List \(FieldList\(\)\), and Template Value \(TemplateValue\(\)\) field types in ServiceNow Fluent APIs. Utility types provide validation at build time for tables both within and outside of an application.

-   **[Generated ServiceNow Fluent code organized in taxonomy-based directories](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=zurich&ft:locale=en-US)**

Configure a custom directory structure for metadata transformed into ServiceNow Fluent code with the `taxonomy` parameter in an application's `now.config.json` file. By default, generated ServiceNow Fluent files are organized in a taxonomy-based directory structure within the `fluent/generated` directory.


-   **[Specify which files to build as JavaScript modules](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=zurich&ft:locale=en-US)**

Configure which files to include or exclude when building JavaScript modules with the `serverModulesIncludePatterns` and `serverModulesExcludePatterns` parameters in an application's `now.config.json` file.


-   **[Develop a user interface with React](https://www.servicenow.com/docs/access?context=ui-development-react&family=zurich&ft:locale=en-US)**

Develop a user interface with the React library and the UI Page API to build a full-stack application in source code.

-   **[Script Action API](https://www.servicenow.com/docs/access?context=fluent-script-action-api&family=zurich&ft:locale=en-US)**

Use the Script Action API to define script actions \[sysevent\_script\_action\] that run when an event occurs.

-   **[Script Include API](https://www.servicenow.com/docs/access?context=fluent-script-include-api&family=zurich&ft:locale=en-US)**

Use the Script Include API to define script includes \[sys\_script\_include\] that store JavaScript functions and classes for use by server-side scripts.

-   **[Service Portal API](https://www.servicenow.com/docs/access?context=fluent-service-portal-api&family=zurich&ft:locale=en-US)**

Use the Service Portal API to create custom widgets \[sp\_widget\] for portal pages.

-   **[UI Action API](https://www.servicenow.com/docs/access?context=fluent-ui-action-api&family=zurich&ft:locale=en-US)**

Use the UI Action API to configure custom user interface actions \[sys\_ui\_action\], such as buttons, links, and context menu items on forms and lists.

-   **[UI Page API](https://www.servicenow.com/docs/access?context=fluent-ui-page-api&family=zurich&ft:locale=en-US)**

Use the UI Page API to configure custom user interface pages \[sys\_ui\_page\] that display forms, dialogs, lists, and other UI components.

-   **[Download application metadata from an instance](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&family=zurich&ft:locale=en-US)**

Download application metadata \(XML\) from a ServiceNow instance to compare it with the metadata in your local application using the `now-sdk download` command.

-   **[Clean or package an application](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&family=zurich&ft:locale=en-US)**

Remove the build artifacts that were output with the previous build using the `now-sdk clean` command. You can also package the build artifacts that were output with the previous build into an installable ZIP file using the `now-sdk pack` command.


</td></tr><tr><td>

Australia

</td><td>

-   **[Create and convert global applications](https://www.servicenow.com/docs/access?context=creating-applications-servicenow-sdk&family=australia&ft:locale=en-US)**

Create and convert applications in the global scope that are accessible to other global applications with instances on the Australia release.

-   **[Move application metadata from the global scope into a global application](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&family=australia&ft:locale=en-US)**

Transform application metadata \(XML\) in the global scope from an instance into ServiceNow Fluent source code to customize it in a local global application using the `now-sdk move` command.

-   **[Configure a default language for field labels](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=australia&ft:locale=en-US)**

Configure a default language for field labels \[sys\_documentation\] in a table or column with the `tableDefaultLanguage` parameter in an application's `now.config.json` file.

-   **[Configure read-only options with the Table API](https://www.servicenow.com/docs/access?context=table-api-now-ts&family=australia&ft:locale=en-US)**

Control the editability of read-only fields by configuring read-only options for a field with the readOnlyOption property in a Column object.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow SDK features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Get type checking and validation of client-side TypeScript files](https://www.servicenow.com/docs/access?context=ui-development-react&family=zurich&ft:locale=en-US)**

Full-stack TypeScript applications support type checking and validation of `.ts` and `.tsx` files in the `src/client` directory when building applications.


-   **[Manage dependencies with additional parameters on the dependencies command](https://www.servicenow.com/docs/access?context=now-sdk-dependencies-command&family=zurich&ft:locale=en-US)**

Control which dependencies and TypeScript definitions to download with additional parameters on the `now-sdk dependencies` command.

-   **[Use additional column types with ServiceNow Fluent](https://www.servicenow.com/docs/access?context=table-api-now-ts&family=zurich&ft:locale=en-US)**

Use the following additional types of table columns with ServiceNow Fluent APIs: Password2Column, GuidColumn, JsonColumn, NameValuePairsColumn, UrlColumn, EmailColumn, HTMLColumn, FloatColumn, MultiLineTextColumn, DurationColumn, TimeColumn, FieldListColumn, SlushBucketColumn, TemplateValueColumn, and ApprovalRulesColumn.


-   **[Download TypeScript definitions for script includes used in JavaScript modules](https://www.servicenow.com/docs/access?context=download-script-dependencies&family=zurich&ft:locale=en-US)**

Download TypeScript definitions for script includes imported in JavaScript modules from an instance using the `now-sdk dependencies` command.

-   **[Apply a template to an existing application](https://www.servicenow.com/docs/access?context=now-sdk-create-command&family=zurich&ft:locale=en-US)**

Add template files and directories for development in ServiceNow Fluent using the `--template` parameter with the `now-sdk init` command in an existing application.


-   **[Automated Test Framework API supports additional test steps](https://www.servicenow.com/docs/access?context=atf-test-now-ts&family=zurich&ft:locale=en-US)**

Use the following test steps with the ServiceNow Fluent Automated Test Framework API.

    -   atf.form.addAttachmentsToForm
    -   atf.form\_SP.addAttachmentsToForm
    -   atf.server.addAttachmentsToExistingRecord
    -   atf.server.runServerSideScript
    -   atf.server.setOutputVariables
-   **[Build command doesn't package build artifacts](https://www.servicenow.com/docs/access?context=servicenow-sdk-cli-commands&family=zurich&ft:locale=en-US)**

Use the `now-sdk pack` or `now-sdk install` commands to package build artifacts. The `now-sdk build` command compiles the source files but doesn't package the build artifacts.


</td></tr><tr><td>

Australia

</td><td>

-   **[Flow API supports Service Catalog triggers and actions](https://www.servicenow.com/docs/access?context=fluent-flow-api&family=australia&ft:locale=en-US)**

Use triggers and actions related to Service Catalog with the Flow API.

-   **[Access Control List API supports protection policies](https://www.servicenow.com/docs/access?context=acl-api-now-ts&family=australia&ft:locale=en-US)**

Control whether someone can view or edit an access control list \(ACL\) with the protectionPolicy property in an ACL object.

-   **[Keys updated for static assets in full-stack applications](https://www.servicenow.com/docs/access?context=building-applications-source-code&family=australia&ft:locale=en-US)**

Static UX Assets \[sys\_ux\_lib\_asset\] in full-stack applications have updated keys in the `keys.ts` file. UX Asset sys\_ids aren’t changed.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow SDK features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   The `now-sdk upgrade` command has been removed. To upgrade the version of the ServiceNow SDK, see [Upgrade the ServiceNow SDK](https://www.servicenow.com/docs/access?context=upgrade-servicenow-sdk&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ServiceNow SDK features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   The $id property is deprecated in the List API and Role API.
-   Property names that use snake case are deprecated in all ServiceNow Fluent APIs. Use the equivalent property name in camel case instead.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

The ServiceNow SDK is available as a Node Package Manager \(npm\) package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see [Install the ServiceNow SDK](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

The ServiceNow SDK is available as a Node Package Manager \(npm\) package from the [public npm registry](https://www.npmjs.com/package/@servicenow/sdk) and installed locally. For information about installing the ServiceNow SDK, see [Install the ServiceNow SDK](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow SDK we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

You must have Node.js and Node Package Manager \(npm\) installed to install the ServiceNow SDK. For more information, see [Install the ServiceNow SDK](https://www.servicenow.com/docs/access?context=install-servicenow-sdk&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow SDK we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

-   Develop a user interface \(UI\) with React to build a full-stack application in source code.
-   Define flows, service catalogs, UI pages and more in source code with ServiceNow Fluent APIs.

 See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Create or convert applications in the global scope with instances on the Australia release.

 See [ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

