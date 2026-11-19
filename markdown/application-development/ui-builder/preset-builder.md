---
title: Create custom presets for components
description: Create presets to save time and make your component configurations reusable across different experiences.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/preset-builder.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create custom presets for components

Create presets to save time and make your component configurations reusable across different experiences.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select **Create**.

3.  Select **Preset**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to track your preset internally.|
    |Component|Select the component you want to create a preset for.|
    |Controller|Select the controller with data and logic to power the preset.|
    |Description|Short description to help find your preset. Write a description that helps page builders understand what content is included in the preset.|

5.  Select **Create**.

    The preset building window opens.

    \[Omitted image "preset-builder-window.png"\] Alt text: Preset building window with no data added.

6.  Enter controller test values to preview data in the component preset.

7.  Configure the component properties you want to apply with the preset.

8.  Bind data from the controller to the component preset by dragging items from the data preview section to the fields in the configure panel.

    \[Omitted image "preset-builder-configured.png"\] Alt text: Configuration panel for component preset

9.  Add events to the component.

    For more information, see [Configure an event handler manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/event-handler.md).

10. Select **Save**.


## What to do next

Apply the preset you just created by [selecting a preset in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/presets.md).

**Parent Topic:**[Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-components.md)

