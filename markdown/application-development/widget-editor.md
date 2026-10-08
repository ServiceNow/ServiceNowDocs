---
title: Widget editor
description: The widget editor is a three-panel workspace for building and previewing a widget. It has a code editor for the component and server script, a live preview, and a panel for widget properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/widget-editor.html
release: brazil
topic_type: concept
last_updated: "2026-10-01"
reading_time_minutes: 2
keywords: [Widget editor, Component and Script tabs, Complex widgets with additional files, Preview tab, Property panel, Save, Publish, and Build, Build Service]
breadcrumb: [Lux Widgets, Build with Lux, Lux Development, Building pro-code applications, Developing your application, Building applications]
---

# Widget editor

The widget editor is a three-panel workspace for building and previewing a widget. It has a code editor for the component and server script, a live preview, and a panel for widget properties.

## Component and Script tabs

Both tabs are code editors with syntax highlighting and autocomplete for the widget component code and its server script. The server script is written as `export default function server(data, options, input) {...}`, with `GlideRecordSecure`, `GlideQuery`, and `gs` available — use `GlideRecordSecure` rather than `GlideRecord` so queries respect ACLs. Call `this.server.get(input)`, `.update()`, or `.refresh()` from the component to run it.

\[Omitted image "aiux-builder-editor-overview.png"\] Alt text: Component tab with syntax highlighting and autocomplete

## Complex widgets with additional files

Widget Builder only edits the widget's component \(`index.js`\) and server script \(`server.js`\). A complex widget that has relative imports to other utility files isn't fully editable here, those additional files aren't shown in the **Component** or **Script** tabs.

**Important:** If a widget imports from files other than its own component and server script, use the [Lux Lab VS Code extension](https://marketplace.visualstudio.com/items?itemName=ServiceNow.now-vscode-extension-ainpx-lab) instead.

\[Omitted image "aiux-builder-complex-widget-vscode.png"\] Alt text: Complex widget with additional utility files, opened in the Lux Lab VS Code extension

## Preview tab

The **Preview** tab renders the widget live, in a resizable and zoomable viewport:

-   Drag the handles on the left, right, bottom, or corner to resize the preview.
-   Use the zoom controls in the bottom-right corner, or hold Ctrl/Cmd and scroll, to zoom in and out. The zoom controls reflow the layout rather than just scaling it visually.
-   Select **Refresh** to reload the preview from the latest build, bypassing the short cache Widget Builder keeps when you switch tabs.

If the preview can't load, it shows the specific problem, such as a missing dependency, a timeout, an import failure, or a registration error with a **Retry** button. A widget that hasn't been built yet shows "Preview not available yet — Click Build to compile" instead of an error.

\[Omitted image "aiux-builder-preview.png"\] Alt text: Preview tab with resize handles and zoom controls

## Property panel

The property panel on the right has two modes:

-   **__Widget Properties__**

    A form for the widget's metadata: name, ID, description, category, and similar fields.

-   **__Preview Props__**

    Inject property values into the running preview to see how the widget behaves with different inputs, without changing the widget's saved defaults.


\[Omitted image "aiux-builder-property-panel.png"\] Alt text: Property panel in Widget Properties mode

\[Omitted image "aiux-builder-preview-props.png"\] Alt text: Property panel in Preview Props mode

## Save, Publish, and Build

-   **__Save__**

    Builds the widget without deploying it. The preview updates right away, so you can iterate quickly. If a build fails, your edits aren't lost — Widget Builder saves a draft and shows the build error. Fix the issue and save or publish again.

-   **__Publish__**

    Builds and deploys the widget to the instance. A new or cloned widget's first publish shows "Widget created and published"; later publishes show "Widget published". If publishing fails after a successful build, Widget Builder shows the error.


