---
title: Roadmap component setup
description: The Roadmap component enables planning personas like Product Manager, Portfolio Manager, and others, to create roadmaps and track them.Configure the behavior and personalization settings of your Roadmap component with these properties.Select event handlers to configure the actions \(events\) provided with the Roadmap component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/roadmap-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 12
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Roadmap component setup

The Roadmap component enables planning personas like Product Manager, Portfolio Manager, and others, to create roadmaps and track them.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Roadmap that differentiates it from other components in the [content tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-tutorial.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "roadmap-component-content-tree.png"\] Alt text: Roadmap component in the content tree.

2.  Select the Roadmap component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Roadmap label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Roadmap component properties

Configure the behavior and personalization settings of your Roadmap component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

### Configuration sections

Roadmap configuration is divided into six sections to make it easier for the users to find configuration based on the usage group. Some properties are dynamically shown or hidden based on the other properties to guide you through the setup process.

-   Core: Core configuration for the roadmap such as items to roadmap, items metadata, locale, start date and end date and so on.
-   Header: Header configuration for the roadmap such as show header, header title and so on.
-   Contextual sidebar: Contextual sidebar configuration for the roadmap.
-   Timeline: Timeline configuration for the roadmap, such as custom calendar data and default timescale.
-   Dependencies: Configuration of the dependency feature for the roadmap such as dependencies, and dependencies metadata.
-   Milestones: Milestone configuration for the roadmap such as Roadmap and roadmap item milestones and milestone metadata.

<table id="table_xv1_ff1_hxb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roadmap Items

</td><td>

roadmapItems

</td><td>

Array of roadmap items. These are the items from the source table for which the roadmap is defined. For example, project, demand, or others.

 It’s an object with the following attributes:

-   `id`: Unique system-generated identifier of the roadmap item.
-   `name`: Name of the roadmap item; displayed on the timeline bar.
-   `startDate`: Start date of the roadmap item in the format of the dateFormat property.
-   `endDate`: End date of the roadmap item in the format of the dateFormat property.
-   `avatar`: Avatar of the assignee of the roadmap item, displayed on the roadmap item bar.

 Default value: `[]`

</td></tr><tr><td>

Roadmap item metadata

</td><td>

roadmapItemMetadata

</td><td>

Metadata of roadmap item fields to plot the roadmap timeline. It’s an object with the following attributes.

-   `startDateField`: The name and label of the field used for the start date.
-   `endDateField`: The name and label of the field used for the end date.
-   `itemNameField`: The name and label of the field used for the roadmap item name.
-   `itemOwnerField`: The name and label of the field used for the roadmap item owner.
-   `percentCompleteField`: The name and label of the field used to show progress on the roadmap bars.
-   `statusField`: The name and label of the field used to show status pill on the roadmap bars.
-   `groupableFields`: Array of fields with name and label used as groupable fields.
-   `colorableFields`: Array of fields with name and label used as colorable fields.
-   `metricsFields`: Array of fields with name and label used as metrics fields.

 The default value is `{"startDateField":{"name":"","label":""},"endDateField":{"name":"","label":""},"itemNameField":{"name":"","label":""},"itemOwnerField":{"name":"","label":""},"percentCompleteField":{"name":"","label":""},"statusField":{"name":"","label":""},"groupableFields":[],"colorableFields":[],"metricsFields":[]}`

</td></tr><tr><td>

Roadmap start date

</td><td>

startDateTime

</td><td>

Start date of the roadmap.

 Expected format is the format of `dateFormat` property, if provided. Otherwise, the value is set to `YYYY-MM-DD HH:mm:ss` for value and displayValue.

 Default value: `{\"value\": \"\",\"displayValue\": \"\"}`

</td></tr><tr><td>

Roadmap end date

</td><td>

endDateTime

</td><td>

End date of the roadmap.

 Expected format is of the `dateFormat` property, if provided. Otherwise, the value is automatically set in the `YYYY-MM-DD HH:mm:ss` format for value and displayValue.

 Default value: `{\"value\": \"\",\"displayValue\": \"\"}`

</td></tr><tr><td>

Roadmap date format

</td><td>

dateFormat

</td><td>

Date-time format of the roadmap item's dates.

 Default value: `{"valueFormat":"YYYY-MM-DD HH:mm:ss","displayValueFormat":"YYYY-MM-DD HH:mm:ss"}`

</td></tr><tr><td>

Roadmap timezone

</td><td>

timezone

</td><td>

Timezone to define the roadmap dates

 Default value: `"GMT"`

</td></tr><tr><td>

