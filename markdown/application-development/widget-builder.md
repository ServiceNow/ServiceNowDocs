---
title: Widget Builder
description: Widget Builder is where you create, edit, and preview Lux widgets without leaving the browser.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/widget-builder.html
release: zurich
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [Widget Builder, Widgets catalog, Editor, Build Service]
breadcrumb: [Lux Widgets, Build with Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Widget Builder

Widget Builder is where you create, edit, and preview Lux widgets without leaving the browser.

## Widgets catalog

The Widgets catalog lists every widget on the instance, except internal widgets.

-   Use the search box to filter widgets by name.
-   Select **Create widget** to open a new widget in the Editor.
-   Select a widget's action menu for **Edit**, **Clone**, or **Delete**.

Use the scope picker in the header to choose which application scope a widget you create lands in.

A widget included with the base system, or one from a store app rather than created by you, shows a locked state. Trying to edit or delete it is blocked. For details, see [Customize a base system widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/customize-a-base-system-widget.md).

## Editor

Selecting or creating a widget opens the Editor, a three-panel workspace, at `/aiux/builder/edit/widget/-1` for a new widget, or `/aiux/builder/edit/widget/{widget_sys_id}` for an existing one.

-   **Chat panel**

    Describe what to build or change in natural language. Collapsible and resizable.

-   **Widget editor**

    Tabs for **Preview**, **Component**, and **Script**. This is where you read and write the widget's code and see it rendered live.

-   **Property panel**

    **Widget Properties** and **Preview Props** modes. Collapsible and resizable.


See [Create a widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-a-widget.md) and [Widget editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/widget-editor.md) for what to do in each panel.

\[Omitted image "aiux-builder-editor-overview.png"\] Alt text: Editor showing the chat, widget editor, and property panels

## Build Service

Selecting Save or Publish hands the widget to the Build Service, an in-browser build tool powered by `now-sdk`. The Build Service compiles the widget to publish and deploy it to your instance.

**Note:** The first time you open the Editor, Widget Builder sets up the Build Service. A modal shows progress while this completes, it can take a few minutes.

\[Omitted image "aiux-builder-build-service-setup.png"\] Alt text: Build Service setup progress modal

