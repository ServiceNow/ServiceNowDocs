---
title: Predicate Builder component setup
description: The Predicate Builder enables users to visually assemble filter conditions. Set the appearance of your predicate builder and the information it displays.Properties in the Predicate Builder component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/predicate-builder-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Predicate Builder component setup

The Predicate Builder enables users to visually assemble filter conditions. Set the appearance of your predicate builder and the information it displays.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Predicate Builder that differentiates it from other components in the content tree.

    \[Omitted image "predicate-builder-content-tree.png"\] Alt text: Predicate Builder in content tree

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the  component using one of these methods:

    -   Click anywhere within the component.
    -   Select the Action bar label you created for your component in the content tree.
    \[Omitted image "predicate-builder-presets.png"\] Alt text: Predicate Builder presetsThe preset selection panel appears in the pane on the right.

3.  Either select **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    \[Omitted image "predicate-builder-controller.png"\] Alt text: Predicate Builder controller configuration

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Predicate Builder component properties

Properties in the Predicate Builder component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Condition builder__**

    This preset allows users to construct a query for a ServiceNow table. This preset requires the **Predicate Builder Controller** controller.

    Properties included in this preset are:

    -   Display
        -   Read Only
        -   Show Sort By
        -   Show Group By
        -   Show Related List Conditions
        -   Selected Tab
        -   Show Saved Filter Sets
        -   Show Save Filter
        -   Show Reference Lookup
        -   Show Add Condition Set
        -   Max Content Height
        -   Show Field Labels
    -   Condition builder selected as Builder Type
        -   Field Operator Relationship
        -   Decoded Query
        -   Panel Definitions
        -   Metadata Cache
        -   Variable Source
    -   Predicate builder selected as Builder Type
        -   Predicate Composition
        -   Grouped Predicate Config
        -   Custom Components
        -   Macroponent SysId
        -   Component Tag

### Properties

<table id="table-uib-props"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type\[builderType\]

</td><td>

Select Condition Builder for creating table queries for use with ServiceNow data or the Predicate Builder for agnostic conditions.Default: **CONDITION\_BUILDER\_TYPE**

Choices:

-   Condition builder

\[CONDITION\_BUILDER\_TYPE\]

-   Predicate builder

\[PREDICATE\_BUILDER\_TYPE\]


</td></tr></tbody>
</table><table id="table_mc5_jxf_yfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source\[source\]

</td><td>

Source for where the data comes from for condition builder. Typically this will be a table name.

</td></tr></tbody>
</table><table id="table_pny_sxf_yfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Basic Filters\[basicFilters\]

</td><td>

Enable basic filters view.Default: **false**

</td></tr><tr><td>

Read Only\[readOnly\]

</td><td>

Prevents users from modifying the filter conditions.Default: **false**

</td></tr><tr><td>

Show Sort By\[showSortBy\]

</td><td>

Allow users to include a sort option when creating a filter.Default: **true**

</td></tr><tr><td>

Show Group By\[showGroupBy\]

</td><td>

Allow users to include a group by option when creating a filter.Default: **true**

</td></tr><tr><td>

Show Related List Conditions\[showRelatedListConditions\]

</td><td>

Allow users to include conditions for a related list in the filter.Default: **true**

</td></tr><tr><td>

Selected Tab\[selectedTab\]

</td><td>

Set the tab to be selected.Default: **condition**

Choices:

-   Conditions

condition

-   Sort by

sort-by

-   Related list conditions

related-list


</td></tr><tr><td>

Show Saved Filter Sets\[showLoadFilter\]

</td><td>

Allow users to access saved filter sets in the saved filters drop down.Default: **true**

</td></tr><tr><td>

Show Save Filter\[showSaveFilter\]

</td><td>

Show the save filter UI to allow users to save filters.Default: **true**

</td></tr><tr><td>

Show Reference Lookup\[showReferenceLookup\]

</td><td>

Show the magnifying glass next to reference or variable type fields to allow users to open a reference list.Default: **true**

</td></tr><tr><td>

Show Add Condition Set\[showAddConditionSet\]

</td><td>

Show the **Add condition set** button to allow users to create comparative conditions.Default: **true**