Roadmap locale

</td><td>

locale

</td><td>

Locale in which roadmap labels display.

 The following value map provides the language code mapping to moment locale language code:

 `{"en":"en", "es": "es", "it": "it", "et": "et", "zt": "zh-cn", "xl": "x-pseudo", "fi": "fi", "pb": "pt-br", "pl": "pl", "fr": "fr", "ko": "ko", "pt": "pt", "ja": "ja", "ru": "ru", "tr": "tr", "zh": "zh-cn", "sv": "sv", "he": "he", "nb": "nb", "hu": "hu", "cs": "cs", "de": "de", "th": "th", "fq": "fa-ca", "nl": "nl"}`

 Default value: `"en"`.

</td></tr><tr><td>

Enable drag/drop and resize

</td><td>

canEditBar

</td><td>

Enables drag and drop and resizing of the roadmap item bar.

 Default value: `false`

</td></tr><tr><td>

Field Color Maps

</td><td>

fieldColorMaps

</td><td>

Field color maps for roadmap bar colors.

 Default value: `null`

</td></tr><tr><td>

Empty state message

</td><td>

emptyStateMessage

</td><td>

Empty state message of the roadmap.Default value: None

</td></tr></tbody>
</table><table id="table_aw1_ff1_hxb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show header

</td><td>

showHeader

</td><td>

Option to display the header. Default value: false.

</td></tr><tr><td>

Show actions slot

</td><td>

showHeaderActionSlot

</td><td>

Option to display header slot with slot name sn-roadmap-header-actions.Default value: false.

</td></tr><tr><td>

Title

</td><td>

headerTitle

</td><td>

Defines the title of the roadmap.

 Default value: `Roadmap Title`

</td></tr></tbody>
</table><table id="table_bw1_ff1_hxb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show panel

</td><td>

showSidePanel

</td><td>

Defines the configuration for the contextual sidebar panel.Default value: `null`

-   `showPanel`: Boolean. Option to display the contextual sidebar panel.

Default value: None

-   `panelName`: String. Name of the panel.
-   `autoOpenUnscheduledPanel`: Boolean.

Default value: None


</td></tr><tr><td>

Side bar custom routes

</td><td>

sideBarActionItems

</td><td>

An array describing contextual side bar actions. Each object has the following properties:

-   `name`: String. Name of the contextual side bar.
-   `routeType`: String. Route type of the contextual side bar.
-   `icon`: String. Icon for the contextual side bar.
-   `order`: Number. Number of the contextual side bar.

</td></tr><tr><td>

Show settings change processing bar

</td><td>

processingSettingsChange

</td><td>

Shows progress bar when settings change is in processing state.

</td></tr><tr><td>

Hide roadmap details

</td><td>

hideToolbarRoadmapDetails

</td><td>

Hides roadmap details in the side toolbar.

 Default value: `false`

</td></tr><tr><td>

Hide personalized settings

</td><td>

hideToolbarSettings

</td><td>

Hides the personalize settings in the side toolbar.Default value: `false`

</td></tr><tr><td>

Hide unscheduled items

</td><td>

hideToolbarUnscheduledItems

</td><td>

Hides the unscheduled items in the side toolbar.Default value: `false`

</td></tr><tr><td class="sub-head" colspan="3">

Personalize panel

</td></tr><tr><td>

Allow personalization

</td><td>

canEditPersonalizedSettings

</td><td>

Option to make the personalized settings editable.Default value: `true`

</td></tr><tr><td>

Metrics limit

</td><td>

metricsLimit

</td><td>

Maximum number of metrics that can be displayed on bar.Default value: `3`

</td></tr><tr><td>

Hide status selector

</td><td>

hideStatusSelector

</td><td>

Option to hide the status selector.Default value: `false`

</td></tr><tr><td>

Hide milestone selector

</td><td>

hideMilestoneSelector

</td><td>

Option to hide the milestone selector.Default value: `false`

</td></tr><tr><td>

Hide item milestone selector

</td><td>

hideItemMilestoneSelector

</td><td>

Option to hide the item milestone selector.Default value: `false`

</td></tr><tr><td>

Hide dependency selector

</td><td>

hideDependencySelector

</td><td>

Option to hide the dependency selector.Default value: `false`

</td></tr><tr><td>

Hide color-by selector

</td><td>

hideColorBySelector

</td><td>

Option to hide the color-by selector.Default value: `false`

</td></tr><tr><td>

Hide group-by selector

</td><td>

hideGroupBySelector

</td><td>

Option to hide the group-by selector.Default value: `false`

