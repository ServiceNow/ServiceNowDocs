---
title: Record Tags component setup
description: The Record Tags component enables you to add tags to records to categorize and organize records.Properties in the Record Tags component have preset configuration values. You can accept these values or override them manually.The Record Tags component doesn't have configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/record-tags-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Record Tags component setup

The Record Tags component enables you to add tags to records to categorize and organize records.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Record Tags that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "record-tags-content-tree.png"\] Alt text: Record Tags content tree.

2.  Select the Record Tags component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Record Tags label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "record-tags-presets.png"\] Alt text: Shows the list of presets in UI Builder for the Record Tags component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a preset for a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "record-tags-preset-config.png"\] Alt text: Shows the panel for connecting the preset with the required controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Record Tags component properties

Properties in the Record Tags component have preset configuration values. You can accept these values or override them manually.

Presets are designed to suit a specific use case. However, you can override a property that has a preset value with a custom configuration, if you find it necessary for your design. For details on overriding and resetting presets, see [Override a preset for a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record tags__**

    This preset allows tagging of a record to assist in organizing, searching and categorizing records. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   Table
    -   Sys ID
    -   recordTags

### Properties

<table id="table_lrn_3bb_knb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

Table of the record the tag applies to.

</td></tr><tr><td>

Sys IDsysId\]

</td><td>

Sys ID of record the tag applies to.

</td></tr><tr><td>

recordTags\[recordTags\]

</td><td>

Tags to load into the component.

</td></tr></tbody>
</table>## Record tags component events

The Record Tags component doesn't have configurable events.

