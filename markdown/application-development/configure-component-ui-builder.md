---
title: Configure a component for UI Builder
description: Add a uiBuilder block to a component's now-ui.json file so that the component appears in the UI Builder toolbox on a workspace landing page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/configure-component-ui-builder.html
release: australia
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 1
breadcrumb: [Configure, UI component CLI extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Configure a component for UI Builder

Add a uiBuilder block to a component's now-ui.json file so that the component appears in the UI Builder toolbox on a workspace landing page.

## Before you begin

-   The ui-component extension must be installed. See [Install the UI component CLI extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/install-ui-component-cli-extension.md).
-   The Next Experience UI component project must exist.

Role required: admin

## About this task

The uiBuilder block controls how the component appears in the UI Builder toolbox. The block is stored in the now-ui.json file, at the root of the project. For the full list of uiBuilder properties, see the component configuration properties reference. For more information about UI Builder, see the [UI Builder overview](https://www.servicenow.com/docs/bundle/yokohama-application-development/page/administer/ui-builder/concept/ui-builder-overview.html).

## Procedure

1.  Open the now-ui.json file at the root of the project.

2.  Add a uiBuilder block to the object for your component under the components property.

    ```
    {
                            "components": {
                            "mycompany-stock-tracker": {
                            "uiBuilder": {
                            "associatedTypes": ["global.core", "global.landing-page"],
                            "label": "My Stock Tracker",
                            "icon": "chart-forecast-fill",
                            "description": "Stock Tracking component",
                            "internalComponent": false,
                            "category": "Stocks",
                            "searchFacets": ["global.stocks:global.tracking"]
                            }
                            }
                            }
                            }
    ```

3.  Set the associatedTypes values that match where the component appears in the toolbox.

    -   `global.layout` for layout components, such as containers.
    -   `global.visualization` for components that visualize data, such as reports or lists.
    -   `global.core` for base components that apply in all contexts, such as Design System components.
    UI Builder currently supports customizing Configurable Workspace landing pages only.

4.  Save the now-ui.json file.

5.  Deploy the component to the instance by running the following command:

    ```
    snc ui-component deploy
    ```

6.  Log in to the instance that you deployed the component to.

7.  Open your workspace landing page in UI Builder.

8.  Select **Add Component**.

    The toolbox displays the component by its label, such as **My Stock Tracker**.

9.  Drag the component onto the landing page.


## Result

The component appears on the workspace landing page.