</td></tr><tr><td>

Max Content Height\[maxContentHeight\]

</td><td>

Max height of the content area.

</td></tr><tr><td>

Show Field Labels\[displayLabelOptions\]

</td><td>

Show labels above fields in the condition builder.

</td></tr></tbody>
</table><table id="table_bby_kgh_p2c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Focus on Render\[focusOnRender\]

</td><td>

Takes keyboard focus on renderDefault: **false**

</td></tr><tr><td>

Field Operator Relationship\[fieldOperatorRelationship\]

</td><td>

Configuration to allow for customization of the operators that appear in condition builder.

</td></tr><tr><td>

Customizations\[customizations\]

</td><td>

Enable configuration on the field and row level.

</td></tr><tr><td>

Decoded Query\[decodedQuery\]

</td><td>

Predicate builder representation of the encoded query model.

</td></tr><tr><td>

Fixed Decoded Query\[fixedDecodedQuery\]

</td><td>

A JSON data model that defines the fixed query conditions for Predicate Builder.**Note:** These conditions are unmodifiable.

</td></tr><tr><td>

Fixed Query Mode\[fixedQueryMode\]

</td><td>

Switch between simple or distributed mode for handling fixed queries.Choices:

-   Simple
-   Distributed

Default: **Simple**

</td></tr><tr><td>

Info Messages\[infoMessages\]

</td><td>

Array of messages to be displayed.

</td></tr><tr><td>

Panel Definitions\[panelDefinitions\]

</td><td>

Data used to display dot walk panels.

</td></tr><tr><td>

Metadata Cache\[metadataCache\]

</td><td>

Shared cache stored in the predicate context.

</td></tr><tr><td>

Variable Source\[variablesSource\]

</td><td>

Configuration to limit the variables that show based on the selected catalog item or variable set.

</td></tr></tbody>
</table><table id="table_a4h_4fh_p2c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Predicate Composition\[predicateComposition\]

</td><td>

Predicate composition data model.

</td></tr><tr><td>

Grouped Predicate Config\[groupedPredicateConfig\]

</td><td>

Grouped predicate config to customize the grouping styling.

</td></tr><tr><td>

Custom Components\[customComponents\]

</td><td>

Used to define any custom components or macroponents which will be prefetched on predicate builder load.

</td></tr><tr><td>

Macroponent SysId\[macroponentSysId\]

</td><td>

Macroponent SysId for custom row rendering that takes precedence over Component Tag.

</td></tr><tr><td>

Component Tag\[componentTag\]

</td><td>

Component Tag for custom row rendering.

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Predicate Builder component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

\[Omitted image "predicate-builder-events-list.png"\] Alt text: Predicate Builder events list

The Events tab shows the events used by the Predicate Builder component. Events with presets are marked with the **Preset** badge. To show events that do not have preset configurations, select **+ Add event mapping**. If the component has only one event and that event does not have a preset, the event is displayed and is ready for configuration.

### Event handlers

\[Omitted image "predicate-builder-event-handlers.png"\] Alt text: Predicate Builders event handlersEvent handlers work with data resources to link the Predicate Builder actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Condition builder__**

    This preset provides data handlers for these events:

    -   Predicate Builder Decoded Query Updated
    -   Predicate Builder Metadata Request
    -   Predicate Builder Panel Definitions Fetch

### Event descriptions

<table id="table_zrn_yd5_m2c"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Predicate Builder Decoded Query Updated\[NOW\_PREDICATE\_BUILDER\#DECODED\_QUERY\_UPDATED\]

</td><td>

An event denoting that the condition builder decoded query has updated.

</td></tr><tr><td>

Predicate Builder Metadata Request\[NOW\_PREDICATE\_BUILDER\#FETCH\_METADATA\]

</td><td>

An event that contains information for the parent to fetch and pass into the metadataCache prop.

</td></tr><tr><td>

Predicate Builder Panel Definitions Fetch\[NOW\_PREDICATE\_BUILDER\#FETCH\_PANEL\_DEFINITIONS\]

</td><td>

Used by Condition Builder to populate dot-walk.

</td></tr></tbody>
</table>