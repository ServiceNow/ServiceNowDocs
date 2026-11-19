---
title: AI Summary Card component setup
description: AI Summary Card displays AI-generated summaries for records and provides options to refresh, refine, and share the content.Properties in the AI Summary Card component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/ai-summary-card-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# AI Summary Card component setup

AI Summary Card displays AI-generated summaries for records and provides options to refresh, refine, and share the content.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for AI Summary Card that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "ai-summary-card-content-tree.png"\] Alt text: AI Summary Card in the UI Builder content tree.

2.  Select the AI Summary Card component using one of these methods:

    -   Click anywhere within the component.
    -   Select the AI Summary Card label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "ai-summary-card-preset-panel.png"\] Alt text: AI Summary Card preset selection panel.

3.  Either select **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## AI Summary Card component properties

Properties in the AI Summary Card component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__AI Summary Card__**

    This preset provides the AI Summary Card component with record data, configuration properties, and event bindings needed to display and manage AI-generated summaries. This preset requires the **Summary** controller.

    Properties included in this preset are:

    -   AMB Channel
    -   Call to Action
    -   Date Time Format
    -   Display Data
    -   Field Descriptions
    -   Hide card
    -   Labels
    -   Pro Active Summarization
    -   Sys id of the record
    -   Table name of the record
    -   Related Lists
    -   Save to Field Label
    -   Save to Field Response
    -   Skill Configuration Id
    -   Summary Response AMB
    -   Table Label
    -   View
    -   WWNA Component ID

### Properties

<table id="table-uib-props"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill Configuration Id\[skillId\]

</td><td>

Custom skill ID that identifies which skill configuration to use.

</td></tr><tr><td>

Sys id of the record\[recordSysId\]

</td><td>

Sys ID of the record to summarize.

</td></tr><tr><td>

Table name of the record\[recordTable\]

</td><td>

Name of the table containing the record.

</td></tr><tr><td>

WWNA Component ID\[wwnaComponentId\]

</td><td>

Unique identifier for the component instance.

</td></tr><tr><td>

AMB Channel\[ambChannel\]

</td><td>

AMB channel for listening to configuration changes and dispatching messages.

</td></tr><tr><td>

Hide card\[isHidden\]

</td><td>

Determines whether to hide the card.Default: **False**

</td></tr><tr><td>

Pro Active Summarization\[proActiveTrigger\]

</td><td>

Enables pro active summarization.

</td></tr><tr><td>

Related Lists\[relatedLists\]

</td><td>

Related lists for the record to summarize.

</td></tr><tr><td>

Save to Field Label\[saveToFieldLabel\]

</td><td>

Label of the field where the summary can be saved.

</td></tr><tr><td>

Save to Field Response\[saveToFieldResponse\]

</td><td>

Response associated with the most recent request to save the summary to a field.

</td></tr><tr><td>

Display Data\[displayData\]

</td><td>

Data object used to render the card.```
"properties": {
                      "content": {
                      "type": "string"
                      },
                      "logId": {
                      "type": "string"
                      },
                      "status": {
                      "type": "string",
                      "enum": ["summary", "error", "info"]
                      }
                      }
```

</td></tr><tr><td>

Table Label\[tableLabel\]

</td><td>

Display label for the table that the component shows a summary for.

</td></tr><tr><td>

Labels\[labels\]

</td><td>

Overrides for labels used in the component.

</td></tr><tr><td>

View\[view\]

</td><td>

View for the card to display.

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## AI Summary Card component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the AI Summary Card component. Events with presets are marked with the **Preset** badge. To show events that do not have preset configurations, select **+ Add event mapping**. If the component has only one event and that event does not have a preset, the event is displayed and is ready for configuration.

### Event handlers

Event handlers work with data resources to link the AI Summary Card actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__AI Summary Card__**

    This preset provides data handlers for these events:

    -   AMB Channel Message
    -   Add notification requested
    -   Save to field requested
    -   Send feedback requested
    -   Summary requested

### Event descriptions