</td></tr><tr><td>

Hide metrics selector

</td><td>

hideMetricsSelector

</td><td>

Option to hide the metrics selector.Default value: `false`

</td></tr><tr><td>

Hide item owner selector

</td><td>

hideItemOwnerSelector

</td><td>

Option to hide the item owner selector.Default value: `false`

</td></tr><tr><td>

Hide percent complete selector

</td><td>

hidePercentCompleteSelector

</td><td>

Option to hide the percent complete selector.Default value: `false`

</td></tr><tr><td>

Hide other settings selector

</td><td>

hideOthersSelector

</td><td>

Option to hide the other settings selector.Default value: `false`

</td></tr><tr><td class="sub-head" colspan="3">

Item details panel

</td></tr><tr><td>

Tab items

</td><td>

detailsPanelTabs

</td><td>

Defines tab items of the item details in the side panel.Default value: None

</td></tr><tr><td>

Table names to hide new button

</td><td>

detailsPanelHideNewBtnForTables

</td><td>

Defines table names that hides the new button.Default value: None

</td></tr><tr><td>

List item selected from details panel list

</td><td>

detailsPanelListItemSelected

</td><td>

Option to list item selected from details panel list.Default value: `false`

</td></tr></tbody>
</table><table id="table_ew1_ff1_hxb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Custom calendar data

</td><td>

timelineHeaderData

</td><td>

Defines timeline custom calendar data.Default value: `{}`

</td></tr><tr><td>

Default timescale

</td><td>

defaultTimeScale

</td><td>

Timescale to be selected by default when the roadmap initializes.

 Default value: None

</td></tr></tbody>
</table><table id="table_fw1_ff1_hxb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roadmap item dependencies

</td><td>

dependencies

</td><td>

Dependencies between the items on the roadmap. The dependency is of the type object with the following attributes:-   `id`: Unique ID of the dependency
-   `relatedItem`: unique ID of the related item
-   `category`: Type of dependency
-   `number`: Unique number of the dependency
-   `canEdit`: Enables edit access for the dependency
-   `canDelete`: Enables delete access for the dependency
-   `relationship`: type of the dependency relationship

 Default value: \{ \}

</td></tr><tr><td>

Roadmap item dependencies metadata

</td><td>

dependenciesMetadata

</td><td>

Metadata of the roadmap item dependencies such as the type of relationship, predecessor, and successor. The dependencies metadata has the following attributes:-   `predecessor`: Translated plural string to be used for the predecessor
-   `predecessorSingleLabel`: Translated singular string to be used for the predecessor
-   `successor`: translated plural string to be used for the successor
-   `successorSingleLabel`: Translated singular string to be used for the successor
-   `isDirectional`: Determines whether the relationship is directional. If directional, dependency lines are drawn between the roadmap items.

 Default value: `{ }`

</td></tr><tr><td>

Allow dependency creation

</td><td>

canCreateDependencies

</td><td>

Enables creation of dependencies between roadmap items.Default value: `None`

</td></tr></tbody>
</table><table id="table_iw1_ff1_hxb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable drag/drop milestone

</td><td>

canEditMilestone

</td><td>

Enables drag and drop of roadmap-level milestone.

 Default value: `false`

</td></tr><tr><td>

Roadmap and roadmap item milestones

</td><td>

milestones

</td><td>

Stores roadmap-level and item-level milestones. Each object has the following properties:

-   `roadmapMilestones`: Roadmap-level or planning organization level milestones.
-   `roadmapItemMilestones`: Milestones of the items planned in the roadmap.

 Default value: `{}`

</td></tr><tr><td>

Milestone metadata

</td><td>

milestoneMetadata

</td><td>

Mapping between milestone type and icon, state and color.

 Default value: `{}`

</td></tr></tbody>
</table>**Note:** The following properties have been planned for deprecation in a future release.

<table id="table_kw1_ff1_hxb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration of the roadmap\(Planned for deprecation\)

</td><td>

config

</td><td>

Defines the configuration for the roadmap.

-   `showHeader`: Boolean. When this property is set to true, header is displayed.

Default value: false.

-   `header`: Properties of the header.
-   `showHeaderActionSlot`: Boolean. Shows header slot with slot name sn-roadmap-header-actions.

Default value: false.

-   `settingsPanel`: Side panel settings.
    -   `hideColorBySelector`: Boolean. Hides the color by selector.

Default value: false.

    -   `hideGroupBySelector`: Boolean. Hides the group by selector.

Default value: false.

    -   `hideMetricsSelector`: Boolean. Hides the metrics selector.

