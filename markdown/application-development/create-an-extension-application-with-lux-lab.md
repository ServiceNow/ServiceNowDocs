---
title: Create an extension application with Lux Lab
description: Lux Lab's VS Code extension scaffolds, builds, and deploys an extension application through a guided UI. An extension application adds pages to an existing ServiceNow experience; it doesn't create a standalone experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/create-an-extension-application-with-lux-lab.html
release: zurich
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 5
keywords: [Create an extension application with Lux Lab, Prerequisites, Create the extension application, Create a new page in the extension application, Extend an existing host page, Add an extension page to host navigation, Add a page to L1 navigation, Add a page to L3 navigation, Wire up and verify the navigation item, Build and deploy the extension application]
breadcrumb: [Extend experiences, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Create an extension application with Lux Lab

Lux Lab's VS Code extension scaffolds, builds, and deploys an extension application through a guided UI. An extension application adds pages to an existing ServiceNow experience; it doesn't create a standalone experience.

## Before you begin

-   Role required: admin
-   Complete the Environment Check.
-   Connect to the ServiceNow instance that contains the experience you want to extend.

## About this task

As an alternative to the CLI walkthrough in [Extend existing ServiceNow experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/extend-existing-servicenow-experiences.md), the guided UI keeps extension pages under the same path convention the CLI uses:

```
src/extensions/<parentScope>/<parentRouteId>/pages/<page-slug>/page.js
```

## Procedure

1.  Create the extension application

    1.  Open the **Lux Lab** Activity Bar view, then open **Script Runner**.

    2.  Select **Create LUX Project**, or run `Lux: Create LUX Project` from the VS Code Command Palette.

    3.  Select the ServiceNow instance that contains the host experience, if it isn't listed, add it first.

    4.  Select the parent folder, then enter the application name and project folder name.

    5.  Select **Extend Existing App**.

    6.  Select the host experience to extend, then confirm the scope name or scope suffix.

    7.  If prompted, choose **Add to Current Workspace** or **Open in New Workspace**.

        Wait for scaffolding and dependency installation to finish.

    8.  Lux Lab opens the generated extension project.

    If the host experience can't be loaded, verify that the selected instance is active and that your credentials can read the available experiences. The host experience must have a valid scope and URL suffix before you can use it.

2.  Create a new page in the extension application

    Use this flow when the extension application needs a page that doesn't already exist in the host experience.

    1.  Open the extension project in VS Code.

    2.  Run `Lux: Create Page` from the Script Runner or the Command Palette.

    3.  Select **New Page**.

    4.  If the project extends more than one host application, select the host application for the new page.

        Lux Lab selects it automatically if it extends only one.

    5.  Enter the page name or title.

    6.  Enter the page route.

        The route is prefilled from the page name and must use lowercase letters, numbers, and hyphens. Lux Lab blocks duplicate routes within the selected host application.

    7.  Confirm the prompts.

        Lux Lab creates and opens `src/extensions/<parentScope>/<parentRouteId>/pages/<page-slug>/page.js`.

    8.  Implement the page in the generated `page.js` file.

    9.  Preview the extension application and verify the page against the host experience.

3.  Extend an existing host page

    Use this flow when the extension application should add an override or extension for a page that already exists in the host experience.

    1.  Open the extension project in VS Code.

    2.  Run `Lux: Create Page` from the Script Runner or the Command Palette.

    3.  Select **Extend from Existing Page**.

    4.  If the project extends more than one host application, select the host application.

    5.  Select the host page from the list loaded from the active ServiceNow instance.

        Use **Refresh** in the picker if the page was recently added or changed on the instance.

    6.  Pages already scaffolded in the extension project appear as already added and can't be selected again.

    7.  Lux Lab derives the extension page route from the selected host page and creates `src/extensions/<parentScope>/<parentRouteId>/pages/<page-slug>/page.js`.

    8.  Update the generated `page.js` while preserving the host page's route contract.

    9.  Preview the extension application and compare the result with the original host page.

    Create only one extension for a given host page unless you intentionally need multiple extension projects. Verify the host experience and page before deploying.

4.  Add an extension page to host navigation

    Creating an extension page doesn't automatically add it to the host navigation. Configure the host-level lifecycle module at:

    ```
    src/extensions/<parentScope>/<parentRouteId>/application.js
    ```

    For example, in an extension project that targets the `example-app` host, the file may be `src/extensions/x_aix_example_a/example-app/application.js`.

    1.  Add a page to L1 navigation

        Use `addNavItem` in `application.js`, setting `action.path` to the route created for the extension page:

        ```
        addNavItem({
          icon: 'document',
          title: i18n.getMessage('Reports'),
          action: {type: 'navigate', path: '/reports'},
        });
        ```

    2.  Add a page to L3 navigation

        Use `setL3Nav` to set the nested \(L3\) tabs for an existing navigation item; the first argument is the parent navigation path:

        ```
        setL3Nav('/reports', [
          {label: 'Overview', path: '/reports/overview'},
          {label: 'Details', path: '/reports/details'},
        ]);
        ```

        To add tabs without replacing existing tabs, use `appendL3Nav` instead. Import the navigation helper you use from `@servicenow/aiux-components-nav`, then save `application.js`.

    3.  Wire up and verify the navigation item

        1.  Use the page route created in the new-page flow, or preserve the host route when extending an existing page.
        2.  Add the corresponding L1 or L3 navigation configuration in the host-level `application.js`.
        3.  Preview the extension application and verify that the page opens from the expected navigation item.
        4.  Build and deploy the extension application.
        5.  Run `Lux: Refresh Instance Explorer` and verify the navigation on the target instance.
5.  Build and deploy the extension application

    1.  Save the generated page and all related files.

    2.  Use the project's preview action in Script Runner to test the extension page.

    3.  Run `Lux: Build` from Script Runner and resolve any build errors.

    4.  Confirm that the correct ServiceNow instance is active.

    5.  Run `Lux: Deploy` to deploy to the active ServiceNow instance.

    6.  Use `Lux: Show Command Output` to monitor the deployment.

    7.  Run `Lux: Refresh Instance Explorer` and verify the extension application and page on the target instance.

    Navigation visibility depends on the host experience configuration, user access, route metadata, and the active ServiceNow instance.


## What to do next

For the decorators, ordering, and record-level mechanics behind what this flow generates, see [https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/supported-extension-points.md](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/supported-extension-points.md). The guided flow does not expose decorators, layout contribution, or per-host lifecycle modules; use the CLI path in [Extend existing ServiceNow experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/extend-existing-servicenow-experiences.md) for those.