<table id="table_ov3_qdm_mhc"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AMB Channel Message\[NOW\_AI\_SUMMARY\_CARD\#AMB\_CHANNEL\_MESSAGE\]

</td><td>

The AMB channel receives a new message.

</td></tr><tr><td>

Summary requested\[NOW\_AI\_SUMMARY\_CARD\#FETCH\_SUMMARY\_REQUESTED\]

</td><td>

The user selects **Summarize**, **Refresh**, or **Retry** on the card.

</td></tr><tr><td>

Send feedback requested\[NOW\_AI\_SUMMARY\_CARD\#SEND\_FEEDBACK\_REQUESTED\]

</td><td>

The user selects the thumbs-up or thumbs-down feedback button.Payload:

```
[
						{
							"name": "feedback",
							"label": "Feedback",
							"fieldType": "choice",
							"typeMetadata": {
								"choices": [
									{
										"label": "None",
										"value": ""
									},
									{
										"label": "Accepted",
										"value": "Accepted"
									},
									{
										"label": "Rejected",
										"value": "Rejected"
									}
								],
								"schema": {
									"type": "string",
									"enum": ["", "Accepted", "Rejected"]
								}
							}
						},
						{
							"name": "logId",
							"label": "logId",
							"description": "ID of the Gen AI Log",
							"readOnly": false,
							"fieldType": "string",
							"valueType": "string",
							"typeMetadata": {
								"schema": {
									"type": "string"
								}
							}
						}
					]
```

</td></tr><tr><td>

Add notification requested\[NOW\_AI\_SUMMARY\_CARD\#ADD\_NOTIFICATION\_REQUESTED\]

</td><td>

A notification is added to the page, for example, to inform the user of errors while copying a summary.Payload:

```
[
						{
							"name": "items",
							"label": "Items",
							"description": "A list of notifications to be displayed",
							"readOnly": false,
							"fieldType": "json",
							"required": true,
							"defaultValue": "[]",
							"typeMetadata": {
								"schema": {
									"type": "array",
									"items": {
										"type": "object",
										"properties": {
											"type": {
												"type": "string",
												"description": "Type of message to be displayed. This determines how the notification is styled (error|info|warning)"
											},
											"message": {
												"type": "string",
												"description": "The notification message"
											}
										}
									}
								}
							}
						}
					]
```

</td></tr><tr><td>

Save to field requested\[NOW\_AI\_SUMMARY\_CARD\#SAVE\_TO\_FIELD\_REQUESTED\]

</td><td>

Saves a summary to a specified field when requested by the user.Payload:

```
[
						{
							"name": "summary",
							"label": "Summary",
							"fieldType": "string",
							"typeMetadata": {
								"schema": {
									"type": "object",
									"properties": {
										"summary": {
											"type": "string",
											"description": "The summary content"
										},
										"userModified": {
											"type": "boolean",
											"description": "Whether the content was edited by user before dispatching "
										},
										"logId": {
											"type": "string",
											"description": "ID of the Gen AI Log"
										}
									}
								}
							}
						}
					]
```

</td></tr><tr><td>

View Set\[NOW\_AI\_SUMMARY\_CARD\#VIEW\_SET\]

</td><td>

The component view changes to a new state.Payload:

```
[
						{
							"name": "value",
							"label": "Value",
							"fieldType": "choice",
							"typeMetadata": {
								"choices": [
									{
										"label": "Error",
										"value": "error"
									},
									{
										"label": "Info",
										"value": "info"
									},
									{
										"label": "Initial",
										"value": "initial"
									},
									{
										"label": "Loading",
										"value": "loading"
									},
									{
										"label": "Regenerating",
										"value": "regenerating"
									},
									{
										"label": "Summary",
										"value": "summary"
									}
								],
								"schema": {
									"type": "string",
									"enum": [
										"error",
										"info",
										"initial",
										"loading",
										"regenerating",
										"summary"
									]
								}
							}
						}
					]
```

</td></tr></tbody>
</table>