Default value: false.

    -   `hideStatusSelector`: Boolean. Hides the status selector.

Default value: false.

    -   `hidePercentCompleteSelector`: Boolean. Hides the percent complete selector.

Default value: false.

    -   `hideMilestoneSelector`: Boolean. Hides the milestone selector.

Default value: false.


**Note:** These values aren’t user-specific.

</td></tr><tr><td>

Settings\(Planned for deprecation\)

</td><td>

settings

</td><td>

Defines the user preferences in the **Settings** &gt; **Personalize** panel:

-   groupBy: Attributes selected in the group by field.
-   colorBy: Attribute selected in the color by field.
-   showItemOwner: Shows owner of the roadmap item on the bar.
-   metrics: Attributes selected to be displayed on the bar.
-   showStatus: Shows status of the roadmap item on its bar.
-   showPercentComplete: Shows percent complete of a roadmap item on its bar.
-   displayRoadmapMilestones: Displays roadmap-level milestones on the roadmap.
-   displayItemMilestones: Displays item-level milestones on the roadmap bars.
-   displayMilestoneLabels: Displays labels of the item-level milestones.
-   displayOnlyMilestones: Displays only the milestones on the roadmap and hides the roadmap bars.

 Default value: `{"groupBy":[],"colorBy":"","metrics":[],"showItemOwner":false,"showStatus":false,"showPercentComplete":false,"displayRoadmapMilestones":true,"displayItemMilestones":false,"displayMilestoneLabels":false,"displayOnlyMilestones":false}`

</td></tr></tbody>
</table>## Roadmap component events

Select event handlers to configure the actions \(events\) provided with the Roadmap component.

The Events tab shows the events used by the Roadmap component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Roadmap actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

<table id="table_dwx_mj1_j4b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roadmap item updated

</td><td>

Dispatched when a user updates a roadmap item. The event contains the roadmap item.

</td></tr><tr><td>

Personalize settings updated

</td><td>

Dispatched when a user updates roadmap preferences. The event contains the information of the updated fields and their values.

</td></tr><tr><td>

Timescale changed

</td><td>

Dispatched when a user changes a timeline calendar and scale. The event contains the roadmap timeline data.

</td></tr><tr><td>

Roadmap item selected

</td><td>

Dispatched when a user selects a roadmap item. The event contains the roadmap item.

</td></tr><tr><td>

Roadmap sidebar button clicked

</td><td>

Dispatched when a user clicks a sidebar button. The event opens the side panel based on the button that the user clicked.

</td></tr><tr><td>

Roadmap side panel toggled

</td><td>

Dispatched when a user toggles the side panel.

</td></tr><tr><td>

Milestone selected

</td><td>

Dispatched when a user selects a milestone on the roadmap.

</td></tr><tr><td>

Milestone updated

</td><td>

Dispatched when a user drags and drops a milestone on the roadmap.

</td></tr><tr><td>

Milestone added

</td><td>

Dispatched when a user clicks the milestone bar to add a new milestone.

</td></tr><tr><td>

Roadmap details panel tab selected

</td><td>

Dispatched when a user selects the details tab in the side panel.

</td></tr><tr><td>

Roadmap item level milestone selected

</td><td>

Dispatched when a user selects an item-level milestone.

</td></tr><tr><td>

Roadmap item level milestone added

</td><td>

Dispatched when a user clicks the new milestone button on roadmap item details in the side panel.

</td></tr><tr><td>

Roadmap item level dependency added

</td><td>

Dispatched when a user clicks the new dependency button on roadmap item details in the side panel.

</td></tr><tr><td>

Roadmap item level dependency selected

</td><td>

Dispatched when a user selects an item dependency.

</td></tr><tr><td>

Roadmap item selected from dependency card

</td><td>

Dispatched when a user selects an item from the dependency card.

</td></tr><tr><td>

Roadmap item level milestone detail form back button clicked

</td><td>

Dispatched when a user clicks the back button on the item milestone form in the side panel.

</td></tr><tr><td>

Roadmap item level dependency detail form back button clicked

</td><td>

Dispatched when a user clicks the back button on the dependency form in the side panel.

</td></tr><tr><td>

External planning item is clicked

</td><td>

Dispatched when a user selects a dependent item from the dependency card.

</td></tr><tr><td>

Filter query updated from the filter in side panel

</td><td>

Dispatched when a user updates the roadmap filters roadmap side panel.

</td></tr><tr><td>

Details panel list item selected

</td><td>

Dispatched when a user selects a list item from details panel

</td></tr></tbody>
</table>