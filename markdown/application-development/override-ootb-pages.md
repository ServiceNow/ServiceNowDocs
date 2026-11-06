---
title: Override a base system page with an extension project
description: Replace a page in a base system experience with your own version of it. You maintain only the page you change, without taking ownership of the entire application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/override-ootb-pages.html
release: australia
topic_type: task
last_updated: "2026-10-29"
reading_time_minutes: 4
keywords: [Override a base system page with an extension project, Prerequisites, Steps, Ownership and upgrade considerations, Common override issues]
breadcrumb: [Use, ServiceNow Lux Lab for VS Code extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Override a base system page with an extension project

Replace a page in a base system experience with your own version of it. You maintain only the page you change, without taking ownership of the entire application.

## About this task

To customize a ServiceNow® base system experience, use an extension project instead of editing the original application. An extension project adds your own page for an existing route, and the original ServiceNow® source stays intact and upgrade-safe.

## Before you begin

Role required: admin

-   You have access to the instance that contains the base system experience you want to extend.
-   You can create and deploy an extension project.
-   You know which application, experience, or route you want to override.
-   You have the required roles and permissions to view source artifact records and download attached source files.

## Procedure

1.  Create an extension project.

    1.  Start a new extension project in your own scope.

        Keeping the project in your own scope keeps your changes separate from the ServiceNow® application.

        \[Omitted image "create-project-extend-existing-app.png"\] Alt text: Project template picker with Extend Existing App selected.

    2.  During project setup, select the application that contains the base system experience you want to extend.

        \[Omitted image "select-parent-application.png"\] Alt text: Application picker filtered to the parent application to extend.

    3.  In the project's extensions folder, create a folder structure that matches the parent scope and route you're overriding.

        `<parent_scope_name>/<baseURL>/pages/…`

        \[Omitted image "extensions-folder-scope-route.png"\] Alt text: Extensions folder organized by parent scope name and route.

        Alternatively, name the folder with the experience record's sys\_id, for example `src/extensions/<experienceSysId>/pages/…`.

        \[Omitted image "extensions-folder-experience-sysid.png"\] Alt text: Extensions folder organized by experience sys\_id

        Pages shared across scopes are created outside the experience's scope, so extending them through the scope may not work as expected. For these pages, update the folder structure after you create the project to use the experience's sys\_id in place of the scope and basename.

2.  Locate the source package.

    1.  Open the `sn_glider_source_artifact_m2m_list` table on your instance.

    2.  Search for the application or experience you want to extend.

    3.  Open the matching source artifact relationship record.

    4.  From the source artifact record, locate the attached source ZIP.

        \[Omitted image "source-artifact-list.png"\] Alt text: Application File to Source Artifacts list with the source artifact link highlighted.

    The source package contains the files used to build the base system experience. Use this source as the starting point for your override, so you keep the same structure and change only what your use case requires.

    **Warning:** Internal ServiceNow® library dependencies and imports aren't available to your extension project. If the page uses them, the build fails.

3.  Review the source package.

    1.  Download the attached source ZIP from the source artifact record.

    2.  Unzip the package locally.

    3.  Review the package's folder structure.

    4.  Identify the page file that corresponds to the route you want to override.

    5.  Before you copy the page into your extension project, confirm whether it depends on shared files, widgets, or libraries.

4.  Copy the page into your extension project.

    1.  Copy the page file from the unzipped source package into the matching folder under your extension project.

        Place it under the `extensions/<parent_scope_name>/<parent_route>/pages/` path, so Lux can resolve it as the override for the existing route.

    2.  Update only the parts of the page that your use case requires.

        Avoid changing unrelated logic or structure unless the override requires it.

5.  Test the override on your instance.

    1.  Build the extension project.

    2.  Deploy the extension project to your target instance.

    3.  Navigate to the route you overrode.

    4.  Confirm that your custom page is displayed.

    5.  Confirm that users with the expected roles can access the page.

    6.  Confirm that the original base system experience remains available when the extension is removed or turned off.


## Ownership and upgrade considerations

-   Keep the base application intact. Don't edit the base system page directly. Create an override in your extension project instead.
-   Own only what you change. You maintain the copied page, and the original ServiceNow-delivered experience can continue to receive updates.
-   Review dependencies carefully. If the source uses internal ServiceNow libraries that aren't exposed through public packages, the override may not build or run as expected.
-   Test after upgrades. Because you own the copied page, validate it after upgrades to confirm that it still works with the latest platform and Lux updates.

## Common override issues

The following table lists common issues and what to check for each one.

|Issue|What to check|
|-----|-------------|
|The source ZIP isn't available.|Confirm that the application ships source on the instance and that you have permission to view and download the source artifact.|
|The project fails to build.|Check for missing dependencies, unsupported internal libraries, or imports that aren't available to customer extension projects.|
|The override doesn't appear at runtime.|Confirm that the folder path matches the parent scope, basename, and route. Then rebuild and redeploy the extension project.|
|Access behaves differently than expected.|Review page, widget, and experience access controls to confirm that the intended users can view the override.|

