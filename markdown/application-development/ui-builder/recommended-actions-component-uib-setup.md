---
title: Recommended Actions component setup
description: The Recommended Actions component uses the recommendation engine to complete fields with recommended values. The Recommended Actions component requires installation of the Recommended Actions for Customer Service application.Configure the source table for the recommended values.Select event handlers to configure the events provided with the Recommended Actions component. Event handlers work with data resources to link the Recommended Actions events to the data you want to display to your users.Properties in the Recommended Actions component have preset configuration values. You can accept these values or override them manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/recommended-actions-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Recommended Actions component setup

The Recommended Actions component uses the recommendation engine to complete fields with recommended values. The Recommended Actions component requires installation of the Recommended Actions for Customer Service application.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin, workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Recommended Actions that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "recommended-actions-content-tree.png"\] Alt text: Shows the recommended actions component in the UI Builder content tree

2.  Select the Recommended Actions component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.\[Omitted image "recommended-actions-properties.png"\] Alt text: Shows the properties for the Recommended Actions component in the config panel


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Recommended Actions component properties

Configure the source table for the recommended values.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Links the property to data from another component by using data resources. For details, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_wdb_mpm_bwb"><thead><tr><th>

Label\[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sys ID\[sysId\]

</td><td>

The sys ID of the record on which the component is rendered.

</td></tr><tr><td>

Table\[table\]

</td><td>

The table name of the record on which the component is rendered.

</td></tr><tr><td>

Context Sys id\[contextSysId\]

</td><td>

The sys id of the context record for which the recommendation is configured. If a context record is not specified, the system uses the latest active context for the given table record by default.

</td></tr><tr><td>

Enable prefetch\[enablePreFetch\]

</td><td>

Checkbox to enable prefetched recommendations.

</td></tr><tr><td>

Prefetched recommendations\[preFetchedReccomendations\]

</td><td>

Array output of prefetched recommendations.

</td></tr><tr><td>

Context inputs\[contextInputs\]

</td><td>

Defines key-value pairs that provide dynamic inputs for generating recommendations. To use a template, navigate to: Recommended Actions → Context → Context Inputs.

</td></tr><tr><td>

Recommended action specific configuration\[actionConfigurations\]

</td><td>

Stores additional Recommended Actions properties. Use this property to define the UI behaviors of different actions on a record page.Example: Attach and share article guidance:

```
{
	"e8421a2a436f0210f81d92621ab8f2da": {
		"actionType": "guidance",
		"actionName": "attachAndShareArticle",
		"configuration": {
			"eventSupported": false,
			"attachAndAddLinkInComment": {
				"isSupported": true,
				"orderInPreview": 100,
				"orderInDetail": 100,
				"visibleInPreview":true,
				"visibleInDetail":true
			},
			"readArticle":{
				"isSupported": true,
				"orderInPreview": 200,
				"visibleInPreview":true
			},
			"readArticleInFullView":{
				"isSupported": true,
				"orderInDetail": 200,
				"visibleInDetail":true
			},
			"attachAndAddLinkInEmail": {
				"isSupported": false,
				"orderInPreview": 300,
				"orderInDetail": 300,
				"visibleInPreview":true,
				"visibleInDetail":true
			},
			"addLinkInWorkNote": {
				"isSupported": true,
				"orderInPreview": 400,
				"orderInDetail": 400,
				"visibleInPreview":true,
				"visibleInDetail":true
			},
			"copyLink":{
				"isSupported": true,
				"orderInPreview": 500,
				"orderInDetail": 500,
				"visibleInPreview":true,
				"visibleInDetail":true
			},
			"markArticle":{
				"isSupported": true,
				"orderInDetail": 600,
				"visibleInDetail":true
			},
			"flagArticle":{
				"isSupported": true,
				"orderInDetail": 700,
				"visibleInDetail":true}
		}
	}
}

```

Example: Share KB in chat interactions guidance:

```
{
    "550918d9439412102280698f38b8f26a": {
        "actionType": "guidance",
        "actionName": "shareKbInChatInteractions",
        "configuration": {
            "sendChat": {
                "isSupported": true,
                "orderInPreview": 100,
                "orderInDetail": 100,
                "visibleInPreview": true,
                "visibleInDetail": true
            },
            "sendPrivateChat": {
                "isSupported": true,
                "orderInPreview": 200,
                "orderInDetail": 200,
                "visibleInPreview": true,
                "visibleInDetail": true
            },
            "copyLink": {
                "isSupported": true,
                "orderInPreview": 300,
                "orderInDetail": 300,
                "visibleInPreview": true,
                "visibleInDetail": true
            },
            "readArticle": {
                "isSupported": true,
                "orderInPreview": 400,
                "visibleInPreview": true
            },
            "readArticleInFullView": {
                "isSupported": true,
                "orderInDetail": 400,
                "visibleInDetail": true
            },
            "markArticle": {
                "isSupported": true,
                "orderInDetail": 500,
                "visibleInDetail": true
            },
            "flagArticle": {
                "isSupported": true,
                "orderInDetail": 600,
                "visibleInDetail": true
            }
        }
    }
}

```

Select **Edit** to open this property in a modal.

Properties:

-   actionSysId: the sys id of the guidance or decision tree
-   actionName: the name of the guidance or decision tree
-   actionType: the type of action, either guidance or decision tree
-   configurations: the JSON object includes action-specific properties

For example: Attach and share article guidance properties:

-   isSupported: true/false:
    -   true: the button for this action is visible on the guidance card
    -   false: the button for this action is hidden on the guidance card
-   orderInDetail: controls the sequence of actions in the secondary actions list. The lowest value is the primary call to action on the guidance card in the detail experience.
-   orderInPreview: controls the sequence of actions in the secondary actions list. The lowest value is the primary call to action on the guidance card for the preview experience.
-   visibleInDetail: visibility in the detail guidance experience \(full article view\)
    -   true: action is shown
    -   false: action is not shown
-   visibleInPreview: visibility in the preview guidance experience \(card view\)
    -   true: action is shown
    -   false: action is not shown

</td></tr><tr><td>

Show by grouping\[grouping\]

</td><td>

Option to show the relevant recommendation cards in a group or as an individual card in a list.Default: **false**

</td></tr><tr><td>

Hide heading\[hideHeading\]

</td><td>

Option to show or hide the main component heading.Default: **false**

</td></tr><tr><td>

Hide recommended actions\[hideRecommendationTab\]

</td><td>

Option to show or hide the Recommended actions tab.Default: **false**

</td></tr><tr><td>

Hide search\[hideSearchTab\]

</td><td>

Option to show or hide the Search tab.Default: **true**

</td></tr><tr><td>

Hide history\[hideTabs\]

</td><td>

Option to show or hide the History icon.Default: **false**

</td></tr><tr><td>

Recommended actions position order\[recommendationPlaceOrder\]

</td><td>

The number that determines the position of the recommended actions tab.Default: **1**

</td></tr><tr><td>

Search position order\[searchPlaceOrder\]

</td><td>

The number that determines the position of the search tab.Default: **2**

</td></tr><tr><td>

Heading title\[heading\]

</td><td>

Option to override the heading or title of the component.

</td></tr><tr><td>

Recommended actions title\[recommendationTab\]

</td><td>

Option to override the title of the Recommended actions tab.

</td></tr><tr><td>

Search title\[searchTab\]

</td><td>

Option to override the title of the Search tab.

</td></tr><tr><td>

History title\[historyTitle\]

</td><td>

Option to override the name of the Action history icon.

</td></tr><tr><td>

Carousel Sliding Type\[carouselSlidingType\]

</td><td>

Option to determine whether a user can move a single item or a set of items in a grouping experience. This property is only valid when **grouping** is set to true.Default: **false**

</td></tr><tr><td>

Carousel Items In View\[carouselItemsInView

</td><td>

Option to define how to display carousel items. You can display either a single item or multiple items. The options are:-   Multiple content items
-   Single content item

Default: Multiple content items

</td></tr><tr><td>

Card's max height\[customExpMaxHeight\]

</td><td>

Maximum height of the grouping cards.

</td></tr><tr><td>

Card's max wdith\[customExpMaxWidth\]

</td><td>

Maximum width of the grouping cards.

</td></tr></tbody>
</table>## Recommended Actions component events

Select event handlers to configure the events provided with the Recommended Actions component. Event handlers work with data resources to link the Recommended Actions events to the data you want to display to your users.

The Events tab shows the events used by the Recommended Actions component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Recommended Actions actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add Recommended Actions notification\[RECOMMENDED\_ACTIONS\#ADD\_NOTIFICATION\_REQUESTED\]

</td><td>

Shows notification when new recommendations are generated on the record page in UI Builder.Payload:

-   **id**: The ID of the notification.
-   **status**: The status of the notification.
-   **icon**: The icon for the notification.
-   **content**: The message in the notification.
-   **action**: The action type, such as Dismiss, for the notification.

</td></tr><tr><td>

Recommended Actions clicked\[RECOMMENDED\_ACTIONS\#ACTION\_CLICKED\]

</td><td>

A user selects call-to-action button on the recommendation card that opens in the contextual side panel or in a sub tab.Payload:

-   **type**: The type of recommendation, such as guidance or decision tree.
-   **recommender**: The sys ID of the parent record containing the guidance.
-   **recommendedBy**: The table name of the parent record containing the guidance.

</td></tr><tr><td>

Recommended Actions open record\[RECOMMENDED\_ACTION\_CARD\#OPEN\_RECORD\]

</td><td>

A user selects the record page link in the recommendation card.Payload:

-   **table**: The table that stores the record.
-   **sys\_id**: The ID of the record.

</td></tr><tr><td>

No Recommended Actions\[RECOMMENDED\_ACTIONS\#NO\_RECCOMENDATIONS\}

</td><td>

There are no recommended actions available for the record.

</td></tr><tr><td>

Recommended Actions request failed\[RECOMMENDED\_ACTIONS\#DATA\_FETCH\_FAILED\]

</td><td>

The request for recommended actions failed.Payload:

-   **name**: error
-   **label**: Error
-   **description**: The error object containing the reason the data fetch failed
-   **fieldType**: json

</td></tr><tr><td>

Recommended Actions component error\[RECOMMENDED\_ACTIONS\#COMPONENT\_ERROR\_THROWN\]

</td><td>

An error occurred with the Recommended Actions component.Payload:

-   **name**: error
-   **label**: Error
-   **description**: The error object containing the reason the component failed
-   **fieldType**: json

</td></tr><tr><td>

Guidance or decision tree triggered actionSN\_NEXT\_BEST\_ACTION\_LIST\_CONNECTED \#ACTION\_TRIGGERED

</td><td>

Event emitted by Recommended Action component for guidance client actions.Payload:

-   **actionSysId**: the sys id of the guidance or decision tree.
-   **actionName**: the name of the Recommended Action guidance or decision tree.
-   **actionType**: the type of Recommended Action, either guidance or decision tree.
-   **eventName**: the guidance action event names. For example in case of **Attach and share article** guidance, event names are:
    -   attachAndAddLinkInComment,
    -   addLinkInWorkNote, or
    -   AttachAndAddLinkInEmail
-   **payload**: JSON payload which includes the additional details related to the event propagated.

</td></tr><tr><td>

Recommended Actions link clickedSN\_NEXT\_BEST\_ACTION\_LIST\_CONNECTED\#LINK\_CLICKED

</td><td>

Dispatched when the user clicks on link which opens record present in recommendation present in workspace.payload: -   Table: The table of the record to be opened with the link
-   sys\_id: sys id of the record to be opened with the link

</td></tr></tbody>
</table>## Recommended Actions preset configuration properties

Properties in the Recommended Actions component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Recommended Actions settings__**

    This preset shows record activity. This activity can be record field changes, journal entries, attachments, and attached knowledge articles. This preset requires the **Recommended Actions** controller.

    Properties included in this preset are:

    -   CarouselItemsInView
    -   CarouselSlidingType
    -   CustomExpMaxHeight
    -   CustomExpMaxWidth
    -   Grouping
    -   Heading
    -   HideCarouselBorder
    -   HideGroupingTitle
    -   HideHeading
    -   HideRecommendationTab
    -   HideSearchTab
    -   HideTabs
    -   HistoryTitle
    -   RecommendationPlaceOrder
    -   RecommendationTab
    -   SearchPlaceOrder
    -   SearchTab
    -   SysId
    -   Table

### Manual configuration

To configure the properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

