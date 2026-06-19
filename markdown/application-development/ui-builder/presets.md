---
title: Automatically configure components using presets
description: Use component presets to automatically configure components on compatible pages.Choose a component preset when adding a component to your page.Override a component preset to enter your own custom values.Reset component presets to their default values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/presets.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Automatically configure components using presets

Use component presets to automatically configure components on compatible pages.

Use component presets to apply predefined configuration values and event mappings to components. UI Builder page templates contain [controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/ui-builder-glossary.md) that presets use to define component configuration values.

Presets apply pre-built configurations to component properties and event handlers and are only available for certain components. They are based on common use cases for components, such as configuring a **Form** component with fields that are typically included on a record page.

Applying a preset automatically configures components to work immediately, simplifying page creation and maintenance for page authors.

Presets offer the following benefits to page authors:

-   Handling of complex data and event binding for components
-   Reduced cost of ownership and maintenance due to being defined external to pages

From the Configuration pane, you can select whether to apply a preset to the selected component or instead manually configure it. Default presets are automatically applied for components when a page is created from a template or the controller required for the preset is already added to the page. Any properties or events configured by the preset display as read-only when a preset is applied.

You can override values configured by a preset but in doing so you assume ownership of the component configuration and maintenance.

Sub-pages do not inherit controllers and are not able to use presets in Australia.

\[Omitted image "preset-list-example.png"\] Alt text: Heading component properties configured by a preset.

## Data and event bindings

Presets can include bindings to:

-   Controller output properties \(@data\)
-   Event payloads \(@payload\)
-   Session context \(@context.session\)
-   Complex formulas \(client transforms\)

Presets can also include event mappings to a controller's handled events. For more information, see [Manage actions in UI Builder pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-events.md).

## Controllers

Presets connect components to data and event mappings using a controller. If the controller required by a preset is not already on the page, the preset prompts you to configure the controller's required properties and adds the controller. After a controller is added to a page, components that have presets associated with the controller appear highlighted in the components list. For more information, see [Bind data to UI Builder pages using controllers \(advanced feature\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/controllers.md).

\[Omitted image "presets-highlighted-components.png"\] Alt text: Components tab showing components with preset label highlighted.

Check the **Presets available** box to view components with presets in the toolbox.

**Parent Topic:**[Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-components.md)

## Select a component preset

Choose a component preset when adding a component to your page.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md).

4.  Open the toolbox.

5.  Select the **Presets available** box.

6.  Select the component you want to add to your page.

    \[Omitted image "preset-component-library.png"\] Alt text: Open toolbox showing components with presets.

7.  The component automatically configures with the default preset.

    \[Omitted image "preset-default-selection.png"\] Alt text: The default component preset displays in the preset drop-down.

8.  Select a different preset from the list in the configuration panel.

    You can configure a component not to use a preset by selecting **Remove current preset**.

    1.  Select a new component preset in the configuration panel.

    2.  Select **Apply** to replace the existing preset.

    \[Omitted image "preset-select-none.png"\] Alt text: Select a different preset or no preset from the list.

9.  Click **Save**.


## Override a component preset

Override a component preset to enter your own custom values.

### Before you begin

Role required: admin

### Procedure

1.  Select a component with a preset.

    \[Omitted image "preset-select-component.png"\] Alt text: Select the component you want to override in the content tree.

2.  Find the data value that you want to override in the configuration panel.

3.  Click the lock icon in the data field.

4.  Enter the data value that you want to override the preset value.

5.  Select **Save**.

    \[Omitted image "preset-select-value-custom.gif"\] Alt text: Override preset component values with custom values.


### Result

The configuration panel displays the custom value in the field.

## Reset a component

Reset component presets to their default values.

### Before you begin

Role required: admin

### Procedure

1.  Select the component that you want to reset in the content tree.

    \[Omitted image "preset-component-custom.png"\] Alt text: Select the component you want to override in the content tree.

2.  Select the component name in the configuration panel.

    \[Omitted image "reset-component-config.png"\] Alt text: Component name in the configuration panel.

3.  Click **Reset component**.

    \[Omitted image "reset-component-link.png"\] Alt text: Reset component values with the reset component option.

4.  Click **Reset**.


### Result

The component preset resets to the default values.

